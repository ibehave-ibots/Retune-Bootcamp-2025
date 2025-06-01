# Git Essentials for Researchers

This lesson covers the most essential operations in Git for everyday use: **staging**, **committing**, **pushing** changes to GitHub, and **cloning** remote repositories to your local machine. These are the core actions that allow you to track your work, collaborate with others, and access your projects from anywhere.

---

## Section 1: Tracking Changes (Staging)

Git helps track changes in your project by monitoring file modifications. You can check the status of your changes, add files to the staging area, and unstage them if needed.

| Command               | Description                                              | VS Code GUI                                                                     |
| --------------------- | -------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `git init`            | Initialize a new Git repository in the current directory | Click **Source Control (Ctrl + Shift + G)** → Click **"Initialize Repository"** |
| `git status`          | Show the status of changes in the working directory      | Click **Source Control (Ctrl + Shift + G)** → See the file changes              |
| `git add file1.txt`   | Stage `file1.txt` for commit                             | Click **➕ (plus) icon** next to the file in **Source Control**                  |
| `git add .`           | Stage all modified and new files                         | Click **➕ (plus) icon** next to each file OR Click **"Stage All Changes"**      |
| `git reset file1.txt` | Unstage `file1.txt`                                      | Click **➖ (minus) icon** next to the file to move it back to "Changes"          |

**Exercises**

1. Initializing a Git repository

   * Open a new folder for your project.
   * Initialize a Git repository in this folder.
   * Check the status of the repository using `git status`.

2. Tracking files and changes

   * Create and stage `experiment_1.txt`.
   * Create `experiment_2.txt` and `experiment_3.txt`. Stage both together.
   * Unstage `experiment_3.txt` and check status.
   * Delete `experiment_3.txt` and check status.

---

## Section 2: Committing Changes and Viewing History

Once staged, changes can be committed with a message describing what was done. Commits are snapshots of your project over time.

| Command                    | Description                                | VS Code GUI                                 |
| -------------------------- | ------------------------------------------ | ------------------------------------------- |
| `git add f1.txt f2.txt`    | Stage specific files for commit            | Click **➕ (plus) icon** next to the files   |
| `git commit -m "Message"`  | Commit staged files with a message         | Click **✔ (checkmark)** and enter a message |
| `git add .`                | Stage all files                            | Click **"Stage All Changes"**               |
| `git commit -am "Message"` | Stage and commit in one step               | Click **✔ (checkmark)**                     |
| `git log`                  | View full commit history                   | N/A                                         |
| `git log --oneline`        | Compact commit history                     | N/A                                         |
| `git log -2`               | Show last two commits                      | N/A                                         |
| `git diff`                 | Compare working directory with last commit | Click on file to view inline diff           |
| `git diff <hash1> <hash2>` | Compare two commits                        | N/A                                         |

**Exercises**

1. Committing changes

   * Commit `experiment_1.txt` and `experiment_2.txt` with message "create files".
   * Add data to `experiment_1.txt` and commit with "add data to exp 1".
   * Modify both files and commit with a suitable message.
   * Stage and commit in one step.

2. View history

   * View full history.
   * View compact history.
   * View last three commits.

3. Comparing differences

   * Compare current state to last commit.
   * Compare two specific commits.

---

## Section 3: Pushing a Local Repository to GitHub

Once you’ve committed changes locally, push them to GitHub to store them online and collaborate.

| Command                       | Description                   | VS Code GUI                                                          |
| ----------------------------- | ----------------------------- | -------------------------------------------------------------------- |
| `git remote add origin <URL>` | Link local repo to GitHub     | Click **Source Control (Ctrl + Shift + G)** → **Publish Repository** |
| `git push -u origin main`     | Push commits and set upstream | Click **...** → **Push**                                             |

**Exercises**

1. Pushing initial commit

   * Open local repo in VS Code.
   * Create **public** GitHub repo **without README**.
   * Add remote URL with `git remote add origin <repo-url>`.
   * Push with `git push -u origin main`.
   * Check GitHub.

2. Pushing new file

   * Add a file, commit locally.
   * Push with `git push -u origin main`.
   * Verify on GitHub.

3. Pushing changes

   * Modify a file, commit locally.
   * Push to GitHub.
   * Confirm on GitHub.

---

## Section 4: Cloning a GitHub Repository to a Local Machine

Clone an existing GitHub repository to your local system to begin working on it.

| Command                | Description                    | VS Code GUI                |
| ---------------------- | ------------------------------ | -------------------------- |
| `git clone <repo-url>` | Clone a repo locally           | Click **Clone Repository** |
| `git pull origin main` | Get latest changes from GitHub | Click **...** → **Pull**   |

**Exercises**

*Start in a fresh folder that is not a Git repository.*

1. Cloning a public repository

   * Note the [workshop GitHub repo](https://github.com/ibehave-ibots/iBOTS-Essential-Computer-Tools-for-Researchers-Workshop).
   * Run `git clone <repo-url>`.
   * Open the cloned folder and verify files.

2. Cloning your own repository

   * Create **public** GitHub repo **with README**.
   * Clone the repository using URL.
   * Check that README exists.

3. Pulling updates

   * Edit README directly on GitHub.
   * Run `git pull origin main`.
   * Confirm local changes are updated.
