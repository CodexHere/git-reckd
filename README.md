# git-reckd

**GIT-REcursively-cheCKeD**

A Bash script to recursively scan directories for Git repositories, check their status, and perform automated actions like committing, pushing, and pulling changes.

## Overview

`git-reckd` is a command-line tool designed to streamline Git repository management across multiple projects. It recursively searches for Git repositories in a specified directory (or the current directory by default), checks their status (clean, dirty, needs push, or needs pull), and provides an interactive menu to update repositories individually or all at once. The script includes colorful output and intuitive icons for a user-friendly experience.

## Features

- **Recursive Repository Discovery**: Automatically finds all Git repositories in the specified directory and its subdirectories.
- **Status Checking**: Displays the status of each repository, indicating:
  - **Clean** (✔): No uncommitted changes.
  - **Dirty** (⚠): Uncommitted changes present.
  - **Needs Push** (↑): Local commits need to be pushed to the remote.
  - **Needs Pull** (↓): Remote changes need to be pulled locally.
- **Interactive Menu**: Choose to:
  - Update a specific repository (commit, push, or pull).
  - Update all repositories at once.
  - Refresh the status of all repositories.
  - Exit the script.
- **Automated Commits**: Option to automatically stage and commit changes with a standardized commit message.
- **Color-Coded Output**: Uses colors (green, red, yellow, blue) and icons to clearly indicate repository status.
- **Error Handling**: Skips non-Git directories and handles invalid user inputs gracefully.

## Installation

1. Clone or download the repository:
   ```bash
   git clone https://github.com/CodexHere/git-reckd.git
   ```
2. Navigate to the project directory:
   ```bash
   cd git-reckd
   ```
3. Make the script executable:
   ```bash
   chmod +x git-reckd
   ```
4. (Optional) Move `git-reckd` to a directory in your PATH (e.g., `/usr/local/bin`):
   ```bash
   mv git-reckd /usr/local/bin/git-reckd
   ```

## Usage

Run the script from the command line, optionally specifying a directory to scan:

```bash
./git-reckd [path]
or
git reckd # must be in user's PATH
```

- If no path is provided, the script scans the current directory (`.`).
- The script displays a list of detected repositories with their statuses and an interactive menu.

### Example

```bash
./git-reckd ~/projects
```

This scans the `~/projects` directory for Git repositories and presents a menu to manage them.

### Menu Options

1. **Update specific repository**: Select a repository by number to view its status, review changes, and optionally commit, push, or pull.
2. **Update all repositories**: Automatically processes all repositories (commit, push, or pull as needed).
3. **Refresh status**: Re-scans repositories and updates their statuses.
4. **Exit**: Quits the script.

## Requirements

- **Bash**: The script requires a Bash-compatible shell.
- **Git**: Git must be installed and available in the system PATH.
- **Unix-like System**: Tested on Linux and macOS. May require modifications for Windows (e.g., via WSL).

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes and commit (`git commit -m "Add your feature"`).
4. Push to your branch (`git push origin feature/your-feature`).
5. Open a pull request.

Please ensure your code follows the existing style and includes appropriate comments.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Issues and Feedback

If you encounter any issues or have suggestions, please open an issue on the [GitHub repository](https://github.com/CodexHere/git-reckd/issues).