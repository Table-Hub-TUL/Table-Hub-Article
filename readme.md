## Installation and Usage Instructions

### Installing MikTeX on Windows

1.  **Download MikTeX:** Go to the official MikTeX website ([https://miktex.org/download](https://miktex.org/download)) and download the installer for Windows.
2.  **Run the Installer:** Execute the downloaded installer. Follow the on-screen instructions. It is recommended to allow MikTeX to install missing packages on-the-fly.
3.  **Add MikTeX to PATH:**
    *   Search for "Environment Variables" in the Windows search bar and open "Edit the system environment variables".
    *   Click on "Environment Variables...".
    *   In the "System variables" section, find the "Path" variable and select it, then click "Edit...".
    *   Click "New" and add the path to the MikTeX binaries. The default path is usually `C:\Program Files\MiKTeX 2.9\miktex\bin\x64` (adjust the `MiKTeX 2.9` part to your installed version if different).
    *   Click "OK" to close all environment variables windows.

### Using the `compile.ps1` Script

This script automates the LaTeX compilation process using XeLaTeX.

1.  **Save the Script:** Save the provided `compile.ps1` script to a directory of your choice (e.g., your LaTeX project directory).
2.  **Create a PowerShell Profile (if you don't have one):**
    *   Open PowerShell.
    *   Check if you have a profile by typing `$PROFILE` and pressing Enter. If it returns a path, you have a profile. If it returns nothing or an error, you need to create one.
    *   To create a profile, type `New-Item -ItemType File -Path $PROFILE -Force`.
3.  **Edit the PowerShell Profile:**
    *   Open your PowerShell profile in Notepad by typing `notepad $PROFILE` and pressing Enter.
4.  **Add an Alias:**
    *   In your PowerShell profile, add a new alias to easily run the `compile.ps1` script. For example:
        ```powershell
        New-Alias compile-latex "powershell -ExecutionPolicy Bypass -File C:\path\to\your\compile.ps1"
        ```
        Replace `C:\path\to\your\compile.ps1` with the actual path to the `compile.ps1` script.
    *   Save the PowerShell profile.
5.  **Restart PowerShell:** Close and reopen PowerShell to load the new profile and alias.
6.  **Run the Script:**
    *   To compile a LaTeX file, use the following command:
        ```powershell
        compile-latex your_latex_filename
        ```
        Replace `your_latex_filename` with the name of your LaTeX file (without the `.tex` extension).

Now you can easily compile your LaTeX documents using the `compile-latex` command in PowerShell.

### If there are some issues let me know
