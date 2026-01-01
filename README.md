# 🃏 Games Database Manager

A sleek, JSON-driven web interface designed for managing digital game libraries. This tool features a custom UI inspired by the aesthetic of *Balatro*, providing a professional environment to browse, search, and edit game metadata.

---

## 🚀 Features

* **Dark Theme:** A high-contrast, dark-mode workspace (`#0e0e0e`) using custom typography and "BalatroFont" for a specialized gaming-tool feel.
* **JSON Persistence:** Import and manage your `games.json` database directly in the browser using the HTML5 FileReader API.
* **Intelligent Migration:** Built-in logic to automatically convert legacy string-based metadata into structured boolean objects for platforms and storefronts.
* **Dynamic Search:** Instant, case-insensitive filtering of large game lists as you type.
* **Metadata Management:** Interactive modal with checkbox grids for rapid updates across 14+ platforms and 9+ stores.
* **Two-Panel Layout:** A rigid $1024 \times 768$ workspace designed for clarity at a glance.

## 🛠️ Technology Stack

* **HTML5 / CSS3:** Uses Flexbox for the main panels and CSS Grid for the interactive checkbox arrays.
* **Vanilla JavaScript:** Lightweight, zero-dependency logic for fast performance.
* **JSON-based:** Designed to work with standardized data entries for easy integration with other databases.

## 📂 Data Structure

The application expects and generates entries formatted as follows:

```json
{
  "games": [
    {
      "id": 1271,
      "name": "The Elder Scrolls: Daggerfall",
      "description": "Experience massive open-world role-playing journey where your choices shape fate of the Empire. Explore thousands of cities, master deep magical systems, and uncover dark conspiracy in this legendary adventure masterpiece.",
      "platform": {"PC":1,"PSX":0,"PS2":0,"PS3":0,"PS4":0,"PS5":0,"PSVita":0,"Nintendo Switch":0,"Nintendo Switch 2":0,"XBOX":0,"Xbox 360":0,"Xbox One":0,"Android":0,"iPhone":0},
      "store": {"Steam":1,"GOG":0,"Epic Games Store":0,"Itch.IO":0,"Play Store":0,"AppStore":0,"PSN":0,"Microsoft Store":0},
      "release": {"Digital":1,"Physical":0}
    }
  ]
}
```

## 📖 How To Use

The **Games Database Manager** is a client-side tool. It does not require a server; it processes your local JSON files directly in the browser.

### 1. Loading Your Data
Click the **"Load JSON"** button in the top-left corner. This opens a file browser. Select your `.json` file. The application will immediately parse the data, run the migration logic to ensure metadata compatibility, and populate the alphabetical list.

### 2. Searching and Filtering
Type any part of a game's title into the **Search Textfield**. The listbox below will filter in real-time. This is particularly useful for large databases where manual scrolling is inefficient.

### 3. Viewing Game Details
Select a game from the list. The right panel will update to show:
* **Narrative Info:** The game's title and its high-quality marketing description.
* **Categorization:** A clear view of compatible platforms, available digital stores, and the release format.

### 4. Editing Entries
1. Click the **EDIT** button.
2. In the modal overlay, modify the text or toggle the checkboxes in the **Platform** and **Store** grids.
3. Click **Save** to commit changes to the session memory.

### 5. Deleting Entries
To remove a game from the current session, select the title and click the **DELETE** button.

> [!IMPORTANT]
> **Saving Changes:** Since this is a client-side tool, clicking "Save" in the modal updates the data in your browser's memory. To keep your changes permanently, you must currently copy the updated state back into your `games.json` file.
