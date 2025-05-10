# 🌱 Smart Agriculture System

A Vue-based smart agriculture web platform for real-time environmental monitoring, historical data visualization, and expert advisory services. Designed with user-friendliness, modularity, and dynamic data presentation in mind.

---

## 📌 Features

### ✅ User Authentication
- **r_Login.vue**: User login page with form validation.
- **r_Enroll.vue**: User registration page.
- Uses centralized API (`/api/index.js`) for login/register requests.

### 🌿 Environmental Visualization
- **r_Charts.vue / r_Charts1.vue / r_Charts2.vue**: Display environmental parameters (temperature, humidity, light).
- **Auto-refresh** using backend API via `request.js`.
- **ECharts framework** used for dynamic chart rendering.
- Sidebar includes a **weather widget component** (in `Sidebar.vue`).

### 📊 Historical Data
- Environmental charts were redesigned and modularized into historical views:
  - Temperature, Humidity, Light Duration.
  - Filters and date ranges applied to extract relevant history data.

### 📰 News & Recommendations
- **r_EvoPage.vue**: “News Vision” interface presenting latest agricultural news.
- **Category Filter**: Implemented search/filter for categorized news.
- **Read Status**: Marking of read/unread news articles.

### 🧠 Expert Advice
- **r_Advise.vue**: Displays expert suggestions or auto-generated advice based on current sensor readings.

### 👥 User Management
- **r_UserManagement.vue**: Admin interface for managing user accounts, roles, and permissions.

### 🖥️ Visualization Dashboard
- **Partial contribution** to large-screen data display components.
- Backend connection via `api/index.js` + dynamic filters using `utils/request.js`.

---

## 📁 Project Structure
```
src/
├── api/ # Central API functions
│ └── index.js
├── assets/ # Static assets (CSS/Images)
│ └── img/logo.png
├── components/ # Reusable UI components
│ ├── common/ # Shared components
│ │ ├── Header.vue
│ │ ├── Sidebar.vue
│ │ ├── Tags.vue
│ │ └── Home.vue
├── page/ # Functional views and pages
│ ├── r_Login.vue
│ ├── r_Enroll.vue
│ ├── r_Charts.vue, r_Charts1.vue, r_Charts2.vue
│ ├── r_EvoPage.vue
│ ├── r_Advise.vue
│ ├── r_UserManagement.vue
├── router/ # Vue Router setup
│ └── index.js
├── utils/ # Utility scripts
│ └── request.js # Axios wrapper
├── App.vue # Root component
└── main.js # Entry point
```
---

## 🧪 Technologies

- **Frontend**: Vue.js 2.x, Vue Router
- **UI Library**: Element-UI / Custom Components
- **Charts**: ECharts
- **HTTP Requests**: Axios (`utils/request.js`)
- **i18n**: Internationalization support (`i18n.js`)

---

## 🚀 Setup & Run

```bash
# Clone repository
git clone https://github.com/your-repo/smart-agriculture-system.git
cd smart-agriculture-system

# Install dependencies
npm install

# Run in development
npm run serve

# Build for production
npm run build
