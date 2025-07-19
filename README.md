# 🍓 Fruit Store - React Vite E-Commerce App

This is a simple yet fully functional **fruit store** web application built using **React** and **Vite**. Users can browse fruits, select quantities, view cart summary, submit delivery and location details, and record orders directly to a **Google Form and Sheet** without needing a backend server.

---

# view (https://fruit-store-react1.onrender.com/)

---

## ⚙️ Tech Stack

| Tool        | Description                                          |
|-------------|------------------------------------------------------|
| 🔥 Vite      | Blazing-fast dev server and bundler for React       |
| ⚛️ React     | Frontend library for building interactive UIs       |
| 🗺 Leaflet   | For map-based location selection                     |
| 📝 Google Form | For backend-free order submissions to Google Sheets |

---

## 🚀 Features

### ✅ General

- Responsive UI for fruit shopping
- Simple **product listing** and **card design**
- Real-time cart updates and total calculation
- One-page navigation (SPA style)

### ✅ Components Used

| Component     | Purpose |
|---------------|---------|
| `Navbar`      | Top nav with page routing (Home, Summary, About, Pay, Recent) |
| `FruitCard`   | Displays each fruit with image, name, price, input |
| `Summary`     | Shows cart summary (items and price) |
| `Footer`      | Contains summary access link |
| `About`       | Displays map + store contact/location |
| `Recent`      | Shows past orders from localStorage |
| `Pay`         | Checkout form with delivery location, Google Form integration |

---

## 🛒 User Flow

1. User lands on **Home Page** with fruits categorized (Popular, Tropical, Citrus...)
2. Can **adjust quantity** per fruit (e.g., 2kg Apple, 1kg Mango)
3. Total **price and quantity auto-calculated**
4. User clicks **Pay**, fills:
   - Name, Date, Contact
   - Location via map 🗺
   - Optional address (building, street)
5. On submission:
   - Form is saved locally (`localStorage`)
   - Order is **sent to Google Form → Google Sheet**
6. After order: Select **payment method**
7. Recent orders can be viewed from **Recent** tab

---

## 🧠 React Concepts Used

- **Component-based architecture** (`Navbar`, `FruitCard`, etc.)
- **State management with `useState()`** to track cart & form
- **Conditional rendering** (`submitted ? ... : ...`)
- **Map and filtering logic** for cart summary
- **Lifting state up** (cart state shared across pages)
- **Event handling** (e.g., `onChange`, `onClick`, `onSubmit`)

---

## ⚡ Vite Highlights

- Superfast dev server
- Instant hot module replacement (HMR)
- Simple project setup with `npm create vite@latest`
- Built-in support for JSX, ESModules

```bash
# Create Project
npm create vite@latest fruit-store --template react

# Install dependencies
npm install

# Start dev server
npm run dev
```
---

## Interface
<h6>UI in Device1</h6>
<p align="center">
  <img src="https://github.com/hsj71/FruitsMarket_ReactVite/blob/main/Screenshot%20(785).png" alt="View" width="700"/>
</p>

<h6>UI in Device2</h6>
<p align="center">
  <img src="https://github.com/hsj71/FruitsMarket_ReactVite/blob/main/Screenshot%20(795).png" alt="View" width="600"/>
</p>
<h6>Summery</h6>
<p align="center">
  <img src="https://github.com/hsj71/FruitsMarket_ReactVite/blob/main/Screenshot%20(786).png" alt="View" width="700"/>
</p>
<h6>Payment Form</h6>
<p align="center">
  <img src="https://github.com/hsj71/FruitsMarket_ReactVite/blob/main/Screenshot%20(787).png" alt="View" width="700"/>
</p>
<h6>About</h6>
<p align="center">
  <img src="https://github.com/hsj71/FruitsMarket_ReactVite/blob/main/Screenshot%20(788).png" alt="View" width="700"/>
</p>
<h6>Payment Mode</h6>
<p align="center">
  <img src="https://github.com/hsj71/FruitsMarket_ReactVite/blob/main/Screenshot%20(792).png" alt="View" width="700"/>
</p>
<h6>Previous Payments</h6>
<p align="center">
  <img src="https://github.com/hsj71/FruitsMarket_ReactVite/blob/main/Screenshot%20(793).png" alt="View" width="700"/>
</p>
<h6>Records sheet</h6>
<p align="center">
  <img src="https://github.com/hsj71/FruitsMarket_ReactVite/blob/main/Screenshot%20(794).png" alt="View" width="700"/>
</p>

---

## 📤 Google Form Integration
Order data is sent to Google Forms

Each field uses its own entry.XXXXXXX ID

Sent via fetch() with FormData and no-cors mode

```
fetch(GOOGLE_FORM_URL, {
  method: "POST",
  mode: "no-cors",
  body: formData,
});
```
---
## 📍 Map Location Selection
Integrated using React-Leaflet

User clicks on the map to select delivery location

Marker and coordinates are saved

```
useMapEvents({
  click(e) {
    onLocationSelect(e.latlng);
  },
});
```
---
🗂 Folder Structure
```
fruit-store/
├── public/
├── src/
│   ├── components/
│   │   ├── Navbar.jsx
│   │   ├── FruitCard.jsx
│   │   ├── Pay.jsx
│   │   ├── Summary.jsx
│   │   ├── About.jsx
│   │   ├── Footer.jsx
│   │   └── Recent.jsx
│   ├── App.jsx
│   └── main.jsx
├── package.json
└── index.css
```
---
##  Credits
Built by: Hrishikesh

---
