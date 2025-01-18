# Repository Setup and Maintenance Guide

## Initial Setup

### 1. Fork the Repository
1. Go to https://github.com/coleam00/ottomator-agents
2. Click the "Fork" button in the top-right corner
3. Select your GitHub account as the destination

### 2. Clone Your Fork
```bash
# Replace YOUR_USERNAME with your GitHub username
git clone https://github.com/YOUR_USERNAME/ottomator-agents.git
cd ottomator-agents
```

### 3. Add Original Repository as Upstream
```bash
git remote add upstream https://github.com/coleam00/ottomator-agents.git
```

## Regular Maintenance

### Getting Updates from Original Repository
```bash
# Fetch all changes from the original repo
git fetch upstream

# Make sure you're on your main branch
git checkout main

# Merge changes from original repo
git merge upstream/main
```

### Working with Your Own Changes

1. Create a new branch for experiments:
```bash
git checkout -b my-experiment
```

2. Make your changes and commit them:
```bash
git add .
git commit -m "Description of your changes"
```

3. Switch between branches:
```bash
# Return to main branch
git checkout main

# Return to your experiment
git checkout my-experiment
```

### Checking Status
```bash
# View which files have changed
git status

# View configured remotes
git remote -v
```

## Quick Reference

- Original repository: `upstream`
- Your fork: `origin`
- Main branch: `main`

## Troubleshooting

### If you have local changes when trying to update:
1. Stash your changes:
```bash
git stash
```

2. Pull updates:
```bash
git fetch upstream
git merge upstream/main
```

3. Reapply your changes:
```bash
git stash pop
```

### If merge conflicts occur:
1. Open the conflicted files (marked in `git status`)
2. Look for conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
3. Edit files to resolve conflicts
4. Stage and commit the resolved files:
```bash
git add .
git commit -m "Resolve merge conflicts"
```

## Best Practices
- Always create a new branch for experiments
- Keep your main branch clean and in sync with upstream
- Commit changes frequently with clear messages
- Pull updates regularly to stay current

## Notes
- Your experiments and changes are safely stored in your fork
- You can have multiple experimental branches simultaneously
- The original repository remains unchanged by your experiments
