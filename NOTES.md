# Field of Faith — build notes

## v1 (generator)
- `python3 generate.py --slug field-of-faith --palette forest --theme "african worship harvest field faith" ...`
- Hero: "A field / of faith." · Scripture anchor: John 4:35 (fields ripe for harvest).
- Palette at v1 was the generator's stock `forest` theme (bright emerald `#2FB37A` + gold `#E8C15A` on near-black).

## Phase 2 — Lovable rebuild refine (2026-07-21)
Old site: `https://faithrevivalcentre.lovable.app` — confirmed as this church's own site (logo reads
"Field of Faith Revival Centre", vision/mission text and pastor photo all consistent with the brief;
no name/pastor conflict found).

**Verified real assets pulled from the old site's own build (not screenshots, not hotlinked):**
- Logo: `assets/img/logo-real.png` — downloaded from `faithrevivalcentre.lovable.app/assets/logo-*.png`.
- Pastor photo (Pastor Ntshengedzani R Nemdaka preaching): `assets/img/pastor-real.jpg` — downloaded from
  `faithrevivalcentre.lovable.app/assets/pastor-*.jpg`. Now used in the Welcome section (replaced the
  generic Pexels congregation stock photo there).
- A third photo appeared in screenshots (hand on cloth/altar, tilted-card style) but its source URL isn't
  in the site's static JS/CSS bundle (likely fetched dynamically from a backend, not build-time bundled) —
  couldn't confirm authenticity or get a non-hotlinked source, so it was **not** used.

**Palette — retinted to match the real site's OKLCH tokens (converted to hex):**
their bg `#fcfcf8`, hero gradient `#002a0e → #093e1b → #34622a`, accent gold `#ddb049`. Kept Katlego's
dark cinematic structure (this is not a light-mode rebuild) but swapped the token hex values:
`ink #081C0F · ash #0F2A18 · ember #3C6B32 · blaze #123A1E · gold #DDB049 · bone #F7F4EA`
(previously `ink #0A130F · ember #2FB37A (neon emerald, no longer used) · gold #E8C15A · bone #EDF5EF`).
Primary CTA button switched from a green gradient fill to a **gold** fill, matching their solid-gold
"Our Mission" button.

**Content carried across verbatim from the old site:**
- Tagline "Grace. Faith. Hope in Christ." → now the heading of a new Vision & Mission section (`#vision`).
- Vision: "Evangelizing the word and reconciling man with God Almighty; spreading the message of grace,
  faith and hope in Christ Jesus through any available voice — word of mouth, literature and media."
- Mission: "To impact the world through preaching, teaching and demonstrating the word of Faith."
- Pastor framing ("A voice for faith & revival", "teaching the uncompromised word of God and equipping
  believers to walk boldly in grace and faith") woven into the Welcome section copy.
- Real service times: Sunday Main Service 10:00, Wednesday Bible Study 18:00, Friday Prayer Night 19:00
  (previously invented/generic template times).

**Deliberately NOT carried across (unconfirmed / placeholder in the source):**
- Address — old site's footer had no street address, just "Field of Faith Revival Centre" + city, so ours
  stays at city/province level too (no invented address).
- Phone (`+000 000 0000`) and email (`info@fieldoffaith.org`) on the old site both read as generated
  placeholders, not real contact details — neither was carried across. Ours keeps the template's existing
  placeholder tel link untouched.
- Copyright footer: old site has one ("© 2026 Field of Faith Revival Centre"), so ours was kept as-is
  (dynamic year via JS).
- No ministries list was shown on the old site, so the template's default four (Prayer & Intercession,
  Worship & Praise, Youth Alive, Community Outreach) were left as-is — "Youth on Fire" was renamed to
  "Youth Alive" only to drop a leftover fire-theme name, not because of source content.

**Design pass:** de-fired the template's leftover "ember/fire/ignite" motif (this church has no fire
imagery at all in its brand — it's a harvest field) → recolored the ambient canvas particles from
neon-emerald/mint to gold/wheat tones, swapped the 🔥 eyebrow bullet for 🌾, retitled a few leftover
copy lines ("Fuel the fire" → "Sow into the harvest", "Youth on Fire" → "Youth Alive"). The one signature
scripture moment stays singular and pinned on John 4:35 — didn't dilute it with their Ephesians 2:8 verse
as a second big moment.

Pushed to `github.com/wdfdev58-hub/field-of-faith`. Live at `https://field-of-faith.wdf.church`.
