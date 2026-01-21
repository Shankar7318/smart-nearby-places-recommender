# Smart Nearby Places Recommender 🗺️

A React application that recommends nearby places based on user preferences (**Work, Date, Quick Bite, Budget**) using **Google Maps API** and **Google Places API**.

---

## 🚀 Features

### 🔹 Four Smart Modes

- 💼 **Work Mode**  
  Find quiet cafes and libraries with WiFi and power outlets.

- ❤️ **Date Mode**  
  Discover romantic restaurants, parks, and entertainment spots.

- 🍔 **Quick Bite**  
  Fast food options open now within walking distance.

- 💰 **Budget Mode**  
  Affordable places with great value nearby.

---

### 🔹 Real-time Data

- Live Google Places API integration  
- Current opening hours status  
- Live ratings and reviews  
- Distance calculation from user location  

---

### 🔹 Advanced Filtering & Sorting

- Filter by price level: `Free`, `$`, `$$`, `$$$`, `$$$$`
- Sort by:
  - Distance
  - Rating
  - Price
  - Popularity
- Open Now filter  
- Minimum rating filter  

---

### 🔹 Interactive Map

- Google Maps integration  
- Visual markers for nearby places  
- User location tracking  
- Interactive navigation  

---

## 🛠️ Tech Stack

- **Frontend:** React 18, JavaScript (ES6+), JSX  
- **Maps:** Google Maps JavaScript API, `@react-google-maps/api`  
- **APIs:**  
  - Google Places API  
  - Geocoding API  
  - Distance Matrix API  
- **UI:** CSS3, React Icons  
- **Utilities:** Axios, Lodash, date-fns  
- **Build Tool:** Create React App  

---

## 📦 Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/Shankar7318/smart-nearby-places-recommender.git
cd smart-nearby-places-recommender

2️⃣ Install dependencies
npm install

3️⃣ Set up environment variables

Create a .env file in the root directory:

REACT_APP_GOOGLE_MAPS_API_KEY=your_google_maps_api_key_here

4️⃣ Start the development server
npm start

🔑 Google Maps API Setup
Step 1: Create Google Cloud Project

Go to Google Cloud Console

Create a new project

Step 2: Enable Required APIs

Enable the following APIs:

Maps JavaScript API

Places API (Most Important)

Geocoding API

Distance Matrix API

Step 3: Create API Credentials

Go to APIs & Services → Credentials

Create an API Key

Step 4: Restrict the API Key

Application Restrictions:

Websites

Add:

http://localhost:3000/*
http://localhost:3001/*
http://localhost:*


API Restrictions:

Allow only the 4 enabled APIs

Step 5: Enable Billing

Required for API usage

Free Tier: $200/month credit
```
## 📁 Project Structure
```
smart-nearby-places-recommender/
├── public/
│   ├── index.html
│   └── favicon.ico
├── src/
│   ├── components/
│   │   ├── ModeSelector.jsx
│   │   ├── PlaceCard.jsx
│   │   ├── FilterSortPanel.jsx
│   │   ├── MapView.jsx
│   │   └── LoadingSpinner.jsx
│   ├── services/
│   │   ├── placesService.js
│   │   └── mapsService.js
│   ├── utils/
│   │   └── filters.js
│   ├── styles/
│   │   └── App.css
│   ├── App.js
│   └── index.js
├── .env
├── package.json
└── README.md
```
## 🎯 How to Use
 # 1️⃣ Allow Location Access

Grant location permissions when prompted

App uses your real-time location

 # 2️⃣ Select a Mode

Choose from Work / Date / Quick Bite / Budget

Each mode applies pre-configured filters

# 3️⃣ Browse Recommendations

View places on the interactive map

Check distance, rating, and opening hours

# 4️⃣ Filter & Sort

Apply additional filters from the sidebar

Sort by distance, rating, or price

Toggle Open Now for current availability

# Configuration
 - Customizing Modes

Modify the MODES object in App.js:
```
const MODES = {
  work: {
    name: 'Work',
    icon: '💼',
    filters: {
      types: ['cafe', 'library', 'coffee_shop'],
      maxDistance: 2000,
      amenities: ['wifi', 'power_outlets']
    }
  },
  // Add more modes here
};```
