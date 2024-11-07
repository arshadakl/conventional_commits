### Overview of the Conventional Commits Specification:

Conventional commits use a specific format for commit messages to improve readability and automation in versioning, changelogs, and CI/CD pipelines.

The general format is:

```
<type>(<scope>): <message>
```

Where:
- **type** is a keyword that describes the purpose of the commit.
- **scope** (optional) specifies the area or module the commit affects.
- **message** is a brief, imperative description of the change.

---

### Common Commit Types:

1. **feat**: A new feature.
   - Used when introducing a new feature to the codebase.
   - Example:  
     ```
     feat(auth): add user login functionality
     ```

2. **fix**: A bug fix.
   - Used for fixing an issue or bug in the codebase.
   - Example:  
     ```
     fix(user-profile): correct email validation logic
     ```

3. **docs**: Documentation changes.
   - Used when updating documentation, README files, or other doc-related files.
   - Example:  
     ```
     docs(readme): update installation instructions
     ```

4. **style**: Code style changes (no production code change).
   - Used for non-functional changes like formatting, semicolons, or spacing.
   - Example:  
     ```
     style(button): fix indentation and spacing
     ```

5. **refactor**: Code refactoring (no functional change).
   - Used for refactoring code without changing functionality.
   - Example:  
     ```
     refactor(api): optimize database query performance
     ```

6. **perf**: Performance improvements.
   - Used for commits that improve performance, e.g., faster algorithms or reduced load times.
   - Example:  
     ```
     perf(cache): improve cache lookup speed
     ```

7. **test**: Adding or modifying tests.
   - Used for commits that add or modify unit tests or integration tests.
   - Example:  
     ```
     test(user-auth): add test for login validation
     ```

8. **chore**: Routine tasks or changes that don't affect application logic.
   - Used for tasks like updating dependencies or cleaning up code without modifying functionality.
   - Example:  
     ```
     chore(package): update dependency lodash to v4.17.21
     ```

9. **ci**: Continuous integration-related changes.
   - Used for changes related to CI configuration or scripts (e.g., `.travis.yml`, `GitHub Actions`, `Jenkins`).
   - Example:  
     ```
     ci: add GitHub Actions CI pipeline
     ```

10. **build**: Build-related changes.
    - Used for changes that affect the build system (e.g., Gulp, Webpack, Maven, Gradle).
    - Example:  
      ```
      build: update webpack config to handle image assets
      ```

11. **revert**: Reverting a previous commit.
    - Used to undo changes made in a previous commit.
    - Example:  
      ```
      revert: undo changes to login validation logic
      ```

---

### Optional Fields:

- **Scope**: The scope defines the specific area or module that the commit affects (e.g., `ui`, `auth`, `db`). This part is optional but can be helpful for context.

  Example with scope:
  ```
  feat(auth): add JWT authentication support
  ```

- **Breaking Changes**: If a commit introduces breaking changes (e.g., API changes that require changes in client code), this should be indicated in the commit message.

  - The breaking change can be added in a special section at the end of the commit message using the `BREAKING CHANGE` footer:
  
  ```
  feat(auth): update authentication logic

  BREAKING CHANGE: The `auth.login()` method now requires an email address as a parameter.
  ```

- **References**: You can also reference issues, pull requests, or tickets in commit messages using `#<issue-number>`.

  Example:
  ```
  fix(auth): resolve issue with token expiration #123
  ```

---

### Example Commit Messages:

1. **Feature Commit**:  
   ```
   feat(notification): add push notification support
   ```

2. **Fix Commit**:  
   ```
   fix(button): resolve color issue on hover state
   ```

3. **Documentation Commit**:  
   ```
   docs(api): update authentication endpoint documentation
   ```

4. **Refactor Commit**:  
   ```
   refactor(user-service): simplify password hashing logic
   ```

5. **Performance Commit**:  
   ```
   perf(image): optimize image loading for faster page speed
   ```

6. **Chore Commit**:  
   ```
   chore(deps): update react to v17
   ```

7. **Test Commit**:  
   ```
   test(cart): add tests for cart checkout functionality
   ```

8. **Revert Commit**:  
   ```
   revert: undo changes to user authentication flow
   ```

