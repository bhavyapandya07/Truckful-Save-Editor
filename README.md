# 🚚 Truckful Save Editor & Currency Tool

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/34c45720-a5bd-4349-8852-a1ea179d7e47" />

An open-source, zero-dependency **Save Editor and Trainer alternative** for Truckful (PC).

Because Unity stores Truckful's save data (`PlayerData`) as binary arrays inside the Windows Registry rather than a standard `.json` or `.sav` file in `AppData`, manual save editing is tedious and traditional memory scanners/trainers often break across game updates.

This tool safely reads your registry save data, lets you set your Coins and Scrap to any custom amount via an interactive menu, and writes it back cleanly in seconds.

---

✨ Features
* **Interactive Menu:** Choose to edit **[1]** Both Coins & Scrap, **[2]** Coins Only, or **[3]** Scrap Only with any custom amount.
* **Version Independent:** Works on all builds of Truckful (Steam, Demo, and offline builds) regardless of game patches.
* **100% Safe & Transparent:** Provided as a plain-text Windows PowerShell script no shady `.exe` injectors, no background processes, and zero antivirus false positives.
* **Bypasses Unity Registry Errors:** Directly handles Unity `REG_BINARY` encoding without crashing on `REG_DWORD` settings.

---

⚡ How to Use (Takes 10 Seconds)
1. **Close Truckful completely.** *(If the game is running in the background, it will overwrite your save when you quit!)*
2. Download the script file (`.ps1` or `.txt` if downloaded from Nexus Mods).
3. Press the **Windows Key**, type `PowerShell`, and open **Windows PowerShell**.
4. Copy the script code, paste it into the PowerShell window, and press **Enter**. *(Alternatively, just right-click the `.ps1` file and select "Run with PowerShell").*
5. Type `1`, `2`, or `3` and press **Enter**.
6. Type the exact amount of Coins and/or Scrap you want (e.g., `11000`) and press **Enter**.
7. Launch Truckful and load your save!

---

❓ FAQ & Troubleshooting
**Q: My Coins/Scrap didn't change when I loaded the game!**
> **A:** Make sure Truckful is **100% closed** before running the script in PowerShell. Also, make sure you have played the game past the first checkpoint at least once so the `PlayerData` registry entry actually exists.

**Q: Where is the Truckful save file located on PC?**
> **A:** While the debug log is located at `%USERPROFILE%\AppData\LocalLow\MythicOwl\Truckful\Player.log`, the actual currency and car upgrade save data is stored in the Windows Registry under `HKEY_CURRENT_USER\Software\MythicOwl\Truckful` (`PlayerData_h...`). This script edits that registry binary automatically.
