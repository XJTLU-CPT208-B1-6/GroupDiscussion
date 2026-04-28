# Requirements Document

## Introduction

This document specifies the requirements for integrating the Playful Geometric design system into the existing X-Thread academic project webpage. X-Thread is a single-page HTML showcase (3027 lines) for an XJTLU Group Discussion Platform, currently featuring a clean, modern, gradient-based design with purple theme (#8c2db9). The redesign will transform the visual presentation to the Playful Geometric style while preserving all existing content, interactive functionality, and maintaining academic professionalism.

The Playful Geometric design system is characterized by primitive shapes, hard shadows, pattern fills, varied radii, and a "Stable Grid, Wild Decoration" philosophy. This redesign aims to create a more engaging, playful, yet professional academic showcase that stands out while remaining accessible and functional.

## Glossary

- **X-Thread_System**: The existing single-page HTML academic project webpage showcasing the XJTLU Group Discussion Platform
- **Playful_Geometric_System**: The target design system featuring primitive shapes, hard shadows, pattern fills, and bouncy animations
- **Design_Token**: A named design value (color, spacing, typography, shadow) used consistently across the system
- **Hard_Shadow**: A shadow effect with no blur, using solid offset (e.g., 4px 4px 0px #1E293B)
- **Decorative_Shape**: Background primitive shapes (circles, triangles, squares) used for visual interest
- **Pattern_Fill**: Repeating visual patterns (polka dots, grid lines, diagonal stripes) applied to elements
- **Interactive_Element**: User-facing components that respond to input (buttons, cards, gallery, navigation)
- **Content_Section**: Distinct areas of the page (hero, features, team, timeline, research, evaluation)
- **Responsive_Breakpoint**: Screen width thresholds where layout adapts (mobile: <768px, tablet: 768-1024px, desktop: >1024px)
- **Accessibility_Standard**: WCAG AAA contrast requirements and interaction guidelines
- **Animation_Easing**: The cubic-bezier timing function for bouncy transitions: cubic-bezier(0.34,1.56,0.64,1)
- **External_Resource**: Third-party fonts (Google Fonts) and icon libraries integrated into the page
- **Single_File_Constraint**: The requirement that all code remains in one HTML file with no build process

## Requirements

### Requirement 1: Visual Design System Integration

**User Story:** As a visitor, I want to see a visually distinctive Playful Geometric design, so that the project stands out and feels modern and engaging.

#### Acceptance Criteria

1. THE X-Thread_System SHALL apply the warm cream background color (#FFFDF5) to the body element
2. THE X-Thread_System SHALL use slate 800 (#1E293B) as the primary foreground color for text
3. THE X-Thread_System SHALL use vivid violet (#8B5CF6) as the primary accent color
4. THE X-Thread_System SHALL use hot pink (#F472B6), amber (#FBBF24), and emerald (#34D399) as secondary, tertiary, and quaternary accent colors
5. THE X-Thread_System SHALL rotate secondary/tertiary/quaternary colors across repeating elements to create a "confetti effect"
6. THE X-Thread_System SHALL apply Hard_Shadow effects (4px 4px 0px #1E293B) to interactive elements
7. THE X-Thread_System SHALL apply larger Hard_Shadow effects (8px 8px 0px #1E293B) to card components
8. THE X-Thread_System SHALL add Decorative_Shape elements (circles, triangles, squares) to section backgrounds
9. THE X-Thread_System SHALL apply Pattern_Fill backgrounds (polka dots, grid lines, diagonal stripes) to decorative elements
10. THE X-Thread_System SHALL mix rounded corners (border-radius: 16px-24px) with sharp corners (border-radius: 0px) across different elements

### Requirement 2: Typography System Implementation

**User Story:** As a visitor, I want clear, readable typography with visual hierarchy, so that I can easily scan and understand the content.

#### Acceptance Criteria

1. THE X-Thread_System SHALL load "Outfit" font from Google Fonts for all heading elements
2. THE X-Thread_System SHALL load "Plus Jakarta Sans" font from Google Fonts for all body text
3. THE X-Thread_System SHALL apply font-weight 700 or 800 to h1 elements
4. THE X-Thread_System SHALL apply font-weight 700 to h2 and h3 elements
5. THE X-Thread_System SHALL apply font-weight 400 to body text and font-weight 500 to emphasized body text
6. THE X-Thread_System SHALL implement a 1.25 (Major Third) scale ratio for font sizes
7. WHEN calculating font sizes, THE X-Thread_System SHALL use base size 16px and multiply by 1.25 for each level up
8. THE X-Thread_System SHALL ensure all text meets WCAG AAA contrast requirements (7:1 for normal text, 4.5:1 for large text)

### Requirement 3: Component Style Transformation

**User Story:** As a visitor, I want interactive components to have consistent Playful Geometric styling, so that the interface feels cohesive and delightful.

#### Acceptance Criteria

1. THE X-Thread_System SHALL style all button elements with pill-shaped borders (border-radius: 9999px)
2. THE X-Thread_System SHALL apply 2px solid borders to all button elements
3. WHEN a button is in default state, THE X-Thread_System SHALL display a Hard_Shadow
4. WHEN a button is hovered, THE X-Thread_System SHALL apply a bounce animation using Animation_Easing
5. THE X-Thread_System SHALL style all card components with "sticker" appearance (2px border, 8px 8px 0px Hard_Shadow)
6. WHEN a card is hovered, THE X-Thread_System SHALL apply a wiggle animation (rotate -1deg, scale 1.02)
7. THE X-Thread_System SHALL style the team cards with Playful_Geometric_System aesthetics while preserving hover flip functionality
8. THE X-Thread_System SHALL style the circular gallery cards with 2px borders and Hard_Shadow effects
9. THE X-Thread_System SHALL maintain all existing card flip and rotation animations
10. THE X-Thread_System SHALL apply entrance animations (scale 0 to 1 with bounce) to cards when they enter viewport

### Requirement 4: Layout and Section Redesign

**User Story:** As a visitor, I want a clear visual hierarchy with the most important content prioritized, so that I can quickly understand the project.

#### Acceptance Criteria

1. THE X-Thread_System SHALL implement a max-width container of 1200px (max-w-6xl equivalent)
2. THE X-Thread_System SHALL redesign the hero section with text content on the left and Decorative_Shape elements on the right
3. THE X-Thread_System SHALL add a massive yellow circle (quaternary color) as a primary decorative element in the hero
4. THE X-Thread_System SHALL add dotted Pattern_Fill elements to the hero section background
5. THE X-Thread_System SHALL maintain the existing section order: hero, features, team, journey, research, evaluation, timeline, references
6. THE X-Thread_System SHALL apply generous spacing between sections (4rem minimum)
7. THE X-Thread_System SHALL style the features section as a grid of 3 cards with alternating accent colors (violet, pink, yellow)
8. THE X-Thread_System SHALL preserve all existing content sections without removing any information
9. WHEN viewport width is less than 768px, THE X-Thread_System SHALL stack grid layouts into single columns
10. THE X-Thread_System SHALL maintain responsive behavior for all breakpoints (mobile, tablet, desktop)

### Requirement 5: Interactive Functionality Preservation

**User Story:** As a visitor, I want all existing interactive features to continue working, so that I can explore the project fully.

#### Acceptance Criteria

1. THE X-Thread_System SHALL preserve the sidebar navigation functionality with scroll-to-section behavior
2. THE X-Thread_System SHALL preserve the active state highlighting in sidebar navigation based on scroll position
3. THE X-Thread_System SHALL preserve the circular gallery carousel with prev/next navigation
4. THE X-Thread_System SHALL preserve the gallery card flip functionality on click
5. THE X-Thread_System SHALL preserve the gallery touch/swipe gestures for mobile devices
6. THE X-Thread_System SHALL preserve the gallery wheel scroll navigation
7. THE X-Thread_System SHALL preserve the timeline layout with alternating left/right positioning
8. THE X-Thread_System SHALL preserve all hover effects on team cards, feature cards, and other interactive elements
9. THE X-Thread_System SHALL preserve the smooth scroll behavior for navigation
10. WHEN an Interactive_Element is clicked, THE X-Thread_System SHALL execute the existing JavaScript event handler

### Requirement 6: Animation and Interaction Effects

**User Story:** As a visitor, I want delightful animations that enhance the experience, so that the interface feels alive and responsive.

#### Acceptance Criteria

1. THE X-Thread_System SHALL apply bouncy transitions using Animation_Easing (cubic-bezier(0.34,1.56,0.64,1))
2. WHEN a card is hovered, THE X-Thread_System SHALL apply a wiggle animation with 300ms duration
3. WHEN a button is hovered, THE X-Thread_System SHALL apply a bounce animation with 200ms duration
4. THE X-Thread_System SHALL apply pop-in entrance animations to cards (scale 0 to 1 with bounce easing)
5. WHEN an icon is hovered, THE X-Thread_System SHALL apply a wiggle animation (rotate ±5deg)
6. THE X-Thread_System SHALL respect prefers-reduced-motion media query by disabling animations
7. WHEN prefers-reduced-motion is set, THE X-Thread_System SHALL use instant transitions (duration: 0ms)
8. THE X-Thread_System SHALL maintain the existing gallery rotation animation for the spinner circle
9. THE X-Thread_System SHALL maintain the existing shine animation for the h1 title
10. THE X-Thread_System SHALL ensure all animations have appropriate performance (use transform and opacity only)

### Requirement 7: Icon Optimization and Integration

**User Story:** As a visitor, I want consistent, optimized icons throughout the page, so that visual communication is clear and cohesive.

#### Acceptance Criteria

1. THE X-Thread_System SHALL identify all emoji icons used in the current design
2. THE X-Thread_System SHALL evaluate whether to keep emoji icons or replace with icon library
3. WHERE icon library is used, THE X-Thread_System SHALL integrate a lightweight External_Resource (e.g., Lucide, Feather Icons)
4. THE X-Thread_System SHALL apply consistent sizing to all icons within each Content_Section
5. THE X-Thread_System SHALL apply the primary accent color (vivid violet) to decorative icons
6. THE X-Thread_System SHALL rotate accent colors (violet, pink, yellow, emerald) for icons in repeating grids
7. WHEN an icon is interactive, THE X-Thread_System SHALL apply hover wiggle animation
8. THE X-Thread_System SHALL ensure all icons meet minimum touch target size (44x44px) on mobile
9. THE X-Thread_System SHALL maintain semantic meaning of all icons from the original design
10. THE X-Thread_System SHALL ensure icon visual weight matches the Playful_Geometric_System aesthetic

### Requirement 8: External Resource Integration

**User Story:** As a developer, I want external resources properly integrated, so that fonts and icons load reliably without impacting performance.

#### Acceptance Criteria

1. THE X-Thread_System SHALL add Google Fonts link tag in the document head for "Outfit" font
2. THE X-Thread_System SHALL add Google Fonts link tag in the document head for "Plus Jakarta Sans" font
3. THE X-Thread_System SHALL specify font-weight values (400, 500, 700, 800) in the Google Fonts URL
4. THE X-Thread_System SHALL use font-display: swap for all Google Fonts to prevent FOIT (Flash of Invisible Text)
5. WHERE icon library is integrated, THE X-Thread_System SHALL add the library CDN link or inline SVG definitions
6. THE X-Thread_System SHALL minimize the number of External_Resource requests (combine font weights in single request)
7. THE X-Thread_System SHALL maintain the Single_File_Constraint by embedding all CSS in style tags
8. THE X-Thread_System SHALL maintain the Single_File_Constraint by embedding all JavaScript in script tags
9. THE X-Thread_System SHALL ensure all External_Resource URLs use HTTPS protocol
10. THE X-Thread_System SHALL add appropriate fallback fonts for "Outfit" (sans-serif) and "Plus Jakarta Sans" (sans-serif)

### Requirement 9: Accessibility and Usability

**User Story:** As a visitor with accessibility needs, I want the redesigned page to be fully accessible, so that I can navigate and understand the content regardless of my abilities.

#### Acceptance Criteria

1. THE X-Thread_System SHALL maintain WCAG AAA contrast ratio (7:1) for all text on cream background
2. THE X-Thread_System SHALL ensure slate-800 (#1E293B) on cream (#FFFDF5) meets AAA contrast requirements
3. THE X-Thread_System SHALL provide high-contrast focus states (3px solid outline with accent color) for all Interactive_Element components
4. THE X-Thread_System SHALL ensure focus states are visible against all background colors
5. THE X-Thread_System SHALL maintain keyboard navigation for all interactive features
6. THE X-Thread_System SHALL preserve ARIA labels on gallery navigation buttons
7. THE X-Thread_System SHALL respect prefers-reduced-motion by disabling decorative animations
8. THE X-Thread_System SHALL ensure all interactive elements meet minimum touch target size (44x44px) on mobile
9. THE X-Thread_System SHALL maintain semantic HTML structure (proper heading hierarchy, section elements)
10. THE X-Thread_System SHALL ensure all images have descriptive alt text (preserve existing alt attributes)

### Requirement 10: Responsive Design and Performance

**User Story:** As a mobile visitor, I want the redesigned page to work perfectly on my device, so that I can access all content and features.

#### Acceptance Criteria

1. THE X-Thread_System SHALL maintain responsive behavior at all Responsive_Breakpoint thresholds
2. WHEN viewport width is less than 768px, THE X-Thread_System SHALL stack multi-column layouts into single column
3. WHEN viewport width is less than 768px, THE X-Thread_System SHALL reduce Decorative_Shape sizes by 50%
4. WHEN viewport width is less than 768px, THE X-Thread_System SHALL reduce Hard_Shadow offsets (2px 2px 0px instead of 4px 4px 0px)
5. THE X-Thread_System SHALL maintain the existing mobile timeline layout (left-aligned with single vertical line)
6. THE X-Thread_System SHALL maintain the existing mobile gallery layout with reduced card sizes
7. THE X-Thread_System SHALL ensure page load time remains under 3 seconds on 3G connection
8. THE X-Thread_System SHALL minimize CSS file size by removing unused styles from original design
9. THE X-Thread_System SHALL use CSS transforms for animations (not position properties) for better performance
10. THE X-Thread_System SHALL maintain the Single_File_Constraint with total file size under 5000 lines

### Requirement 11: Content Preservation and Migration

**User Story:** As a project stakeholder, I want all existing content preserved exactly, so that no information is lost during the redesign.

#### Acceptance Criteria

1. THE X-Thread_System SHALL preserve all text content from the original page without modification
2. THE X-Thread_System SHALL preserve all section headings and subheadings
3. THE X-Thread_System SHALL preserve all team member information (names, roles, descriptions)
4. THE X-Thread_System SHALL preserve all timeline entries with dates and descriptions
5. THE X-Thread_System SHALL preserve all feature descriptions and icons
6. THE X-Thread_System SHALL preserve all research paper information (titles, authors, years, abstracts)
7. THE X-Thread_System SHALL preserve all evaluation data (SUS scores, survey statistics, pain points)
8. THE X-Thread_System SHALL preserve all image references (VoiceChat.png, AIRealtimeChat.png, etc.)
9. THE X-Thread_System SHALL preserve the footer copyright information
10. THE X-Thread_System SHALL preserve all internal anchor links and navigation targets

### Requirement 12: Design System Consistency

**User Story:** As a designer, I want consistent application of Design_Token values, so that the visual system is cohesive and maintainable.

#### Acceptance Criteria

1. THE X-Thread_System SHALL define all Design_Token values in CSS custom properties (variables)
2. THE X-Thread_System SHALL define color tokens: --color-bg, --color-fg, --color-accent-primary, --color-accent-secondary, --color-accent-tertiary, --color-accent-quaternary
3. THE X-Thread_System SHALL define spacing tokens using a consistent scale (0.25rem, 0.5rem, 1rem, 1.5rem, 2rem, 3rem, 4rem)
4. THE X-Thread_System SHALL define shadow tokens: --shadow-hard-sm (4px 4px 0px), --shadow-hard-md (8px 8px 0px)
5. THE X-Thread_System SHALL define border-radius tokens: --radius-sm (8px), --radius-md (16px), --radius-lg (24px), --radius-full (9999px)
6. THE X-Thread_System SHALL define typography tokens: --font-heading, --font-body, --font-weight-normal, --font-weight-medium, --font-weight-bold, --font-weight-extrabold
7. THE X-Thread_System SHALL use Design_Token variables consistently throughout all CSS rules
8. THE X-Thread_System SHALL avoid hardcoded color values except in token definitions
9. THE X-Thread_System SHALL document all Design_Token values in CSS comments
10. THE X-Thread_System SHALL ensure Design_Token values match the Playful_Geometric_System specification exactly

### Requirement 13: Academic Professionalism Balance

**User Story:** As an academic evaluator, I want the redesign to maintain professional credibility, so that the project is taken seriously despite the playful aesthetic.

#### Acceptance Criteria

1. THE X-Thread_System SHALL maintain clear visual hierarchy with prominent headings and structured content
2. THE X-Thread_System SHALL ensure Decorative_Shape elements do not obscure or distract from content
3. THE X-Thread_System SHALL use Pattern_Fill elements sparingly and with low opacity (10-20%)
4. THE X-Thread_System SHALL maintain readable line-height (1.6-1.8) for all body text
5. THE X-Thread_System SHALL maintain adequate spacing between content blocks (minimum 2rem)
6. THE X-Thread_System SHALL ensure accent color rotation does not create visual chaos (use consistent pattern)
7. THE X-Thread_System SHALL maintain professional tone in all preserved text content
8. THE X-Thread_System SHALL ensure animations are subtle and do not interfere with reading
9. THE X-Thread_System SHALL maintain the academic structure (introduction, research, methodology, evaluation, conclusion)
10. THE X-Thread_System SHALL ensure the overall aesthetic is "playful yet professional" not "childish"

### Requirement 14: Browser Compatibility and Standards

**User Story:** As a visitor using any modern browser, I want the page to work correctly, so that I can access the content regardless of my browser choice.

#### Acceptance Criteria

1. THE X-Thread_System SHALL function correctly in Chrome version 90 and above
2. THE X-Thread_System SHALL function correctly in Firefox version 88 and above
3. THE X-Thread_System SHALL function correctly in Safari version 14 and above
4. THE X-Thread_System SHALL function correctly in Edge version 90 and above
5. THE X-Thread_System SHALL use CSS features with broad browser support (avoid experimental features)
6. WHERE modern CSS features are used, THE X-Thread_System SHALL provide fallbacks for older browsers
7. THE X-Thread_System SHALL use standard JavaScript (ES6+) without requiring transpilation
8. THE X-Thread_System SHALL validate as correct HTML5 (no syntax errors)
9. THE X-Thread_System SHALL use vendor prefixes where necessary for CSS properties (-webkit-, -moz-)
10. THE X-Thread_System SHALL test all Interactive_Element functionality across all supported browsers

### Requirement 15: Testing and Validation

**User Story:** As a quality assurance tester, I want clear validation criteria, so that I can verify the redesign meets all requirements.

#### Acceptance Criteria

1. THE X-Thread_System SHALL pass HTML validation with no errors (W3C validator)
2. THE X-Thread_System SHALL pass CSS validation with no errors (W3C CSS validator)
3. THE X-Thread_System SHALL achieve Lighthouse performance score of 90 or above
4. THE X-Thread_System SHALL achieve Lighthouse accessibility score of 95 or above
5. THE X-Thread_System SHALL achieve Lighthouse best practices score of 95 or above
6. THE X-Thread_System SHALL load all External_Resource fonts successfully (no 404 errors)
7. THE X-Thread_System SHALL display all image references correctly (no broken images)
8. THE X-Thread_System SHALL execute all JavaScript functionality without console errors
9. THE X-Thread_System SHALL maintain visual consistency across all Responsive_Breakpoint sizes
10. THE X-Thread_System SHALL pass manual testing checklist covering all Interactive_Element components
