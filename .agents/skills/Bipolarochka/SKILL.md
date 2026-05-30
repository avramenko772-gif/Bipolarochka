```markdown
# Bipolarochka Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the Bipolarochka TypeScript codebase. It covers file organization, import/export styles, commit message habits, and testing patterns. By following these guidelines, contributors can maintain consistency and readability throughout the project.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example: `user-profile.ts`, `data-service.ts`

### Import Style
- Use **relative imports** for referencing other modules.
  - Example:
    ```typescript
    import { fetchData } from './data-service';
    ```

### Export Style
- Use **named exports** for all exported functions, classes, or constants.
  - Example:
    ```typescript
    // In data-service.ts
    export function fetchData() { ... }
    export const API_URL = '...';

    // In another file
    import { fetchData, API_URL } from './data-service';
    ```

### Commit Patterns
- Commit messages are **freeform** with no strict prefix, averaging 35 characters.
  - Example: `fix user profile loading bug`

## Workflows

*No automated workflows detected in this repository.*

## Testing Patterns

- **Test files** follow the pattern: `*.test.*`
  - Example: `user-profile.test.ts`
- **Testing framework** is unknown; check existing test files for conventions.
- Place test files alongside the code they test or in a dedicated `tests` directory if present.

  Example test file:
  ```typescript
  // user-profile.test.ts
  import { getUserProfile } from './user-profile';

  describe('getUserProfile', () => {
    it('returns user data for valid id', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command | Purpose |
|---------|---------|
| /test   | Run all test files matching `*.test.*` |
```