

# Plan: Generate Complete Flutter Rebuild Prompt

This is not an implementation task — it's a documentation/artifact generation task. I will create a single, comprehensive prompt document that captures every pixel-level detail of the ChicSalon React app so an AI in another IDE can rebuild it entirely in native Flutter.

## What the prompt will contain

### 1. Project Overview & Architecture
- App name, purpose, navigation structure (5 tabs: At Salon, At Home, Explore, Bookings, Profile)
- 11 screens total with exact routing
- State management: Gender context (male/female theme switching), Cart context (multi-salon cart with switch modal)

### 2. Complete Design System (pixel-exact)
- **Fonts**: DM Sans (headings + body), Cormorant Garamond (serif accents), Plus Jakarta Sans (sans)
- **Color palette**: 3 theme variants (neutral default, male/blue, female/pink) with every HSL value extracted from index.css
- **Spacing/sizing**: All exact pixel values from components (e.g., avatar 40px, category chips 62px, card radius 20px, bottom nav bar radius 36px)
- **Shadows**: card-shadow, card-shadow-hover, bottom-bar-shadow values
- **Button styles**: btn-themed gradient, sizes, border-radius values

### 3. Component Specifications (every component)
- **BottomNav**: Glassmorphic floating bar, spotlight beam animation with amber glow, 5 tabs with SVG/Lucide icons, exact colors for active/inactive states
- **AppHeader**: Profile avatar + greeting, location picker pill, notification bell with dot indicator
- **GlassGenderToggle**: Glassmorphic container, blue (#3b82f6) for men, pink (#ec4899) for women
- **MiracleSearchBar**: "Find" prefix in Georgia serif, light beam with particle effects, wedge-shaped gradient beam
- **FeaturedCarousel**: Infinite scroll, gradient cards with masked images, pagination dots
- **CategoryChips**: 62px circular images, ring highlight on selection
- **NearbySalonCard**: 200px wide horizontal scroll cards
- **CartPill**: Floating pill with salon thumbnail, count, total, gradient background
- **SalonSwitchModal**: Side-by-side salon comparison with swap icon

### 4. Screen-by-Screen Specifications
Each screen with exact layout, spacing, typography, colors, animations:
- **Home (Index)**: Header → GenderToggle → SearchBar → Categories → FeaturedCarousel → Nearby (horizontal scroll) → Suggested (list) → Book Again
- **SalonDetail**: Hero carousel (280px, rounded-b-28px) → Info card → Tab bar (services/about/reviews/gallery/packages/offers) → Service cards with +/- → Artists → Reviews → Bottom CTA bar
- **BookingFlow**: 3-step wizard (datetime → barber → summary) with step indicator, date selector (14 days), time grid (3 cols), barber selection cards
- **Bookings**: Tab bar (upcoming/completed/cancelled), booking cards with image header + gradient overlay + status badge
- **Explore**: Search + category filter + salon cards (vertical list with 16:10 aspect images)
- **Profile**: Avatar with edit button, menu items list, edit drawer
- **AtHome**: Empty state with MapPin illustration
- **Offers**: Offer cards with copy-code buttons
- **ArtistProfile**: Artist detail page
- **AtHomeBooking**: At-home service booking flow

### 5. Animation Specifications
- fade-in-up: 0→12px translateY, 0.4s
- bounce-in: scale 0.8→1.05→1, 0.35s
- slide-up: translateY 100%→0, 0.3s
- icon-bump: scale 1→1.22→1.08→1.12, 0.35s
- jelly/jelly-avatar: complex scale transforms
- cart-pill-pulse: scale 1→1.03→1, 3s infinite
- Spotlight beam transition: 0.4s cubic-bezier(0.42, 0, 0.58, 1)

### 6. Gender Theme System
- Exact HSL values for all 3 themes (neutral, male, female)
- Background SVG gradients: Male (#C7E3FE → #BDD1F8 → #C7E3FE), Female (#FECCF2 → #DABDF8 → #FDCBF0)
- Animated dots and sparkle particles on background

### 7. Data Models & Mock Data
- Complete type definitions (Salon, Service, Artist, Review, Booking, Category)
- All mock data entries with exact values

### 8. Interaction Patterns
- Active states: opacity 0.7, scale 0.98 on press
- Min touch targets: 44px or 48px
- Horizontal scroll areas with hidden scrollbars
- Drawer/bottom sheet patterns for filters, notifications, location picker, edit profile

## Delivery
I will generate this as a downloadable markdown file at `/mnt/documents/FLUTTER_REBUILD_PROMPT.md` — a single copy-paste-ready prompt that any AI IDE can use to recreate the entire app in native Flutter with pixel accuracy.

