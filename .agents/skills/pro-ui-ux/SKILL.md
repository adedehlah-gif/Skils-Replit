---
name: pro-ui-ux
description: Enforces a polished, professional, responsive UI/UX standard for building or changing websites, dashboards, SaaS apps, landing pages, admin panels, and web app interfaces. Use this skill before designing, implementing, or reviewing any user-facing interface. Do not use for backend-only tasks that do not change the interface.
---

# Pro UI/UX — Design and Build Rules

## Mission

Create interfaces that feel intentionally designed, production-ready, accessible, responsive, and consistent—not generic, unfinished, or assembled from unrelated components.

Use the supplied E-Learning dashboard image as a visual direction, not as a pixel-perfect template. Its defining traits are a calm white canvas, soft rounded surfaces, a clear left navigation, a strong teal feature banner, restrained coral/red and yellow accents, compact data cards, clean typography, and generous spacing. Adapt the same design principles to the actual product and audience.

## Mandatory workflow — do this before coding

1. **Read this entire `SKILL.md` before making UI decisions.**
2. Inspect the existing app, framework, routes, components, assets, package scripts, and current design conventions. Do not replace working architecture just to impose a preferred stack.
3. Identify the target user, primary task, key screen(s), content hierarchy, and important states. If requirements are unclear, make sensible assumptions and state them briefly; ask only when a missing decision blocks implementation.
4. Create or update a concise design plan: visual direction, layout, reusable components, responsive behavior, and states.
5. Build the complete working interface, not only a static mockup. Connect controls to real app behavior where the backend or data is available. Never pretend a nonfunctional control works.
6. Run the available checks (build, typecheck, lint, tests) and inspect the result in the browser/preview when tools are available. Fix errors caused by the changes.
7. Before finishing, complete the quality checklist at the end of this file and report what was tested and any genuine limitations.

## Non-negotiable rules

- **No generic, unfinished UI.** Avoid a default-looking page with a plain heading, a few unstyled buttons, and large empty areas.
- **No decorative-only functionality.** Buttons, links, search, tabs, filters, menus, forms, pagination, and toggles must work or be clearly disabled with a reason. Do not use `href="#"` as a fake link.
- **No invented product facts.** Use real app data where available. If data is unavailable, use realistic clearly illustrative sample data, and do not imply it is live.
- **Preserve existing behavior.** Do not remove routes, features, data, or user flows without explicit approval. Prefer incremental improvements.
- **Use the existing stack and design system first.** Reuse the project's framework, component library, tokens, icons, and styling approach. Add dependencies only when needed and justified.
- **Avoid visual clutter.** Use purposeful hierarchy, alignment, whitespace, and restrained accents. Do not add gradients, glassmorphism, animations, or shadows merely because they are trendy.
- **Avoid emoji as interface icons.** Prefer the project's icon library or consistent inline SVG icons. Icons must have a clear meaning and accessible labels when needed.
- **Do not hard-code secrets** or expose API keys, private data, or environment variables in client-side code.

## Visual design system

### 1. Design direction

Default direction: modern, warm, minimal SaaS dashboard with a friendly editorial touch, inspired by the reference image.

- Canvas: soft neutral background outside the main app surface when appropriate; white or near-white content surfaces.
- Primary: teal / mint for the main brand action and positive emphasis.
- Accent: coral / warm red for high-attention actions or highlights.
- Secondary accent: sunny yellow for selected metrics, badges, or supporting emphasis.
- Text: deep navy/charcoal for primary content; muted gray for secondary content.
- Keep accent colors limited and consistent. Do not use all accents at equal strength.
- If the product already has a brand palette, preserve it and adapt these principles rather than forcing the reference colors.

Suggested starting tokens (adjust for contrast, brand, and context):
- `--color-primary: #49B7A8`
- `--color-primary-strong: #238F83`
- `--color-coral: #F0645A`
- `--color-yellow: #F4C52E`
- `--color-text: #20233F`
- `--color-muted: #777B8C`
- `--color-surface: #FFFFFF`
- `--color-page: #F5F6F8`
- `--color-border: #E9EBF0`

