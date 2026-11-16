# rules.md — Bourne Shellfish app

## Must stay
- **Every section stays in the design:** Status, Your spot, All spots, Dates open, Conditions (weather, water quality, tides, other), Permits, Regulations, Maps, Education.
- **Map and tide table stay as they are.**
- **Status sits at the top** of Home, above everything else. "Your spot" comes directly below it.
- **Every status answers the same five things in the same place:**
  1. **State**, shown as a word, a color and an icon (never color alone)
  2. **Why** (the reason)
  3. **When**: "Open through [date]", "Closed through [date]", "Opens to the public [date]" or "Possible closure from [date]"
  4. **Next step**: check back, sign up for alerts, see dates, or view the map
  5. **Source and last update time**, e.g. "Set by Town of Bourne Natural Resources · Updated 8:02 AM"
- **A way to sign up for notifications is always one tap away:** the bell, the status card button, or the menu.

## May change
- **Status is the main thing that changes:** the state, reason, dates and next step.
- **Live values come from an API:** tides, weather, water quality and other conditions.
- **Regulation text may be shortened** or shown another way, e.g. "Key rules in 1 minute" plus the full PDF.
- **Wording, order of spots in a list, and which spot is "Your spot".**

## Must never happen
- **Users never have to question whether a spot is open or closed, or why.** No status without a reason and a date.
- **No directions and no "Go" for a closed spot.** Only Open and May close rows show "Directions".
- **No vague end times.** Write "Closed through Fri, Nov 20", not "until the Town reopens it".
- **The app never shows "Open" while a closure is in effect.**

## When two states apply
Show the one that stops you going now, and add the other as one line:
1. Closed due to conditions
2. Not open to the public
3. May close soon
4. Open

Example: Closed (heavy rain) + "Also out of season until [date]".

## Reasons a spot may close (closed or anticipated)
- **Weather:** heavy rain, storm, hurricane, coastal flooding
- **Water quality:** failed sample, results pending
- **Red tide:** harmful algae / shellfish toxins
- **Sewage:** sewer overflow or treatment plant problem
- **Spill:** fuel, oil or chemical spill nearby
- **Summer heat:** Vibrio controls for oysters
- **Restocking:** area closed so seed shellfish can grow
- **Season:** season ending or not started yet

## Visual rules (all built as Figma Variables)

**Color: Town of Bourne website palette**
| Use | Color |
|---|---|
| Brand, buttons | purple #846496 |
| Links | deep purple #63368B |
| Closed | mauve #8A525F (tint #F3E8EA) |
| May close, accents | khaki gold #AC9762 (tint #F4EEDF) |
| Open | sage #557563 (tint #E6EEE8) |
| Not public | warm gray #6B6670 (tint #EDEBEF) |
| Page background | #F4F4F4 |
| Text | #222222 / #555555 |
| Borders | #E5E5E5 |

- **Status cards are soft tints** with a thin colored border. Only the chip and the icon carry the strong color.

**Type: the Town website's fonts**
- **Headings:** Roboto Condensed. **Body:** Roboto.
- **Sizes:** 12 / 14 / 16 / 20 / 28 / 36.
- **Text styles:** Display/XL, Heading/LG, Heading/MD, Body/MD, Body/MD Strong, Body/SM, Label/XS. Each one is bound to the type variables.

**Grid and base**
- **4 px base unit.** Spacing scale: 4, 8, 12, 16, 24, 32, 48.
- **Frame:** 390 wide, with a 4-column grid, 16 px margins and 16 px gutters.
- **Corner radius:** 8 / 12 / 20 / full.

**Accessibility**
- Touch targets are at least 44 px.
- Text contrast is at least 4.5:1.

## Reusable parts (Figma components)
- **Status card:** 4 states (Open / Closed / Not public / May close). The spot name is editable.
- **Spot row:** the same 4 states. The "never directions when closed" rule is built into the component.
- **Button:** two versions, on dark and on light.
- **Stat tile:** one live condition value.
- **Section tile:** an entry to Permits, Regulations, Maps or Education.
- **Checkbox row:** one option in the alert sign-up screen.
- **Menu item:** one row in the hamburger menu.
