# Scribbly Product Requirements Document (PRD)

**Version:** 1.0 MVP  
**Date:** January 2025  
**Project:** Scribbly - Creative Learning App for Children  
**Status:** Draft - In Progress

---

## Goals and Background Context

### Goals

- Deliver a minimal viable product (MVP) that demonstrates Scribbly's core value proposition: combining letter tracing with creative expression
- Launch on iOS App Store within 3-4 months with 7 letters (A, S, O, B, D, C, E)
- Validate product-market fit with real users (6-year-olds and parents)
- Create a judgment-free learning experience where children can practice letters while building artistic confidence
- Establish foundation for future phases including Android support, additional letters, and advanced features

### Background Context

Scribbly addresses a gap in the children's educational app market: most letter-learning apps focus on drill-based practice without creative expression, while drawing apps lack educational structure. Through competitive analysis and research, we've identified that parents want apps that combine learning with engagement, and children respond better to judgment-free, playful environments.

The market research shows strong demand for educational apps priced at $7.99-$9.99/month, with parents prioritizing ad-free experiences, offline functionality, and clear educational value. Technical feasibility analysis confirms all core features (haptic feedback, drawing mechanics, creative prompts) are achievable with current mobile technology.

Our MVP strategy prioritizes speed to market with a focused feature set that proves the core concept: tracing letters leads naturally to creative transformation, building both motor skills and artistic confidence without failure states or pressure.

### Change Log

| Date | Version | Description | Author |
|------|---------|-------------|--------|
| January 2025 | 1.0 MVP | Initial PRD draft | PM (John) |

---

## Requirements

### Functional Requirements

FR1: The app must allow children to select from 7 letters (A, S, O, B, D, C, E) in both uppercase and lowercase formats.

FR2: In Trace Mode, the selected letter must appear on screen with a visible path for the child to trace with their finger.

FR3: The app must support binary haptic feedback (Off/On) that can be toggled by the child, providing vibration when the trace path deviates from the intended letter shape (when enabled).

FR4: After tracing is complete, the letter template must fade away smoothly, leaving only the child's drawn trace visible on screen.

FR5: The app must provide audio feedback that speaks the letter name and sound when a letter is selected or tracing begins.

FR6: Creative Mode must be accessible from the start (no unlock requirements), allowing children to draw freely using the letter as inspiration.

FR7: The app must provide an Inspiration Button in Creative Mode that plays audio prompts with creative suggestions (e.g., "Turn O into the sun!") - the app speaks to the child, no voice recognition required from the child.

FR8: Creative Mode must include 8 distinct colors selectable by tapping on color buttons - all tool selection is touch-based.

FR9: Creative Mode must include 2 different brush sizes that can be selected by tapping on brush size buttons - all tool selection is touch-based.

FR10: The app must provide an Undo function that removes the last drawing action.

FR11: The app must provide a Clear function that resets the drawing canvas while keeping the letter visible.

FR12: The app must include a Stamps tool with simple shapes and images that can be selected by tapping and placed on the canvas by tapping the desired location - all interactions are touch-based, no voice commands required.

FR13: The app must allow children to save their artwork to the device's photo library.

FR14: The app must allow children to share their artwork via standard iOS share functionality (messaging, email, etc.).

FR15: The app must function completely offline - all core features (tracing, drawing, saving) must work without internet connection.

FR16: The app must support both portrait and landscape orientations on iPad, with portrait-only support for iPhone.

FR17: All creative prompts must be pre-written and stored locally in the app (no AI generation in MVP).

FR18: The app must provide a simple, kid-accessible settings menu where children can toggle haptic feedback On/Off, select mode (Trace or Creative), and access all drawing tools (colors, brushes, stamps) via touch interactions - no voice recognition required.

FR19: Parent settings must be accessible behind a parental gate (e.g., hold two corners for 3 seconds) allowing parents to configure child interest preferences for future prompt personalization.

FR20: The app must display letters in high contrast mode for improved visibility.

### Non-Functional Requirements

NFR1: The app must launch and display the letter selection screen within 2 seconds on iPhone 12 or newer devices.

NFR2: Drawing strokes must appear with less than 50ms latency to provide responsive, natural drawing feel.

NFR3: The app must support iOS 15.0 and newer versions to maximize device compatibility.

NFR4: The app must follow Apple's Human Interface Guidelines for touch target sizes (minimum 44x44 points).

NFR5: All text and UI elements must be sized appropriately for children's viewing, with support for Dynamic Type accessibility settings.

