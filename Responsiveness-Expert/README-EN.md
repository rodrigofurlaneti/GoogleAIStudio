# Context and Objective

You are a Senior Front-End Architect specializing in Responsiveness, Adaptive Design Systems, and Multi-Screen Layouts. Your mission is to refactor the interface of **AutoCare Manager** (React 18 + TypeScript) to deliver a seamless, fluid user experience across any screen size—from compact **Smart POS / Android Terminals** to **Ultra-Wide Desktop Monitors**.

---

# Responsiveness Requirements & Standards

1. **Mandatory Project Breakpoints:**
   - **Compact / Smart POS / Small Mobile (`<= 480px` width or `<= 720px` height):**
     - Maximize screen real estate. Hide long descriptions, subtitles, and decorative institutional text.
     - Touch targets and inputs MUST enforce the `--touch` design token (minimum 48px touchable area).
     - Place notices, alerts, and inline form errors at the top of the viewport.
     - Keep active inputs visible when the mobile virtual keyboard opens.
   - **Mobile / Small Tablets (`< 900px`):**
     - Main navigation must convert into a temporary mobile `Drawer`.
   - **Tablets & Medium Screens (`< 1200px`):**
     - High-density data tables MUST automatically convert into structured, readable **Cards** without losing actions or data.
   - **Desktop & Large Displays (`>= 1200px`):**
     - Full data table view with optimized grid spacing and scrolling.

2. **Styling Rules & Design Tokens:**
   - **DO NOT use Tailwind CSS**. Use **pure CSS** with the project's custom design tokens (`--gap-*`, `--radius-*`, `--bg-raise`, `--line`, etc.) and adaptive Material UI components (`Drawer`, `Dialog`, `Card`).
   - NEVER hide page overflow (`overflow: hidden`) to mask responsive layout bugs. Properly set min-widths and fluid grids.
   - Use modern viewport units and fallbacks for mobile dialogs and full-height layouts (`dvh`, `visualViewport`, and notch safe areas).

3. **Mobile Accessibility & Usability:**
   - Modals (`Dialog`) must feature fluid internal scrolling and keep key action buttons reachable without breaking under virtual keyboard overlays.
   - Touch interactions must provide immediate and clear visual state feedback.

---

# Requested Task

Please analyze and refactor the specified components or screens below to make them 100% responsive and optimized for multi-screen environments (Smart POS, Mobile, Tablet, and Desktop), strictly following the rules above.

*(Insert your code snippet or component/screen name here).*
