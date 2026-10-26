# Studymark: status

_Last updated: 26 Oct 2026 (Cowork)._

## Now
- **Studymark = HabitAI + TaskFlow merged into one app** (habits/streaks + tasks/planner + focus + squads). Those are no longer separate projects.
- **The relaunch is uncommitted on `main`** (76 changed paths): new tabs today / plan / squad / feed / me, focus mode with social lock, Android app blocker (Kotlin, `modules/app-blocker`), local study reminders, squads + chat, community feed, peer grading.
- New backend: **Supabase (Mumbai)**, schema in `supabase/migrations/` (4 files, 15–16 Oct). Firebase kept only for push.
- Root `README.md` still describes the old "TrackMe" app.

## Next
1. **Move the relaunch to a feature branch before any commit** (`git switch -c relaunch/v2`). Don't push it to main as is.
2. Test the app blocker and reminders on a real Android phone.
3. Create/link the Supabase project, push migrations, set `EXPO_PUBLIC_SUPABASE_URL` / `_ANON_KEY` (never the service_role key).

## Open to-dos
- [ ] Rewrite README for the relaunch
- [ ] Decide what's left of `apps/backend` (old Firebase/Cloudinary/cron) vs Supabase
- [ ] Portfolio: Studymark waitlist page

## Key facts
- Monorepo: `apps/mobile` (Expo SDK 56, Expo Router), `apps/backend` (Express on Vercel), `supabase/`.
- DB rules: 18+, can't edit own stats, squad 3–10, members-only chat. Cron (IST): 06:00 read-today, 22:15 assign graders, 02:00 close day.
- Designs: "Studymark Design" canvas artifact (claude.ai).

## Log
- 26 Oct 2026: noted that HabitAI and TaskFlow are merged into Studymark.
- 26 Oct 2026: STATUS.md/AGENTS.md added (committed alone; relaunch work still uncommitted).
