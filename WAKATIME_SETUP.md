# WakaTime Setup Guide

## Step 1: Create WakaTime Account
1. Visit https://wakatime.com
2. Sign up using your GitHub account (recommended) or email
3. Download the WakaTime extension for your IDE:
   - **VS Code**: Search for "WakaTime" in Extensions
   - **PyCharm**: Search for "WakaTime" in Plugins
   - **Sublime Text**: Via Package Control
   - Other IDEs: https://wakatime.com/plugins

## Step 2: Get Your API Key
1. Log in to https://wakatime.com
2. Go to Settings → API Key
3. Copy your API key (keep it secret!)

## Step 3: Add Secret to GitHub
1. Go to your repository on GitHub
2. Navigate to Settings → Secrets and variables → Actions
3. Click "New repository secret"
4. Name: `WAKATIME_API_KEY`
5. Value: Paste your API key
6. Click "Add secret"

## Step 4: Add WakaTime Plugin to Your Editor
1. Install the WakaTime plugin for your IDE
2. When prompted, paste your API key
3. That's it! It will automatically track your coding time

## Step 5: Trigger the Workflow
1. Go to your repo on GitHub
2. Click "Actions" tab
3. Select "Waka Readme" workflow
4. Click "Run workflow"
5. The README will be updated automatically

## Available Metrics

The workflow will display:
- **Coding time** (last 30 days or custom period)
- **Language breakdown** with percentages
- **Top languages** by time spent
- **Most edited files**
- **Coding insights** and trends
- **Project breakdown**

## Customization Options

Edit `.github/workflows/waka-readme.yml` to customize:

```yaml
SHOW_TITLE: true                    # Show WakaTime title
CODE_LANG_LIMIT: 10                # Number of languages to show
TIME_RANGE: "last_30_days"         # last_7_days, last_30_days, last_90_days, last_year, all_time
SHOW_SHORT_STATS: true             # Show summary stats
SHOW_COMMIT_STATS: true            # Show commit breakdown
SHOW_LANGUAGE_PER_REPO: true       # Show languages per repository
SHOW_PROFILE_VIEWS: true           # Show profile view count
```

## Tips for Best Results

1. **Keep the plugin running**: Ensure WakaTime plugin stays enabled in your IDE
2. **Privacy settings**: Adjust visibility settings on wakatime.com as needed
3. **Multiple devices**: Install WakaTime on all your development machines
4. **Automatic updates**: The GitHub Action runs daily at 12:00 AM UTC

For more info, visit: https://github.com/athul/waka-readme
