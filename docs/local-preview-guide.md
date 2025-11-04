# Previewing the Site Locally

These steps walk you through finding your project folder and starting a local preview server. Follow them in order—each step has the exact commands to type.

## 1. Find the project folder path

1. **Open your file manager** (Finder on macOS, File Explorer on Windows, or your Linux file browser).
2. **Navigate to the folder that contains this project.** If you downloaded a ZIP or cloned from GitHub, look for a folder named `dca` (or the name you chose).
3. Once you can see the files (like `index.html`, `style.css`, and the `js` folder), copy the full path:
   - **macOS:** Press `⌘ + ↑` until you see the project folder highlighted, then choose **Edit → Copy “dca” as Pathname**.
   - **Windows:** Click the address bar at the top of File Explorer; it will change to the full path. Press `Ctrl + C` to copy it.
   - **Linux:** Right-click the folder name and choose **Copy** or **Copy Location**, depending on your file manager.

> ✅ Tip: If you’re not sure whether you’re in the right place, make sure you can spot files like `index.html` and folders like `news` or `careers`. That’s the root of the project.

## 2. Open a terminal window

- **macOS:** Open Spotlight (`⌘ + Space`), type `Terminal`, and press Enter.
- **Windows:** Press `Start`, type `cmd` or `PowerShell`, and open it.
- **Linux:** Use your application launcher and search for “Terminal”.

## 3. Move (change directory) into the project folder

1. In the terminal, type `cd ` (include the trailing space).
2. Paste the path you copied earlier:
   - macOS: `⌘ + V`
   - Windows/Linux: `Ctrl + V`
3. Press Enter. Your prompt should now show the project folder. To double-check, type:
   ```bash
   ls
   ```
   or on Windows Command Prompt:
   ```cmd
   dir
   ```
   You should see files like `index.html`, `style.css`, and folders such as `js` and `news`.

## 4. Start a simple preview server

With Python 3 installed (comes with macOS and most Linux distributions, and is easy to install on Windows):

```bash
python3 -m http.server 8000
```

If your system only recognizes `python`, try:

```bash
python -m http.server 8000
```

Keep this terminal window open—the server will keep running until you stop it.

### Windows: "Python was not found" message

If you see the message **“Python was not found; run without arguments to install from the Microsoft Store…”**, it means Python
isn’t installed yet (the shortcut that forwards you to the Microsoft Store is just a placeholder). Do this:

1. Visit [python.org/downloads](https://www.python.org/downloads/) in your browser.
2. Download the latest **Windows installer (64-bit)**.
3. Run the installer and **check “Add python.exe to PATH”** on the first screen, then click **Install Now**.
4. When the installer finishes, close and reopen your Command Prompt/PowerShell window.
5. Try the server command again. On Windows you can use either:
   ```powershell
   python -m http.server 8000
   ```
   or
   ```powershell
   py -3 -m http.server 8000
   ```

If you prefer using the Microsoft Store version, click the link in the error message, install Python, then restart your terminal
and run the same command (`python -m http.server 8000`).

## 5. View the site in your browser

1. Open your favorite browser (Chrome, Safari, Firefox, Edge, etc.).
2. Type `http://localhost:8000/` into the address bar and press Enter.
3. The site will load exactly as it would on a real web host. Use your browser’s mobile device emulator or resize the window to test the mobile menu.

## 6. Stop the server when you’re done

Return to the terminal window that’s running the server and press `Ctrl + C`. You’ll be back at the command prompt, ready to start again later.

---

If anything doesn’t look right, double-check the earlier steps—especially that you’re inside the correct folder before starting the server. Feel free to repeat the process each time you make changes so you can instantly preview your updates.