These are starting values, not rigid requirements. Verify foreground/background contrast and adjust as needed.

### 2. Layout and hierarchy

- Establish one obvious primary action or focal point per screen.
- For dashboard layouts, use a clear navigation region, a top bar for page context and utilities, and a content area with well-grouped sections.
- Use a responsive sidebar on desktop and a drawer, compact navigation, or bottom navigation on mobile when appropriate.
- Use a consistent spacing scale, preferably based on 4px or 8px increments. Avoid arbitrary one-off spacing values.
- Keep content aligned to a coherent grid. Use consistent gutters and card edges.
- Use whitespace to separate sections; do not make the interface feel cramped or excessively sparse.
- Establish hierarchy through size, weight, color, and spacing—not through making every heading large or bold.
- Use clear page titles, section titles, helpful supporting text, and empty states that explain what to do next.
- Prefer content-first layouts. Do not add cards to every piece of text if a simple section is clearer.

### 3. Typography

- Use a readable, consistent type scale with a limited number of sizes and weights.
- Use the existing project font when appropriate; otherwise choose a clean, legible sans-serif.
- Body text should be comfortable to read on mobile and desktop. Avoid tiny labels and low-contrast secondary text.
- Use sentence case for most interface labels. Keep terminology consistent across navigation, buttons, and page titles.
- Make important numbers and status values scannable without overwhelming surrounding content.
- Prevent awkward wrapping, clipped headings, and long unbroken text.

### 4. Cards, surfaces, and components

- Use consistent corner radii, borders, and shadow intensity. Shadows should communicate elevation, not decorate every container.
- Use cards for related information such as course lists, activity summaries, progress, and instructor profiles—similar to the reference dashboard.
- A card must have a clear purpose and meaningful content. Avoid nested cards unless there is a strong information-architecture reason.
- Buttons need consistent height, padding, radius, typography, hover, focus, disabled, and loading states.
- Use one primary button style; secondary and destructive actions must look distinct.
- Forms require persistent labels, helpful hints where useful, clear validation, and visible success/error feedback.
- Lists and tables should have aligned columns, legible row spacing, empty/loading/error states, and responsive overflow behavior.
- Use consistent icons from one icon set; do not mix arbitrary icon styles.

### 5. Reference-inspired dashboard composition

When building an education, analytics, or admin dashboard, consider this structure where it fits the task:

1. **Navigation:** brand mark/name and a short list of clearly labeled destinations.
2. **Top bar:** search (if useful), notifications/messages (if supported), and account/profile menu.
3. **Page heading:** descriptive title and optional contextual actions.
4. **Feature banner:** teal or brand-primary surface with a short headline, supporting line, one meaningful action, and optional illustration. Ensure text remains readable and never place important content beneath an illustration.
5. **Main dashboard grid:** a course/activity list, a progress or analytics panel, and a compact ranking/team/instructor panel if relevant.
6. **Metric cards:** highlight a small number of useful metrics with clear labels, values, and optional trend context.
7. **Responsive behavior:** stack sections in a sensible order on small screens; do not simply shrink a desktop layout.

Do not force this exact structure onto landing pages, mobile-first tools, forms, or products where it does not suit the user journey.

### 6. Imagery and visual assets

- Use imagery only when it improves comprehension, brand character, or emotional appeal.
- Prefer cohesive illustrations, photography, or product screenshots over unrelated stock images.
- If using an illustration in a hero/banner, keep it secondary to the headline and CTA.
- Use stable local assets or verified image sources. Do not invent asset paths or rely on broken external URLs.
- Provide descriptive alt text for meaningful images; use empty alt text for purely decorative images.
- Use appropriate aspect ratios and object positioning. Avoid stretching images or cropping important content.
- If no suitable image is available, create a polished layout with typography, shapes, or existing assets rather than leaving a broken image placeholder.

### 7. Responsive design

Design and verify at minimum these approximate widths:
- Mobile: 320–390px
- Tablet: 768px
- Desktop: 1024–1440px

