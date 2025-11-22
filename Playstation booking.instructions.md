<!doctype html>
<html lang="en">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PlayStation Booking System - Deployment Package</title>
  <style>
        body {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            color: #ffffff;
            min-height: 100vh;
            overflow-x: hidden;
        }

        * {
            box-sizing: border-box;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 40px;
        }

        .header h1 {
            font-size: 48px;
            margin: 0 0 10px 0;
            color: #0072ff;
            text-shadow: 0 0 20px rgba(0, 114, 255, 0.5);
        }

        .header p {
            font-size: 18px;
            opacity: 0.8;
            margin: 10px 0;
        }

        .deployment-options {
            display: grid;
            gap: 30px;
            margin-top: 40px;
        }

        .option-card {
            background: rgba(255, 255, 255, 0.08);
            padding: 30px;
            border-radius: 15px;
            border-left: 4px solid #0072ff;
        }

        .option-card h2 {
            margin: 0 0 15px 0;
            font-size: 28px;
            color: #0072ff;
        }

        .option-card h3 {
            margin: 20px 0 10px 0;
            font-size: 20px;
            color: #00ff00;
        }

        .difficulty {
            display: inline-block;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: bold;
            margin-bottom: 15px;
        }

        .easy {
            background: rgba(0, 255, 0, 0.2);
            color: #00ff00;
            border: 1px solid #00ff00;
        }

        .medium {
            background: rgba(255, 165, 0, 0.2);
            color: #ffa500;
            border: 1px solid #ffa500;
        }

        .advanced {
            background: rgba(255, 0, 0, 0.2);
            color: #ff6b6b;
            border: 1px solid #ff6b6b;
        }

        .code-block {
            background: rgba(0, 0, 0, 0.4);
            padding: 20px;
            border-radius: 10px;
            margin: 15px 0;
            overflow-x: auto;
            position: relative;
        }

        .code-block pre {
            margin: 0;
            color: #00ff00;
            font-family: 'Courier New', monospace;
            font-size: 14px;
            white-space: pre-wrap;
        }

        .filename {
            color: #ffa500;
            font-weight: bold;
            margin-bottom: 10px;
            display: block;
        }

        .step {
            margin: 20px 0;
            padding-left: 30px;
            position: relative;
        }

        .step::before {
            content: "→";
            position: absolute;
            left: 0;
            color: #0072ff;
            font-weight: bold;
            font-size: 20px;
        }

        .feature-list {
            list-style: none;
            padding: 0;
            margin: 15px 0;
        }

        .feature-list li {
            padding: 8px 0;
            padding-left: 25px;
            position: relative;
        }

        .feature-list li::before {
            content: "✓";
            position: absolute;
            left: 0;
            color: #00ff00;
            font-weight: bold;
        }

        .warning-box {
            background: rgba(255, 165, 0, 0.1);
            border: 2px solid rgba(255, 165, 0, 0.5);
            padding: 15px;
            border-radius: 10px;
            margin: 15px 0;
        }

        .warning-box strong {
            color: #ffa500;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: #0072ff;
            color: #ffffff;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            font-size: 16px;
            cursor: pointer;
            text-decoration: none;
            transition: all 0.3s ease;
            margin: 10px 10px 10px 0;
        }

        .btn:hover {
            background: #0056cc;
        }

        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }

        .comparison-table th,
        .comparison-table td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .comparison-table th {
            background: rgba(0, 114, 255, 0.2);
            font-weight: bold;
        }

        .comparison-table td:first-child {
            font-weight: 600;
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 32px;
            }

            .code-block {
                font-size: 12px;
            }
        }
    </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
  <script src="/_sdk/element_sdk.js" type="text/javascript"></script>
  <script src="https://cdn.tailwindcss.com" type="text/javascript"></script>
 </head>
 <body>
  <div class="container">
   <div class="header">
    <h1>🚀 Deployment Guide</h1>
    <p>Choose your deployment method to make your PlayStation Booking System live!</p>
   </div>
   <div class="deployment-options"><!-- Option 1: Netlify/Vercel (Easiest) -->
    <div class="option-card"><span class="difficulty easy">⭐ EASIEST - RECOMMENDED</span>
     <h2>Option 1: Deploy to Netlify (Free)</h2>
     <p><strong>Best for:</strong> Beginners, no coding experience needed, completely free!</p>
     <ul class="feature-list">
      <li>No server setup required</li>
      <li>Free SSL certificate (HTTPS)</li>
      <li>Free custom domain support</li>
      <li>Instant global CDN</li>
      <li>100% free forever</li>
     </ul>
     <h3>📝 Step-by-Step Instructions:</h3>
     <div class="step"><strong>Step 1:</strong> Create a new folder on your computer called <code>playstation-booking</code>
     </div>
     <div class="step"><strong>Step 2:</strong> Inside that folder, create a file called <code>index.html</code> and paste this code:
     </div>
     <div class="code-block"><span class="filename">📄 index.html</span>
      <pre>&lt;!-- Copy the standalone HTML code I provided earlier --&gt;
