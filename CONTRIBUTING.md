# Contributing to my Personal project

Welcome to the "Personal" project! This document outlines our development standards and commit message conventions.

## 📝 Commit Message Convention

We follow the **Conventional Commits** specification to maintain a clean and readable commit history that enables automated tooling and clear communication.

### Format

```
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

### Commit Types

| Type          | Description                                       | Example                                               |
| ------------- | ------------------------------------------------- | ----------------------------------------------------- |
| `feat` ✨     | New feature for the user                          | `feat(auth): add Google OAuth integration`            |
| `fix` 🐛      | Bug fix                                           | `fix(leaderboard): correct score calculation logic`   |
| `docs` 📚     | Documentation changes                             | `docs(readme): update installation instructions`      |
| `style` 💄    | Code style changes (formatting, semicolons, etc.) | `style(components): fix indentation in AuthModal`     |
| `refactor` ♻️ | Code refactoring without changing functionality   | `refactor(api): simplify user data fetching logic`    |
| `perf` ⚡     | Performance improvements                          | `perf(dashboard): optimize chart rendering`           |
| `test` 🧪     | Adding or modifying tests                         | `test(auth): add unit tests for login validation`     |
| `chore` 🔧    | Maintenance tasks, dependency updates             | `chore(deps): update Next.js to version 15.3.3`       |
| `ci` 🔄       | CI/CD configuration changes                       | `ci(github): add automated testing workflow`          |
| `build` 📦    | Build system or external dependency changes       | `build(webpack): update configuration for production` |

### Scope (Optional but Recommended)

The scope should be the name of the affected module/component:

- `auth` - Authentication related changes
- `dashboard` - Dashboard page and components
- `leaderboard` - Leaderboard functionality
- `api` - API routes and logic
- `ui` - UI components (buttons, forms, etc.)
- `types` - TypeScript type definitions
- `data` - Static data and services
- and many more like these...

### Examples

#### Good Commit Messages ✅

```bash
feat(leaderboard): add district-wise filtering functionality

fix(auth): resolve infinite redirect loop on logout

docs(api): document user analytics endpoints

style(ui): improve button hover animations with Motion

refactor(data): restructure leaderboard service for better performance

chore(deps): bump @supabase/supabase-js to 2.50.0

test(components): add comprehensive tests for UserProfileDropdown
```

#### Bad Commit Messages ❌

```bash
fix stuff                           # Too vague
Added new feature                   # Not following format
updated files                       # No meaningful description
WIP                                 # Work in progress should be rebased
Fixed bug in the thing              # Not specific enough
```

### Body and Footer Guidelines

#### Body (Optional)

- Use when the commit needs more explanation than the subject line can provide
- Wrap at 72 characters
- Explain **what** and **why**, not **how**

#### Footer (Optional)

- Reference issues: `Closes #123` or `Fixes #456`
- Breaking changes: `BREAKING CHANGE: API endpoint /users renamed to /profiles`

### Complete Example

```
feat(auth): implement role-based access control

Add middleware to check user permissions for protected routes.
Supports admin, teacher, and student roles with different
access levels to dashboard features.

- Add role field to user profile types
- Implement permission checking middleware
- Update dashboard navigation based on user role

Closes #45
```

## 🚀 Development Workflow

1. **Before Committing:**

   - Ensure your code follows the project's coding standards
   - Run `npm run lint` to check for linting errors
   - Test your changes locally

2. **Making Commits:**

   - Write meaningful commit messages following the convention above
   - Keep commits atomic (one logical change per commit)
   - Avoid committing work-in-progress code

3. **Before Pushing:**
   - Review your commit history
   - Consider squashing fixup commits
   - Ensure all tests pass

## 🔒 Security

- **Never commit sensitive information** (.env files, API keys, passwords)
- **Review .gitignore** to ensure sensitive files are excluded
- **Use environment variables** for configuration that varies between environments

## 📋 Code Style

- Use **TypeScript** for type safety
- Follow **ESLint** configuration
- Use **Prettier** for consistent formatting
- Write meaningful comments for complex logic
- Prefer descriptive variable and function names

## 🤝 Pull Request Guidelines

1. **Title:** Follow the same convention as commit messages
2. **Description:** Explain what changes were made and why
3. **Testing:** Describe how to test the changes
4. **Screenshots:** Include for UI changes
5. **Breaking Changes:** Clearly document any breaking changes

---

Thank you for contributing to my Personal Project! 🎓✨
