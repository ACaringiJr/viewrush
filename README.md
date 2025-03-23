# DocuDash: Instant Document Viewer

![DocuDash Logo](docudash-logo-128.png)  
**Quickly open documents and media files in your browser with a right-click or local upload.**

DocuDash is a Chrome extension that lets you view a wide range of file types—documents (e.g., `.docx`, `.pdf`), spreadsheets (e.g., `.xlsx`), presentations (e.g., `.pptx`), images (e.g., `.png`), audio (e.g., `.mp3`), and video (e.g., `.mp4`)—directly in your browser. Right-click links or elements like buttons on webpages, or upload local files via the popup, and DocuDash handles the rest.

## Features
- **Right-Click Viewing**: Open supported files from webpage links or buttons using the context menu ("Open Document in Browser").
- **Local File Upload**: Drag and drop or browse local files in the popup to view them instantly.
- **Wide Format Support**: Works with `.docx`, `.pdf`, `.xlsx`, `.pptx`, `.png`, `.mp3`, `.mp4`, and more via services like Microsoft Office Online and Google Docs Viewer.
- **Privacy-Friendly**: Local files like PDFs and images open via blob URLs; others upload temporarily to tmpfiles.org (deleted after 60 minutes).

## Installation

### From Chrome Web Store
1. Visit the [DocuDash Chrome Web Store page](#) (link TBD after publication).
2. Click "Add to Chrome" and confirm the installation.
3. Pin the extension to your toolbar for easy access.

### From Source (Developer Mode)
1. Download the `docudash-extension.zip` file from the [Releases](https://github.com/acaringijr/docudash/releases) page.
2. Extract the ZIP file to a folder on your computer.
3. Open Chrome and navigate to `chrome://extensions/`.
4. Enable "Developer mode" (top right).
5. Click "Load unpacked" and select the extracted `docudash-extension` folder.
6. The extension will appear in your toolbar.

## Usage

### Right-Click on Webpages
1. Find a file link (e.g., `report.docx`) or button referencing a file on any webpage.
2. Right-click it and select **"Open Document in Browser"**.
3. The file opens in a new tab using an appropriate viewer (e.g., Office Online for `.docx`, direct view for `.pdf`).

### Upload Local Files
1. Click the DocuDash icon in your toolbar to open the popup.
2. Drag a file into the "Drag & Drop a File Here" area or click "Browse Files".
3. Click "Upload"
4. The file opens in a new tab.

*Note*: Files uploaded to tmpfiles.org are temporary (60-minute lifespan) and unlikely to be seen by others, though not impossible.

## Supported File Types
- **Documents**: `.docx`, `.doc`, `.pdf`, `.rtf`, `.odt`, `.txt`
- **Spreadsheets**: `.xlsx`, `.xls`, `.ods`, `.csv`
- **Presentations**: `.pptx`, `.ppt`, `.odp`
- **Images**: `.png`, `.jpg`, `.jpeg`, `.gif`, `.bmp`
- **Media**: `.mp3`, `.mp4`, `.wav`
- **Web**: `.html`, `.htm`

## Development

### Prerequisites
- Chrome browser
- Basic knowledge of JavaScript, HTML, and Chrome extensions

### Project Structure
- `background.js`: Handles context menu actions and tab creation.
- `content.js`: Detects right-clicks on non-link elements (e.g., buttons).
- `popup.html` / `popup.js`: Manages the file upload interface.
- `manifest.json`: Defines extension permissions and structure.

### Build & Test
1. Modify the code as needed.
2. Reload the extension in `chrome://extensions/` after changes.
3. Test with the sample page (`index.html`) or real websites.

## Permissions
- `contextMenus`: Adds the right-click option.
- `tabs`: Opens files in new tabs.
- `activeTab`: Processes right-clicked elements in the current tab.

No unnecessary permissions are requested.

## Contributing
1. Fork this repository.
2. Create a feature branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m "Add feature"`).
4. Push to your fork (`git push origin feature-name`).
5. Open a pull request.

## License
This project is licensed under the MIT License:
