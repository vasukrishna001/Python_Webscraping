# Web Scraping Project - Auto Sorting Files and Challenges

## Project Overview
This project involves **web scraping** to extract cricketer data and manage the scraped files by **automatically sorting** them based on their types (extensions) using Python. Additionally, the project includes the functionality to **undo** the sorting operation and restore the original structure. 

The web scraping script retrieves data about cricketers from an online source, but due to limitations with **BeautifulSoup** (which only extracts visible content before loading the entire page), not all players could be retrieved. The project aims to organize the resulting data files in a manner that makes it easier for users to access and analyze.

---

## Key Features:
1. **Web Scraping**: Extracts cricketer data from a web page. However, due to the limitation of BeautifulSoup's ability to scrape only visible content, the script may not retrieve the entire list of players.
2. **File Sorting**: Automatically sorts the downloaded files based on their types (extensions), such as `.csv`, `.jpg`, `.txt`, etc.
3. **Undo Sorting**: Allows you to revert the file sorting and move the files back to the original location.

---

## Challenges Faced:
- **Web Scraping Limitation**:
  The main challenge faced in this project was that **BeautifulSoup** could only extract content that was directly visible when the page was loaded. However, the cricketer data was revealed only after further page interactions, which BeautifulSoup wasn't able to handle. As a result, only a limited number of cricketers were scraped from the page.

  **Problem**: BeautifulSoup does not handle dynamically loaded content (like data revealed after page buffering).
  **Solution**: Consider using other tools like **Selenium** or **Playwright** to handle dynamic content scraping.

---

## File Sorting Functionality

### 1. **sort_files(path)**
   - **Description**: Automatically organizes files into folders based on their extensions. For example, all `.txt` files will go into a folder named `txt`, `.csv` files into a folder named `csv`, etc.
   - **Functionality**:
     - Identifies the unique file types in the given directory.
     - Creates folders for each file type.
     - Moves the files into their respective folders.

### 2. **undo_sort(path)**
   - **Description**: Reverts the file sorting operation by moving all files back to their original location and removing the empty folders created during sorting.
   - **Functionality**:
     - Moves files from the subdirectories back to the main directory.
     - Deletes the empty subdirectories after restoring the files.

### 3. **user_choice()**
   - **Description**: Prompts the user to choose between sorting files or undoing the sorting operation.
   - **Functionality**:
     - Based on the user's input (1 for sorting, 2 for undoing), it calls either `sort_files()` or `undo_sort()`.

---

## How to Use

1. **Run the Program**:
   - The program will ask whether you want to sort the files or undo the sorting operation.

2. **Sort Files**:
   - Choose option 1 to sort files by type. Enter the path to the directory where the files are stored, and the program will sort them into folders based on their extensions.

3. **Undo Sorting**:
   - Choose option 2 to undo the sorting. Provide the directory path where the files were sorted, and the program will move the files back to the original location and delete the subfolders.

---

## Example

### Example 1: Sorting Files
```bash
Do you want to (1) Sort files or (2) Undo sorting? Enter 1 or 2: 1
Enter the path to the directory to sort files: /path/to/your/directory
