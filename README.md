## 📄 Repository Description

**Restore Manifest V2 Extensions in Chrome**

This repository provides a workaround to continue using Manifest V2 browser extensions in Chromium-based browsers (such as Google Chrome, Brave, and Edge) even after Manifest V3 becomes the default. Many extensions—including **uBlock Origin (Legacy MV2)**—still rely on Manifest V2 for full functionality, but Google has begun phasing it out.

This repo documents the process of re-enabling support for Manifest V2 via hidden Chrome flags and manually installing extensions in developer mode. The approach is intended for personal use, testing, and preserving functionality of legacy extensions.

⚠️ **Disclaimer**: This is an unsupported method. Future browser updates may break it at any time.

Credit for this method belongs to [Tech Decode](https://www.youtube.com/@techdecode85).

---

## 🛠️ Guide: How to Restore Manifest V2 Extensions

### 1. Enable Chrome Flags

1. Open Chrome (or your Chromium-based browser).

2. In the address bar, type:

   ```
   chrome://flags
   ```

   and press **Enter**.

3. In the search bar, type: `unexpire`

   * Locate: **Temporarily unexpire M138 flags**
   * Locate: **Temporarily unexpire M139 flags**
   * Set both to **Enabled**.
   * Click the **Relaunch** button in the bottom right corner.

4. Search again, this time for: `allow legacy`

   * Locate: **Allow legacy extension manifest versions**
   * Set it to **Enabled**.
   * Click **Relaunch**.

---

### 2. Download & Prepare uBlock Origin (MV2)

1. Visit the official **uBlock Origin GitHub Releases** page.
2. Download the **source code zip** file.
3. Extract (unzip) the file.
4. Rename the extracted folder to:

   ```
   uBlock
   ```
5. Move this folder to a permanent location on your system (since Chrome will always reference it from there).

---

### 3. Load Extension in Developer Mode

1. In the Chrome address bar, type:

   ```
   chrome://extensions
   ```

   and press **Enter**.

2. In the top right, toggle **Developer mode** to **ON**.

3. Click **Load unpacked**.

4. Navigate to the folder you renamed (`uBlock`) and select it.

The extension will now appear in your list of installed extensions.

---

### 4. Notes

* The extension will work normally, but you will see a **warning about Manifest V2**.
* This process can be repeated for other Manifest V2 extensions you want to keep.
