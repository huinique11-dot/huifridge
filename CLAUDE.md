# 우리집 냉장고

Single-file mobile web app: `index.html` (Tailwind CDN + vanilla JS, no build step). `manifest.json` and `icons/` support "add to home screen". Deployed via GitHub Pages from `main`.

## Keep the guide in sync

This app has two user-facing guides. **Whenever a change is significant enough that a first-time user would notice it (a new feature, a changed flow, a renamed button/behavior), update both:**

1. **In-app guide boxes** — the collapsible "❓ OO 탭 사용법" section at the top of each of the 4 tabs (`view-fridge`, `view-shopping`, `view-log`, `view-menu`) in `index.html`. Keep these short and concrete.
2. **Illustrated guide artifact** — a separately published Claude Artifact (HTML), linked from the settings modal as "📖 그림으로 보는 전체 설명서". To update it: edit the guide source, then republish with `Artifact` passing the existing artifact `url` (find it via the link in the settings modal, or `action: "list"`) so it updates in place rather than creating a new one.

Small internal refactors, bug fixes with no visible behavior change, or styling tweaks don't need guide updates — only things a family member using the app would actually need to know.

## Repo notes

- `huinique11-dot/huifridge` is the active repo going forward (an earlier `huinique11-dot/hui` repo exists but was intentionally left as-is, not deleted).
- Family real-time sync is optional, via Firebase Firestore, configured per-device in the settings modal (not baked into source — no secrets in this repo).
