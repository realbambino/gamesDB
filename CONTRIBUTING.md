# Contributing to Games Database Manager

Thank you for your interest in improving this project! To maintain the clean, "Balatro-inspired" aesthetic and code quality, please follow these guidelines.

## 🛠️ Development Setup
1. Fork the repository.
2. Clone your fork locally: `git clone https://github.com/realbambino/gamesDB.git`
3. Open `index.html` in your browser. No build steps are required.

## 🎨 UI & Design Guidelines
* **Fixed Dimensions:** The app is strictly designed for a 1024x768 container. Do not break the flex-panel constraints.
* **Typography:** Always use `BalatroFont` for labels and values to maintain the theme.
* **Colors:** Use the established variables (e.g., `#121212` for panels, `#3a3a3a` for borders).

## 🧪 Submission Process
1. **Branching:** Create a feature branch (`git checkout -b feature/AmazingFeature`).
2. **Standardization:** If adding new platforms or stores, update the `PLATFORM_ORDER` or `STORE_ORDER` constants in the `<script>` tag.
3. **Commit:** Keep commit messages concise (e.g., `feat: add Nintendo eShop support`).
4. **PR:** Open a Pull Request with a clear description of your changes.

## 🐞 Reporting Issues
Please use the GitHub Issues tab to report bugs. Include:
* A copy of the JSON file that caused the error (if applicable).
* Your browser and OS version.
