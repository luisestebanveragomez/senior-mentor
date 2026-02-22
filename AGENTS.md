# AGENTS.md

## Agentic Workflow Guide for Code Modification and Contribution

Welcome to the comprehensive workflow and standards documentation for this TypeScript/React/Vite project. This guide is designed for both human contributors and agentic/automated tools to ensure code quality and maintainability. It describes build/lint instructions, code style conventions, React/TypeScript best practices, and recommended automation workflows. All instructions are actionable and backed by actual project configuration and source files.

---

### 1. Build & Lint Instructions

#### Build:
- **Run build:**
  ```bash
  npm run build
  ```
- **Purpose:** Bundles and optimizes the app for production using Vite.

#### Development:
- **Start dev server:**
  ```bash
  npm run dev
  ```
- **Purpose:** Launches Vite’s hot-reloading development environment.

#### Lint:
- **Run lint:**
  ```bash
  npm run lint
  ```
- **Purpose:** Enforces code quality and style via ESLint.

#### Test:
- **No test script or test setup currently defined.**
  - If adding tests, choose a suitable framework (e.g. Jest, Vitest) and add scripts to package.json.

---

### 2. Code Style & Formatting

#### Imports:
- Use ES module syntax.
- Group React-related imports first, then external libraries, then local files (CSS, assets).

#### Typing:
- Always type function, component, and prop inputs.
- Prefer explicit types for props and state.
- Use generics and union types where appropriate.
- Enforce TypeScript strictness for reliability.

#### Naming:
- Use clear, consistent naming—camelCase for variables/functions, PascalCase for components/classes.
- Folder and file names mirror component names (App.tsx, main.tsx).

#### Formatting:
- Keep lines concise; prefer single responsibility functions.
- Indent with 2 spaces; no trailing whitespace.
- Use Prettier or ESLint’s formatting recommendations where available.

#### Error Handling:
- Use try/catch for async boundaries.
- Render fallback UI components when handling errors (future enhancement).

#### React Patterns:
- Functional components only; avoid classes.
- Use hooks (`useState`, etc.) for state and side effects.
- Prefer props over direct external context for component customization.
- Separate component CSS (App.css) from global CSS (index.css).

#### ESLint Rules:
- ESLint config extends recommended, React, and TypeScript plugins.
- Enforce unused variable checks, no explicit any, and React recommended practices.
- Expand ESLint config as needed for stricter enforcement.

---

### 3. Automation & Agentic Rules

- The project supports agentic modification via build/lint scripts and code style enforcement.
- No explicit Cursor/Copilot agent rules present; workflow is designed for compatibility.
- Automated agents/tools must:
  - Run build and lint after any modification.
  - Follow ESLint/TypeScript style as above.
  - Document workflow changes in README.md if modifying scripts/configs.
  - Update AGENTS.md if creating new agentic or automation patterns.

---

### 4. Typical Workflow for Humans & Agents

1. Clone or pull repository.
2. Install dependencies:
    ```bash
    npm install
    ```
3. Make code modifications in src/, following code style above.
4. Run lint to check for style/code issues:
    ```bash
    npm run lint
    ```
5. Build project to verify correctness:
    ```bash
    npm run build
    ```
6. Add or update documentation as necessary (README.md, AGENTS.md).
7. If automation frameworks or tests are introduced, update scripts and documentation accordingly.

---

### 5. Real-World Examples from Codebase

#### App.tsx:
- Functional component with typed props
- Uses `useState` from React
- Imports CSS and assets cleanly
- Component files mirror naming conventions

#### main.tsx:
- Entry point rendering App component
- Uses ReactDOM, properly typed

#### App.css, index.css:
- Structured, readable CSS
- Use of CSS variables and media queries
- Clear distinction between component CSS and global styles

---

### 6. Technical Decisions & Notes

- Vite chosen for fast build/dev experience
- TypeScript enforced for reliability and maintainability
- React hooks and function components for modern UI patterns
- ESLint config is extendable and responsive to project needs
- No tests present; future test setup should follow modern React/TypeScript standards (jest/vitest)

---

### 7. Contributor & Agent Guidance

- All modifications must pass lint and build checks
- Strive for clarity, type safety, and maintainability
- Expand AGENTS.md and documentation to reflect new practices or automation
- Use readable commit messages describing WHY the change was made
- Automated agents: must update scripts and documentation if rules/workflow change

---

_For questions, refer to README.md or project maintainers. AGENTS.md should be revised with any workflow or automation changes._
