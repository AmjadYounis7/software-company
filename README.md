# NovaDev — Two-person Git & GitHub assignment

A simple, responsive software company website built with HTML and CSS. No dependencies or build step. Open `index.html` in your browser.

## Requirements
- Header with a text logo and navigation.
- Hero with heading, description, and working contact CTA.
- Three services: web development, mobile applications, custom software.
- Footer with an example email address and copyright.

Replace the demo company name and email before using this for a real business.

## Files
- `index.html`: page structure and content.
- `styles.css`: shared styles, section styles, and mobile layout.
- `.github/pull_request_template.md`: review checklist.

## Divide the work
| Contributor | Branch | Responsibility |
| --- | --- | --- |
| Teammate A | `feature/header-hero` | Header, navigation, hero, and corresponding CSS |
| Teammate B | `feature/services-footer` | Three service cards, contact footer, and corresponding CSS |

The included website is a finished reference. To demonstrate real collaboration, agree on meaningful changes or build these sections incrementally in your own repository. Each teammate should make and push their own commits; do not invent another person's contributions.

## 1. Create the shared repository (Teammate A)
Create an empty GitHub repository named `software-company`, without a generated README. Invite Teammate B under Settings → Collaborators. In this project folder, run the following, replacing YOUR_USERNAME:

```bash
git init
git add .
git commit -m "Add software company website starter"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/software-company.git
git push -u origin main
```

If Git asks for your identity, configure your own name and email. Authenticate to GitHub when prompted; do not share passwords or access tokens.

## 2. Start a feature branch
Teammate A, from the existing project:

```bash
git switch main
git pull origin main
git switch -c feature/header-hero
```

Teammate B, on their own computer, replaces YOUR_USERNAME with the repository owner's username:

```bash
git clone https://github.com/YOUR_USERNAME/software-company.git
cd software-company
git switch -c feature/services-footer
```

## 3. Edit, check, commit, push
Make your assigned changes. Open the page and check desktop and mobile layouts. Each teammate runs:

```bash
git status
git diff
git add index.html styles.css
git commit -m "Describe your actual section changes"
```

Teammate A pushes with:

```bash
git push -u origin feature/header-hero
```

Teammate B pushes with:

```bash
git push -u origin feature/services-footer
```

## 4. Pull requests and review
On GitHub, create a pull request from your branch into `main`. Explain the changes and request your teammate's review. Review the diff, test the page, leave useful feedback, and merge when ready. Merge one PR first, then update the second branch before merging it.

To update your current feature branch:

```bash
git fetch origin
git merge origin/main
```

If a conflict occurs, open the affected file, combine the correct changes, and remove all conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`). Recheck the page, then run:

```bash
git add index.html styles.css
git commit -m "Resolve conflicts with main"
git push
```

If Git merged automatically, no extra conflict-resolution commit is needed. Push the updated branch normally.

## 5. Synchronize after merging
Each teammate runs:

```bash
git switch main
git pull origin main
git log --oneline --graph --all
```

## Before submission
- Confirm all four required sections appear.
- Check navigation and the contact button.
- Check a narrow phone viewport and a desktop viewport.
- Tab through links to verify visible keyboard focus.
- Submit the repository URL and both reviewed pull request links.
- Confirm the history contains actual contributions from both teammates.

This download does not create a GitHub repository or make contributions on behalf of either teammate.
