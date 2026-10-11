# Exploratory Testing Session Notes

## 🎯 Session Charter
* **Mission:** Explore the mobile web version of the application to identify responsive design defects, layout overlaps, or functional breaks.
* **Duration:** 15 minutes
* **Environment:** Google Chrome Mobile Emulation (iPhone / Pixel Viewport)
* **Tester:** Ivan Suarez Alva

## 🔍 Areas Explored
* Authentication / Login screen responsiveness.
* Navigation menu scaling on portrait and landscape modes.
* Interactive buttons touch-target sizes.

## 🐛 Findings & Observations
* [Describe here any minor issue or behavior found, e.g., "Login button padding collapses slightly when keyboard pops up on mobile portrait view."]

## 🧠 Advanced Exploratory Heuristics Applied
* **Touring Heuristics (The Guidebook Tour):** Validated all main navigation menus, hamburger toggles, and footer links in a compressed mobile viewport (390x844px).
* **Network Throttling Simulation:** Tested mobile performance under simulated "Fast 3G" and "Slow 3G" conditions using Chrome DevTools to evaluate loading spinners and timeout behavior on API requests.
* **Console Error Monitoring:** Verified that no unhandled JavaScript exceptions or broken resource links (`404` / `500`) occur when switching between portrait and landscape orientations.

## 📊 Summary of Mobile Quality Risks
* **Risk Identified:** Potential layout shift (CLS) when dynamic images load inside cards on narrow screens.
* **Recommendation:** Implement strict bounding boxes (`object-fit`) and skeleton loaders to enhance the mobile user experience.