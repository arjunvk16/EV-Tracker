⚡ EV Charge Tracker — Kerala Edition

A sleek, mobile-first Progressive Web App (PWA) designed to meticulously track your Electric Vehicle (EV) charging sessions, costs, and efficiency. Tailored specifically for EV owners in Kerala, this app features built-in tariff calculators for KSEB Domestic (Home charging) and ChargeMOD (Outside fast charging).

✨ Features

📱 Mobile-First Design & PWA: Feels exactly like a native app. Install it directly to your smartphone's home screen.

🏠 Home Charging (KSEB): Automatically calculates energy usage and cost based on the latest KSEB telescopic domestic tariff slabs (₹3.25 to ₹8.20/unit). Just enter your Start and End battery percentages.

⏱️ Auto-Time Calculation: No need to manually enter charging durations at home. The app uses a customizable calibration profile to automatically calculate how long your car took to charge.

⚡ Outside Charging (ChargeMOD): Input the exact kWh from your ChargeMOD invoice. Automatically calculates the service charge and 18% GST for accurate out-of-pocket tracking.

📊 Comprehensive Reports: Dynamic dashboard and reporting tools to view your data by Week, Month, or Year. Features a beautiful, Retina-ready bar chart comparing Home vs. Outside spending.

☁️ Cloud Sync: Powered by Firebase Firestore. Your charging history is securely saved in the cloud and synced across all your devices.

🛠️ Configuration & Settings

Before logging your first session, navigate to the Settings (⚙️) tab to customize the app for your specific vehicle:

Battery Configuration:

Enter your EV's usable battery capacity in kWh (e.g., 3.97).

This is strictly used to convert your home charging battery percentages into accurate kWh usage.

Home Charging Speed Calibration:

Set a benchmark for your home charger.

Example: If charging from 47% to 100% takes exactly 3 Hours and 7 Minutes, enter those values. The app will use this benchmark to automatically calculate the duration of all future home charging sessions.

📝 How to Log a Session

For Home Charging:

Select 🏠 Home (KSEB).

Enter the Date.

Enter your Start Battery % and End Battery %.

The app will instantly preview your estimated energy added, charging duration, and KSEB cost.

Add a location/note (optional) and click Save Session.

For Outside Charging:

Select ⚡ Outside (Fast).

Enter the Date.

Enter the exact kWh Used from your ChargeMOD app or invoice.

Enter the Start and End time of your session.

The app will preview your effective cost (Service + GST).

Click Save Session.

(Note: If you make a mistake, you can easily update or delete any log from the History tab).

🚀 Hosting & Deployment

This application is built as a highly portable, single-file application.

Quick Start

Drop index.html onto any static hosting provider (GitHub Pages, Vercel, Netlify, etc.).

That's it!

Enabling PWA (Install to Home Screen)

While the app injects a dynamic Web Manifest, for full offline and PWA capabilities on your custom domain:

Open the app in your browser.

Go to the Settings tab.

Under the 📲 Install as App section, click "Export sw.js & manifest.json".

Place the downloaded sw.js and manifest.json files in the exact same root folder as your index.html on your web host.

Firebase Setup (For Developers)

If you are forking this project for your own use, you will need to replace the firebaseConfig object at the top of the index.html file with your own Firebase project credentials to ensure your data is kept private in your own Firestore database. Ensure you have initialized a Firestore Database and enabled unrestricted Web SDK access (or configured App Check).
