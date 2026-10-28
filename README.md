# Week 3 Lab — Source Code Management using GitHub

## Aim
Practice source code management on GitHub by creating a repository, committing a source file, and pushing it to GitHub.

## Files
- `index.html` — simple event registration form with HTML, CSS, and JavaScript.

## Step-by-step execution (Windows)

### 1. Install/check the tools
1. Install Git from https://git-scm.com/downloads if it is not installed.
2. Install Visual Studio Code, or use another text editor.
3. Sign in to https://github.com.

Open Command Prompt or the VS Code terminal and run:
```bash
git --version
```
If Git prints a version number, it is available.

### 2. Run the web page locally
1. Extract this ZIP file.
2. Open the `Week3_GitHub_Source_Code_Management` folder in VS Code.
3. Open `index.html` in a browser (double-click it in File Explorer).
4. Enter the details and press **Register** to test the form.

### 3. Create a GitHub repository
1. On GitHub, click **New repository**.
2. Repository name: `Week3`
3. Choose **Public** (or your class-required visibility).
4. For the simplest first push, leave **Add a README file** unchecked.
5. Click **Create repository**.
6. Copy the HTTPS repository URL shown by GitHub.

### 4. Open a terminal in the project folder
In VS Code, choose **Terminal → New Terminal**. Confirm the terminal is inside this folder. If not, use `cd` to navigate to it.

### 5. Initialize Git and push the file
Run these commands one at a time. Replace the name, email, and repository URL with your own details.

```bash
git init
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
git add index.html
git commit -m "Added event registration form"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/Week3.git
git push -u origin main
```

Important:
- Replace `https://github.com/YOUR-USERNAME/Week3.git` with the exact HTTPS URL copied from your GitHub repository.
- GitHub may open a browser sign-in/authorization step. Complete it if prompted.
- If `git remote add origin` says `origin already exists`, run `git remote set-url origin YOUR-REPOSITORY-URL` instead.
- The lab manual uses `master` in its example. This guide uses `main`; use the branch name your repository/class requires.

### 6. Verify the result
1. Refresh your GitHub repository page.
2. Confirm that `index.html` is listed.
3. In the terminal, run:
```bash
git status
```
A clean repository should report that the working tree is clean.

## Common errors
- **`git` is not recognized:** install Git, then close and reopen the terminal.
- **Authentication failed:** complete GitHub's browser authentication, or follow GitHub's current sign-in instructions.
- **Wrong remote URL:** copy the HTTPS URL from the repository page and set it with:
  `git remote set-url origin https://github.com/YOUR-USERNAME/Week3.git`
- **`src refspec main does not match any`:** make sure you successfully ran `git add index.html` and `git commit` before pushing.

## Expected result
The event registration page works in a browser, and `index.html` is uploaded to your GitHub repository.
