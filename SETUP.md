# Setup: Cyberpunk GitHub Profile

## 1. Create the special profile repository

1. Open GitHub and create a **new public repository**.
2. Name it **exactly your GitHub username** (for example, if your username is `octocat`, the repository must be `octocat`).
3. Add the files in this kit and commit them to the default branch.
4. GitHub will display that repository's `README.md` on your profile.

## 2. Replace placeholders in `README.md`

Use Find/Replace in VS Code (`Ctrl + H`) and replace:

- `cybparam` is already filled in as your GitHub username
- `cybparam` is already filled in as the displayed handle
- The Tic-Tac-Toe AI link currently points to your repositories page because the exact repository slug has not been confirmed yet.

Also replace the sample project link and remove any section you don't want.

## 3. File layout

```text
cybparam/
├── README.md
├── SETUP.md
├── .gitignore
└── assets/
    ├── cyber-terminal-banner.svg   # Animated HUD terminal banner
    ├── terminal-session.svg        # Animated terminal session dossier card
    ├── cyber-divider.svg           # Animated cyber pulse conduit divider
    ├── cyber-telemetry-hud.svg     # Animated hardware & neural telemetry HUD
    ├── cyber-terminal-rain.svg     # Epic Netrunner matrix rain & tactical radar terminal console
    ├── matrix-rain.svg             # Continuous digital matrix rain stream
    ├── matrix-continuous.gif       # Continuous CMatrix rain GIF backup
    └── cyberpunk-banner.png        # Static cyber banner backup
```

Keep all assets in `assets/` so relative image paths render correctly on GitHub.

## 4. Upload with Git

Open a terminal inside the folder and run:

```bash
git init
git add README.md SETUP.md .gitignore assets/
git commit -m "Build cyberpunk profile README"
git branch -M main
git remote add origin https://github.com/cybparam/cybparam.git
git push -u origin main
```

If you created the repository on GitHub with a README already, Git may reject the first push because the remote has a commit. Easiest option: create the remote repository empty (do not initialize it with a README), then push.

If `origin` already exists, update it instead of adding it again:

```bash
git remote set-url origin https://github.com/cybparam/cybparam.git
```

## 5. Pin the right projects

On your GitHub profile, use **Customize your pins** and pin up to six strong repositories. Recommended starting point:

1. Tic-Tac-Toe AI
2. Your next project once it is documented and runnable
3. Any open-source contribution or useful tool you actually shipped

A small number of well-documented projects beats a wall of unfinished repositories.

## 6. Make each repository look intentional

For every project you pin:

- Write a one-line description.
- Add a useful README: what it does, how to run it, what you learned, and limitations.
- Include a screenshot or short demo when relevant.
- Add a `requirements.txt` or `pyproject.toml` when appropriate.
- Add a `.gitignore`; never commit `.venv/`, secrets, API keys, or local machine files.
- Use meaningful commits. Don't rewrite history just to make the graph look busy.

## 7. About the live stats

The stats cards are hosted by third-party services and can occasionally rate-limit or fail. If they break, remove the image blocks under `// live telemetry`; the profile itself will still work. Don't treat the numbers or language breakdown as a measure of skill.

## 8. Optional elite touches

- Add a custom avatar that remains recognizable at small sizes.
- Keep the banner and profile README in the same repository for easy maintenance.
- Update the “current experiments” section only when you have something new to show.
- Make a separate showcase/demo repository for a project only when it adds value.
