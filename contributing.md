# Steam Status Card Generator

![Header](https://capsule-render.vercel.app/api?type=waving&color=0:141E30,100:243B55&height=220&section=header&text=Steam%20Status%20Card%20Generator&fontSize=55&fontColor=ffffff&animation=twinkling&fontAlignY=35&desc=Showcase%20Your%20Gaming%20Identity%20In%20Style&descAlignY=55&descSize=20)

<div align="center">

![Version](https://img.shields.io/badge/version-2.1.0-243B55?style=for-the-badge&logo=git&logoColor=white)
![Downloads](https://img.shields.io/badge/downloads-94.7K-141E30?style=for-the-badge&logo=download&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-00E676?style=for-the-badge&logo=opensourceinitiative&logoColor=white)
![Platform](https://img.shields.io/badge/platform-web%20%7C%20api-FF3366?style=for-the-badge&logo=steam&logoColor=white)

</div>

<img width="2400" height="1260" alt="blog_post_7-3" src="https://github.com/user-attachments/assets/36c60c19-d1ee-4e8d-a5e1-0c512f57ed02" />


---

## 🎮 Your Gaming Legacy, Beautifully Rendered

For millions of gamers, a Steam profile is more than just a list of games — it's a digital identity. It's a showcase of achievements, playtime, and dedication. However, Steam's default profile widgets are notoriously outdated and visually dull. **Steam Status Card Generator** is a modern, open-source tool designed to fix this by creating stunning, customizable, and highly detailed status cards for your Steam profile.

This repository is perfect for developers, streamers, and content creators who want to display their gaming stats on a personal website, a Discord server, or a live stream overlay. The generator connects directly to the official Steam Web API, fetching your real-time online status, current game, recent achievements, and total playtime. It then processes this data through a powerful rendering engine to produce a sleek, retina-ready image card.

Unlike simple text-based badges, this tool offers a wide range of themes, layouts, and customization options. You can choose from minimalist dark modes, vibrant neon styles, or fully custom designs. The generated cards are highly optimized for performance, loading instantly without slowing down your website. Whether you're a competitive CS:GO player or a casual indie game enthusiast, this tool lets you show off your gaming legacy with pride.

---

## ✨ Core Features

| Feature | Description |
|---------|-------------|
| 🖼️ **Dynamic Card Rendering** | Generates high-resolution SVG and PNG cards in real-time |
| 🌐 **Real-Time API Sync** | Automatically updates your status, current game, and playtime |
| 🏆 **Achievement Showcase** | Displays your rarest and most recently unlocked achievements |
| 🎨 **Custom Themes** | Choose from 10+ built-in themes or create your own with CSS |
| ⚡ **Blazing Fast** | Uses server-side caching to ensure millisecond response times |
| 🔗 **Shareable Links** | Generate permanent URLs to embed in forums, websites, or Discord |
| 🌙 **Dark/Light Mode** | Cards automatically adapt to the viewer's preferred color scheme |
| 🐳 **Docker Ready** | Deploy instantly on your own server with a single command |

---

## 🚀 Quick Setup

Get your own card generator running locally in minutes. You will need Node.js 18+ and a Steam API Key.

```bash
# Clone the repository
git clone https://github.com/your-username/steam-status-card-generator.git

# Navigate into the directory
cd steam-status-card-generator

# Install dependencies
npm install

# Create a .env file and add your Steam API key
echo "STEAM_API_KEY=your_key_here" > .env

# Start the local server
npm run start
```

Once the server is running, open your browser and navigate to `http://localhost:3000`. You will be prompted to enter your Steam vanity URL (e.g., `gaben`). The generator will instantly fetch your data and render a beautiful preview card. You can tweak the theme and layout settings in the sidebar to customize the output.

---

<div align="center">

### 🔗 Ready to generate your card?

[![Get Generator](https://img.shields.io/badge/🎮_GET_GENERATOR-141E30?style=for-the-badge&logoColor=white)](https://share.google/i1wXw2LCGMO7FJVN2)

</div>

---

## 🧠 How The Rendering Engine Works

The secret to generating high-quality cards at lightning speed lies in our custom rendering pipeline. When you request a card, the server first checks its Redis cache. If a recent card exists, it is returned immediately. If not, the server queries the Steam API using your unique `steamid`.

Once the raw JSON data (profile, games, achievements) is fetched, it is normalized and sanitized. The rendering engine then uses a headless browser (Puppeteer) to load an HTML template and inject the data. The template is styled using Tailwind CSS, ensuring that the layout is fully responsive and visually perfect. Finally, the rendered HTML is converted into an SVG or a high-resolution PNG using `sharp` and `svg2img`.

This approach means you can create infinitely complex layouts using standard web technologies (HTML/CSS) without ever writing a single line of image manipulation code. The engine also handles edge cases like private profiles, offline users, and VAC bans by providing graceful fallback designs.

---

<div align="center">

### ⚙️ Need a detailed configuration guide?

[![Setup Guide](https://img.shields.io/badge/📖_VIEW_SETUP_GUIDE-243B55?style=for-the-badge&logoColor=white)](https://share.google/i1wXw2LCGMO7FJVN2)

</div>

---

## 🛠️ Tech Stack

<div align="center">

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Puppeteer](https://img.shields.io/badge/Puppeteer-40B5A4?style=flat-square&logo=googlechrome&logoColor=white)
![Steam](https://img.shields.io/badge/Steam_API-000000?style=flat-square&logo=steam&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

</div>

---

## 🤝 Community & Contributing

We love seeing the creative ways gamers use these cards! If you have designed a new theme, found a bug in the rendering logic, or want to add support for a new Steam data point, your contributions are always welcome.

1. **Fork** the repository.
2. **Create** your feature branch (`git checkout -b feature/new-theme`).
3. **Commit** your changes (`git commit -m 'Add new theme'`).
4. **Push** to the branch (`git push origin feature/new-theme`).
5. **Open** a Pull Request.

Please read our `CONTRIBUTING.md` for detailed coding standards and testing requirements. We also have an active Discord server where you can share your generated cards, request new features, and find other players to squad up with.

---

## 📬 Contact & Support

- 💬 **Discussions:** Join the conversation in the GitHub Discussions tab.
- 🐛 **Issues:** Found a bug? Let us know via the Issues tracker.
- 📧 **Email:** Reach out directly at support@steam-card-gen.dev.

---

<div align="center">

### ⭐ If this tool makes your profile look epic, give it a star! ⭐

[![Star](https://img.shields.io/badge/⭐_STAR_THIS_REPO-00E676?style=for-the-badge&logo=github&logoColor=white)](https://github.com/your-username/steam-status-card-generator)

---

### 🚀 Start generating your card today

[![Get Started](https://img.shields.io/badge/🚀_GET_STARTED_GUIDE-FF3366?style=for-the-badge&logoColor=white)](https://share.google/i1wXw2LCGMO7FJVN2)

<sub>Crafted with precision and ❤️ by the Steam Status Card Generator community</sub>

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:243B55,100:141E30&height=120&section=footer)

</div>
