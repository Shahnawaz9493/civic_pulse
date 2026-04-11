<div align="center">

<img src="assets/Logo.png" alt="CivicPulse Logo" width="120" height="120" onerror="this.style.display='none'"/>

# 🏛️ CivicPulse
### *Your City. Your Voice. Your Change.*

**A modern, full-featured civic issue reporting platform that bridges the gap between citizens and local authorities.**

[![Made with HTML](https://img.shields.io/badge/Made%20with-HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Styled with CSS](https://img.shields.io/badge/Styled%20with-CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![Powered by JS](https://img.shields.io/badge/Powered%20by-JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Google Maps](https://img.shields.io/badge/Google%20Maps-API-4285F4?style=for-the-badge&logo=googlemaps&logoColor=white)](https://developers.google.com/maps)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

<br/>

[🚀 Live Demo](#) · [🐛 Report a Bug](../../issues) · [✨ Request a Feature](../../issues)

<br/>

> **Built for Hackathon** — Zero dependencies. Zero build steps. Pure vanilla power. 💪

</div>

---

## 📸 Screenshots

<div align="center">

| Home Dashboard | Issue Reporting | Issue Tracking |
|:-:|:-:|:-:|
| ![Home](https://via.placeholder.com/280x180/2563eb/ffffff?text=Home+Dashboard) | ![Report](https://via.placeholder.com/280x180/10b981/ffffff?text=Report+Issue) | ![Track](https://via.placeholder.com/280x180/f59e0b/ffffff?text=Track+Status) |

| Agent Dashboard | Find Workers | Reviews |
|:-:|:-:|:-:|
| ![Agent](https://via.placeholder.com/280x180/6366f1/ffffff?text=Agent+Dashboard) | ![Workers](https://via.placeholder.com/280x180/ec4899/ffffff?text=Find+Workers) | ![Reviews](https://via.placeholder.com/280x180/14b8a6/ffffff?text=Community+Reviews) |

</div>

---

## ✨ Why CivicPulse?

Potholes ignored. Streetlights broken for months. Illegal dumping with no action taken.

Sound familiar?

**CivicPulse** puts the power back in citizens' hands — a one-stop platform to report, track, upvote, and resolve local civic issues, with full community collaboration and a dedicated agent workflow baked right in.

---

## 🚀 Feature Highlights

### 🗺️ Smart Issue Reporting
- Submit issues with title, description, category, and precise GPS coordinates
- Interactive **Google Maps** integration — search or tap to pin your exact location
- Optional **image upload** to give visual context to your report
- Instant **Issue ID** generated for tracking upon submission

### 📊 Live Issue Dashboard
- View all community-reported issues in a responsive card grid
- **Filter** by category (Infrastructure, Safety, Environment, Transportation, Utilities)
- **Filter** by status: `Open` → `In Progress` → `Resolved`
- **Sort** by Newest, Oldest, or Most Upvoted

### 🔍 Issue Tracking
- Track any issue's full lifecycle using its unique **Issue ID**
- Visual **progress stepper** showing current resolution stage
- Real-time status updates

### 👷 Find Workers
- Browse and connect with verified local service workers
- Worker **registration** portal built-in
- Helps fast-track resolution for reported issues

### 🕵️ Agent Dashboard
- Dedicated view for civic agents and authority personnel
- Manage, assign, and update issue statuses from one place
- Streamlined workflow for faster community response

### 💬 Community Interaction
- **Upvote** issues to signal urgency and community support
- **Comment** on any issue to add context or updates
- **Reviews page** for community feedback and transparency

### 🌐 Multilingual Support
Built to serve diverse communities — supports:

| Language | Code |
|---|---|
| English | `en` |
| Hindi (हिंदी) | `hi` |
| Telugu (తెలుగు) | `te` |
| Tamil (தமிழ்) | `ta` |
| Kannada (ಕನ್ನಡ) | `kn` |

### 🤖 Built-in AI Chatbot
- Floating **CivicPulse Assistant** chatbot available on every page
- Instant answers to user queries about the platform

### 🔐 User Authentication
- Full **Login / Register** system with form validation
- Profile management with optional email or phone signup
- Session-aware navigation (profile icon, logout)

### 🎨 Design & UX
- **Mobile-first** responsive design — works flawlessly on all screen sizes
- Smooth animations, hover effects, and micro-interactions
- **Toast notifications** for instant action feedback
- **Modal dialogs** for detailed issue views and comments
- Respects `prefers-reduced-motion` for accessibility

---

## 🛠️ Tech Stack

```
Frontend Only — No frameworks, no build tools, no complexity.
```

| Technology | Purpose |
|---|---|
| **HTML5** | Semantic structure, ARIA accessibility |
| **CSS3** | Responsive layout, animations, CSS variables |
| **Vanilla JavaScript** | All app logic, state management, DOM manipulation |
| **Google Maps JS API** | Interactive maps, location search, coordinate picking |
| **LocalStorage API** | Client-side persistent data storage |
| **Google Places API** | Address autocomplete |

---

## ⚡ Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/your-username/civicpulse.git
cd civicpulse
```

### 2. Set up Google Maps API Key

1. Visit [Google Cloud Console](https://console.cloud.google.com/)
2. Create or select a project
3. Enable **Maps JavaScript API** and **Places API**
4. Generate an API Key under **Credentials**
5. Open `index.html` and replace `YOUR_API_KEY`:

```html
<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&libraries=places" async defer></script>
```

> 🔒 **Security Tip:** Restrict your API key to your domain in the Google Cloud Console before going live.

### 3. Launch

```bash
# Option A — Just open in browser
open index.html

# Option B — Use a local server (recommended)
npx serve .
# or
python -m http.server 8080
```

That's it. **No npm install. No build step. No config files.** 🎉

---

## 📁 Project Structure

```
civicpulse/
│
├── 📄 index.html          # App shell — all pages, modals, navigation
├── 🎨 styles.css          # Full styling — responsive, animated, themed
├── ⚙️  script.js           # All functionality — routing, CRUD, maps, auth
├── 📁 assets/             # Logo and static assets
└── 📖 README.md           # You are here!
```

---

## 🗄️ Data Structure

Issues are stored in `localStorage` with the following schema:

```javascript
{
  id:          "unique-uuid",
  title:       "Broken streetlight on MG Road",
  description: "The streetlight near the bus stop has been broken for 3 weeks.",
  category:    "infrastructure",       // infrastructure | safety | environment | transportation | utilities | other
  status:      "open",                 // open | in-progress | resolved
  location:    "MG Road, Bengaluru",
  lat:         12.9716,
  lng:         77.5946,
  image:       "base64-string | null",
  upvotes:     14,
  upvotedBy:   ["user-id-1"],
  comments: [
    { id: "cmt-1", text: "Still broken as of today!", date: "2025-04-10T08:00:00Z" }
  ],
  createdAt:   "2025-04-01T10:00:00Z",
  updatedAt:   "2025-04-10T08:30:00Z"
}
```

---

## 🎨 Customization

### Changing Theme Colors

Edit the CSS variables in `styles.css`:

```css
:root {
  --primary-color:   #2563eb;   /* Main brand blue */
  --secondary-color: #10b981;   /* Success green */
  --accent-color:    #f59e0b;   /* Warning amber */
  --danger-color:    #ef4444;   /* Error red */
  --bg-color:        #f8fafc;   /* Page background */
}
```

### Adding New Issue Categories

1. Add an `<option>` to the category `<select>` in `index.html`
2. Update the `categoryLabels` object in `script.js`

### Adding a New Language

1. Add a new `<option>` in the language `<select>` in `index.html`
2. Add translation keys to the `translations` object in `script.js`

---

## ♿ Accessibility

CivicPulse is built with accessibility as a first-class concern:

- ✅ Semantic HTML5 elements throughout
- ✅ ARIA roles and labels on all interactive elements
- ✅ Full keyboard navigation support
- ✅ Focus management on modal open/close
- ✅ Screen reader compatible
- ✅ `prefers-reduced-motion` media query respected
- ✅ Sufficient color contrast ratios

---

## 🌱 Roadmap

Things we'd love to add next:

- [ ] 🔗 Backend API integration (Node.js / Firebase / Supabase)
- [ ] 📧 Email & SMS notifications on status updates
- [ ] ☁️ Cloud image storage (Cloudinary / S3)
- [ ] 🔎 Advanced full-text search
- [ ] 📤 Export issues to PDF / CSV
- [ ] 🗺️ Heatmap view of issue density by area
- [ ] 📱 PWA support — installable as a mobile app
- [ ] 🔔 Push notifications
- [ ] 📊 Analytics dashboard for authorities
- [ ] 🌍 More regional language support

---

## 🤝 Contributing

Contributions make open source great! Here's how to get involved:

```bash
# 1. Fork the repo
# 2. Create your feature branch
git checkout -b feature/amazing-feature

# 3. Commit your changes
git commit -m "feat: add amazing feature"

# 4. Push to the branch
git push origin feature/amazing-feature

# 5. Open a Pull Request
```

Please read our [Contributing Guidelines](CONTRIBUTING.md) before submitting a PR.

---

## 🙌 Acknowledgements

- [Google Maps Platform](https://developers.google.com/maps) for location services
- [MDN Web Docs](https://developer.mozilla.org/) — always the best reference
- Every civic-minded developer who believes tech can fix potholes 🕳️

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for details.

---

<div align="center">

**Made with ❤️ for communities everywhere**

*If CivicPulse helps your city — give it a ⭐ and spread the word!*

[![GitHub stars](https://img.shields.io/github/stars/your-username/civicpulse?style=social)](../../stargazers)
[![GitHub forks](https://img.shields.io/github/forks/your-username/civicpulse?style=social)](../../forks)

</div>
