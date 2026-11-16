# brief.md — Bourne Shellfish app

## Question
How do people check conditions before they go out to collect shellfish?

## Who it is for
Members of the public, alone or in groups (families, friends), who want to collect shellfish in the Town of Bourne, MA.

## What they need to do
Open the app and know right away:
1. **Can I go today?** Is my spot open, closed, closed to the public, or likely to close soon?
2. **Why?** What is the reason (weather, water quality, season, or another cause)?
3. **When?** Which dates is it open to the public, and through what date is it closed?
4. **What next?** Check back, or sign up to be notified when something changes.

## The one result we want
Nobody drives to the water and then finds the spot closed. Nobody has to wonder whether a spot is open, or why.

## Context
- **This is an app**, run by the **Town of Bourne**. The Town sets the status for every area. In this app an "area" and a "spot" are the same thing.
- **There is no alert system today.** Information is spread across the Town website: regulations as PDFs, many separate maps, education in several places, tide tables in a separate app, and permits on the home page.
- **Status sits at the top of the page.** It can be one of four states:
  1. **Open**
  2. **Closed due to conditions**, with the reason
  3. **Not open to the public** (not a public date)
  4. **Anticipated closure**: a warning that a spot may close. The user can sign up to be notified.
- **Anticipated closures can come from** weather, water quality, or any other cause (see rules.md).
- **Live data comes from an API:** tides, weather, water quality and other conditions.
- **The status itself is set by the Town,** following state notices.

## Reference
- `reference-1-wireframes.png`: Home screen plus the four status states (team sketch)
- `reference-2-current-site-map.png`: how the current Town site is organized, and what is missing (team sketch)
- `reference-3-user-flow.png`: user flow from Home to "Go!" (team sketch)
- Final design (Figma): https://www.figma.com/design/0c7xevsdlg0ijGucKJmcR7
