# macOS Quick Action: Image Resize & Convert (v16)

An Automator Quick Action for macOS to quickly resize, change compression, or convert image files directly from the Finder context menu.

This script uses the built-in macOS `sips` command-line tool for image manipulation.

## Features

- Right-click one or more image files in Finder.
- Choose "Image Resize & Convert" (or your action's name) from the Quick Actions menu.
- Select one of the following actions:

  - **Reduce File Size (Change Compression):**

    - Prompts to select JPG quality: High, Medium, Low, or Custom (0-100).
    - Prompts to select an output folder (once per batch).
    - Asks if you want to confirm/edit each filename individually _or_ use default names for the batch.
      - **Default Naming:** `OriginalName-compressed-QualityLabel.jpg` (e.g., `MyPhoto-compressed-Medium.jpg`, `MyPhoto-compressed-75%.jpg`). Collision avoidance (`-1`, `-2`, etc.) is automatically applied if using default naming.
      - **Confirm Each:** Prompts for each filename, defaulting to the name above. Relies on macOS to handle overwrites if the chosen name exists.
    - Output is always JPG.

  - **Resize Image (Change Dimensions):**

    - Prompts to select resize percentage: 75%, 50%, or 25%.
    - If PNG files are detected in the batch, asks _once_ whether to keep them as PNG or convert all PNGs to JPG for this batch run. Non-PNG files retain their original format.
    - Prompts to select an output folder (once per batch).
    - Asks if you want to confirm/edit each filename individually _or_ use default names for the batch.
      - **Default Naming:** `OriginalName.FinalExtension` (e.g., `MyPhoto.png`, `MyPngConverted.jpg`). Collision avoidance (`-1`, `-2`, etc.) is automatically applied if using default naming.
      - **Confirm Each:** Prompts for each filename, defaulting to the name above. Relies on macOS to handle overwrites if the chosen name exists.

  - **Quick Save as JPG (75%, Same Folder):**
    - Immediately saves a 75% quality JPG copy in the _same folder_ as the original file(s).
    - Automatically handles filename collisions by appending `-1`, `-2`, etc. if a file with the target name already exists.
    - No user interaction required beyond selecting the action.

## Installation

1.  **Download:** Go to the [Releases page](link-to-your-releases-page-if-you-create-one) of this repository OR click the green "Code" button and choose "Download ZIP".
2.  **Unzip:** If you downloaded a ZIP, unzip the file.
3.  **Locate:** Find the file named `Image Resize & Convert.workflow` (or the actual name of the workflow file) inside the folder.
4.  **Install:** Double-click the `.workflow` file. macOS should ask if you want to install the Quick Action. Click **Install**.
    - _Alternatively:_ Manually copy the `.workflow` file into your `~/Library/Services` folder. You can open this folder by clicking **Go > Go to Folder...** in Finder and entering `~/Library/Services`.

## Usage

1.  In Finder, select one or more image files (e.g., JPG, PNG, HEIC, TIFF).
2.  Right-click (or Control-click) on the selected file(s).
3.  Navigate to the **Quick Actions** sub-menu.
4.  Select **Image Resize & Convert** (or the name you see).
5.  Follow the on-screen dialog prompts based on the action you chose.

## Requirements

- macOS (tested on [Mention your macOS version, e.g., Sonoma 14.x])
- Uses the built-in `sips` command-line tool. No external dependencies are required.
