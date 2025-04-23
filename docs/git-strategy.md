# Git Branching Strategy

## Branch Types
1. **Main Branch**
   - `main`: The central branch containing stable and production-ready code. All feature branches are merged into `main` after code review. Direct commits to `main` are prohibited.

2. **Feature Branches**
   - `feature/<developer-name>/<feature-name>`: Created by developers to work on individual tasks or features. Branch names should include the developer's name and a short description of the feature for clarity.
   - Examples: `feature/alex/user-authentication`, `feature/jessica/docker-integration`

## Workflow
1. **Starting Development**
   - Pull the latest changes from `main`: `git pull origin main`
   - Create a new feature branch: `git checkout -b feature/<developer-name>/<feature-name>`
   - Example: `git checkout -b feature/john/user-registration`

2. **Working on the Feature**
   - Make changes, commit them locally with clear messages: `git add .`, `git commit -m "Add user registration feature"`
   - Push the feature branch to the remote repository: `git push origin feature/<developer-name>/<feature-name>`

3. **Code Review and Merging**
   - Open a Pull Request (PR) to merge the feature branch into `main`:
     - Go to your repository on GitHub.
     - Select Compare & Pull Request for your branch.
     - Add a description of the feature or task completed.
     - Assign at least one team member as a reviewer.
     - Address feedback and update the branch if necessary.
     - Once approved, the branch is merged into `main`.

4. **Keeping Your Branch Up-to-Date**
   - Before merging, ensure your branch is updated with the latest changes from `main`:
     - Pull the latest changes from `main`: `git pull origin main`
     - Resolve any merge conflicts locally, if needed.

5. **Cleaning Up**
   - After a successful merge:
     - Delete the feature branch locally: `git branch -d feature/<developer-name>/<feature-name>`
     - Delete the branch on the remote repository: `git push origin --delete feature/<developer-name>/<feature-name>`

## Git Guidelines
- **Descriptive Commit Messages**: Use clear and concise messages describing what was changed. Example: `Fix login validation bug`.
- **One Feature Per Branch**: Keep branches focused on a single feature or task.
- **Avoid Direct Commits to `main`**: Always use feature branches for any changes.
- **Pull Frequently**: Regularly pull changes from `main` to avoid merge conflicts.
