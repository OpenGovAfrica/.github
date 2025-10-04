# Contributing to OpenGov Africa

Welcome! All of Africa is thrilled that you're considering contributing to OpenGov Africa. This document outlines our contribution guidelines to help you get started.

## Code of Conduct

By participating in this project, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md). Please take a moment to read it.

## How to Contribute
### Contributing to OpenGov Africa

We’re excited that you want to contribute to OpenGov Africa!  
Our community welcomes both **code** and **no-code** contributions; from technical writing, design, and community management, to development, documentation, and research.  

---

### Step 1: Learn About Us
Before you get started, we encourage you to explore our **[Org Wide Community Drive](https://drive.google.com/drive/folders/1EF5yA7_0STfUdrRYWvRItOtY95bhVVQS).**

Inside, you’ll find:  
- Background on OpenGov Africa and our mission.  
- Past project documentation and resources.  
- Guides on how our teams are structured.  
- Reference materials to help you understand our work.  

---

### Step 2: Join the Community and Support

Join our community to collaborate, ask questions, and seek support:

- **GitHub Issues**: For bug reports, feature requests, and enhancements.
- **Discussion Forums**: Look out for one or ask questions yourself. [OpenGov Africa Discussions](https://github.com/OpenGovAfrica/OpenGovAfrica/discussions)
- Join our **[Discord server](https://discord.gg/Eswe4cvvMM)**
   - Introduce yourself in the welcome channel  
   - Choose and join your **subteam(s)**:  
     - Code Contributors (Development, Bug Fixes, Features)  
     - No-Code Contributors (Documentation, Design, Community, Marketing, Hosting, Research)  
     - Maintainers (long-term ownership of repositories, reviewing PRs, onboarding contributors)
- **Social Media**: Follow us on [Twitter](https://twitter.com/OpenGovAfrica), [LinkedIn](https://www.linkedin.com/company/104341081), [Instagram](https://instagram.com/OpenGovAfrica) and [Facebook](https://facebook.com/OpenGovAfrica).

---

### Step 3: Review the 90-Day Roadmap
We operate on a rolling **[90-Day Roadmap](https://docs.google.com/document/d/13ELP1Azq7UFlbLQ0nIKrirszMJaRBs9qhlVLIlMij1s/edit?usp=drivesdk)** that outlines our goals, priorities, and active projects.  
 

This roadmap helps you:  
- Understand where we’re focused right now.  
- See how your contributions align with bigger goals.  
- Join efforts where extra support is most needed.  

---

### Step 4: Get Access
- Fill out the **[Contributor Form](https://forms.gle/63BwMW3r7MxuJGYE6).**  
  This allows us to:  
  - Add you to the correct GitHub team.  
  - Give you the right permissions for repositories.  
  - Keep track of contributions across subteams.  

---

### Step 5: Start Contributing
- Browse our [GitHub repositories](https://github.com/orgs/OpenGovAfrica/repositories).  
- Look for open issues labeled `good first issue`, `documentation`, `design`, or `help wanted`.  Don’t see any issue? Open one.
- Engage with your sub team on Discord to find tasks that match your interests and skills.  

### Reporting Issues

If you encounter a bug or have a feature request, please create an issue in our [GitHub repository](https://github.com/OpenGovAfrica/OpenGovAfrica/issues). 

**When reporting an issue, please include:**
- A clear and descriptive title
- Steps to reproduce the issue
- Expected behavior
- Actual behavior
- Screenshots or logs, if applicable
- Any additional context or information

### Proposing Enhancements

We welcome suggestions for new features or improvements. To propose an enhancement, please open an issue in the exact team repository and provide a detailed description of the enhancement.
## Step 5.1: Git & PR Workflow

### 1. Fork the Repository

Click the **Fork** button in the top-right corner of the repository page. This creates your own copy of the project.

### 2. Clone Your Fork

Open your terminal and run:

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

Replace `<your-username>` with your GitHub username and `<repo-name>` with the repository name.

### 3. Set Up the Upstream Remote

This connects your local repository to the original project so you can sync changes:

```bash
git remote add upstream https://github.com/OpenGovAfrica/<repo-name>.git
git fetch upstream
```

### 4. Create a Feature Branch

Always create a new branch for your changes:

```bash
git checkout -b feature/your-feature-name
```

**Branch naming conventions:**

- `feature/` for new features
- `fix/` for bug fixes
- `docs/` for documentation updates
- Example: `docs/update-readme` or `fix/typo-in-homepage`

## Making Your Contribution

### 1. Make Your Changes

Keep your changes focused on a single improvement:

- Fix a bug
- Add documentation
- Improve code readability
- Add tests

### 2. Stage Your Changes

Review what you've changed:

```bash
git status
```

Stage the files you want to commit:

```bash
git add <filename>
# Or stage all changes:
git add .
```

### 3. Commit Your Changes

Write a clear, descriptive commit message:

```bash
git commit -m "type: brief description of changes"
```

**Commit message types:**

- `feat:` new feature
- `fix:` bug fix
- `docs:` documentation changes
- `style:` formatting, missing semicolons, etc.
- `refactor:` code restructuring
- `test:` adding tests
- `chore:` maintenance tasks

**Example:**

```bash
git commit -m "docs: add installation instructions to README"
```

### 4. Push Your Branch

```bash
git push origin feature/your-feature-name
```

### 5. Open a Pull Request

1. Go to your fork on GitHub
2. You'll see a **Compare & pull request** button—click it
3. Fill out the PR template:

**Title:** Use the same format as your commit message

```
docs: add installation instructions to README
```

**Description template:**

```markdown
## What does this PR do?
Briefly describe your changes

## Why is this needed?
Explain the problem this solves or the value it adds

## Type of change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Code refactoring

## Testing
- [ ] I have tested these changes locally
- [ ] I have added tests (if applicable)

## Screenshots (if applicable)
Add before/after screenshots for UI changes
```

4. Click **Create pull request**
5. Wait for a maintainer to review your PR

## Handling Merge Conflicts

Merge conflicts happen when someone else has changed the same files you're working on. Don't panic—they're easy to fix!

### Method 1: Rebase (Recommended)

This keeps your commit history clean:

```bash
# Update your main branch
git checkout main
git pull upstream main

# Rebase your feature branch
git checkout feature/your-feature-name
git rebase upstream/main
```

If conflicts occur:

1. Git will pause and show which files have conflicts
2. Open the conflicted files and look for conflict markers:

```
<<<<<<< HEAD
Current code from main branch
=======
Your changes
>>>>>>> feature/your-feature-name
```

3. Edit the file to keep the correct code and remove the markers
4. Stage the resolved files:

```bash
git add <resolved-file>
```

5. Continue the rebase:

```bash
git rebase --continue
```

6. Force push your changes:

```bash
git push --force-with-lease origin feature/your-feature-name
```

### Method 2: Merge (Simpler Alternative)

```bash
git checkout feature/your-feature-name
git merge upstream/main
```

Resolve conflicts as described above, then:

```bash
git add <resolved-file>
git commit -m "merge: resolve conflicts with main"
git push origin feature/your-feature-name
```

## Testing Your Changes

### For Documentation Changes

Preview your markdown files to ensure formatting is correct. Most documentation PRs don't require additional testing.

### For Code Changes

**Python projects:**

```bash
# Create a virtual environment
python -m venv .venv

# Activate it
# Windows:
.venv\Scripts\activate
# Mac/Linux:
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run tests
pytest

# Run linting
flake8
```

**JavaScript/Node.js projects:**

```bash
# Install dependencies
npm ci

# Run tests
npm test

# Run linting
npm run lint

# Build (if applicable)
npm run build
```

## Best Practices

### Do's ✅

- Keep PRs small and focused on one thing
- Write clear, descriptive commit messages
- Test your changes before submitting
- Ask questions if you're unsure
- Be patient and respectful during code review
- Update your branch if maintainers request changes

### Don'ts ❌

- Don't work directly on the `main` branch
- Don't submit massive PRs with unrelated changes
- Don't force push to `main` (you can't anyway, but good to know!)

## Getting Help

Stuck? We're here to help!

- **Issues:** Check existing [issues](../../issues) or open a new one
- **Discussions:** Join our [community discussions](../../discussions)
- **Discord/Slack:** [Join our community](#) (add your community link)
- **Maintainers:** Tag maintainers in your PR if you need guidance

Remember: Everyone was a beginner once. Don't be afraid to ask questions or make mistakes—that's how we all learn!

---

## Quick Reference

```bash
# Initial setup
git clone https://github.com/<your-username>/<repo>.git
cd <repo>
git remote add upstream https://github.com/OpenGovAfrica/<repo>.git

# For each contribution
git checkout main
git pull upstream main
git checkout -b feature/your-feature
# Make changes
git add .
git commit -m "type: description"
git push origin feature/your-feature
# Open PR on GitHub

# Update your branch
git fetch upstream
git rebase upstream/main
git push --force-with-lease origin feature/your-feature
```

---

### Step 6: Stay Connected
- Join livestreams, community calls, and mentorship sessions.  
- Share your progress and ask questions in your subteam channels.  
- Collaborate, learn, and grow with contributors from across Africa and beyond.  

---

### Maintainers at OpenGov Africa
We’re actively looking for **maintainers** to help us sustain our projects.  
Maintainers:  
- Review pull requests and provide feedback.  
- Ensure issues are well-scoped and labeled.  
- Onboard and mentor new contributors.  
- Help keep projects aligned with our roadmap.  
- Share responsibility for long-term stability and growth.  

If you’d like to step up as a maintainer, please indicate this in the Contributor Form or reach out directly on Discord.  

---

## Style Guidelines

### Code Style

- Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/) for Python code.
- Use meaningful variable and function names.
- Write clear and concise comments where necessary.

### Documentation
We maintain comprehensive documentation to help users and contributors understand and use the project. Please ensure that any changes to the project are accompanied by appropriate updates to the documentation.
- Update the relevant documentation for your changes.
- Follow the [Markdown Guide](https://www.markdownguide.org/basic-syntax/) for writing Markdown files.
- Ensure documentation is clear, concise, and easy to understand.

### JSON Data

- Use clear and consistent naming conventions.
- Validate JSON structure and format.
- Include necessary metadata and context for each entry.

## Thank You!

Thank you for considering contributing to OpenGov Africa. Your support and contributions are invaluable to the African community. Together, we can promote transparency, accountability, and good governance across Africa.
