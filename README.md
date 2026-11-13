# CapForge Rosters

Real-life NFL rosters for **[CapForge: Football GM](#loading-the-files-into-capforge)**, free to use.

I've been building rosters for custom games for a while, and for Madden for years, so I've got the process
down. These are real NFL rosters converted for CapForge, and a few pieces are still in progress (see
[Known gaps](#known-gaps-please-read)).

## Quick links: paste these into the app

In CapForge, go to **NEW GAME → IMPORT**, paste each link into its row, press **VALIDATE**, and start at
**Reg Season**. [Full steps below.](#loading-the-files-into-capforge)

**PLAYERS**
```
https://github.com/jmansfield96/capforge-custom-rosters/blob/main/player-files/madden-27-players.json
```

**TEAMS**
```
https://github.com/jmansfield96/capforge-custom-rosters/blob/main/teams-files/nfl-teams.json
```

**STAFF**
```
https://github.com/jmansfield96/capforge-custom-rosters/blob/main/staff-files/example-staff.json
```

### 2018 season (Madden 19)

The real 2018 NFL season: Week 1 rosters, Madden 19 ratings, real 2018 contracts, and 2018 team names and
stadiums (the Oakland Raiders, the Washington Redskins, the Rams at the Coliseum). Use all three files together,
and start at **Reg Season**.

**PLAYERS**
```
https://github.com/jmansfield96/capforge-custom-rosters/blob/main/player-files/madden-2018-players.json
```

**TEAMS**
```
https://github.com/jmansfield96/capforge-custom-rosters/blob/main/teams-files/2018-teams.json
```

**STAFF**
```
https://github.com/jmansfield96/capforge-custom-rosters/blob/main/staff-files/2018-staff.json
```

---

## What's in here

| Folder | File | What it is |
|---|---|---|
| `player-files/` | `madden-27-players.json` | **2,051 players** on all 32 clubs, with ratings, positions, ages, colleges, jersey numbers, draft info and real contracts. It also includes each club's 2026 dead money. |
| `teams-files/` | `nfl-teams.json` | **All 32 clubs** with real city, name, stadium, conference/division and team colors. |
| `staff-files/` | `example-staff.json` | **672 staff**: 7 chairs per club (HC, OC, DC, special teams, 2 scouts, team doctor) plus a free-agent pool. |
| `player-files/` | `madden-2018-players.json` | **2018 season: 2,514 players**, 1,663 on Week 1 rosters. Madden 19 ratings, real 2018 contracts scaled from the $177.2M cap to CapForge's $300M, draft history, potentials set from how each player actually developed (his best Madden 20-23 rating), and faces matched to each player's real headshot. |
| `teams-files/` | `2018-teams.json` | **2018 clubs:** Oakland Raiders, Washington Redskins, and 2018 stadiums and colors. Use it with the 2018 players file. |
| `staff-files/` | `2018-staff.json` | The same made-up staff, set up for the 2018 team file (Raiders as `OAK`). |

You can use any of the three files on its own. Use only the ones you want.

---

## Known gaps (please read)

- **Staff isn't done yet.** I haven't finished putting the real coaching staffs in. The staff file is complete
  and loads fine, so every chair is filled, but many clubs still have made-up coaches in some or all of their
  seats. I'll keep updating it.
- **Most player faces aren't right yet.** CapForge draws players from its own set of cartoon portraits, and
  there isn't one for every real player. Each player was given the closest match I could manage, so many of
  them won't look like the real guy. That only affects looks. Ratings and gameplay aren't touched by it.
- **Ratings are a translation.** CapForge rates players differently from Madden, so every Madden rating was
  converted into CapForge's attributes. The overall ratings should land close to Madden's. Individual
  attributes won't always match one for one.
- **Rosters are a snapshot.** They reflect roughly the start of the 2026 season, so later trades, cuts and
  injuries aren't in them.

If you spot something wrong, open an issue and I'll fix it when I can.

---

## Loading the files into CapForge

The game loads these files from a web link when you start a new save.

1. **Copy the links** from [Quick links](#quick-links-paste-these-into-the-app) at the top of this page.
   Any other GitHub file link works too, and so does the **Raw** link. The link must start with `https://`.
2. In CapForge, tap **NEW GAME** and choose the **IMPORT** roster type.
3. Paste each link into its row: **PLAYERS**, **TEAMS**, **STAFF**. Any row you leave blank uses the game's
   default league for that part.
4. Press **VALIDATE** on each row. The game checks the file and tells you if anything is wrong.
5. **For the start date, pick "Reg Season"** (it should already be selected).
   > ⚠️ **Don't pick "Draft Day".** These rosters already include the real 2026 rookie class. Starting at
   > Draft Day runs a fresh 2026 draft instead, and the real 2026 draftees get dropped from your league.
6. Tap continue, pick the team you want to run, and start your career. You begin at Week 1 of 2026.

**Already have a save?** You can apply the team file there too: **Settings → EDIT TEAMS → LOAD TEAMS**, then
paste the `nfl-teams.json` link. That only changes names, colors and stadiums. Players and staff can only be
imported when you start a new save.

**Tips**
- Use the players and teams files together. The players are assigned to clubs by team number (1–32), so
  loading the players on top of the default fictional team names still works, but it will look odd.
- The files are big (the players file is about 2.5 MB), so give the download a few seconds on a slow
  connection.

---

## Where the data came from

Credit to the sources that did the real work:

- **Player ratings:** [EA SPORTS Madden NFL 27](https://www.ea.com/games/madden-nfl/ratings) player
  ratings, converted into CapForge's rating system. 2018 season: Madden NFL 19 launch ratings, via
  [theedgepredictor/nfl-madden-data](https://github.com/theedgepredictor/nfl-madden-data).
- **2018 rosters and contracts:** Week 1 2018 rosters and OverTheCap contract history from
  [nflverse](https://github.com/nflverse/nflverse-data), licensed
  [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/). Contracts are scaled by 300 / 177.2 to CapForge's cap;
  a few clubs over the cap after scaling were trimmed to fit.
- **Contracts and dead money:** [Spotrac](https://www.spotrac.com/nfl/) team cap pages (cap hits, guarantees,
  contract years, dead cap).
- **Draft year and pick number:** [nflverse](https://github.com/nflverse/nflverse-data)
  (`players` and `draft_picks` data), licensed
  [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/).
- **Portrait matching:** player headshots listed in nflverse were used only to pick the closest CapForge
  cartoon face. No photos are in this repo.
- **Team info:** public team names, stadiums and official color hex codes.
- **Built with:** [Claude](https://claude.ai) by Anthropic. It helped write the conversion scripts, check
  the data and fix mistakes.

---

## Coming later

At some point I'd like to add a guide to making these files yourself: the file format, how ratings are
converted, and how to edit or build your own league. For now this repo is just the finished files.

---

## Disclaimer

This is an unofficial, non-commercial fan project. It is not affiliated with or endorsed by the NFL, the
NFLPA, any NFL club, Electronic Arts, Spotrac, or the makers of CapForge. Team and player names and all
trademarks belong to their owners. Ratings are derived from Madden NFL 27 and Madden NFL 19 and are © Electronic Arts.
If you own something here and want it removed, open an issue and it will be taken down.