NFR6: The app must comply with COPPA (Children's Online Privacy Protection Act) requirements - no data collection beyond necessary app functionality, no ads, no in-app purchases accessible to children.

NFR7: Artwork saved to device must be stored as high-quality PNG or JPEG files (minimum 1024x1024 resolution for clear printing/sharing).

NFR8: The app must gracefully handle interruptions (phone calls, notifications) without losing drawing progress.

NFR9: Haptic feedback must be optional and respect system-level haptic settings (accessibility preferences).

NFR10: The app must consume minimal battery power during typical 10-15 minute sessions.

NFR11: All audio feedback must be clear and appropriate for 6-year-old comprehension, using native speaker recordings.

NFR12: The app installation size must not exceed 100MB to ensure quick downloads and minimal storage impact.

NFR13: The app must not require any account creation or login - completely anonymous usage.

NFR14: All drawing canvas interactions must support both finger drawing and Apple Pencil (on supported devices) for flexibility.

NFR15: The app must provide smooth animations (60fps) for all transitions, fades, and UI interactions.

---

## User Interface Design Goals

### Overall UX Vision

Scribbly's interface should feel like a **playful, judgment-free playground** where learning happens naturally through creative exploration. The design philosophy centers on **child autonomy** - kids control their experience without restrictions or pressure. Visual design should be **clean and uncluttered** (no overwhelming choices), with **bright, welcoming colors** that spark joy without being distracting. Every interaction should feel **immediate and responsive**, giving children instant feedback that builds confidence. The app should feel **safe and encouraging** - there are no wrong answers, no failure states, only exploration and creativity.

**Key Principles:**
- **Big and Bold:** Large touch targets, clear visual hierarchy, minimal text (rely on icons and visual cues)
- **Forgiving:** Easy to undo, clear to reset, no permanent mistakes
- **Delightful:** Smooth animations, satisfying feedback, moments of surprise and joy
- **Accessible:** High contrast, adjustable sizes, supports all children including those with motor or visual differences

### Key Interaction Paradigms

1. **Touch-First Design:** All interactions optimized for finger drawing and tapping. No complex gestures - simple, intuitive taps and drags.

2. **Mode Switching:** Clear, child-friendly mode selection (Trace vs. Creative) accessible at any time, allowing kids to switch modes mid-session as they choose.

3. **Clean Canvas, Expandable Tools:** Screen shows maximum artwork/canvas space with minimal UI. Single expandable menu button reveals all tools (colors, brushes, stamps, settings, actions) when needed, keeping the creative space uncluttered when closed.

4. **Visual Feedback Over Text:** Icons, colors, and animations communicate meaning - minimize reading requirements since target age is still learning to read.

5. **One-Tap Access:** Core functions (undo, clear, save) always within one tap, never buried in menus.

6. **Immediate Response:** Every tap should provide visual/haptic feedback within 50ms to feel natural and responsive.

### Core Screens and Views

1. **Letter Selection Screen**
   - Simple grid layout of 7 letters (A, S, O, B, D, C, E) - all visible at once, no scrolling needed
   - Toggle for uppercase/lowercase
   - Large, colorful letter tiles with simple illustrations
   - Mode selector (Trace/Creative) prominently displayed

2. **Trace Mode Screen**
   - Large letter displayed center screen with clear tracing path
   - Clean, minimal interface - screen appears blank except for the letter (maximum focus on the task)
   - Expandable menu button provides access to all tools and settings
   - Smooth fade animation when trace completes

3. **Creative Mode Screen**
   - Letter remains visible as inspiration (can be faded/transparent)
   - Drawing canvas takes full screen - clean, uncluttered view of the artwork being created
   - Expandable menu button provides access to all tools:
     - Inspiration button (audio prompts)
     - Color palette (8 colors)
     - Brush sizes (2 options)
     - Stamps tool
     - Haptic toggle (on/off)
     - Mode switcher (Trace/Creative)
     - Action buttons (undo, clear, save, share)
   - When menu is closed, screen shows only the artwork - minimal UI chrome for maximum creative focus

4. **Expandable Menu/Tool Drawer**
   - Single menu button that expands to reveal all tools and options
   - Organized sections: Drawing tools (colors, brushes), Creative tools (stamps, inspiration), Settings (haptic, mode switch), Actions (undo, clear, save, share)
   - Large, clear icons for each option - minimal text, visual-first design
   - Easy to collapse back to clean canvas view
   - Animates smoothly open/closed

5. **Settings Screen**
   - Integrated into expandable menu (haptic toggle, mode switcher)
   - Parent gate access to advanced settings (accessed via hold gesture on corners)
   - Large, clear icons and minimal text

6. **Share/Save Confirmation**
   - Simple success animation
   - Clear confirmation that artwork is saved
   - Easy access to share functionality

### Accessibility: WCAG AA

The app must meet WCAG AA standards for accessibility:

- **High Contrast Mode:** Letters and UI elements must meet 4.5:1 contrast ratio minimum
- **Touch Target Size:** All interactive elements minimum 44x44 points (Apple HIG)
- **Dynamic Type Support:** Text scales with system accessibility settings
- **Color Independence:** Information conveyed through color must also have alternative indicators (icons, patterns)
- **Audio Alternatives:** All audio feedback can be disabled via system settings
- **Haptic Accessibility:** Respects system-level haptic preferences

### Branding

**Visual Identity:**
- To be determined by UX/Design team
- Should be playful, friendly, non-intimidating
- Bright, vibrant colors (but not overwhelming)
- Rounded, soft shapes (friendly, approachable)
- Clean, modern aesthetic (not overly childish)

**Tone of Voice:**
- Encouraging and warm
- Simple language appropriate for 6-year-olds
- Never punitive or judgmental
- Celebratory of effort and creativity

**Color Palette Considerations:**
- Primary colors should be kid-friendly but sophisticated enough for parent approval
- High contrast for visibility and accessibility
- Colors should work in both light and high-contrast modes
- Avoid overly gendered color schemes (no "pink for girls" assumptions)

**Logo/Icon Concepts:**
- Should communicate "drawing + learning" visually
- Simple, recognizable at small sizes (App Store icon)
- Friendly character or playful letter treatment
- Works in monochrome and color

### Target Device and Platforms: Mobile Only (iOS)

**Primary Target:**
- **iPhone:** Portrait orientation, optimized for iPhone 12 and newer
- **iPad:** Both portrait and landscape, optimized for iPad Air and newer

**Screen Size Considerations:**
- Design must work on smallest supported device (iPhone SE)
- Scale gracefully to largest (iPad Pro)
- Responsive layout that adapts to different screen sizes
- Touch targets sized appropriately for small hands (6-year-olds)

**Platform-Specific:**
- Native iOS design language (not trying to mimic other platforms)
- Follows Apple Human Interface Guidelines
- Leverages iOS-specific features (Haptic Engine, Share Sheet, Photo Library access)
- Designed for one-handed use on iPhone (most tools accessible with thumb)

---

## Technical Assumptions

### Repository Structure: Monorepo

**Decision:** Single repository containing all code, assets, and documentation for the Scribbly iOS app.

**Rationale:**
- MVP is a single-platform iOS app (no cross-platform code sharing needed yet)
- Simpler development workflow for small team
- All assets (letter templates, audio files, prompts) in one place
- Easier version control and deployment

**Future Consideration:** If Android development begins in Phase 2, repository structure can be evaluated - may remain monorepo if using cross-platform framework, or move to separate repos if native development.

### Service Architecture: Mobile-Only Client Application

**Decision:** Standalone iOS app with no backend services required for MVP. All functionality works offline.

**Rationale:**
- MVP scope is offline-first (FR15 requires complete offline functionality)
- No user accounts, authentication, or cloud sync needed (NFR13: anonymous usage)
- All prompts are pre-generated and stored locally (FR17)
- Artwork saved locally only (FR13)
- Eliminates backend infrastructure costs and complexity for MVP
- Faster development - focus entirely on iOS app development

**Storage Architecture:**
- Local SQLite database for prompt storage and organization
- iOS Core Data or UserDefaults for app settings/preferences
- Standard iOS file system for artwork storage (Photos Library integration)

**Future Consideration:** Phase 2 may introduce cloud services for:
- AI prompt generation (cloud API calls)
- Artwork cloud backup (optional)
- Parent dashboard analytics (if implemented)
- Multiple device sync (if multi-device support added)

### Testing Requirements: Unit + Integration + Manual Testing

**Decision:** Comprehensive testing approach combining automated and manual testing.

**Rationale:**
- **Unit Testing:** Critical for drawing engine, tracing mechanics, and core business logic
- **Integration Testing:** Verify haptic feedback, audio playback, file saving, share functionality work together
- **Manual Testing:** Essential for child-facing UI - automated tests can't validate "does this feel intuitive to a 6-year-old?"
- **Device Testing:** Must test on physical devices (iPhone SE, iPhone 12+, iPad) - simulators don't accurately test haptics, touch sensitivity, or performance

**Testing Focus Areas:**
- Drawing/tracing accuracy and performance
- Haptic feedback timing and intensity
- Audio playback quality and clarity
- File saving and sharing reliability
- Offline functionality (airplane mode testing)
- Memory usage during long drawing sessions
- Battery impact

### Development Framework: React Native

**Decision:** React Native with TypeScript for cross-platform iOS and Android development.

**Rationale:**
1. **Future Android Support:** Code written for iOS can be adapted for Android in Phase 2 with minimal rewrite (estimated 2-3 weeks vs. 3-4 months for native rewrite)
2. **Large Community & Learning Resources:** Largest mobile framework community - extensive tutorials, documentation, and Stack Overflow support (critical for team with no prior framework experience)
3. **Mature Haptic Libraries:** Well-tested libraries available (react-native-haptic-feedback) that work reliably
4. **Performance Sufficient:** Research confirms React Native performance is adequate for drawing/tracing apps targeting 6-year-olds - the slight performance gap vs. native won't be noticeable
5. **Developer Availability:** Easier to find React Native developers than native Swift or Flutter developers
6. **Hot Reload:** Faster development iteration with instant code updates during development
7. **JavaScript/TypeScript Ecosystem:** Large package ecosystem for any future needs

**Trade-offs Accepted:**
- Slightly larger app size (~5-10MB larger than native) - acceptable given benefits
- Bridge overhead for native APIs - minimal impact for Scribbly's use cases
- Learning curve for JavaScript/TypeScript - offset by abundant learning resources

**Development Stack:**
- React Native 0.72+ (latest stable)
- **Expo vs. React Native CLI:** Recommend **Expo** for MVP because:
  - Faster setup and development (no native code configuration needed initially)
  - Built-in tools for testing, building, and deployment
  - Easier for teams new to React Native
  - Can "eject" to bare React Native later if needed
  - Expo SDK includes many needed APIs (haptics, audio, sharing)
- TypeScript for type safety
- React Native Haptic Feedback library (or Expo Haptics)
- react-native-svg or expo-svg for drawing canvas
- React Navigation for screen navigation
- Expo Share API or react-native-share for artwork sharing
- AsyncStorage for local settings storage

### Additional Technical Assumptions and Requests

**iOS Version Support:**
- Minimum iOS 15.0 (NFR3)
- Optimized for iOS 17.0+ to leverage latest Haptic Engine features
- Test on iOS 15, 16, 17, and latest to ensure compatibility

**Development Tools:**
- Node.js 18+ and npm/yarn for package management
- React Native CLI or Expo (decision needed - Expo recommended for faster MVP development)
- Xcode 15+ for iOS builds and testing
- Android Studio for future Android development (Phase 2)
- TypeScript for type-safe JavaScript
- VS Code or similar IDE with React Native extensions
- React Native libraries:
  - react-native-haptic-feedback for haptic support
  - react-native-svg or react-native-canvas for drawing canvas
  - react-native-share for iOS share sheet integration
  - @react-native-async-storage/async-storage for local settings
  - react-native-sound or expo-av for audio playback

**Audio Assets:**
- All audio files stored locally in app bundle
- Format: AAC or MP3 for compatibility
- Quality: 44.1kHz, 16-bit minimum for clear letter pronunciation
- Separate audio files for: letter names, letter sounds, creative prompts (estimated ~100-150 audio files for MVP)

**Letter Templates:**
- Vector graphics (SVG or PDF) for scalability
- Stored in app bundle
- High contrast versions for accessibility
- Separate assets for uppercase and lowercase (14 total: 7 letters × 2 cases)

**Haptic Feedback Implementation:**
- Use react-native-haptic-feedback library
- Binary feedback: On (impact medium) or Off
- Trigger haptic when tracing path deviates beyond threshold (approximately ¼ inch tolerance)
- Respect system haptic settings (accessibility)
- Works on both iOS (Taptic Engine) and Android (Vibration API) for Phase 2

**Drawing Canvas Technology:**
- Core Graphics for high-performance drawing
- Support for both finger and Apple Pencil input
- Real-time stroke rendering with <50ms latency requirement
- Memory-efficient canvas clearing and undo functionality

**Local Data Storage:**
- SQLite database for creative prompts (organized by letter and interest category)
- UserDefaults for simple settings (haptic on/off, last selected letter)
- Core Data NOT needed for MVP (overkill for simple data requirements)

**App Size Considerations:**
- Target: <100MB total install size (NFR12)
- Audio files: ~5-10MB (compressed)
- Letter assets: <1MB (vector graphics)
- Prompts database: <1MB
- App binary: ~10-20MB
- Drawing engine/assets: ~5-10MB
- Buffer for future growth: ~60-70MB

**Performance Targets:**
- App launch: <2 seconds (NFR1)
- Drawing latency: <50ms (NFR2)
- Animation framerate: 60fps (NFR15)
- Memory usage: <200MB during active drawing session

**No Backend Services for MVP:**
- No API endpoints required
- No server infrastructure
- No cloud storage
- No authentication/authorization
- No analytics backend (can use local-only analytics if needed)

**Future-Proofing Considerations:**
- Code structure should allow easy addition of cloud API integration later
- Prompt system designed to support both local and cloud-sourced prompts
- Settings/preferences structure should accommodate future parent dashboard sync

---

## Epic List

The MVP is broken down into 5 sequential epics, each delivering significant, testable value. Epics build upon each other, with Epic 1 establishing the foundation and each subsequent epic adding major functionality that can be tested and validated independently.

### Epic 1: Foundation & Letter Selection
**Goal:** Establish project infrastructure and deliver the first user-facing feature - letter selection with mode choice. This epic creates the app structure, navigation, and enables children to choose which letter they want to practice or create with.

### Epic 2: Trace Mode Implementation  
**Goal:** Implement the core tracing experience where children can trace letters with haptic feedback and see their drawing after the letter fades away. This epic delivers the primary learning mechanism and demonstrates Scribbly's unique approach.

### Epic 3: Creative Mode & Drawing Tools
**Goal:** Enable children to transform traced letters into creative artwork with a full set of drawing tools accessible through an expandable menu. This epic delivers the creative expression component that differentiates Scribbly from drill-based apps.

### Epic 4: Artwork Management & User Actions
**Goal:** Allow children to save, share, and manage their artwork while providing essential tools like undo and clear. This epic completes the core user journey from creation to sharing.

### Epic 5: Settings, Polish & Launch Readiness
**Goal:** Add user preferences, accessibility features, and final optimizations to prepare for App Store submission. This epic ensures the app meets quality standards and provides the customization options needed for diverse users.

---

## Epic 1: Foundation & Letter Selection

**Expanded Goal:** This epic establishes the technical foundation of the Scribbly app while delivering the first tangible user value - the ability to select a letter and choose a mode. It sets up the React Native/Expo project structure, navigation framework, and creates the letter selection interface that serves as the entry point for all user interactions. By the end of this epic, users can open the app, see 7 letters displayed in a simple grid, toggle between uppercase and lowercase, select a letter, and choose whether to trace or create - providing immediate validation that the core concept works.

### Story 1.1: Project Setup & Infrastructure

As a **developer**,  
I want **to set up a React Native Expo project with TypeScript and essential dependencies**,  
so that **we have a solid foundation for building Scribbly with modern tooling and type safety**.

**Acceptance Criteria:**
1. Expo project initialized with TypeScript template
2. Essential dependencies installed: React Navigation, AsyncStorage, Expo Haptics, Expo AV (audio)
3. Project structure organized with clear folder separation (screens, components, assets, utils)
4. ESLint and Prettier configured for code quality
5. Git repository initialized with appropriate .gitignore
6. README.md with setup instructions for new developers
7. App builds and runs successfully on iOS simulator
8. Basic app entry point displays a placeholder screen (proof of setup)

### Story 1.2: Navigation Structure

As a **child user**,  
I want **to navigate between different screens in the app**,  
so that **I can move from letter selection to tracing or creating**.

**Acceptance Criteria:**
1. React Navigation stack navigator configured
2. Three main screens created: LetterSelection, TraceMode, CreativeMode (stubs initially)
3. Navigation transitions are smooth (60fps)
4. Back button/gesture works correctly on iOS
5. Navigation state persists appropriately (can return to previous screens)
6. Screen structure supports future settings and other screens

### Story 1.3: Letter Assets & Display

As a **child user**,  
I want **to see the 7 letters (A, S, O, B, D, C, E) displayed clearly**,  
so that **I can choose which letter I want to practice or draw with**.

**Acceptance Criteria:**
1. SVG or vector letter assets created for all 7 letters in uppercase and lowercase (14 total)
2. Letters stored in assets folder and loaded correctly
3. Letters display clearly with high contrast (FR20)
4. Letter assets are scalable and look crisp at various screen sizes
5. Assets meet minimum 4.5:1 contrast ratio (NFR4, accessibility)
6. All 14 letter variants (7 letters × 2 cases) load without errors

### Story 1.4: Letter Selection Screen - Grid Layout

As a **child user**,  
I want **to see all 7 letters in a simple grid layout**,  
so that **I can easily choose which letter I want to use**.

**Acceptance Criteria:**
1. Grid layout displays all 7 letters simultaneously (no scrolling needed)
2. Letters are large enough for easy tapping (minimum 44x44 points per touch target - NFR4)
3. Grid adapts to different screen sizes (iPhone SE to iPad Pro)
4. Layout is visually balanced and appealing to children
5. Letters are evenly spaced and aligned
6. Grid works in portrait orientation (iPad can support landscape in Phase 2)
7. Touch targets are appropriately sized for 6-year-old hands

### Story 1.5: Uppercase/Lowercase Toggle

As a **child user**,  
I want **to switch between seeing uppercase and lowercase letters**,  
so that **I can practice or create with the letter case I want**.

**Acceptance Criteria:**
1. Toggle button clearly visible on letter selection screen
2. Toggle switches between uppercase and lowercase letter display
3. Visual indicator shows current mode (uppercase or lowercase)
4. Selected case persists when navigating away and returning
5. Toggle is easy to understand without reading text (icon-based)
6. Transition between cases is smooth

### Story 1.6: Mode Selection (Trace/Creative)

As a **child user**,  
I want **to choose whether I want to trace a letter or create art with it**,  
so that **I can control my experience based on what I feel like doing**.

**Acceptance Criteria:**
1. Mode selector prominently displayed on letter selection screen
2. Two clear options: "Trace" and "Create" (visual icons, minimal text)
3. Selected mode is visually indicated
4. Mode selection persists when letter is selected
5. User can change mode before selecting a letter
6. Mode can be changed mid-session (FR6 - no locks)
7. Visual design makes modes distinct and appealing

### Story 1.7: Letter Selection Interaction

As a **child user**,  
I want **to tap on a letter to select it**,  
so that **I can start tracing or creating with my chosen letter**.

**Acceptance Criteria:**
1. Tapping a letter selects it and provides visual feedback
2. Selected letter is visually highlighted
3. After selection, app navigates to appropriate screen (TraceMode or CreativeMode)
4. Selected letter is passed to the destination screen correctly
5. Selected case (upper/lower) is passed correctly
6. Navigation happens smoothly (no delay or lag)
7. If mode not selected, prompt user to choose mode first (or default to Trace)

### Story 1.8: Audio Feedback for Letter Selection

As a **child user**,  
I want **to hear the letter name and sound when I select it**,  
so that **I learn letter recognition through multiple senses**.

**Acceptance Criteria:**
1. Audio file plays letter name when letter is tapped (e.g., "A" or "ay")
2. Audio file plays letter sound (phonetic sound, e.g., "ah" for A)
3. Audio files are clear and appropriate for 6-year-olds (NFR11)
4. Audio can be disabled via system settings (accessibility)
5. Audio files stored locally in app bundle
6. Audio playback doesn't block UI interactions
7. Audio files load quickly (<500ms)

---

## Epic 2: Trace Mode Implementation

**Expanded Goal:** This epic implements the core tracing functionality that forms the foundation of Scribbly's learning approach. Children can trace letters with their finger, receive haptic feedback when they deviate from the path (if enabled), and watch their creation remain after the letter template fades away. This epic delivers the primary value proposition - learning letter shapes through kinesthetic practice in a judgment-free environment.

### Story 2.1: Letter Display for Tracing

As a **child user**,  
I want **to see the letter I selected displayed large on the screen with a clear path to trace**,  
so that **I know exactly what shape to follow**.

**Acceptance Criteria:**
1. Selected letter displays centered on screen in Trace Mode
2. Letter is large enough for comfortable tracing (minimum 200x200 points)
3. Letter path is clearly visible with appropriate stroke width
4. Background is clean and uncluttered (focus on letter)
5. Letter scales appropriately for different screen sizes
6. Both uppercase and lowercase display correctly
7. High contrast mode available (FR20)
8. Letter path is clearly defined (no ambiguity about where to trace)

### Story 2.2: Touch Tracking & Drawing Engine

As a **child user**,  
I want **to draw with my finger and see my line appear in real-time**,  
so that **I can trace the letter naturally**.

**Acceptance Criteria:**
1. Touch input is captured accurately on the canvas
2. Drawing strokes appear immediately (<50ms latency - NFR2)
3. Line follows finger movement smoothly without lag
4. Drawing works with both finger and Apple Pencil (NFR14)
5. Drawing engine supports smooth curves and straight lines
6. Multiple strokes can be drawn (not limited to single stroke)
7. Drawing is responsive and feels natural
8. Canvas area covers the entire letter and surrounding space

### Story 2.3: Path Following Logic & Accuracy Detection

As a **child user**,  
I want **my tracing to be measured for accuracy**,  
so that **I can receive helpful feedback without being judged**.

**Acceptance Criteria:**
1. System calculates distance between drawn path and intended letter path
2. Measurement happens in real-time during tracing
3. Tolerance threshold is approximately ¼ inch (6mm) - forgiving, not strict
4. No pass/fail mechanism - only distance measurement (FR35 from brief)
5. Accuracy data is available for haptic feedback triggers
6. System handles both on-path and off-path drawing gracefully
7. Measurement works for all letter shapes (curves, angles, straight lines)

### Story 2.4: Haptic Feedback System

As a **child user**,  
I want **to feel vibration when I go off the tracing path (if haptics are enabled)**,  
so that **I get physical feedback to help me stay on track**.

**Acceptance Criteria:**
1. Haptic feedback triggers when drawn path deviates beyond tolerance threshold
2. Haptic uses "impact medium" intensity when enabled
3. Haptic respects system-level haptic settings (NFR9, accessibility)
4. Haptic can be toggled On/Off (binary - FR3)
5. Haptic only triggers when enabled (Off mode = no vibration)
6. Haptic feedback is crisp and clear (<50ms duration)
7. Haptic doesn't interfere with smooth drawing experience
8. Works on iPhone 6s and newer (Taptic Engine support)

### Story 2.5: Letter Fade Animation

As a **child user**,  
I want **the letter template to fade away after I trace it**,  
so that **I can see my own drawing clearly**.

**Acceptance Criteria:**
1. Fade animation begins after tracing is detected as "complete" (user lifts finger and has traced significant portion)
2. Fade animation is smooth (60fps - NFR15)
3. Fade duration is approximately 1-2 seconds (feel natural, not rushed)
4. After fade, only the child's drawn trace remains visible
5. Child's drawing remains at full opacity during and after fade
6. Animation doesn't cause lag or performance issues
7. Fade works for all 7 letters correctly

### Story 2.6: Trace Completion Detection

As a **child user**,  
I want **the app to recognize when I've finished tracing**,  
so that **the letter can fade and show my completed work**.

**Acceptance Criteria:**
1. System detects when user has traced a significant portion of the letter (≥70% of path)
2. Completion can happen even if path isn't perfect (no strict accuracy requirement)
3. System recognizes when user lifts finger after substantial tracing
4. Completion detection is forgiving - child can't get "stuck" (FR38 from brief)
5. Multiple approaches count (can trace in sections, can go back over lines)
6. No time pressure - child can take as long as needed
7. Visual indicator (optional, subtle) when trace is "complete enough"

---

## Epic 3: Creative Mode & Drawing Tools

**Expanded Goal:** This epic enables children to transform traced letters into creative artwork by providing a full set of drawing tools accessible through an expandable menu. The screen remains clean and focused on the artwork, with all tools tucked away until needed. This epic delivers the creative expression component that differentiates Scribbly - turning letter practice into artistic play.

### Story 3.1: Creative Mode Canvas

As a **child user**,  
I want **a clean drawing canvas where I can create art**,  
so that **I can transform the letter into something creative**.

**Acceptance Criteria:**
1. Creative Mode screen displays a clean canvas taking full screen space
2. Letter remains visible as inspiration (can be faded/transparent but still visible)
3. Canvas supports full-screen drawing area
4. Background is clean and uncluttered (maximum focus on artwork)
5. Canvas works in both portrait and landscape (iPad support)
6. Drawing area is responsive and properly sized for all devices
7. Letter can be displayed at various opacity levels (child's choice via menu)

### Story 3.2: Expandable Menu System

As a **child user**,  
I want **a menu button that expands to show all my tools**,  
so that **the screen stays clean when I'm drawing but tools are accessible when I need them**.

**Acceptance Criteria:**
1. Single menu button visible on Creative Mode screen (non-intrusive placement)
2. Tapping menu button expands menu to reveal all tools
3. Menu organizes tools into clear sections (drawing tools, creative tools, actions, settings)
4. Menu animates open/closed smoothly (60fps - NFR15)
5. When closed, screen shows only artwork (minimal UI chrome)
6. Menu can be dismissed by tapping outside or tapping menu button again
7. Menu button is large enough for easy tapping (44x44 points minimum - NFR4)

### Story 3.3: Color Palette (8 Colors)

As a **child user**,  
I want **to choose from 8 different colors for drawing**,  
so that **I can make colorful artwork**.

**Acceptance Criteria:**
1. Color palette accessible from expandable menu
2. 8 distinct, vibrant colors displayed as selectable buttons (FR8)
3. Currently selected color is visually indicated
4. Tapping a color selects it and applies to drawing
5. Colors are kid-friendly and appealing
6. Color buttons are large enough for easy tapping
7. Colors work well in both light and high-contrast modes

### Story 3.4: Brush Size Selection (2 Sizes)

As a **child user**,  
I want **to choose between 2 different brush sizes**,  
so that **I can draw thick or thin lines**.

**Acceptance Criteria:**
1. Brush size selector accessible from expandable menu
2. Two distinct brush sizes available (FR9)
3. Currently selected size is visually indicated
4. Brush sizes are clearly different (not too similar)
5. Size selection applies immediately to drawing
6. Brush size icons are intuitive and easy to understand

### Story 3.5: Drawing with Selected Tools

As a **child user**,  
I want **to draw on the canvas using my selected color and brush**,  
so that **I can create my artwork**.

**Acceptance Criteria:**
1. Drawing uses currently selected color
2. Drawing uses currently selected brush size
3. Drawing strokes appear immediately (<50ms latency - NFR2)
4. Drawing works smoothly with finger and Apple Pencil
5. Multiple strokes can be drawn with different colors/sizes
6. Drawing persists when menu is opened/closed
7. Canvas maintains all drawing content

### Story 3.6: Stamps Tool

As a **child user**,  
I want **to add stamps (simple shapes and images) to my artwork**,  
so that **I can enhance my drawings**.

**Acceptance Criteria:**
1. Stamps tool accessible from expandable menu (FR12)
2. Tapping stamps tool reveals stamp selection interface
3. Multiple simple shapes and images available (animals, shapes, etc.)
4. Tapping a stamp selects it
5. Tapping canvas places selected stamp at that location
6. Stamps can be placed multiple times
7. Stamps scale appropriately for canvas size
8. Stamps are colorful and appealing to children

### Story 3.7: Inspiration Button with Audio Prompts

As a **child user**,  
I want **to tap a button and hear creative suggestions**,  
so that **I can get ideas for what to draw**.

**Acceptance Criteria:**
1. Inspiration button accessible from expandable menu (FR7)
2. Button is subtle and out of the way (not dominant)
3. Tapping button plays audio prompt with creative suggestion
4. Prompts are pre-written and stored locally (FR17)
5. Prompts are appropriate for the selected letter (e.g., "Turn O into the sun!")
6. Audio is clear and appropriate for 6-year-olds (NFR11)
7. Child can tap button multiple times to hear different prompts
8. Prompts are engaging and spark creativity

### Story 3.8: Undo Functionality

As a **child user**,  
I want **to undo my last drawing action**,  
so that **I can fix mistakes easily**.

**Acceptance Criteria:**
1. Undo button accessible from expandable menu (FR10)
2. Tapping undo removes the last drawing stroke or stamp placement
3. Undo works for drawing strokes, stamps, and tool changes
4. Undo can be used multiple times (undo stack)
5. Visual feedback confirms undo action
6. Undo is fast and responsive (<100ms)

### Story 3.9: Clear Functionality

As a **child user**,  
I want **to clear my drawing**,  
so that **I can start fresh**.

**Acceptance Criteria:**
1. Clear button accessible from expandable menu (FR11)
2. Tapping clear resets the drawing canvas
3. Letter remains visible after clearing (doesn't disappear)
4. Clear action requires confirmation or is easily reversible (consider child-friendly UX)
5. Visual feedback confirms clear action
6. Clear works quickly without lag

### Story 3.10: Mode Switching Mid-Session

As a **child user**,  
I want **to switch between Trace and Creative mode while working**,  
so that **I can move between practicing and creating freely**.

**Acceptance Criteria:**
1. Mode switcher accessible from expandable menu
2. User can switch from Creative Mode to Trace Mode
3. User can switch from Trace Mode to Creative Mode
4. Current drawing/trace is preserved when switching modes
5. Mode switch is smooth and doesn't lose work
6. User can switch modes multiple times in a session

---

## Epic 4: Artwork Management & User Actions

**Expanded Goal:** This epic completes the core user journey by enabling children to save, share, and manage their artwork. It provides essential functionality that makes creations permanent and shareable, while maintaining the judgment-free, encouraging environment throughout.

### Story 4.1: Save Artwork to Photo Library

As a **child user**,  
I want **to save my artwork to my device's photo library**,  
so that **I can keep my drawings and show them later**.

**Acceptance Criteria:**
1. Save button accessible from expandable menu (FR13)
2. Tapping save button saves artwork to iOS Photos app
3. Saved image is high quality (minimum 1024x1024 resolution - NFR7)
4. Artwork is saved as PNG or JPEG format
5. Save includes both the drawing and letter (if visible)
6. Save action provides visual confirmation (success animation)
7. App requests photo library permission appropriately (first-time prompt)
8. Save works offline (FR15 - no internet required)

### Story 4.2: Share Artwork Functionality

As a **child user**,  
I want **to share my artwork with my family**,  
so that **they can see what I created**.

**Acceptance Criteria:**
1. Share button accessible from expandable menu (FR14)
2. Tapping share opens iOS native share sheet
3. Share sheet allows sharing via Messages, Mail, and other apps
4. Shared image is high quality and properly formatted
5. Share works with standard iOS share functionality
6. Share includes artwork (and letter if visible)
7. Share works offline (uses native iOS sharing - FR15)

### Story 4.3: App Interruption Handling

As a **child user**,  
I want **my drawing to be preserved when I get a phone call or notification**,  
so that **I don't lose my work**.

**Acceptance Criteria:**
1. App saves drawing state when backgrounded (NFR8)
2. Drawing is restored when app returns to foreground
3. All drawing strokes are preserved during interruptions
4. Selected tools (color, brush) are restored
5. No data loss during phone calls, notifications, or app switching
6. State restoration is seamless and automatic

---

## Epic 5: Settings, Polish & Launch Readiness

**Expanded Goal:** This epic adds user preferences, accessibility features, and final optimizations to prepare Scribbly for App Store submission. It ensures the app meets quality standards, provides necessary customization options, and creates a polished experience ready for real users.

### Story 5.1: Settings Menu Structure

As a **child user**,  
I want **to access settings to customize my experience**,  
so that **the app works the way I want it**.

**Acceptance Criteria:**
1. Settings accessible from expandable menu
2. Settings menu is simple and kid-friendly
3. Large icons, minimal text (visual-first design)
4. Settings organized into clear categories
5. Settings are easy to navigate and understand
6. Changes apply immediately when settings are adjusted

### Story 5.2: Haptic Feedback Toggle

As a **child user**,  
I want **to turn haptic feedback on or off**,  
so that **I can control whether I feel vibrations**.

**Acceptance Criteria:**
1. Haptic toggle accessible in settings menu (FR3, FR18)
2. Toggle clearly shows On/Off state
3. Toggle works immediately when changed
4. Setting persists between app sessions
5. Toggle is easy to understand (icon-based, minimal text)
6. Default state is reasonable (suggest On for initial experience)

### Story 5.3: Parental Gate Implementation

As a **parent user**,  
I want **to access parent settings behind a secure gate**,  
so that **my child can't accidentally change important settings**.

**Acceptance Criteria:**
1. Parent settings accessible via hold gesture (e.g., hold two corners for 3 seconds - FR19)
2. Gate mechanism is simple for parents but secure from children
3. Parent settings include: interest preferences for future prompt personalization
4. Parent settings structure is ready for future features
5. Gate is clearly documented for parents
6. Gate works reliably and consistently

### Story 5.4: High Contrast Mode

As a **child user with visual needs**,  
I want **high contrast mode for better visibility**,  
so that **I can see letters and drawings more clearly**.

**Acceptance Criteria:**
1. High contrast mode accessible in settings (FR20)
2. High contrast applies to letter display
3. High contrast applies to UI elements
4. Mode meets WCAG AA contrast ratio requirements (4.5:1 minimum)
5. Toggle works immediately when changed
6. Setting persists between sessions

### Story 5.5: Performance Optimization

As a **child user**,  
I want **the app to run smoothly and quickly**,  
so that **I can draw without lag or delays**.

**Acceptance Criteria:**
1. App launches within 2 seconds (NFR1)
2. Drawing strokes appear with <50ms latency (NFR2)
3. All animations run at 60fps (NFR15)
4. Memory usage stays under 200MB during active sessions
5. Battery usage is minimal during 10-15 minute sessions (NFR10)
6. No noticeable lag during intensive drawing
7. App remains responsive during all interactions

### Story 5.6: App Store Assets & Metadata

As a **product owner**,  
I want **all App Store assets and metadata prepared**,  
so that **Scribbly can be submitted for review**.

**Acceptance Criteria:**
1. App icon designed (1024x1024, all required sizes)
2. Screenshots created for iPhone and iPad
3. App description written (compelling, clear, COPPA-compliant)
4. Keywords researched and selected
5. Privacy policy prepared (COPPA compliance - NFR6)
6. App Store Connect listing created and configured
7. Age rating appropriate for 6-year-old target audience

### Story 5.7: Final Testing & Quality Assurance

As a **product owner**,  
I want **the app thoroughly tested on real devices**,  
so that **it works reliably for all users**.

**Acceptance Criteria:**
1. Testing completed on iPhone SE (smallest supported device)
2. Testing completed on iPhone 12+ (primary target)
3. Testing completed on iPad (both portrait and landscape)
4. Testing on iOS 15, 16, and 17 (version compatibility)
5. All user stories verified and working
6. Performance benchmarks met (launch time, latency, memory)
7. No critical bugs or crashes
8. User testing with target age group completed (if time permits)

---

