# 🚀 My GitHub Activity Game

<p align="center">
  <img src="assets/space-shooter.gif" alt="GitHub Space Shooter Game" />
</p>

---

## 👋 About This Project

This README features an **automated Space Shooter game** that visualizes my GitHub contribution graph! The game updates automatically every day using GitHub Actions.

- 🎮 **Contribution-based gameplay**: Each square in my GitHub activity becomes an enemy
- ⚡ **Auto-updating**: The game regenerates daily with my latest contributions
- 🎨 **Dynamic strategies**: Uses random attack patterns for variety

---

## 🛠️ How It Works

This project uses the [`gh-space-shooter`](https://github.com/czl9707/gh-space-shooter) GitHub Action to:
1. Fetch my GitHub contribution data
2. Generate an epic space shooter animation
3. Automatically commit the updated GIF to this repo

The workflow runs daily at midnight UTC and can also be triggered manually.

---

## 🎯 Want Your Own?

Follow these simple steps to add this to your GitHub profile:

### Step 1: Create a Repository
- Create a new repository named **`<your-username>`** (same as your GitHub username)
- Make it **PUBLIC**
- Initialize with a `README.md`

### Step 2: Create Workflow File
Create `.github/workflows/space-shooter.yml`:

```yaml
name: Update Space Shooter GIF

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      
      - name: Create assets directory
        run: mkdir -p assets
      
      - uses: czl9707/gh-space-shooter@v1
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
          output-path: assets/space-shooter.gif
          strategy: random
```

### Step 3: Update Your README
Add this to your `README.md`:

```markdown
# 🚀 My GitHub Activity Game

<p align="center">
  <img src="assets/space-shooter.gif" />
</p>
```

### Step 4: Run the Workflow
- Go to **Actions** tab in your repo
- Click **Update Space Shooter GIF**
- Click **Run workflow**
- Wait for it to complete!

### Step 5: Verify
The workflow will automatically create `assets/space-shooter.gif` and your game will appear on your profile!

---

## 🔗 Original Project

This uses the awesome [gh-space-shooter](https://github.com/czl9707/gh-space-shooter) project.

**Try it yourself:**
- 🌐 [Web Interface](https://gh-space-shooter.kiyo-n-zane.com) - Generate instantly without setup
- 📦 [PyPI Package](https://pypi.org/project/gh-space-shooter/) - Install with `pip install gh-space-shooter`
- 🎮 [GitHub Action](https://github.com/marketplace/actions/github-space-shooter) - Automate on your profile

---

## 📬 About the Author

**Md Farid** – Web Developer | Open Source Enthusiast | Automation Lover

### Connect With Me:
- 🐦 **X (Twitter)**: [@MdFarid7886](https://x.com/MdFarid7886)
- 💼 **LinkedIn**: [md-farid-1aa563291](https://www.linkedin.com/in/md-farid-1aa563291/)

---

<p align="center">
  <i>If this helped you, feel free to share and tag me! ⭐</i>
</p>
