# Monologue — Improvements Backlog

Running list of issues and improvements to work through. Newest notes go at the
bottom of each section; move items to **Done** once shipped.

---

## Open

### 1. Can't check in or create checkpoints mid-ride

**Priority:** High — blocks the core use case.

**What happens:** While a ride is in progress, checkpoints are effectively
read-only. Two things are impossible:

1. **Checking in to an existing checkpoint** — passing a checkpoint during the
   ride does not let me record that I reached it.
2. **Creating a new checkpoint** — I can't add a checkpoint on the fly for a
   spot I decided to mark while already riding.

**Why it matters:** The middle of a ride is exactly when checkpoint data is
worth capturing. If both actions are only available before or after the ride,
the feature doesn't cover the moment it exists for. Anything not recorded live
has to be reconstructed from memory afterwards, which defeats the purpose.

**Notes / open questions to settle before implementing:**

- Is this a UI gap (the controls aren't reachable from the active-ride screen)
  or a state-machine restriction (checkpoints are locked once a ride starts)?
- Check-in should be usable one-handed / glanceable while moving — big tap
  target, no multi-step confirmation dialog.
- Consider automatic check-in by proximity (GPS radius around the checkpoint)
  with a manual override, so no interaction is needed at all in the common case.
- New checkpoints created mid-ride should default to the current location and
  current timestamp, with naming optional and editable later.
- Offline behaviour: check-ins must queue locally and sync later — no signal is
  normal mid-ride.

---

## Done

_(nothing yet)_