&lt;!-- The complete code from the previous message --&gt;</pre>
     </div>
     <div class="step"><strong>Step 3:</strong> Go to <a href="https://www.netlify.com" target="_blank" class="btn">Netlify.com</a>
     </div>
     <div class="step"><strong>Step 4:</strong> Sign up for free (use your email or GitHub)
     </div>
     <div class="step"><strong>Step 5:</strong> Drag and drop your <code>playstation-booking</code> folder onto the Netlify dashboard
     </div>
     <div class="step"><strong>Step 6:</strong> Wait 30 seconds... Done! 🎉 Your site is live!
     </div>
     <div class="warning-box"><strong>⚠️ Important:</strong> With this free option, bookings are saved in the user's browser (localStorage). Each visitor has their own separate data. For shared bookings across all users, see Option 3 below.
     </div><a href="https://www.netlify.com" target="_blank" class="btn">Deploy to Netlify Now →</a>
    </div><!-- Option 2: GitHub Pages -->
    <div class="option-card"><span class="difficulty easy">⭐ EASY</span>
     <h2>Option 2: GitHub Pages (Free)</h2>
     <p><strong>Best for:</strong> Free hosting with version control</p>
     <h3>📝 Instructions:</h3>
     <div class="step"><strong>Step 1:</strong> Create a GitHub account at <a href="https://github.com" target="_blank" class="btn">GitHub.com</a>
     </div>
     <div class="step"><strong>Step 2:</strong> Create a new repository named <code>playstation-booking</code>
     </div>
     <div class="step"><strong>Step 3:</strong> Upload your <code>index.html</code> file
     </div>
     <div class="step"><strong>Step 4:</strong> Go to Settings → Pages → Select "main" branch → Save
     </div>
     <div class="step"><strong>Step 5:</strong> Your site will be live at: <code>https://yourusername.github.io/playstation-booking</code>
     </div>
     <div class="warning-box"><strong>⚠️ Important:</strong> Same as Option 1 - bookings are saved per browser. For centralized data, use Option 3.
     </div>
    </div><!-- Option 3: Full Backend Solution -->
    <div class="option-card"><span class="difficulty medium">⭐⭐ RECOMMENDED FOR PRODUCTION</span>
     <h2>Option 3: Firebase (Shared Database)</h2>
     <p><strong>Best for:</strong> Real booking system where all users see the same bookings</p>
     <ul class="feature-list">
      <li>All bookings saved in one database</li>
      <li>Real-time updates across all devices</li>
      <li>Free tier: 50,000 reads/day, 20,000 writes/day</li>
      <li>Automatic backups</li>
      <li>Mobile app support</li>
     </ul>
     <h3>📝 Complete Setup:</h3>
     <div class="step"><strong>Step 1:</strong> Go to <a href="https://firebase.google.com" target="_blank" class="btn">Firebase.google.com</a>
     </div>
     <div class="step"><strong>Step 2:</strong> Create a new project called "PlayStation Booking"
     </div>
     <div class="step"><strong>Step 3:</strong> Enable Firestore Database (choose "Start in test mode" for now)
     </div>
     <div class="step"><strong>Step 4:</strong> Enable Firebase Hosting
     </div>
     <div class="step"><strong>Step 5:</strong> Create these files in your project folder:
     </div>
     <div class="code-block"><span class="filename">📄 index.html (Frontend with Firebase)</span>
      <pre>&lt;!DOCTYPE html&gt;
&lt;html lang="en"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;PlayStation Booking System&lt;/title&gt;
    
    &lt;!-- Firebase SDK --&gt;
    &lt;script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-app-compat.js"&gt;&lt;/script&gt;
    &lt;script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-firestore-compat.js"&gt;&lt;/script&gt;
    
    &lt;!-- Your styles from the standalone version --&gt;
    &lt;style&gt;
        /* Copy all the CSS from the standalone version */
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;!-- Copy all the HTML from the standalone version --&gt;
    
    &lt;script&gt;
        // Firebase Configuration (Get this from Firebase Console)
        const firebaseConfig = {
            apiKey: "YOUR_API_KEY",
            authDomain: "YOUR_PROJECT.firebaseapp.com",
            projectId: "YOUR_PROJECT_ID",
            storageBucket: "YOUR_PROJECT.appspot.com",
            messagingSenderId: "YOUR_SENDER_ID",
            appId: "YOUR_APP_ID"
        };
        
        // Initialize Firebase
        firebase.initializeApp(firebaseConfig);
        const db = firebase.firestore();
        
        // Replace localStorage functions with Firebase
        async function saveBooking(bookingData) {
            try {
                await db.collection('bookings').add(bookingData);
                return true;
            } catch (error) {
                console.error('Error saving booking:', error);
                return false;
            }
        }
        
        async function loadBookings() {
            try {
                const snapshot = await db.collection('bookings').get();
                return snapshot.docs.map(doc =&gt; ({
                    id: doc.id,
                    ...doc.data()
                }));
            } catch (error) {
                console.error('Error loading bookings:', error);
                return [];
            }
        }
        
        async function deleteBooking(bookingId) {
            try {
                await db.collection('bookings').doc(bookingId).delete();
                return true;
            } catch (error) {
                console.error('Error deleting booking:', error);
                return false;
            }
        }
        
        // Real-time updates
        db.collection('bookings').onSnapshot((snapshot) =&gt; {
            allBookings = snapshot.docs.map(doc =&gt; ({
                id: doc.id,
                ...doc.data()
            }));
            renderBookings(allBookings);
            checkAvailability();
        });
        
        // Rest of your JavaScript code from standalone version
        // Replace localStorage calls with Firebase functions
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;</pre>
     </div>
     <div class="code-block"><span class="filename">📄 firebase.json</span>
      <pre>{
  "hosting": {
    "public": ".",
    "ignore": [
      "firebase.json",
      "**/.*",
      "**/node_modules/**"
    ]
  },
  "firestore": {
    "rules": "firestore.rules"
  }
}</pre>
     </div>
     <div class="code-block"><span class="filename">📄 firestore.rules</span>
      <pre>rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /bookings/{booking} {
      allow read: if true;
      allow write: if true;
      allow delete: if true;
    }
  }
}</pre>
     </div>
     <div class="warning-box"><strong>🔒 Security Note:</strong> The rules above allow anyone to read/write. For production, add proper authentication!
     </div>
     <div class="step"><strong>Step 6:</strong> Deploy using Firebase CLI:
     </div>
     <div class="code-block">
      <pre># Install Firebase CLI
