# 🚀 macOS Quick Action: Image Resize & Convert (v16)

**Problem:** 😩 Opening heavy image editors (like Photoshop) or fiddling with clunky online tools just to resize, compress, or convert an image? It's slow and interrupts your workflow!

**Solution:** ✨ This Automator Quick Action brings essential image adjustments directly into your macOS Finder context menu (right-click!).

---

Need to quickly shrink photos for your website? 🖼️➡️🤏 Make images smaller for email attachments? 📎 Batch-convert PNGs to JPGs without leaving Finder? 🔄 This tool provides a **lightweight, fast, and efficient** way to handle common image tasks.

It leverages macOS's built-in `sips` command-line tool, so **no extra software or dependencies** are required!

## 🤔 Why Use This?

- **⚡️ Speed:** Stop waiting for bulky apps to load for simple tasks.
- **🖱️ Convenience:** Everything is right there in your Finder right-click menu. Stay in your flow!
- **⚙️ Batch Processing:** Select multiple images and process them all in one go. Huge time saver!
- ** гибкость (Flexibility):** Choose quick automatic saves or get more control with folder selection and optional filename confirmation.
- **✅ Simple & Native:** Uses built-in macOS tools you already have. No installs needed (besides the Quick Action itself!).

---

## ✨ Features

- Right-click one or more image files in Finder.
- Choose "**Image Resize & Convert**" (or your action's name) from the **Quick Actions** menu.
- Select one of the following actions:

  - **Reduce File Size (Change Compression):**

    - Prompts to select JPG quality: High, Medium, Low, or **Custom...** (0-100).
    - Prompts to select an output folder (once per batch).
    - Asks if you want to confirm/edit each filename individually _or_ use default names for the batch.
      - _Default Naming:_ `OriginalName-compressed-QualityLabel.jpg` (e.g., `MyPhoto-compressed-Medium.jpg`, `MyPhoto-compressed-75%.jpg`). Collision avoidance (`-1`, `-2`, etc.) is automatically applied.
      - _Confirm Each:_ Prompts for each filename, defaulting to the name above. Relies on macOS to handle overwrites if the chosen name exists.
    - Output is always JPG.

  - **Resize Image (Change Dimensions):**

    - Prompts to select resize percentage: 75%, 50%, or 25%.
    - If PNG files are detected in the batch, asks _once_ whether to **Keep PNG** or **Convert PNGs to JPG** for this batch run. Non-PNG files retain their original format.
    - Prompts to select an output folder (once per batch).
    - Asks if you want to confirm/edit each filename individually _or_ use default names for the batch.
      - _Default Naming:_ `OriginalName.FinalExtension` (e.g., `MyPhoto.png`, `MyPngConverted.jpg`). Collision avoidance (`-1`, `-2`, etc.) is automatically applied.
      - _Confirm Each:_ Prompts for each filename, defaulting to the name above. Relies on macOS to handle overwrites if the chosen name exists.

  - **Quick Save as JPG (75%, Same Folder):**
    - Instantly saves a 75% quality JPG copy in the _same folder_ as the original file(s).
    - Automatically handles filename collisions by appending `-1`, `-2`, etc.
    - No user interaction needed beyond selecting the action. Super fast! 💨

---

## 🛠️ Installation

1.  **Download:**
    - Go to the [**Releases Page**](link-to-your-releases-page-if-you-create-one) of this repository (Recommended for easiest download).
    - OR click the green **Code** button above and choose **Download ZIP**.
2.  **Unzip:** If you downloaded a ZIP, unzip the file. You should find the `.workflow` file inside.
3.  **Locate:** Find the file named `Image Resize & Convert.workflow` (or the actual name of the workflow file).
    - **Important:** Make sure you are using the `.workflow` file _after_ unzipping, not the ZIP file itself!
4.  **Install:**
    - **Double-click** the `.workflow` file.
    - macOS should ask if you want to install the Quick Action. Click **Install**.
    - _(Alternatively):_ Manually copy the `.workflow` file into `~/Library/Services`. (In Finder, click **Go > Go to Folder...** and enter `~/Library/Services`).

---

## 🚀 Usage

1.  In Finder, select one or more image files (e.g., JPG, PNG, HEIC, TIFF).
2.  **Right-click** (or Control-click) on the selected file(s).
3.  Navigate to the **Quick Actions** sub-menu.
4.  Select **Image Resize & Convert** (or the name you see).
5.  Follow the on-screen dialog prompts based on the action you chose. Enjoy the speed!

---

## ✅ Requirements

- macOS (tested on [Mention your macOS version, e.g., Sonoma 14.x])
- Uses the built-in `sips` command-line tool. No external dependencies are required.

---

## 📜 License & Disclaimer

This script is shared freely in the hope that it's useful, but please use it thoughtfully! It's provided "as is" without any guarantees. While it's designed to work safely, the author isn't responsible for any unexpected behavior or data loss that might occur from its use. Always make sure you have backups of important images before processing them, just in case. Feel free to modify and share it!
