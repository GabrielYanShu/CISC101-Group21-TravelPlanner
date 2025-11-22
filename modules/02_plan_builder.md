Changelog:
  Added changelog
  Extended loop (everything that doesn't begin with "pick") for more clarity and robustness.

Create a short list of candidate activities (e.g., attractions, restaurants, parks).  
Each activity includes type, estimated duration, cost range, and distance.

Use a simple loop to build days:

for each day:  
    pick Morning activity (near lodging)  
    pick Midday activity (close by)  
    pick Afternoon activity (different theme)  
    pick Evening restaurant or optional event
    Apply budget, mobility, dietary, and accessibility rules to every slot.
    Enforce theme variety across the day (no redundant activities).
    Validate opening hours and ticket availability.
    Respect weather conditions: swap outdoor with indoor equivalents.
    Prioritize spatial clustering to minimize backtracking.
    Anchor morning near lodging, then build outward logically.
    Ensure each slot flows geographically (short hops, no zig-zagging).
    If lodging missing → default to central anchor.
    If budget missing → assume midrange with callout.
    If weather unavailable → mix indoor/outdoor with contingencies.
    Normalize to minimum viable plan (free/low-cost items).
    Add note explaining limitations.
    Cap total duration at 8–9 hours.
    Insert buffer slots.
    Mark optional activities that can be skipped.
