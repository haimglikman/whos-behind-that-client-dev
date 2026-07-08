### v1.15.8 (client-dev) | Server: v1.19.3 | Admin: v2.13.13
- Same fix — timeline and legend preserve postIds order when reopening clusters from history

### v1.15.7 — DISCARDED (duplicate of v1.15.5)

### v1.15.6 — bug fix (client-dev) | Server: v1.19.3 | Admin: v2.13.11
- Same P-number fix — timeline and legend now assign P-numbers from the original postIds order

### v1.15.5 (client-dev) | Server: v1.19.3 | Admin: v2.13.10
- Clusters history: uses saved posts data for reconstruction — consistent P-numbers and entity data even for older clusters
- Investigate: cluster ID now shown at top above timeline in live results (not injected after render)
- Investigate: frame and event shown as prominent labeled cards in live results
- Tab title changed to "WBT - Client DEV"

### v1.15.4 — bug fix (client-dev) | Server: v1.19.2 | Admin: v2.13.8
- Clusters history: connection lines now restored when reopening a cluster — was passing [] instead of c.connections
- Clusters history: omitted posts now show their one-liner summary in hover popup, same as included posts
- Clusters history: cluster ID shown prominently at top above timeline, as a link
- Clusters history: URL updates to cluster ID on open (e.g. #WBT-CLU-...) — direct linking supported
- Clusters history: frame and event shown as prominent labeled cards, not tiny bottom text

### v1.15.3 — bug fix (client-dev) | Server: v1.19.2 | Admin: v2.13.8
- Post history: filter fields now use flex layout with consistent widths — no more uneven gaps
- Post history: actor filter is now a dropdown populated from researched actors
- Post history: new entity alignments and news sources now appear in dropdowns immediately after scanning, without needing a page reload
- Timeline: fixed "CLUSTER undefined" — CLIENT_CLUSTER_COLORS was missing label property (A/B/C/D)
- Clusters history: fixed clusters not appearing — saveClientCluster now passes deviceId and connections to server

### v1.15.2 — bug fix (client-dev) | Server: v1.19.2 | Admin: v2.13.8
- Post history: fixed uneven grid gaps — switched to auto-fill layout
- Post history: removed separate "News site" filter — merged into "Source" dropdown which auto-populates with news domains found in history (e.g. Ynet appears after first Ynet scan)
- Post history: entity match now shows a dropdown populated from entities in history, filters by prefix (startsWith) matching admin behavior
- Clusters history: now shows only the current device's clusters — fixed privacy issue where all users' clusters were visible
- FAQ: fixed rendering — answers now display correctly with proper formatting

### v1.15.1 — bug fix (client-dev) | Server: v1.19.1 | Admin: v2.13.8
- Fixed server connection error on load — SERVER_URL was pointing at placeholder instead of https://whos-behind-that-server-dev.onrender.com

### v1.15.0 (client-dev) | Server: v1.19.1 | Admin: v2.13.8
- Timeline: Y-axis entity lanes — same design as admin v2.13.x (LABEL_W=120, entity labels wrap, hover popup, no secondary below circles)
- Timeline: hover popup shows primary, secondary, date, summary; flips left when near right edge
- Legend: secondary entity shown between primary and post summary; ↗ Go to post link added
- Post history: pending banner expanded — shows basket posts with primary, secondary, date, scan ID, × remove button
- Post history: "Run investigation →" auto-navigates to Investigate tab and runs immediately
- FAQ: now fetched dynamically from server DB instead of hardcoded HTML
- All dates: switched to DD/MM/YYYY format throughout
- App version in bottom bar and topbar: always reads from CLIENT_VERSION constant — fixes stale version showing
- Basket cleared after investigation runs successfully

### v1.14.4 — bug fix (client-dev) | Server: v1.18.3 | Admin: v2.12.4
- Timeline: same label clamping and hover tooltip fixes as admin
- Cluster cards: cluster ID shown at top, editable name field with Save button
- Rename works from both live investigation results and cluster history view

### v1.14.3 — bug fix (client-dev) | Server: v1.18.2 | Admin: v2.12.3
- Timeline: same fixes as admin — stacked vertical labels for same-date posts, crisp font
- Cluster history: omitted posts now shown when reopening a saved cluster
- Cluster save: now passes isolated post IDs to server for full reconstruction

### v1.14.2 — bug fix (client-dev) | Server: v1.18.1 | Admin: v2.12.2
- Added full cluster visualization to investigate results — timeline SVG with color-coded nodes, connection arcs, cluster labels, split-ring for multi-cluster posts, and legend with post summaries (mirrors admin)
- Timeline: same-date posts sit side by side with horizontal offset; date labels skip when too close; entity titles constrained to node width
- Clusters history: view button now works — fixed double JSON.stringify bug
- Clusters history → full view now includes timeline and legend reconstructed from saved post data

### v1.14.1 (client-dev) | Server: v1.18.1 | Admin: v2.12.1
- Basket: hovering a post shows tooltip with entity, score and post excerpt
- Synopsis cards: post summaries shown below synopsis for each post in cluster
- Clusters history: each cluster is clickable — opens full synopsis view in Investigate tab
- Investigate: buttons auto-clear after Run investigation is pressed

### v1.14.0 (client-dev) | Server: v1.18.0 | Admin: v2.12.0
- Renamed "My history" to "Post history" throughout
- New Clusters history tab (between Investigate and FAQ) — shows all previous cluster analyses
- Investigation: clusters now saved to server DB after synthesis with auto-generated cluster ID

### v1.13.0 (client) | Server: v1.17.1 | Admin: v2.11.0

- New Investigate tab (between History and FAQ) — cross-analyze posts to detect connections and narrative patterns
- Investigate basket — persistent across sessions, add/remove posts, clear when done
- + Investigate button on every history card and on scan result screen
- Pending banner in History tab shows basket count with quick-open link
- History filters: ID, URL, platform, news site (dynamic from history), date range, entity match, actor handle
- New FAQ: How does Investigate work? (Scanning logic)
- New FAQ terms: Frame, Event, Connection, Cluster, Synopsis (Terminology)
- DOMAIN_NAMES lookup for news site display names (Ynet, BBC, etc.)
