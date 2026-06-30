---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.19.4
  kernelspec:
    display_name: leleka_ctx (3.12.3)
    language: python
    name: python3
---

<!-- #region -->
# 🕸️ SPIDERWEB MANIFESTO

## ABSTRACT


## WORKSPACE
<!-- #endregion -->

```python tags=["input-hidden"]

```

## AI stack
- Ollama is running on 'bradley' and I can ssh to bradley from all hosts. So far have OpenWebUI as a service on bradley, but i dont really use it much, its just there for quick references etc.
- Main use case so far: Have a typer system running and i have a few basic commands. This is the main focus atm: to evolve the system

### Leleka

**Goal**
- `spiderweb` is a Python CLI application designed for managing local infrastructure and interacting with local LLMs.
- The AI fleet: geek: coder, architect, my professor for everything around coding, tech, advocate: Knows personal stuff, helps me with legal issues (atm dicorce), also with opening up a business, bro: my digital bestie (future front of house), promptimizer: Listens to my garbage and makes a sweet and efficient prompt out of it.
- Main params of the models are defined in the modelfile, main context needed to form the personality is injected within the python function. In the Command line the user can to give a project file (.md). In the
file the rest of the needed context is referenced and then axtracted and injected into the ollama call.




## Workflow

GEMINI: define workflow for claude code qas we discussed. Integrate the projectfile_template (CLAUDE.md?)

### projectfile_template


<!-- #raw -->
# meta_data
- **last_touch:** [timestamp]
- **project_id: **[project_name in snake case]
- **project_type_: **[dev | ops | life]
- **status:** [permanent | active | frozen | completed ]
- progress: [0-100%]

## abstract
[First sentence = mission_brief for system_pulse.csv. Rest = context and vision.]

## references
[Defining model params and or constraints, communication style etc. giving context]
[Bullet list of paths and or files that needs to be fed to the AI]
[Intertwined projects should be stated here]

## manifesto
[Detailed logic and or road map for the project hub]
[Content and or formatting may differ individually by type and even project]

## scratch
[Passive storage for thoughts or code snippets.]
<!-- #endraw -->




## standards

### general_file_rules
- **Naming Syntax:** All files and folders must be strictly `lowercase` and use `snake_case` with absolutely **no spaces**[cite: 1].
- **File Prefix/Suffix Convention:** Use a consistent `[type]_[name].[ext]` structure to group files by category (e.g., `project_leleka.md`, `script_backup.py`).
- If sequential ordering is required, prepend a numeric ID: `[id]_[type]_[name].[ext]` (e.g., `001_project_leleka.md`).
- **Dates:** Strictly adhere to ISO 8601 `YYYY-MM-DD` format (e.g., `log_2026-03-25.md`)[cite: 1].
- **Versioning:** No version numbers in filenames; versioning is handled exclusively via Git or internal metadata headers[cite: 1].

### markdown_standards
- **Headlines:** Use unnumbered headlines for all sections to maintain a flat, modular, and easily parsable structure[cite: 1].
- **Placeholders:** Use square brackets `[ ]` to denote dynamic variables or placeholders within templates that require user or system input (e.g., `[project_name]`).
- **Metadata Frontmatter:** Start core context or project files with a YAML-style or bulleted metadata block for rapid parsing by AI agents.
- **Tables:** Mandatory for lists containing >3 attributes per item to ensure readability[cite: 1].
- **Relational Logic:** Use `->` for execution flow and `decision:` for binding results[cite: 1].

### specific_formats
- **Text & Documentation:** Use `.md` (Markdown). UTF-8 encoding[cite: 1].
- **Structured Data:** Use `.csv`. Separator: Comma (`,`). Headers must be in `snake_case`[cite: 1].
- **Logic & Scripts:** Use `.py` (Python). Follow PEP 8 standards and include comprehensive `docstrings`[cite: 1].
- **Web Development:** `.html` (semantic tags) and `.css` (kebab-case for classes)[cite: 1].
- **Data Exchange:** `.json`. Keys strictly in `snake_case`. Indent set to 2[cite: 1].

### python_standards
- **Style Guide:** Follow **PEP 8**.
- **Naming:** `snake_case` for variables, functions, and files.
- **Paths:** Use `pathlib` for OS-independent path handling. Use relative paths.
- **Documentation:** Every function needs a short `docstring` (Summary, Args, Returns).
- **Structure:** `if __name__ == "__main__":` block for executable scripts.

### web_standards
- **HTML:** Use **HTML5 semantic tags** (`<main>`, `<section>`, `<nav>`).
- **CSS:**
  - Use **kebab-case** for classes and IDs (e.g., `.nav-bar`).
  - Use variables (`:root`) for colors/spacing to ensure consistency.
- **Separation:** Keep HTML, CSS, and JS in separate files.

### json_standards
- **Keys:** Use `snake_case` for all keys.
- **Formatting:** Use `indent=2` for human readability.
- **Data Integrity:** Arrays must contain objects or values of a uniform schema. Optional values must be explicitly represented as `null` or empty strings rather than omitting the key entirely.
- **Structure:** Avoid nesting deep objects beyond 3 levels to maintain readability and simplify parsing.

### language_standards
- **System Language:** All file content (Logic, Docs, Comments, Code) must be strictly in **ENGLISH**.
- **Interaction Language:** The primary language for interaction and outputs is **ENGLISH**. However, the system must dynamically adapt to the user's language: if the user writes in German, Spanish, or any other language, the response and reasoning must switch completely to that language.
