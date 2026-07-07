```markdown
# remotion Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `remotion` repository, a TypeScript-based codebase with no detected framework. You'll learn about file naming, import/export styles, commit message habits, and how to write and run tests. This guide also provides suggested commands for common workflows to streamline your development process.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `videoRenderer.ts`, `audioMixer.ts`

### Import Style
- Use **relative imports** for referencing other modules.
  - Example:
    ```typescript
    import { renderVideo } from './videoRenderer';
    ```

### Export Style
- Use **named exports** for functions, classes, or constants.
  - Example:
    ```typescript
    // videoRenderer.ts
    export function renderVideo(params: RenderParams) { ... }
    ```

### Commit Patterns
- Commit messages are **freeform** (no strict prefixes).
- Average commit message length: **54 characters**.
  - Example:
    ```
    Fix bug in audio mixing when input is empty
    ```

## Workflows

### Adding a New Feature
**Trigger:** When you want to introduce a new capability.
**Command:** `/add-feature`

1. Create a new file using camelCase naming.
2. Implement your feature using TypeScript.
3. Use relative imports to include dependencies.
4. Export your feature using named exports.
5. Write corresponding tests in a `.test.ts` file.
6. Commit your changes with a descriptive message.

### Fixing a Bug
**Trigger:** When you need to resolve a defect.
**Command:** `/fix-bug`

1. Locate the relevant file(s) using camelCase naming.
2. Apply your fix using TypeScript.
3. Ensure all imports remain relative.
4. Update or add tests in a `.test.ts` file.
5. Commit your fix with a clear, descriptive message.

### Writing and Running Tests
**Trigger:** When you add or update functionality.
**Command:** `/run-tests`

1. Create or update test files matching the `*.test.*` pattern.
2. Write tests for your features or bug fixes.
3. Use the project's test runner (framework unknown; check project docs or package.json).
4. Run the test suite to verify correctness.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern (e.g., `videoRenderer.test.ts`).
- The testing framework is not specified; refer to project documentation or dependencies for details.
- Example test file:
  ```typescript
  // videoRenderer.test.ts
  import { renderVideo } from './videoRenderer';

  test('renders video with correct duration', () => {
    const result = renderVideo({ duration: 10 });
    expect(result.duration).toBe(10);
  });
  ```

## Commands
| Command      | Purpose                                      |
|--------------|----------------------------------------------|
| /add-feature | Start the process to add a new feature       |
| /fix-bug     | Begin workflow to fix a bug                  |
| /run-tests   | Run the test suite for the codebase          |
```
