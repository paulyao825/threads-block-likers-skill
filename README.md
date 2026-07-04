# threads-block-likers-skill

A Claude Cowork skill that blocks every account that liked a specific Threads post or comment, driven through the browser on your own logged-in Threads account.

## Download

- **Easiest:** click `threads-block-likers.skill` above, then use the "Download raw file" button (the download icon) on that file's page.
- Or clone the whole repo: `git clone https://github.com/paulyao825/threads-block-likers-skill.git`
- Or use the green "Code" button above and choose "Download ZIP".

## Install into Claude Cowork

1. Download `threads-block-likers.skill` from this repo.
2. Drop it into a Claude Cowork chat, or open it and use the "Save skill" button if your workspace supports installing skills this way.
3. Once installed, just ask Claude things like "block everyone who liked this post: <Threads URL>".

## Files

- `threads-block-likers.skill` — packaged skill file, ready to install.
- `threads-block-likers-SKILL.md` — the skill's instructions (source of truth for how it behaves).
- `threads-block-likers-USER_GUIDE_zh-TW.md` — a plain-language usage guide in Traditional Chinese for non-technical users.

## What it does

Given one Threads post or comment URL, the skill:

1. Opens that post's like list (via "View activity" -> "Liked by").
2. Shows you the full list of accounts before touching anything, and waits for confirmation.
3. Blocks each account one by one, at a human-like pace, from your own Threads account.
4. Reports back what was blocked, skipped, or failed.

It only ever touches the one post/comment you name, never asks for your password, and never solves CAPTCHAs on your behalf.
