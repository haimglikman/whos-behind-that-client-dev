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
