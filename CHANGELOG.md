# Changelog

## [0.0.7] - 2026-03-19

### Added

- Worker instance IDs — each worker gets a unique ID, scoping merge history per user
- User ownership tracking — workers and changes are tied to the user who created them
- Cross-window auth sync — sign in/out in one window updates all open windows instantly
- Automated commit-rebase-merge flow — when Main has uncommitted changes during merge, prompts to commit then automatically rebases and merges
- Auto Commit inline spinner — closes popup immediately, shows spinner next to Changes heading with buttons disabled until done

### Changed

- Rebase button disabled when worker has uncommitted changes (tooltip: "Commit changes first before rebasing")
- Changes list scoped by user — signed-in users only see their own commits and merges, guests only see guest activity
- Uninit no longer deletes .git directory, preserving the repo for continued use
- Server sync optimized — single fetchSync() call replaces multiple separate API calls on auth change and startup
- Sign-in no longer flashes default worker names — customizations load before UI updates

### Fixed

- "wId is not defined" error when merging a worker
- Worker ID tag stripped from merge commit display in Changes list

## [0.0.6] - 2026-03-17

### Fixed

- Fix extension activation failure ("CONVEX_SITE_URL is not defined")

## [0.0.5] - 2026-03-16

### Initial Release

- Visual dashboard in VS Code secondary sidebar for managing git worktrees
- Up to 8 color-coded workers, each with its own isolated worktree and branch
- One-click rebase from main and merge back with conflict resolution
- Full task history with revert and remerge support
- Worker customization — names, initials, shapes, colors, text colors, and SVG icons (Sponsor tiers)
- GitHub OAuth sign-in with settings sync across devices
- Keyboard shortcuts for quick worker switching (`Alt+1`–`Alt+8`)
- In-panel settings with Main Branch and Commit Command configuration
- Searchable FAQ with expand/collapse
- Free tier: 2 workers. Patron ($10/mo): 4 workers + shortcuts. Patron Max ($20/mo): 8 workers + full customization.
