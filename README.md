# Valuator App Development - 8th Semester Internship Presentation

![Slidev](https://img.shields.io/badge/Built%20with-Slidev-brightgreen)
![Node.js](https://img.shields.io/badge/Node.js-18+-green)
![GitHub Pages](https://img.shields.io/badge/Deployed%20on-GitHub%20Pages-blue)

## 📋 Overview

This is a comprehensive **Slidev presentation** for Meet Bhanushali's 8th semester internship report at **Resollect**, focusing on the development of a **Property Valuator Management System**.

### 🎯 Project Highlights
- **50+ Interactive Slides** with modern design
- **7 Interactive Diagrams** with zoom functionality
- **Complete API Documentation** with examples
- **Technical Architecture** details
- **Security Implementation** documentation

## 🚀 Live Presentation

🌐 **[View Live Presentation]([[https://workw.github.io/sides_8_sem](https://meetkool.github.io/8-sem-iiitl-final-project-talk-/1)](https://meetkool.github.io/8-sem-iiitl-final-project-talk-/1)/)**

## 🛠️ Technology Stack

- **Slidev** - Modern slide presentation framework
- **Vue.js 3** - Interactive components
- **Mermaid** - Architecture diagrams
- **TypeScript** - Type-safe development
- **GitHub Actions** - Automated deployment
- **GitHub Pages** - Static hosting

## 📁 Project Structure

```
sides_8_sem/
├── slides.md              # Main presentation file
├── package.json           # Dependencies and scripts
├── .github/
│   └── workflows/
│       └── deploy.yml     # GitHub Pages deployment
├── components/            # Vue components (if any)
├── public/               # Static assets
└── README.md             # This file
```

## 🔧 Local Development

### Prerequisites
- Node.js 18+ 
- npm or yarn

### Setup & Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/workw/sides_8_sem.git
   cd sides_8_sem
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start development server**
   ```bash
   npm run dev
   ```

4. **Open browser**
   Navigate to `http://localhost:3030`

### Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build for GitHub Pages |
| `npm run build-local` | Build for local hosting |
| `npm run export` | Export as PDF |
| `npm run preview` | Preview built version |

## 🌐 GitHub Pages Deployment

### Automatic Deployment

The presentation is automatically deployed to GitHub Pages using GitHub Actions:

1. **Push to main/master branch**
2. **GitHub Actions workflow runs** (`.github/workflows/deploy.yml`)
3. **Builds Slidev presentation**
4. **Deploys to GitHub Pages**

### Manual Setup (First Time)

1. **Enable GitHub Pages**
   - Go to repository Settings
   - Navigate to "Pages" section
   - Set Source to "GitHub Actions"

2. **Push your changes**
   ```bash
   git add .
   git commit -m "Add Slidev presentation"
   git push origin main
   ```

3. **Check deployment**
   - Go to Actions tab
   - Monitor the deployment workflow
   - Access via: `https://workw.github.io/sides_8_sem/`

## 🎨 Features

### 📊 Interactive Diagrams
- **System Architecture** with zoom controls
- **Component Architecture** with relationships
- **API Authentication Flow** sequence diagram
- **Database ER Diagram** with full schema
- **Scaling Architecture** visualization
- **Webhook Processing Flow** security diagram

### 🔐 Technical Documentation
- **Authentication API** (OTP system, token management)
- **Assignment Management API** (workflow states)
- **Webhook & Admin APIs** (bulk operations)
- **Security Implementation** (encryption, rate limiting)
- **Database Design** (15+ tables, relationships)

### 🎯 Business Content
- **Project Overview** and objectives
- **Company Background** (Resollect)
- **Technical Implementation** details
- **Challenges & Solutions**
- **Key Achievements** and metrics
- **Future Enhancements**

## 🎛️ Customization

### Themes
Current theme: `@slidev/theme-default`

To change theme:
```bash
npm install @slidev/theme-[theme-name]
```

Update `slides.md` header:
```yaml
theme: [theme-name]
```

### Styling
Custom CSS is defined in the `css: |` section of `slides.md`:
- Glass-morphism effects
- Interactive button styling
- Responsive design
- Zoom functionality

## 📱 Navigation

### Keyboard Shortcuts
- **Arrow Keys** - Navigate slides
- **Space** - Next slide
- **Shift + Space** - Previous slide
- **F** - Fullscreen mode
- **O** - Overview mode
- **D** - Dark mode toggle

### Interactive Elements
- **Zoom Buttons** on diagrams (🔍 Zoom In/Out, ↺ Reset)
- **Click & Drag** on Mermaid diagrams
- **Responsive Design** for mobile devices

## 📊 Metrics & Performance

### Presentation Stats
- **50+ Slides** of technical content
- **7 Interactive Diagrams** with zoom functionality
- **200+ Users** supported in system
- **1000+ Assignments** processed
- **₹50L+ Value** processed through platform

### Technical Metrics
- **Django 5.2.1** backend framework
- **PostgreSQL** database with 15+ tables
- **Redis** for caching and sessions
- **AWS S3** for file storage
- **RESTful APIs** with comprehensive documentation

## 🔍 Troubleshooting

### Common Issues

**Build Errors:**
```bash
npm run build-local  # Test local build first
```

**Port Already in Use:**
```bash
npm run serve  # Uses port 3030 instead of 3031
```

**GitHub Pages 404:**
- Check repository name in `package.json` build script
- Ensure GitHub Pages is enabled in repository settings
- Verify workflow permissions in repository settings

## 📞 Contact

**Meet Bhanushali**  
- 📧 Email: meet.bhanushali@resollect.com
- 💼 LinkedIn: [linkedin.com/in/meetbhanushali](https://linkedin.com/in/meetbhanushali)
- 👨‍💻 GitHub: [github.com/meetbhanushali](https://github.com/meetbhanushali)

## 📄 License

This project is licensed under the ISC License - see the package.json file for details.

---

**Built with ❤️ using [Slidev](https://sli.dev/)** 
