# Python Script for GitHub CLI Extension Overview 🐍🔧

This script is designed to be used as an extension for the GitHub command-line tool. It performs a variety of repository management and dependency-checking operations within a Git repository.

## 1. Searching `.gitmodules` File 🔍

- **Function:** `search_gitmodules()`
- **Description:** Searches for URLs in the `.gitmodules` file, if it exists.
- **Output:** A list of extracted URLs.

## 2. Parsing URLs 🌐

- **Function:** `parse_url(line)`
- **Description:** Extracts URLs from a given line using regular expressions.

## 3. Checking Directories 📂

- **Function:** `check_directories(directories)`
- **Description:** Compares a list of directories with the current directories in the base path.
- **Output:** List of found directories that match the given list.

## 4. Searching `.tf` Files for Git HTTPS URLs 🗃️

- **Function:** `search_tf_files_for_git_https()`
- **Description:** Looks for `git::https` URLs in `.tf` files.
- **Output:** A list of extracted Terraform Git HTTPS URLs.

## 5. Extracting Terraform Git HTTPS URLs 📜

- **Function:** `extract_tf_git_url(line)`
- **Description:** Extracts Terraform Git HTTPS URLs from a line using regular expressions.

## 6. Listing Workflow Files in `.github/workflows` 🔄

- **Function:** `list_workflow_files()`
- **Description:** Lists YAML or YML files in the `.github/workflows` directory.
- **Output:** A list of workflow files.

## Main Execution 🚀

- **Operations:**
  - Gets the current working directory's base name.
  - Gathers URLs from `.gitmodules` and `.tf` files.
  - Checks specified directories.
  - Lists workflow files.

- **Output:** Prints a CSV-formatted line to the console with the following information:
  - Base directory name.
  - Count of found directories.
  - Concatenated URLs.
  - Found directories.
  - Workflow files.

## Intended Use 🎯

- This script is intended to be used as an extension with the GitHub command-line tool, enhancing its capabilities for repository analysis and management.
