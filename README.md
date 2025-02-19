
# Classic Spreadsheet Editor - TrailSheet

![HTML5](https://img.shields.io/badge/HTML5-E34F26.svg?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6.svg?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E.svg?style=flat&logo=javascript&logoColor=black)
![jQuery](https://img.shields.io/badge/jQuery-0769AD.svg?style=flat&logo=jquery&logoColor=white)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) 
[![GitHub](https://img.shields.io/github/stars/SafwanGanz/TrailSheet?style=social)](https://github.com/SafwanGanz/TrailSheet)

A sleek, modern take on the classic spreadsheet experience using LuckySheet.

## 🚀 Overview

**TrailSheet** leverages the power of LuckySheet to bring a clean, user-friendly interface for managing data in a tabular format. This project aims to provide an intuitive web-based tool for data entry, analysis, and visualization, with a focus on simplicity and performance.

## ✨ Features

- **Modern Design:** Custom CSS variables for a cohesive, professional look.
- **Responsive Layout:** Optimized for various screen sizes, ensuring usability across devices.
- **Core Spreadsheet Operations:** Basic functionalities like selection, editing, and formatting cells.
- **Customizable:** Easy to tweak via CSS variables for branding or theme changes.
- **Lightweight:** Minimized dependencies for faster load times and better performance.

## 🛠️ Tech Stack

- **HTML5** for structure
- **CSS3** with CSS Variables for styling
- **JavaScript** with jQuery for DOM manipulation
- **LuckySheet** for spreadsheet functionality

## 📦 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/SafwanGanz/TrailSheet.git
   cd TrailSheet
   ```

2. **Open in Browser:**
   - Simply open the `index.html` file in your preferred web browser.

## 🔧 Usage

- **Start Editing:** Click on any cell to start typing immediately.
- **Selection & Navigation:** Use your mouse or keyboard to navigate through cells.
- **Customization:** Modify the CSS variables in the `<style>` section of `index.html` for a personalized look.

## 🔍 Customization

The editor uses CSS variables for easy theme customization:

```css
:root {
    --primary-bg: #e6e6e6;
    --secondary-bg: #ffffff;
    --border-color: #d3d3d3;
    --text-color: #333333;
    --primary-color: #0070c0;
    --highlight-color: #ffff00;
}
```

Change these values to alter the appearance of the spreadsheet editor.

## 🧪 Development

For development or extending functionality:

- **jQuery:** Used for handling DOM interactions; update via CDN or local inclusion.
- **LuckySheet:** The core library; ensure you're using the latest version for updates and security patches.

## 📋 Roadmap

- **Enhanced Features:** Adding support for more advanced spreadsheet functions like formulas, charts, etc.
- **Accessibility Improvements:** Making the spreadsheet editor fully accessible.
- **Performance Optimization:** Further optimizations for handling large datasets.

## 🪟 Creating an .exe File

To package this web application into a desktop application (`.exe` file), you'll need to use Electron with tools like `electron-packager`. Here's how you can do it from the command line:

1. **Install Node.js and npm** if not already installed. This is required for npm packages.

2. **Install Electron and electron-packager:**

   ```bash
   npm install electron --save-dev
   npm install electron-packager --global
   ```

3. **Create a `main.js` for Electron:**

   ```javascript
   const { app, BrowserWindow } = require('electron')
   const path = require('path')

   function createWindow () {
     const win = new BrowserWindow({
       width: 800,
       height: 600,
       webPreferences: {
         nodeIntegration: true,
         contextIsolation: false
       }
     })

     win.loadFile('index.html')
   }

   app.whenReady().then(createWindow)

   app.on('window-all-closed', () => {
     if (process.platform !== 'darwin') app.quit()
   })

   app.on('activate', () => {
     if (BrowserWindow.getAllWindows().length === 0) createWindow()
   })
   ```

4. **Package the App:**

   ```bash
   electron-packager . TrailSheet --platform=win32 --arch=x64 --out=release-builds
   ```

   This command will package your application into an `.exe` file for Windows x64 architecture. Adjust the platform and architecture as needed.

5. **Find Your .exe:** The resulting `.exe` file will be in the `release-builds` folder.

**Note:** Ensure you're using an admin command prompt or have the necessary permissions when executing these commands.

## 🛡️ License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- [LuckySheet](https://github.com/mengshukeji/Luckysheet) - for providing the backbone of this project.
- [jQuery](https://jquery.com/) - for simplifying JavaScript interactions.
- All contributors and testers who help make this project better.

---

Feel free to reach out or contribute to enhance this tool further!
