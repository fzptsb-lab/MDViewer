# MDViewer

A lightweight, zero-installation, single-file Markdown viewer that runs directly in any modern web browser. Browse individual markdown documents or entire folder trees with multi-tab browsing and clean GitHub typography.

---

## 🌟 Key Features

- **100% Portable**: A single, standalone HTML file. Double-click to open in any web browser without needing to install packages, run local background servers, or configure ports.
- **Multi-Tab Document Browsing**: Open multiple markdown files simultaneously in tabs, switch between them instantly, and close tabs as needed.
- **Multi-File & Folder Selection**: Load multiple individual `.md` files or upload entire folder structures at once using the toolbar buttons.
- **Hierarchical Folder Tree**: Automatically preserves directory hierarchies with collapsible `(+)` / `(-)` folders, item counts, and dark bullet indicators.
- **GitHub Markdown Styling**: Styled with `github-markdown-light.min.css` and powered by `marked.js` for authentic GitHub typography, tables, task lists, code blocks, and blockquotes.
- **Full-Screen Focus Mode**: Smooth collapsible sidebar (`«` / `☰ Menu`) to maximize reading area on any display.
- **Document Scroll Reset**: Automatically resets reading scroll position to the top whenever switching documents.
- **Clean Document Management**: Individual remove buttons (`✕`) for files/folders and a one-click **Clear All** action.

---

## 🚀 Getting Started

### Local Use (Direct from Disk)
1. Download or clone this repository.
2. Double-click `MDViewer.html` (or `index.html`) to open it in your default browser (Chrome, Edge, Firefox, Safari, or Brave).
3. Click **Files** to load one or more `.md` documents, or click **Folder** to import an entire documentation folder.

### Free Hosting via GitHub Pages
You can host your own live copy on GitHub Pages in under a minute:
1. Push this repository to your GitHub account.
2. Navigate to **Settings** > **Pages**.
3. Under **Build and deployment** > **Branch**, select `main` (or `master`) and folder `/ (root)`.
4. Click **Save**. Your viewer will be live at `https://<your-username>.github.io/<repo-name>/`.

---

## 🔒 Security, Privacy & Local Disk Isolation

### 1. 100% Client-Side Privacy
All markdown parsing, file reading, and rendering happen strictly inside your browser session using standard Web APIs (`FileReader` and `marked.js`). **No files, documents, text content, or telemetry are ever uploaded or transmitted to any server.** Your data never leaves your computer.

### 2. Browser Sandbox & Local Disk Policy (`file://`)
Modern web browsers (such as Google Chrome, Microsoft Edge, and Mozilla Firefox) enforce strict security boundaries when running pages locally via the `file://` protocol. 

To honor this security sandbox and prevent browser permission conflicts:
- The **Files** button utilizes `<input type="file" multiple>` to grant explicit, safe access to selected documents.
- The **Folder** button utilizes `<input type="file" webkitdirectory>` to safely scan nested markdown documents while preserving relative folder hierarchy paths.
- No background daemons, local HTTP ports (like `8080`), or native batch scripts are required.

### 3. External Dependencies & Offline Usage
`MDViewer` references two widely trusted, standard public CDNs for styling and rendering:
- `marked.min.js` (via jsDelivr CDN)
- `github-markdown-light.min.css` (via Cloudflare CDNJS)

If you require 100% offline or air-gapped usage, you can simply download both assets and inline them directly into the `<head>` of `MDViewer.html`.

---

## ⚠️ Disclaimer

This software is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the software or the use or other dealings in the software.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
