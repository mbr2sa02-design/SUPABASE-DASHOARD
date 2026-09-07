MBR2 App Package — Install Instructions
ការណែនាំដំឡើងកម្មវិធី MBR2
=========================================

WHAT'S IN THIS FOLDER / អ្វីដែលមាននៅក្នុងកញ្ចប់នេះ
-----------------------------------------
1. dashboard/            → MBR2 Sponsorship Management Dashboard
                            (the CVC App is built into this same file —
                             open it and add "?view=cvc" to the link to
                             get the phone-friendly CVC-only view, e.g.
                             https://yoursite.com/dashboard/?view=cvc)
2. rc-monitoring-app/    → RC Monitoring App (the one just fixed)

Both are installable web apps (PWAs) — no app store needed. They must be
hosted online (e.g. your existing GitHub Pages site) over HTTPS for the
"Install" feature to appear; opening the files directly from your computer
(file://) will NOT show an install option in most browsers.

ចំណារ: កម្មវិធីទាំងពីរនេះជាកម្មវិធីវេប (PWA) — មិនចាំបាច់ទាញយកតាម App Store ទេ។
ត្រូវតែដាក់ឡើងលើអ៊ីនធឺណិត (ដូចជា GitHub Pages ដែលអ្នកកំពុងប្រើ) តាមរយៈ HTTPS
ដើម្បីឲ្យប៊ូតុង "ដំឡើង / Install" លេចឡើង។ ការបើកឯកសារផ្ទាល់ពីកុំព្យូទ័រ
(file://) នឹងមិនបង្ហាញជម្រើសដំឡើងទេ។


STEP 1 — UPLOAD TO YOUR HOSTING
--------------------------------
Upload each folder's contents to its own page/repo on GitHub Pages (or
wherever you currently host the dashboard and monitoring app), keeping
index.html together with its manifest.json and icon files in the same
folder. Do not rename or move icon-192.png / icon-512.png / manifest.json
away from index.html — the dashboard looks for them right next to itself.

ជំហានទី ១ — ផ្ទុកឡើងទៅកន្លែងបង្ហោះរបស់អ្នក
ផ្ទុកឯកសារនីមួយៗឡើងទៅ GitHub Pages (ឬកន្លែងបង្ហោះបច្ចុប្បន្នរបស់អ្នក)
ដោយរក្សា index.html ជាមួយ manifest.json និងឯកសាររូបតំណាង (icon) នៅក្នុង
ថតតែមួយ។


STEP 2 — INSTALL ON PHONE / ជំហានទី ២ — ដំឡើងលើទូរស័ព្ទ
--------------------------------------------------------

ANDROID (Chrome):
  1. Open the app's link in Chrome.
  2. Tap the ⋮ menu (top right).
  3. Tap "Install app" or "Add to Home screen".
  4. Confirm — the app icon appears on your home screen like a normal app.

  ១. បើកតំណកម្មវិធីនៅក្នុង Chrome។
  ២. ចុចម៉ឺនុយ ⋮ (ខាងលើស្តាំ)។
  ៣. ចុច "ដំឡើងកម្មវិធី" ឬ "បន្ថែមទៅអេក្រង់ដើម"។
  ៤. បញ្ជាក់ — រូបតំណាងកម្មវិធីនឹងបង្ហាញនៅលើអេក្រង់ដើមរបស់អ្នក។

iPHONE (Safari — must use Safari, not Chrome):
  1. Open the app's link in Safari.
  2. Tap the Share icon (square with an arrow, bottom bar).
  3. Scroll down and tap "Add to Home Screen".
  4. Tap "Add" — the app icon appears on your home screen.

  ១. បើកតំណកម្មវិធីនៅក្នុង Safari (ត្រូវប្រើ Safari ប៉ុណ្ណោះ)។
  ២. ចុចរូប Share (ការចែករំលែក)។
  ៣. រំកិលចុះក្រោម ហើយចុច "Add to Home Screen"។
  ៤. ចុច "Add" — រូបតំណាងកម្មវិធីនឹងបង្ហាញនៅលើអេក្រង់ដើម។


STEP 3 — INSTALL ON COMPUTER / ជំហានទី ៣ — ដំឡើងលើកុំព្យូទ័រ
---------------------------------------------------------------

CHROME or EDGE (Windows/Mac/Linux):
  1. Open the app's link.
  2. Look for an install icon (a small monitor with a ↓ arrow) at the
     right side of the address bar — click it.
     (If you don't see it: click the ⋮ menu → "Install [app name]...")
  3. Click "Install" in the popup.
  4. The app opens in its own window and is added to your Start
     Menu / Applications, like a desktop program.

  ១. បើកតំណកម្មវិធី។
  ២. រកមើលរូបតំណាងដំឡើង (រូបអេក្រង់តូចមានព្រួញ ↓) នៅខាងស្តាំរបារអាសយដ្ឋាន
     ហើយចុចវា។ (ប្រសិនបើមិនឃើញ សូមចុចម៉ឺនុយ ⋮ → "Install...")
  ៣. ចុច "Install" នៅក្នុងផ្ទាំងលេចឡើង។
  ៤. កម្មវិធីនឹងបើកនៅក្នុងបង្អួចផ្ទាល់ខ្លួន ហើយបន្ថែមទៅ Start Menu /
     Applications ដូចកម្មវិធីធម្មតា។

SAFARI (Mac, macOS Sonoma or later):
  1. Open the app's link.
  2. File menu → "Add to Dock..."
  3. Confirm — the app appears in your Dock.


NOTES / កំណត់សម្គាល់
----------------------
- These are the same files, not new apps — installing just gives you a
  home-screen/desktop shortcut that opens full-screen without browser
  tabs or address bars. Your data (Firestore) is unchanged either way.
- If "Install" never appears, double-check the site is served over
  HTTPS and that manifest.json / icon files are reachable at the same
  path as index.html (check browser DevTools → Console for a 404).
- The RC Monitoring App generates its own icon automatically and needs
  no extra files — only the dashboard needs the manifest.json + icons
  included in this package.
