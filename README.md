[README.md](https://github.com/user-attachments/files/32075983/README.md)
# WFPD-BIDNIGHT
The 2026 WFPD Shift Bid!
# Woodside Fire — Bid Night

Live shift-bid board for the 2026 shift bid. Replaces the call-in-and-update-the-spreadsheet process with a board the whole department can watch in real time.

**Live app:** https://YOURNAME.github.io/bid-night

Open it in any browser. Nothing to install.

---

## What it does

Members call in their bid the way they always have. A union president records it on the console, and the board updates for everyone watching — bay screen, phones, and the crews on shift.

| Screen | Who it's for |
| --- | --- |
| **Hub** | Landing page — start here |
| **Big Board** | The 85" screen in the apparatus bay |
| **Roster Board** | Full seniority list, all three shifts |
| **Member View** | Phone view for members riding out the night |
| **Broadcast** | Video feed + board for crews on shift |
| **Mock Bid** | Practice board — run a fake draft to learn the flow |
| **Control** | Operator console (union presidents + admin only) |

## Access

Anyone can watch without signing in. Recording bids needs a code:

- **Union presidents** — can record bids and pass
- **Administrator** — everything above, plus undo, reset, timer, manual placement, and seniority override

Codes are distributed separately by Erik Lohmann. They are **not** in this repo.

> These codes keep honest people out; they are not real security. Anyone who views the page source can find them. Don't treat a recorded bid as legally binding without a president confirming it verbally.

## Running draft night

1. Open the app on the bay laptop and click **TEST STINGER** once — browsers block audio until you interact with the page.
2. Load your walk-up track under **Control → Broadcast → Walk-up track** (stays on the laptop; re-pick it after any reload).
3. Put the bay screen into kiosk mode by adding `?kiosk=1` to the URL. All controls disappear so nobody can bump the laptop into making a pick.
4. A president signs in on their own device and records bids as members call in.

Each pick fires the walk-up track, then a spoken announcement 1.5 seconds later. **CHEER** and **BOO** are manual — the operator taps them.

## Known limits

- **No live sync yet.** Every device runs its own copy, so picks do not currently travel between them. A Firebase URL field is in Control → Live Sync for when we turn it on.
- **Members cannot enter their own picks.** Deliberate — a bid is final under Policy 403, and a soft code can't prove identity. See below.
- Timer is the 10:00 notification-to-bid window from Policy 403.

## Under consideration

**Propose-then-confirm.** The member on the clock taps their choice on their phone. It does not land on the board — it lands in the president's queue as *pending*. The president, still on the phone with them, reads it back and confirms. Keeps one accountable human in the loop while killing the transcription errors, and gives us a real audit trail.

## Requesting changes

Open an [issue](../../issues) — one per request. Include which screen, what you expected, and what happened. Screenshots help.

---

Bid date: October 2026.