Rules:
- Start from the existing responsive strategy; use mobile-first CSS when practical.
- No unintended horizontal page scrolling.
- Navigation, dialogs, tables, cards, charts, and forms must remain usable on narrow screens.
- Use flexible grids (`minmax`, responsive columns, wrapping) rather than fixed desktop widths.
- Touch targets should generally be around 44×44px or larger.
- Avoid hiding essential actions or content on mobile.
- Use breakpoints based on layout needs, not device brand names.
- Respect safe areas on mobile where relevant.

### 8. Accessibility and interaction

- Use semantic HTML and native controls wherever possible.
- Ensure keyboard access, visible focus states, logical focus order, and accessible names.
- Do not communicate status using color alone; include text, icons, or another cue.
- Meet WCAG AA contrast targets where applicable: 4.5:1 for normal text and 3:1 for large text and meaningful UI graphics.
- Label inputs and associate validation messages with the relevant field.
- Dialogs and menus must support expected keyboard behavior and focus handling.
- Respect `prefers-reduced-motion`; motion must not be required to understand the interface.
- Add loading, empty, error, success, disabled, and confirmation states where relevant.
- Confirm destructive actions when the consequence is significant.
- Do not trap users in modals, overlays, or multi-step flows.

### 9. Motion and feedback

- Keep transitions subtle, short, and purposeful.
- Use motion to explain state changes, hierarchy, or navigation—not as decoration.
- Provide immediate feedback after meaningful user actions.
- Prevent layout shifts during loading; use skeletons only when they genuinely help.
- Do not animate every card or element on page load.
- Honor reduced-motion preferences.

### 10. Data visualization

- Give each chart a clear title, meaningful units, legible labels, and appropriate scales.
- Use a restrained palette consistent with the product.
- Include a textual summary or accessible equivalent when possible.
- Avoid misleading axes, unexplained percentages, and decorative charts that imply nonexistent data.
- Ensure charts reflow or scroll accessibly on smaller screens.

### 11. Content and microcopy

- Write concise, specific interface copy. Labels should describe the action or content accurately.
- Use consistent names for the same feature throughout the product.
- Empty states should explain why there is no content and what the user can do next.
- Error messages should say what happened and how to recover when possible.
- Avoid filler copy, fake testimonials, fake user counts, and meaningless placeholder paragraphs in production-facing screens.
- Use the user's language and locale consistently, including date, number, and currency formatting.

### 12. Implementation quality

- Build reusable components for repeated patterns; avoid copy-paste UI variants.
- Keep design tokens in one place where the project architecture allows it.
- Separate layout, presentation, and business logic sensibly.
- Use stable keys for repeated elements and handle missing/long data safely.
- Avoid unnecessary dependencies, oversized component files, and fragile CSS overrides.
- Do not rewrite the whole application for a small UI request.
- Use real routes and state management already present in the project.
- Never claim tests, builds, accessibility checks, or browser verification passed unless they were actually run.

## Required acceptance checklist

Before declaring UI work complete, verify each relevant item:

- [ ] Read this skill and inspected the existing project before coding.
- [ ] Clear visual hierarchy and one obvious primary action per screen.
- [ ] Typography, spacing, colors, borders, radii, and icons are consistent.
- [ ] UI matches the product's audience and does not blindly copy the reference.
- [ ] All visible controls have real behavior or are clearly disabled.
- [ ] Loading, empty, error, success, and disabled states exist where relevant.
- [ ] Responsive layout checked at mobile, tablet, and desktop widths.
- [ ] No unintended overflow, clipping, overlapping, or broken images.
- [ ] Keyboard navigation and visible focus states work.
- [ ] Labels, contrast, semantic structure, and alt text are addressed.
- [ ] Existing routes and functionality remain intact.
- [ ] Available build/typecheck/lint/tests were run and relevant failures fixed.
- [ ] Final response accurately lists changes, verification performed, and remaining limitations.

## Final response format

When reporting completion, summarize:
1. Main UI/UX changes.
2. Responsive and accessibility work.
3. Checks actually run and their results.
4. Any missing data, unavailable tooling, or remaining issues.

Be concise, factual, and do not claim perfection or verification that did not happen.
