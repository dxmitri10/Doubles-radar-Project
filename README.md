DoubleFinder

Find the best doubles vendors near you in Trinidad live, rated, and mapped.

DoubleFinder is a Progressive Web App (PWA) that helps users discover doubles vendors across Trinidad in real time. It features an interactive map, vendor leaderboard, user profiles with gamification, and full account management — all running client-side with no backend required.

Overview
DoubleFinder is built as a multi-page static web application with a consistent dark saffron-and-green design theme inspired by Trinidadian street food culture. All data is persisted via localStorage and live vendor data is pulled from the OpenStreetMap Overpass API and Google Maps.

 Features
Home (index.html)

Hero section with animated headline and CTAs
Platform stats: 240+ vendors listed, 18K users, 4.8★ average rating
Feature highlights and vendor showcase sections
Fully responsive navigation with auth-aware links

Authentication (login.html, register.html)

Login with username or email
Demo credentials auto-fill: bob / bobpass
Registration with first/last name, username, email, password
Live password strength meter (5-level scoring)
Field-level validation with inline error hints
Session stored in localStorage as df_user
Auto-redirect if already logged in

Map (map.html)

Powered by Google Maps JavaScript API with Places library
Vendor data loaded live from OpenStreetMap Overpass API
Vendor sidebar with scrollable cards and open/closed status
Filter buttons: All, Open Now, Has Hours
Click-to-select vendor with animated map marker popups
"Locate Me" button for GPS-based centering
Star ratings overlaid on map popups
Inverted dark map theme to match app aesthetic

Leaderboard (leaderboard.html)

Live data from OpenStreetMap Overpass API
Tabs: All Doubles Spots / Open Now / Has Hours
Ranked table with vendor name, area, hours, and open status
Smart area detection by GPS coordinates across Trinidad regions
Graceful loading and empty states

Profile (profile.html)

Displays logged-in user's name, username, and email
Stats panel: Reviews written, Favourites saved, Badges earned
Gamification system:

XP earned from reviews (+20), favourites (+10), comments (+15)
Levels: Doubles Newbie → Bara Beginner → Channa Chaser → Pepper Pilgrim → Bara Boss
Animated XP progress bar


Badge system: 6 unlockable badges (e.g., First Review, Double Dozen, Flavour Fanatic)
Tabs: Favourites | Activity | Reviews
Favourites pulled from df_favourites in localStorage
Reviews pulled from df_ratings in localStorage
Logout button clears session and redirects to login

Settings (settings.html)

Profile Information — Edit display name and email (saved locally)
Doubles Preferences — Customize how vendors are shown
Notifications — Toggle update preferences (stored locally)
Privacy & Security — Visibility controls and password change
Danger Zone — Permanent account actions (clear data, delete account)
Sidebar navigation with scroll-spy active state highlighting


PWA Support
DoubleFinder is installable as a Progressive Web App on Android and iOS.

Manifest (manifest.json): Defines app name, icons, theme colour (#F4A300), display mode (standalone), orientation, and language (en-TT)
Service Worker (sw.js): Caches all core pages on install, serves them offline with a cache-first strategy, and cleans up old caches on activation
Supports apple-mobile-web-app-capable and theme-color meta tags for native-like appearance on iOS and Android

External Dependencies
Google Maps JavaScript API
OpenStreetMap Overpass API
Google Fonts

To test the full experience, use the demo account:
Username: bob
Email: bob@gmail.com
Password: bobpass

