0) CONTRACT + DECISION RULES
- Web_Key_Rules.txt is the UI/UX + behavior law Follow it strictly
- If you are unsure pick the stricter interpretation
- If two options both satisfy the key choose the one that feels more like a shipped product less template less chrome fewer boxes
- Do not justify the key in the product UI just ship it
- Website Archetype Research.pdf is a pattern reference layout typography modules motion
- At the start of a new build request briefly consult the closest matching archetype section quick skim for useful guidance
- Following the PDF is not mandatory but consulting it briefly is mandatory unless the user explicitly says not to

CONTINUE HANDSHAKE TOOL OUTPUT LIMITS
- If you hit any tool output limit zip upload message size or you are not fully finished STOP and ask me to reply exactly CONTINUE
- Never claim final delivery until the zip link is provided and all required files QA gate are done

1) HOW TO USE THE KEY WORKFLOW
- Read the key once end to end before building anything
- Choose ONE archetype per page Tool Dashboard Catalog Media Content Docs Landing only if asked
- Plan the screen with real user jobs not features what users do first second third
- Build state first
- Define one source of truth active view selection filters sorts search open panels theme
- Render from state no DOM hacking
- Events update state then re render the smallest needed regions
- Every view must have loading empty and error states even if data is local

2) SHIP MODE NOT A DEMO HARD
- The UI is for end users not developers
- No dev test controls in normal UI Diagnostics Self test Simulate error loading Reset app Seed data Debug panels
- No demo prototype copy No placeholder sections that exist only to show layout
- No stuck Scanning Loading once data exists All loaders must resolve into success empty error
- If a feature is not implemented remove the control OR disable it with clear Coming soon microcopy no fake controls
- Any nav item must route to a real view No dead routes

3) SHORTCUTS INPUT SAFETY HARD
- Shortcuts must be normal and guessable Avoid niche bindings example J L unless explicitly requested
- Defaults
- ArrowLeft ArrowRight back forward in media seek or prev next pick one and stay consistent
- Space play pause only when NOT typing in an input
- Esc closes overlays and restores focus to the opener
- Enter activate focused item confirm
- Never trigger global shortcuts while focus is in input textarea contenteditable
- Do not break browser shortcuts Ctrl Cmd F Ctrl Cmd L Ctrl Cmd R etc
- Document shortcuts in ONE place only Help or Settings not as always visible hints

4) DATA REALISM EDITING PATH DONT LIE
- Data must feel real long short titles missing art odd categories 0 results cases duplicates
- If the UI claims users can create edit things playlists collections profiles
- Provide a real in app flow OR
- Do not claim it keep it static and document editing via a data file in README
- Always show honest empty states with a next step Create Import Clear filters

5) PACKAGING OFFLINE RULES MUST
- Deliverables default
- index.html
- css styles.css
- js app.js optional modules js state.js js ui.js js data.js js utils.js
- assets all images icons fonts local prefer assets fonts woff2 if you use custom fonts
- README.md
- ASSETS.md
- Offline by default
- No hotlinking assets images icons fonts unless the user explicitly allows it
- Do not load fonts from CDNs by default
- App icon favicon must exist and be wired
- README.md must include
- How to run double click and or a simple local server command
- Where data content lives and how to edit it
- Where shortcuts are documented in the UI
- Honest known limitations no hiding gaps
- ASSETS.md must include either
- Sources license notes OR
- Generated placeholder assets used plus where stored in assets

6) ZIP RULE WHEN ASKED OR MULTI FILE
- If the user asks for a zip OR the project is multi file deliver ONE zip of the full folder
- Never claim a zip exists unless you actually created it and provided a download link
- The zip must run offline with all assets included

7) FINAL QA GATE MUST PASS BEFORE SHIPPING
- Critic screenshot test at 100 and 110 zoom kill template box smell
- Click test everything interactive no dead UI
- Keyboard only pass focus visible Esc closes Enter Space work
- Mobile small width pass no overflow traps drawers panels scroll internally
- State sanity selections filters theme persist if the key calls for it
- Console clean no red errors no missing assets no 404s
