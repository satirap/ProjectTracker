# Project Tracker - Notification System UI/UX Design

## Context
Project Tracker is an organizations > projects > phases > tasks management system. We need to design a modern, user-friendly notification and reminder system to prevent notification fatigue while keeping users informed about critical updates.

## Design Challenge
Create a 3-level notification control hierarchy that:
- Prevents notification fatigue (40% of PM tool churn)
- Gives users granular control
- Keeps critical alerts visible
- Works across devices (desktop, mobile)

---

## Components to Design

### 1. **In-App Notification Center**
**Purpose:** Central hub showing all notifications
**Show me options for:**
- Design A: Notification panel (sidebar, similar to Slack)
- Design B: Dropdown notification tray (bell icon menu)
- Design C: Dedicated notification page (full-page view)

**Must include:**
- Notification items with timestamp
- Mark as read / Archive actions
- Filters (All, Unread, Mentions, Due dates, Assignments)
- Clear/Snooze options
- Dark/Light mode support

---

### 2. **Preference Center (Settings)**
**Purpose:** Global notification preferences
**Show me options for:**
- Design A: Tabbed settings (Notifications > Events > Channels > Quiet Hours)
- Design B: Sidebar menu (simpler, linear flow)
- Design C: Card-based layout (each category as a separate card)

**Must include:**
```
Event Type Toggles:
☐ Task assignment
☐ Due date approaching
☐ Comments/mentions
☐ Status changes
☐ Phase updates

Channels:
○ Email (Off | Real-time | Digest)
○ In-App (Off | Real-time | Batched)
○ Push (Off | Enabled)

Quiet Hours:
From [9 PM] To [7 AM]

Digest Frequency:
○ Real-time ○ Daily (9 AM) ○ Weekly
```

---

### 3. **Task-Level Reminder Picker**
**Purpose:** Quick inline reminder configuration on each task
**Show me options for:**
- Design A: Modal popup (click clock icon → modal form)
- Design B: Inline expandable section (no modal, expands in-place)
- Design C: Floating action menu (right-click context menu)

**Must include:**
```
Reminder Settings
├─ Status: [○ Off  ● On]
├─ Timing: [Dropdown: 5 min | 15 min | 1 hour | 1 day | 3 days | 1 week | Custom]
├─ Repeat: [○ Once  ○ Daily  ○ Weekly  ○ Monthly]
└─ Channel: [Dropdown: In-app | Email | Push]

Visual feedback:
- Clock icon changes color when reminder is active
- Shows "Due in 3 days" label
- "Reminder set ✓" toast notification
```

---

### 4. **Mobile Notification Design**
**Purpose:** How reminders appear on mobile (push notification)
**Show me options for:**
- Design A: Standard iOS/Android style (native feel)
- Design B: In-app banner notification (dismissible header)
- Design C: Custom notification card (branded style)

**Must include:**
- Task name
- Due date / Reminder type
- Action buttons (View, Snooze, Dismiss)
- Rich notification (image thumbnail if phase has icon)

---

## Design Constraints & Requirements

### Visual Design
- **Color Scheme:** 
  - Primary: #667eea (current purple)
  - Alert/Urgent: #e74c3c (red)
  - Success: #27ae60 (green)
  - Warning: #f39c12 (orange)

- **Typography:**
  - Font: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif
  - Heading: 16-18px, bold
  - Body: 13-14px, regular
  - Small labels: 11-12px, medium

- **Icons:** Use simple, clean icons (Feather-style or Heroicons)

- **Spacing:** 8px grid, consistent padding (8px, 12px, 16px, 20px, 24px)

- **Accessibility:**
  - WCAG AA compliant
  - Color-blind friendly (not relying solely on color)
  - Keyboard navigation support
  - Focus indicators visible

### Interaction Patterns
- Smooth transitions (200-300ms)
- Confirmation before destructive actions
- Snooze options (5 min, 1 hour, 1 day, 1 week)
- Undo for dismissals (5-second window)
- Loading states for async actions

### Responsive Design
- Desktop: Full settings UI in sidebar/modal
- Tablet: Compact version, collapsible sections
- Mobile: Bottom sheet drawer for settings, simplified pickers

---

## Design Options Preference

**Please show me 2-3 design variations for:**
1. Each major component (Notification Center, Preference Center, Task Reminder Picker)
2. Compare visual approaches (minimal, modern, comprehensive)
3. Show light + dark mode for each

**For each option, highlight:**
- Pros (why this approach works)
- Cons (usability trade-offs)
- Recommended for [desktop/mobile/both]

---

## Success Criteria

✓ Users can enable/disable notifications in < 3 clicks
✓ Preference changes take effect immediately (visual feedback)
✓ Task-level reminders override global preferences
✓ No more than 5 notification types initially
✓ Dark mode is equally usable as light mode
✓ Mobile experience is not cramped

---

## Reference Information

### Current Project Tracker UI
- Primary colors: #667eea (purple), #764ba2 (dark purple)
- Cards with shadows (0 2px 4px rgba(0,0,0,0.1))
- Rounded corners (6-12px)
- Clean, minimal aesthetic (similar to Asana, Monday.com)

### Notification Types (MVP)
1. **Task Assignment** - "John assigned you to 'Design Homepage'"
2. **Due Date Alert** - "Design Homepage due in 1 day"
3. **Comment/Mention** - "Sarah mentioned you: 'John, what do you think?'"
4. **Status Change** - "Phase 'Design' moved to In Progress"
5. **Phase Update** - "New task added to Phase 'Design': 'QA Review'"

---

## Deliverables Expected

1. **3 Notification Center Designs** (mobile + desktop each)
2. **2 Preference Center Layouts** (mobile + desktop)
3. **Task Reminder Picker** (3 interaction patterns)
4. **Mobile Push Notification** (2 styles)
5. **Dark Mode Variants** (key screens)
6. **Interaction Flows** (GIF/video showing how user sets a reminder)
7. **Component Library** (buttons, toggles, badges, chips for notifications)

---

## Questions for Designer

- Should notifications be real-time (instant bell icon) or batched by default?
- For mobile, should preference center be a bottom sheet or full-page modal?
- How do we handle "snooze" duration options? Dropdown or quick-select chips?
- Should quiet hours automatically snooze notifications, or just prevent notifications?
- Do you recommend toast notifications for "Reminder set"? Or inline confirmation?

---

## Next Steps After Design

Once designs are approved:
1. Create interactive Figma prototype (clickable flows)
2. Hand off to dev team with component specs
3. Implement in code (Week 1-2)
4. User test (Week 3)
5. Iterate based on feedback

---

## Budget
- Design exploration: 4-6 hours
- Interaction flows/prototyping: 3-4 hours
- Total: 7-10 hours design work

**Timeline:** 1 week for all design options
