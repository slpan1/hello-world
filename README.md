# Rooftop Social · Invite Tracker

A single-page web app to track RSVPs, dietary restrictions, and who you're still
waiting to hear from for the **Aberdeen & Visors Rooftop Social**.

## The event
- **What:** Casual summer rooftop get-together, family welcome
- **When:** Sunday, June 28 · 12–6pm
- **Where:** Kavir's place, Ukrainian Village (Chicago)
- **Food:** Catering by Green Street Smoked Meats
- **Host:** Kavir Naik & family · **Organizer:** Leon Pan
- **RSVP by:** Thursday 6/18 (accept/decline calendar invite + note any +1s, kids, allergies)

## Run it
Just open `index.html` in any browser — no build step, no server, no dependencies.
Edits (status changes, dietary notes, added people) save automatically to your
browser via `localStorage`. Use **Reset to original data** to restore the seed.

## What it shows
- **Summary stats** — going / maybe / awaiting reply / declined, plus a live
  headcount (adults + kids) computed from everyone marked *Going*.
- **Dietary & allergies board** — consolidated list for the caterer.
- **Still waiting on** — everyone who hasn't responded yet.
- **All invitees** — filterable cards; change anyone's status or dietary note inline.
- **Export for caterer** — one tap builds a clean summary (headcount + allergies +
  confirmed-guest list) you can copy to the clipboard or download as a `.txt`.

## Data source & reconciliation
Seeded from the calendar invite (17 invitees + organizer Leon Pan) and reconciled
against the **latest** Slack thread responses. Where Slack is newer than the
calendar, Slack wins:

| Person | Status | Notes |
|---|---|---|
| Leon Pan (organizer) | Going | +1 adult (Lucy) |
| Kavir Naik (host) | Going | Hosting |
| Liv DeSantis | Going | +1 adult & family · **shellfish allergy** |
| Ludan Wu | Going | +1 adult · **mushroom allergy** |
| Ryo Kondo | Going | +1 adult, +1 kid (7 yr old) |
| Philip Read | Going | — |
| Simon Huleatt | Going | — |
| Tavleen Chahal | Going | — |
| Suraj Sehgal | **Can't make it** | Calendar shows ✅, but his newer Slack reply says out of town |
| David Wise | Declined | — |
| Marco Oropeza | Declined | Traveling / in-law's 95th in Michigan |
| Alakh Patel | Maybe | Tentative |
| Michael Church Carson | Maybe | Optional invitee |
| Aaron Sandler | No response | Waiting |
| Annie Walsh | No response | Waiting |
| Chloe Martin | No response | Waiting |
| Henry Nicewick | No response | Waiting |
| Jonathan Chang | No response | Waiting |
