# RideEase — Smart Ride Booking and Fleet Management System

An interactive, responsive React application faithfully implementing the **RideEase Admin Portal** high-fidelity designs from Figma.

> **Local Server URL:** [http://localhost:3000](http://localhost:3000)  
> **Project Directory:** `C:\Users\11ths\OneDrive\Documents\7th semester\7th semester\assessments\uiux\final demo`

---

## 🌟 Key Architecture & Critical Requirements Met

1. **True Single-Screen Admin Portal UX:**
   - **No horizontal screen carousel / design galleries.**
   - Only the currently active screen is rendered inside the application viewport.
   - Smooth navigation between views without reloading the browser.
2. **Dedicated Separate Screens:**
   - **Screen 1 — Admin Login:** Independent login page without admin sidebar. Validates demo input (`admin@rideease.com` / `admin123`) and redirects to Dashboard.
   - **Screen 2 — Dashboard Overview:** System health metrics (Active Rides: 124, Drivers: 84, Complaints: 17, Revenue: ₹8,540), Ride Activity chart, Operations Required warning banner, and live dispatch summary.
   - **Screen 3 — Driver Management:** Vehicle category filters (`Car`, `Bike`, `Auto`), real-time search, driver profiles (`D124 Arun Kumar`, `D117 Meena S`, `D102 Rahul P`, etc.), with interactive **[Approve]** and **[Suspend]** actions with a safety confirmation modal.
   - **Screen 4 — Ride Monitoring:** Live rides table, status badges (`Ongoing`, `Flagged`), fare details, and animated **Google Maps GPS Route Telemetry** illustration. Includes a ride details modal.
   - **Screen 5 — Data Privacy Visualization:** Interactive data flow topology (`Customer ➔ API Gateway ➔ Driver ➔ Vault`), category inspection schema drawer, **97% Active Consent** progress bar, **92% Compliance Score**, and searchable audit logs.
   - **Screen 6 — AI Assistant & Confidence Dashboard:** Autonomous recommendations (`Fraud Alert - 85%`, `Driver Risk Flag - 82%`, `Surge Prediction - 68%`) with decision criteria modals, dismiss actions, and consequential action confirmations.
   - **Screen 7 — Settings:** Independent expandable sections for Admin Profile, Security & 2FA, Notification preferences, and Telemetry Retention policies with save feedback.
   - **Screen 8 — Logout Confirmation Modal:** Dialog with Cancel and Confirm Logout actions that cleanly clears the session and returns to Screen 1.

---

## 🚀 How to Run in VS Code

### Step 1: Open the Project in VS Code
1. Open **VS Code**.
2. Click **File ➔ Open Folder...** and select:
   ```text
   C:\Users\11ths\OneDrive\Documents\7th semester\7th semester\assessments\uiux\final demo
   ```

### Step 2: Start the Web Application
In the integrated terminal (`Ctrl + ~`):
```bash
npm start
```
*(or `npm run dev`)*

### Step 3: Open in Browser
Navigate to:
👉 **[http://localhost:3000](http://localhost:3000)**

---

## 🔑 Demo Login Credentials
- **Email:** `admin@rideease.com`
- **Password:** `admin123`

---

## 📁 Component Directory Structure

```text
src/
├── components/
│   ├── AdminLayout.jsx         # Persistent admin shell with sidebar and header
│   ├── Header.jsx              # Dynamic top header with title and live telemetry status
│   ├── Sidebar.jsx             # Left navigation menu with active highlight
│   └── LogoutModal.jsx         # Screen 8: Logout confirmation dialog
├── pages/
│   ├── LoginPage.jsx           # Screen 1: Admin login with field validation
│   ├── DashboardPage.jsx       # Screen 2: System health, charts, recent activity
│   ├── DriverManagementPage.jsx# Screen 3: Driver cards, search, approve/suspend
│   ├── RideMonitoringPage.jsx  # Screen 4: Live rides, GPS map route visualization
│   ├── DataPrivacyPage.jsx     # Screen 5: Privacy topology, consent, audit logs
│   ├── AIAssistantPage.jsx     # Screen 6: Confidence dashboard, fraud alerts
│   └── SettingsPage.jsx        # Screen 7: Modular expandable preferences
├── data/
│   └── mockData.js             # High-fidelity sample state data
├── App.jsx                     # Root router & global state manager
├── App.css                     # Custom component styling matching Figma palette
├── index.css                   # Global reset, typography, and animations
└── main.jsx                    # React entrypoint
```
