# SQUARED

**Black-and-white retro 2D space arcade survival and exploration game.**

Created by Shaurya Singh, a 14-year-old self-taught programmer and aspiring technology entrepreneur.

## Overview

SQUARED is a browser-based game where you play as Captain Tim navigating the dangerous debris field around the exoplanet Spored in the year 2200.

## Storyline

The year is 2200. Humanity has developed advanced technology that enables intergalactic travel. Approximately eight million humans live on a habitable exoplanet called **SPARTUS**, located in the Andromeda Galaxy.

Our protagonist is **Captain Tim**, a curious human explorer who lives on Spartus. Tim decides to explore another exoplanet called **SPORED**, located in a satellite galaxy of the Milky Way.

Spored has been severely damaged by human technology and is surrounded by enormous quantities of artificial debris, abandoned machinery, and spacecraft remnants.

Tim must survive hostile aliens, black holes, comets, neutron stars, space creatures, and debris while collecting energy and managing his reactor — without harming innocent inhabitants.

## Visual Identity

Strict black, white, and shades of grey. Inspired by vintage science-fiction comic posters, retro arcade cabinets, and simple cartoon proportions (original designs).

## Gameplay Mechanics

| Mechanic | Description |
|----------|-------------|
| Movement | Left/Right (keyboard or touch) |
| Reactor | ON/OFF. OFF = 10s countdown to freeze |
| Bombs | Start with 20 hydro-nuclear bombs |
| Laser | Fire at hostiles only |
| Energy | Collect from stars (neutron faster). Click prompt within ~1s |
| Hazards | Aliens, black holes (gravity), comets, debris |
| Peaceful Creatures | Harming them = Space Police arrest → GAME OVER |

## Controls

- **Arrow Keys / A D**: Move left/right
- **Space**: Laser
- **B**: Bomb
- **Reactor button**: Toggle
- Touch buttons on mobile
- Click near stars to collect energy when prompt appears

## Features

- Single-file application (`index.html`)
- Supabase email authentication
- No gameplay data persistence (resets on refresh)
- Responsive monochrome design
- Canvas-rendered game with procedural elements

## Technical Architecture

- HTML5 + CSS3 + Vanilla JavaScript
- HTML5 Canvas for game
- Supabase Auth (public anon key only)
- SPA routing with Netlify `_redirects` for clean URLs
- requestAnimationFrame loop
- AABB-style collision

## Installation / Local Development

1. Clone the repository.
2. Open `index.html` in a modern browser (auth requires live Supabase).
3. For full SPA routes, serve with a static server that supports redirects, or use Netlify.

## Deployment

Deployed on Netlify free domain. Connect this GitHub repo to Netlify with:

- Build command: none
- Publish directory: `.`
- Add `_redirects` for SPA.

## Authentication Configuration

Uses Supabase project `xdbhaxmjqdyaupjkwofx` (Hauntit AI).

- URL: `https://xdbhaxmjqdyaupjkwofx.supabase.co`
- Public anon key embedded (safe for client).
- Email signup/login. Confirm email if required by project settings.
- Project must be active (not paused).

## Third-party Dependencies

- `@supabase/supabase-js` via CDN (Apache-2.0)

## Open-source Research

Investigated multiple MIT/Apache licensed Canvas space shooters (e.g. patrikpentikainen/space-shooter, hatchr/ApogeeZero, bohdan0/SpaceWar). No code was directly copied. Original implementation using standard patterns: rAF loop, simple physics, collision checks, starfield.

## Known Limitations

- Art is procedural Canvas drawings (image generation limit reached during development).
- Auth requires the Supabase project to be active and email confirmation configured.
- No sound (can be added via Web Audio).
- Difficulty is procedural and can vary.
- Mobile touch works via buttons; full gesture support basic.

## Future Possibilities

- More enemy types and AI
- Sound effects
- Additional levels / destinations
- Improved procedural art or sprite sheets
- Leaderboards (if data storage allowed later)

## License

Original work by Shaurya Singh. MIT-compatible for any reusable patterns.

---

*Play the live game after deployment.*