npm install -g firebase-tools

# Login to Firebase
firebase login

# Initialize project
firebase init

# Deploy
firebase deploy</pre>
     </div><a href="https://firebase.google.com/docs/hosting/quickstart" target="_blank" class="btn">Firebase Hosting Guide →</a>
    </div><!-- Comparison Table -->
    <div class="option-card">
     <h2>📊 Comparison Table</h2>
     <table class="comparison-table">
      <thead>
       <tr>
        <th>Feature</th>
        <th>Netlify/GitHub</th>
        <th>Firebase</th>
       </tr>
      </thead>
      <tbody>
       <tr>
        <td>Setup Difficulty</td>
        <td>⭐ Very Easy</td>
        <td>⭐⭐ Moderate</td>
       </tr>
       <tr>
        <td>Cost</td>
        <td>Free Forever</td>
        <td>Free (50K reads/day)</td>
       </tr>
       <tr>
        <td>Shared Bookings</td>
        <td>❌ No (per-browser)</td>
        <td>✅ Yes (everyone sees same data)</td>
       </tr>
       <tr>
        <td>Real-time Updates</td>
        <td>❌ No</td>
        <td>✅ Yes</td>
       </tr>
       <tr>
        <td>Data Persistence</td>
        <td>Browser only</td>
        <td>Cloud database</td>
       </tr>
       <tr>
        <td>Mobile App Ready</td>
        <td>✅ Yes (responsive web)</td>
        <td>✅ Yes (+ native apps)</td>
       </tr>
       <tr>
        <td>Custom Domain</td>
        <td>✅ Yes (free)</td>
        <td>✅ Yes (free)</td>
       </tr>
       <tr>
        <td>SSL Certificate</td>
        <td>✅ Auto (free)</td>
        <td>✅ Auto (free)</td>
       </tr>
      </tbody>
     </table>
    </div><!-- Quick Start Recommendation -->
    <div class="option-card">
     <h2>🎯 My Recommendation</h2>
     <h3>For Testing &amp; Quick Demo:</h3>
     <p>→ Use <strong>Option 1 (Netlify)</strong> - Takes 5 minutes, completely free, perfect for showing to clients or testing.</p>
     <h3>For Real Business Use:</h3>
     <p>→ Use <strong>Option 3 (Firebase)</strong> - Proper database, all users see same bookings, real-time updates, professional solution.</p>
     <div class="warning-box"><strong>💡 Pro Tip:</strong> Start with Option 1 to test everything. Once you're happy with how it works, upgrade to Option 3 for the real deployment. The code is 90% the same!
     </div>
     <h3>Need Help?</h3>
     <p>Common questions:</p>
     <ul class="feature-list">
      <li><strong>Q:</strong> Can I use my own domain name?<br><strong>A:</strong> Yes! All options support custom domains (like www.yourlounge.com)</li>
      <li><strong>Q:</strong> Will it work on mobile phones?<br><strong>A:</strong> Yes! Fully responsive design works on all devices</li>
      <li><strong>Q:</strong> Can I edit the design/colors later?<br><strong>A:</strong> Yes! Just edit the HTML file and re-deploy</li>
      <li><strong>Q:</strong> Is my data safe?<br><strong>A:</strong> With Firebase (Option 3), yes! Google handles all security and backups</li>
     </ul>
     <div class="step"><strong>Ready to deploy?</strong> Pick the option that works best for you above! 🚀
     </div>
    </div>
   </div>
  </div>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9a19ea97f27818ec',t:'MTc2MzY2MjM1NS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>