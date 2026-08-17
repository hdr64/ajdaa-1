# React App Luxury Design & UX Improvement Plan

Enhance the design and user experience of the **React App (`aqar-react-ts`)** for **دار الأوج العقارية**, bringing it to a luxury, state-of-the-art real estate platform with high-end dark glassmorphism visuals, smooth micro-animations, interactive property quick views, grid/list view toggles, functional search filtering, and an elevated booking workflow.

## User Review Required

> [!NOTE]
> All changes strictly target `aqar-react-ts` (the React version) and leave the standalone HTML version untouched as requested.

> [!TIP]
> The app is running locally on Vite (`http://localhost:5174/`). Changes will be verified in the browser.

## Proposed Changes

### Styling & Theme Foundations

#### [MODIFY] [`index.css`](file:///d:/projects/html/aqar1/aqar-react-ts/src/index.css)
- Upgrade luxury color system with deep midnight canvas, cyan/teal neon glow (`--accent`), and warm champagne gold accents (`--gold`).
- Add glassmorphism utilities (`glass-card-luxury`, `gradient-border`, `glow-shadow`, `shimmer-text`).
- Add smooth entrance transitions, modal backdrop blurs, and hover micro-animations.

---

### Components & Features

#### [NEW] [`PropertyModal.tsx`](file:///d:/projects/html/aqar1/aqar-react-ts/src/components/common/PropertyModal.tsx)
- Create a luxury Property Details Modal popping up when clicking a property card.
- Includes high-res image showcase, property type & status tags, feature chips (Smart Home, Swimming Pool, Parking, Security, Garden, Central AC), full specs (bedrooms, bathrooms, area, city), contact buttons (WhatsApp, Call), and direct "احجز معاينة" trigger.

#### [MODIFY] [`PropertyCard.tsx`](file:///d:/projects/html/aqar1/aqar-react-ts/src/components/common/PropertyCard.tsx)
- Elevate design with gradient borders on hover, floating status badge ("بيع" / "إيجار"), heart favorite animation with instant toast feedback.
- Add "عرض التفاصيل" (Quick View) button alongside "احجز الآن".

#### [MODIFY] [`HeroSection.tsx`](file:///d:/projects/html/aqar1/aqar-react-ts/src/components/home/HeroSection.tsx) & [`HeroScene.tsx`](file:///d:/projects/html/aqar1/aqar-react-ts/src/components/home/HeroScene.tsx)
- Enhance quick search bar with interactive buy/rent tabs, styled select dropdowns, and active filter hand-off to the `WorksPage`.
- Upgrade badge visual style and stats cards.
- Refine 3D geometry in `HeroScene.tsx` for smooth rotation and subtle ambient ambient glow particles.

#### [MODIFY] [`WorksPage.tsx`](file:///d:/projects/html/aqar1/aqar-react-ts/src/components/works/WorksPage.tsx)
- Add Grid vs. List View mode switcher.
- Add instant search query filtering, price range / transaction type filter pills, city filter dropdown, and category badges with live property counts.
- Integrate property quick view modal trigger.

#### [MODIFY] [`BookingView.tsx`](file:///d:/projects/html/aqar1/aqar-react-ts/src/components/booking/BookingView.tsx)
- Enhance 3-step booking flow with visit type selection (حضور شخصي / جولة افتراضية 3D), time slot picker (10:00 AM, 2:00 PM, 5:00 PM, 8:00 PM), property summary panel, and animated confirmation receipt card.

#### [MODIFY] [`ServicesSection.tsx`](file:///d:/projects/html/aqar1/aqar-react-ts/src/components/home/ServicesSection.tsx), [`ProcessSection.tsx`](file:///d:/projects/html/aqar1/aqar-react-ts/src/components/home/ProcessSection.tsx), [`StatsSection.tsx`](file:///d:/projects/html/aqar1/aqar-react-ts/src/components/home/StatsSection.tsx) & [`Testimonials.tsx`](file:///d:/projects/html/aqar1/aqar-react-ts/src/components/home/Testimonials.tsx)
- Refine layout aesthetics, border glows, quote accents, star ratings, and subtle hover animations.

#### [MODIFY] [`Navbar.tsx`](file:///d:/projects/html/aqar1/aqar-react-ts/src/components/common/Navbar.tsx) & [`App.tsx`](file:///d:/projects/html/aqar1/aqar-react-ts/src/App.tsx)
- Integrate Property Quick View Modal state globally in `App.tsx`.
- Enhance main Footer with multi-column quick links, brand highlights, social media icons, and newsletter form.
- Enhance Toast Notification with animated progress bar and icon.

## Verification Plan

### Automated Verification
- Run `npm run build` inside `aqar-react-ts` using `run_command` to verify TypeScript compilation and TailwindCSS v4 build with zero errors.

### Manual / Visual Verification
- Use `browser_subagent` to navigate `http://localhost:5174/` and verify visual design, page transitions, modal opening, filters in Works page, and booking flow.
