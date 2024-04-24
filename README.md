# task2

note:- it does not open in normal browser.The browser should disable its securities due to cross orgin issue.
we should ues the commend called "chrome.exe --user-data-dir="C://chrome-dev-disabled-security" --disable-web-security --disable-site-isolation-trials"

# Updating Data from Google Sheets

This repository demonstrates how to pull data from a Google Sheets spreadsheet and update the repository with the latest information. Follow the steps below to understand and implement this process.

## Overview

The process involves publishing a Google Sheets spreadsheet to the web in TSV (Tab-separated values) format, modifying the `pull-sheet/index.html` page to fetch data from the published spreadsheet, creating a GitHub token for programmatic access to the repository, and running the `pull-sheet` script to update the repository with the latest data.

## Steps to Update Data

1. **Publish Google Sheets Spreadsheet**:
   - Open your Google Sheets spreadsheet.
   - Go to File > Share > Publish to the web.
   - Choose the format "Tab-separated values (tsv)" and click "Publish."
   - Copy the generated link, which will be used to access the data programmatically.

2. **Modify `pull-sheet/index.html` Page**:
   - Open the `pull-sheet/index.html` file in your code editor.
   - Update the URL in the JavaScript code to point to your published TSV file.

3. **Create a GitHub Token**:
   - Go to your GitHub account settings.
   - Navigate to Developer settings > Personal access tokens.
   - Click on "Generate new token" and give it appropriate permissions (e.g., repo access).
   - Copy the generated token, which will be used to programmatically access and update the repository.

4. **Update GitHub Token in the URL**:
   - Replace `ghp_...` in the URL (`/pull-sheet/?ghtoken=ghp_...`) with your generated GitHub token.

5. **Run the Pull-Sheet Script**:
   - Navigate to the `/pull-sheet/?ghtoken=ghp_...` URL in your web browser.
   - This will trigger the script to pull data from the Google Sheets spreadsheet and update your repository with the latest data.

## Example

For a practical demonstration, refer to the `pull-sheet` directory in this repository.

## Contributing

Contributions are welcome! If you have suggestions for improving this process or encounter any issues, feel free to open an issue or submit a pull request.
