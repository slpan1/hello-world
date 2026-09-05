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
- **KPI bar** — live metrics: total RSVP'd (of invited), pending replies, attending
  adults, attending kids, and how many guests have dietary needs.
- **Collapsible name list** — each row shows the name, RSVP status, +1 party size,
  and a ⚠️ dietary indicator. Tap a row to expand and edit status, adult/kid
  counts (steppers), and dietary restrictions inline. Filter by Going / Maybe /
  Pending / Declined.
- **Export for caterer** — one tap builds a clean summary (headcount + allergies +
  confirmed-guest list) you can copy to the clipboard or download as a `.txt`.

All edits auto-save to your browser; **Reset data** restores the screenshot seed.

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

---

# Mexico City · Area Guide (`mexico-city.html`)

An interactive, self-contained map for learning the neighbourhoods of Mexico City
before a trip. Open `mexico-city.html` in any browser — no build step, no server, no libraries.
The only network request is the Google Fonts stylesheet (Archivo + Newsreader);
it falls back to system faces offline.

## What it does
- **38 clickable zones** covering the city and its inner suburbs, coloured by
  character (historic core, trendy/dining, upscale, everyday local, colonial &
  arts, parks & water, outer/transit). Click one for a short description plus
  *best for*, *feel*, *nearest metro* and a practical tip.
- **114 pins** in seven filterable categories: Michelin, sights, museums,
  shopping, bars, food & markets, parks. Click a pin for a description, address
  and a "good to know" line.
- **Michelin data follows the 2026 MICHELIN Guide México selection** — the two
  two-star kitchens (Pujol, Quintonil), the nine one-stars, and El Califa de León
  flagged as formerly starred — plus several Bib Gourmand entries.
- **Day trips view** — a hub-and-spoke map of 15 destinations around the valley
  with drive times, from Teotihuacán to Taxco.
- **Search** across every zone, place and day trip; **All areas** and
  **Highlights** browsers; and a **Basics** tab (altitude, transport, money,
  meal times, Monday museum closures, safety).

## How it's drawn
There are no map tiles or external libraries. Zone shapes are generated at load
time: every area carries one or more real lat/lon seed points, and the page
computes a clipped nearest-neighbour partition of an urban-footprint polygon, so
the zones tile without gaps and sit in geographically correct positions. Main
avenues, the airport runways, the Xochimilco canal grid and the big parks are
drawn as separate layers. Labels and pins are laid out in screen space with
collision detection, so the map thins out when zoomed out and fills in as you
zoom in.

Zones are simplified for clarity — good for orientation, not for navigation.
Hours, prices and bookings change; verify before you go.
