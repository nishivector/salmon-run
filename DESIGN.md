DESIGN_DOC
game_name: salmon-run
display_name: Salmon Run

---

# SALMON RUN
### *"He Was Not Built For This. He Will Do It Anyway."*

---

## IDENTITY

**Game Name:** Salmon Run
**Tagline:** He Was Not Built For This. He Will Do It Anyway.

---

### Protagonist: Gary

Gary is a middle-aged sockeye salmon who has never been particularly fast, coordinated, or impressive. He has one slightly bent dorsal fin from a close call with a rock in 2019 that he still talks about. His eyes are too far apart. He has a mild underbite. He is the most determined living creature on the planet.

Gary doesn't smirk. He doesn't have cool sunglasses. He is not ironic. He is 100% sincere, straining against the current with everything he has, and the music takes him *completely seriously* — which is what makes him so funny and so heroic at the same time.

**Backstory:**
Gary hatched in Clearwater Creek, Washington, four years ago. He spent those years in the Pacific Ocean eating krill and having a perfectly unremarkable life. Now, instinct has pulled him back to the exact gravel bed where he was born, upstream, through rapids, past bears, past fishing lines, past physics itself. Nobody told Gary it would be easy. Gary didn't ask.

---

### World: Pacific Northwest River — Peak Autumn

The river is Clearwater Creek, Washington state, in the third week of October. The water is glacially cold, green-tinted from algal bloom (#3D7A52 base), running fast over rounded granite boulders. The banks are thick with old-growth Douglas fir and big-leaf maple — the maples are exploding in amber and deep crimson, leaves skimming the water surface. Morning mist clings to the far bank. The sun is low and warm, cutting through the tree canopy in god-rays that hit the water and scatter into caustic light patterns on the riverbed.

The bear — a large coastal grizzly, maybe 600 lbs — stands knee-deep near the right bank, utterly still, waiting. He has been here for three weeks. He is very good at this.

**World Feel:**
This river is ancient and indifferent — it was here before humans, before bears, before salmon, and it will be here after. Gary doesn't belong here in the dramatic sense; he belongs here in the *biological* sense, and that difference is what gives him his dignity.

**Emotional Experience:**
The player should feel the specific absurdity of complete sincerity — rooting for this small, slightly derpy fish who is giving absolutely everything he has, while the orchestral score acts like he is storming Normandy. By level 3, the player is genuinely invested. By level 5, they are Gary.

---

### Reference Games & DNA

| Game | What We're Stealing |
|---|---|
| **Crossy Road** | One-tap lane logic, cartoon character with earnest personality, instant restart with no shame |
| **Alto's Adventure** | Ambient world-beauty that makes obstacles feel like interruptions of something peaceful; momentum-based hold mechanic |
| **Metal Slug** | Absurd heroism played completely straight; enemy telegraphing that feels fair even when lethal; death animations with personality |

---

## VISUAL SPEC

### Color Palette

| Role | Hex | Usage |
|---|---|---|
| Background / River | `#3D7A52` | Base water color, fills background |
| Deep Water | `#2A5C3F` | Water shadow, depth on far side of boulders |
| River Highlight | `#5FA373` | Water surface glint, foam edges |
| Water Caustics | `#7EC49A` | Animated light patterns on riverbed |
| Gary — Body | `#C0392B` | Deep spawning-red sockeye body |
| Gary — Belly | `#E8B4A0` | Pale salmon belly, visible in side profile |
| Gary — Stripe | `#8B1A1A` | Dark lateral line, dorsal markings |
| Gary — Eye | `#F5F0E0` | Off-white sclera with `#2C1A0E` pupil |
| Gary — Fin | `#A93226` | Slightly translucent, same red family |
| Rock — Base | `#5C5248` | Wet granite, dark brown-grey |
| Rock — Highlight | `#8A7E76` | Dry top face of boulder catching light |
| Rock — Moss | `#4A6741` | Moss patches on river rocks |
| Forest BG — Dark | `#1C3520` | Deep tree shadow layer |
| Forest BG — Mid | `#2D5C34` | Mid-canopy, Douglas fir |
| Forest BG — Light | `#8B4513` | Maple trunks, warm autumn |
| Autumn Leaves | `#D4831A` | Maple canopy, parallax layer |
| Bear — Body | `#3D2B1F` | Dark brown grizzly silhouette |
| Bear — Highlight | `#6B4C38` | Rim light on fur edges |
| Fishing Line | `#D4D0C8` | Near-invisible monofilament, slight shimmer |
| Fishing Line Lure | `#E8C84A` | Yellow spinner, high visibility |
| UI / HUD | `#F5EDD6` | Parchment-warm for HP hearts and score |
| Accent / Warning | `#F0A500` | Pre-obstacle warning glow, charge meter |
| Critical Warning | `#E03030` | Bear paw shadow incoming, 1 HP flash |

---

### Gary's Appearance

Gary is drawn in a clean 2D side-view sprite style — not pixel art, not vector-flat, somewhere between *Crossy Road* charm and a field guide illustration.

**Size:** Gary occupies approximately 18% of the screen width at rest. He is a medium-sized adult sockeye — about 60cm in real terms, rendered as roughly 180px wide × 70px tall at 1920px canvas width.

**Body Shape:** Classic salmon silhouette — streamlined fusiform body, widest at the pectoral region, tapering to a distinct forked tail. Not a rectangle. Not a triangle. A *fish.*

- **Body:** Deep spawning crimson (`#C0392B`), lighter on the belly (`#E8B4A0`)
- **Head:** Slightly pronounced kype (hooked jaw) — Gary has begun his spawning transformation. One side of his jaw curves slightly downward. This is accurate and also makes him look like he's grimacing with effort.
- **Eye:** Proportionally large, off-white with a dark pupil. Slightly too far apart (character beat). A single white specular dot.
- **Lateral Line:** Dark stripe (`#8B1A1A`) running mid-body from gill plate to tail base
- **Dorsal Fin:** 5 distinct rays, slightly ragged at the tips — the right side has a small notch (the 2019 rock incident)
- **Pectoral Fins:** Two small fins just behind the gill plate, animate independently during swimming
- **Tail (Caudal Fin):** Forked, wide, powerful-looking relative to his body — this is what drives him upstream. Fan-shaped with subtle ray detail. Primary red, slightly translucent at tips.
- **Adipose Fin:** Small, fleshy bump between dorsal and tail — present and correct (Gary is anatomically accurate)

**Swim Animation:**
- Body S-curve oscillation: 12 frames, tail sweeps ±22° from centerline
- Pectoral fins fold/extend on opposite phase to tail
- Body compresses slightly (squash) at peak effort, extends (stretch) at glide
- At full charge (waterfall hold): Gary's body arches backward, mouth opens slightly, eyes go wide

**Player Silhouette (5 words):** Crimson arc, kype, forked tail.

---

### Environment Details

**Foreground (Lane Layer):**
- 3 lanes defined by subtle ripple lines — not hard borders, just current-break foam lines that suggest channels. Lane width: equal thirds of playfield, approximately 320px each at 1920px wide.
- Boulder tops break the surface — visible as dark silhouettes with foam halos at their waterline
- Occasional leaf on the water surface, floating downstream (cosmetic, not obstacle)

**Midground (River Bed):**
- Animated caustic light patterns, 8-second loop, subtle — `#7EC49A` at 25% opacity over base color
- Rounded smooth stones visible through water at shallow sections (Levels 1–2 only)

**Background Layer 1 (Forest):**
- Dark silhouette of Douglas fir treeline — flat dark green `#1C3520`
- Parallax rate: 15% of scroll speed (much slower than Gary's apparent movement)
- A few fir trees break into warm `#2D5C34` mid-tones for depth

**Background Layer 2 (Autumn Canopy):**
- Big-leaf maple canopy in amber/orange `#D4831A` and `#C4692A`
- Parallax rate: 8% of scroll speed
- Leaves fall from this layer: spawn at top edge, drift diagonally downstream at ~30° angle, fade out at 80% screen height. Average 3 leaves visible at any time. Purely cosmetic.

**Bear Silhouette (Level 3+):**
- Grizzly stands in right side of screen, knee-deep in water
- Rendered as 2-layer silhouette: `#3D2B1F` body, `#6B4C38` rim light along top edge
- At rest: weight shifting animation (subtle, 3-second cycle)
- When active (Level 3+): rears up, telegraphed with a roar animation before paw swipe

**Water Surface:**
- Fast-moving horizontal ripple lines, white-to-transparent, scrolling right-to-left at 1.3× game scroll speed
- Foam/whitecaps accumulate behind rocks and at lane edges
- At waterfall approach: water surface gains a downward pull (new particle stream pointing toward waterfall)

**Bloom:**
- Strength: 0.4
- Threshold: 0.72
- Applied to: water caustics, Gary's eye specular, warning indicator glow, waterfall mist
- NOT applied globally — targeted only

---

### Camera

- **Type:** Side-scrolling, locked horizontal
- **Gary's Position:** Gary is always locked at 28% from left edge horizontally
- **Vertical:** Gary occupies center 60% of screen height. Camera does not track vertically (no vertical movement — this is a lane game).
- **World Scroll Speed:** See Difficulty table per level. World scrolls right-to-left; Gary appears to move left-to-right.
- **Lane Switch:** Camera does not move vertically. Gary moves between lanes with an animated lateral shift.
- **Zoom:** Fixed. No zoom. No camera shake on normal hits. On bear paw SLAM (near miss only): 3-frame push-in zoom (1.0 → 1.04 → 1.0) over 80ms — barely perceptible but visceral.

---

## SOUND SPEC

### Music Identity

**Genre/Vibe:** Full orchestral score — not chiptune, not lo-fi — genuine heroic orchestral that treats Gary's journey with the same gravity as *Lawrence of Arabia* or a John Williams nature documentary score, then earns its laughs purely from the contrast between the music's conviction and Gary's slight absurdity.

**Character:** The music never winks at the audience — it believes in Gary completely, which is exactly why it's funny and moving.

**The Hook — "The Gary Motif":**
A French horn plays a 4-note ascending motif: **G–B–D–G** (root → major third → fifth → octave), each note held slightly longer than the last, with a slight ritardando on the fourth note before the phrase repeats. It sounds like a call to action — noble, round, slightly too grand for a fish. This motif appears in every music state: sometimes triumphant, sometimes tentative (muted horn, half-tempo), sometimes collapsed into a dying wheeze (death state). The player will hear it in their head for days.

---

### Arrangement

**BPM:** 132
**Bar length:** 4/4
**Loop length:** 16 bars (normal swim loop), 8 bars (danger loop), 4 bars (waterfall loop)

| Instrument | Tone.js Type | Role | Entry/Exit |
|---|---|---|---|
| **Kick / Snare / Rim** | `Tone.MembraneSynth` (kick: pitch 60Hz→40Hz, decay 0.4s) + `NoiseSynth` (snare: noise "white", envelope 0.01/0.15) | Rhythmic foundation, steady 4/4 kick on 1&3, snare on 2&4, rim-shot fills at bar 4 | Enters immediately; drops to kick-only in danger state |
| **Timpani (accent)** | `Tone.MembraneSynth` (lower pitch, decay 1.2s, resonance 0.8) | Punctuates Gary Motif hits, rolls before waterfall | Enters bar 5 of normal loop; sustains through all states |
| **Bass / Cello** | `Tone.Synth` (oscillator "sawtooth", filter LP 400Hz, Q 2) | Harmonic foundation, walking bass line in G major, quarter notes | Constant; simplifies to root-fifth drone in danger state |
| **French Horn (the hook)** | `Tone.Synth` (oscillator "triangle" + slight detune 8 cents, envelope: attack 0.08s, decay 0.3s, sustain 0.7, release 0.6s) | Carries the Gary Motif; primary melodic identity | Enters bar 3 of normal loop; mutes in waterfall charge state |
| **Strings / Pad** | `Tone.PolySynth` (4 voices, "triangle", reverb send 0.6) | Harmonic warmth, fills inner voices, swells on bar 8 | Enter bar 1, fade to single sustained note in danger state |
| **Piccolo (comedy punctuation)** | `Tone.Synth` (oscillator "sine", high register, staccato: attack 0.01s, release 0.08s) | Plays a quick descending trill when Gary fumbles — a sort of "whoops" voice that mirrors his near-misses. Also plays the death wheeze. | Triggered by events, not continuous |

---

### Dynamic Music State Table

| State | Music Change |
|---|---|
| **Normal Swim** | Full arrangement: kick+snare, walking cello bass, Gary Motif in French horn every 4 bars, strings sustaining harmony, timpani accents. 16-bar loop. |
| **Near Bear / Close Call** | Snare drops; strings thin to a single tremolo note (minor 7th coloring); bass simplifies to root-fifth; horn plays Gary Motif at half tempo, muted (as if sneaking); piccolo holds a high, quiet note (tension); tempo *does not change* but the rhythm feels suspended |
| **Waterfall Charge (holding)** | All melodic content drops; timpani begins a slow roll that grows in volume proportional to charge (0%→100% charge = pp→ff timpani); strings swell on a held dominant chord (D major over G bass = anticipation); piccolo silent; horn silent; bass holds low G pedal point |
| **Gary Dies** | All instruments cut to silence for exactly 1 beat, then piccolo plays Gary Motif compressed into a descending 3-note wheeze (G–E–C, quarter tempo, staccato, ending on a flat smear downward). Tuba (implemented as low `Tone.Synth` with "sawtooth", very low register) plays a single "waaah" descent underneath the piccolo. Fades to silence in 2 seconds. |
| **Level Complete** | Brass stab on beat 1 (all synths, high velocity); full orchestra plays Gary Motif in augmentation (double speed, full volume, major key, no muting); timpani rolls continuously; strings play ascending scale run underneath; piccolo trills on top; total duration 8 bars, ends with a held high G with reverb tail. |
| **Start Screen** | Same as Normal Swim loop but: lower volume (−8dB), strings only + French horn plays Gary Motif once slowly (half tempo), then a 4-bar solo horn version of the motif, then strings join. No percussion. Loops quietly. Creates anticipation without fatigue. |

---

### Sound Effects

Each SFX is triggered, implemented in Tone.js, and justified for Gary's character:

**1. Gary Swims (Looping Ambient)**
- **Trigger:** Continuous while Gary is alive and in a lane
- **Tone.js:** `Tone.Player` with looping audio buffer of water rush noise (white noise shaped with LP filter at 800Hz, gentle LFO at 0.3Hz on filter cutoff ±100Hz for organic movement). Layer a second quiet `NoiseSynth` with shorter envelope bursting every 0.4s (fin-stroke rhythm)
- **Why:** Gary is always fighting the current; the ambient water never stops. The fin-stroke rhythm makes you feel his effort even when nothing dramatic is happening.

**2. Lane Switch — Gary's Tail Flap**
- **Trigger:** On tap left or tap right, at the moment of directional input
- **Tone.js:** `Tone.Synth` oscillator "sine", quick pitch sweep from 400Hz→200Hz, envelope attack 0.01s / decay 0.12s / sustain 0 / release 0.05s. Add a subtle "slap" transient: `NoiseSynth` burst (1ms attack, 0.06s decay, band-pass filter at 600Hz)
- **Why:** The thwack of a fish tail slapping water. Satisfying, physical, and slightly comedic — it sounds like Gary is throwing himself sideways, which he is.

**3. Rock Dodge — Near Miss**
- **Trigger:** When Gary passes within one body-length of a boulder without hitting it
- **Tone.js:** `Tone.Synth` "sawtooth", fast pitch drop 800Hz→300Hz in 80ms, short envelope. Wet reverb (room size 0.2). Volume: quiet — this is a whisper, not a shout.
- **Why:** The stone-on-water proximity sound. Close enough to make your stomach drop, not dramatic enough to distract. Gary doesn't celebrate near-misses. He just keeps swimming.

**4. Bear Paw SLAM — Missed By Inches**
- **Trigger:** Bear paw swipe animation completes within Gary's lane (Gary dodged in time)
- **Tone.js:** Two-layer hit: (a) `Tone.MembraneSynth`, very low pitch (80Hz→40Hz), long decay (0.8s), high volume — the water impact. (b) `NoiseSynth`, burst (white noise, BP filter 200–400Hz, 0.3s envelope) — the splash. Hard-pan slightly right (bear is right side). The camera push-in at 80ms happens on this exact beat.
- **Why:** The SLAM should be physically present — you feel it in your chest. The bear is not messing around. Neither is the sound design.

**5. Fishing Line Snap**
- **Trigger:** When Gary successfully ducks under a fishing line (Level 4+)
- **Tone.js:** `Tone.Synth` "sine", very high frequency 2000Hz, instant attack, fast exponential decay (0.08s). A second quieter note at 1800Hz, offset by 15ms, with slight pitch wobble (LFO 40Hz ±50Hz) — the shimmer of monofilament under tension.
- **Why:** Fishing line has a unique tense-wire quality. The shimmer sells that Gary is close enough to hear the line vibrate. It's a small, precise sound for a small, precise dodge.

**6. Waterfall Charge — Building Rush**
- **Trigger:** Continuous during hold input, from 0ms to 1200ms
- **Tone.js:** `Tone.Player` or filtered `NoiseSynth` (white noise, HP filter starting at 2000Hz, sweeping DOWN to 200Hz over 1200ms as charge builds — counter-intuitively, the low rumble coming in is what makes it feel powerful). Volume rises 0% → 85% linearly. The timpani roll in the music mirrors this perfectly.
- **Why:** The approach to a waterfall sounds like a jet engine powering up from a distance. The low frequency building in as Gary charges makes the eventual leap feel inevitable.

**7. Waterfall Leap — Gary Goes Airborne**
- **Trigger:** On release of hold after minimum 300ms charge
- **Tone.js:** Layer 1: `Tone.Synth` "sine" sweep 200Hz→1200Hz over 400ms (Gary's upward arc). Layer 2: `NoiseSynth` burst (pink noise, 0.3s decay — the splash of takeoff). Layer 3: For a PERFECT LEAP (800–1000ms charge): add a high shimmer, `Tone.Synth` "triangle", 1800Hz, sustained 0.6s with slow fade — Gary hanging in the air.
- **Why:** The leap needs to feel heroic. The upward pitch sweep is Gary's arc visualized in sound. The shimmer on a perfect leap rewards precision with a musical "yes."

**8. Gary Gets Hit / Dies**
- **Trigger:** On collision with any obstacle (each hit), and on third hit (death)
- **Hit (1 or 2 HP remaining):** `Tone.Synth` "sawtooth", 300Hz, fast attack, short decay (0.2s), then immediately `NoiseSynth` short burst — a thud and a gurgle. Gary flashes red. Music continues.
- **Death (3rd hit):** All music cuts (see dynamic table). `Tone.Synth` descending pitch sweep 500Hz→80Hz over 0.8s, slightly detuned, with `Tone.Reverb` (decay 2s) — Gary's final, dignified glub. Then piccolo death wheeze. Then silence. Gary sinks briefly before the restart screen appears.
- **Why:** The hit sound is immediate and unambiguous — you felt it. The death sound gives Gary a proper, slightly tragic exit. He deserves it.

---

## MECHANIC SPEC

**Core Loop:** Tap left/right to survive obstacles; hold to charge waterfall leaps; reach the spawning grounds upstream.

---

### 3-Lane System

- **Lane Width:** Equal thirds of playfield width. At 1920px canvas: each lane is 640px wide. At mobile (390px canvas): each lane is 130px wide.
- **Lane Visual Markers:** Three "current channels" separated by two thin foam-line ripples — a light horizontal streak of `#7EC49A` at 20% opacity, 4px wide, animated to flow right-to-left. Not a grid. Not hard lines. Just the suggestion of a channel.
- **Lane Switch Speed:** 180ms animated transition — Gary slides laterally with a slight body lean (12° banking toward direction of travel) and one strong tail stroke.
- **Lane Switch Feel:** Animated, not instant. Input is registered immediately (no input lag), but Gary takes 180ms to arrive. You can queue the next switch while one is in progress; the second executes immediately when the first completes. No sliding through multiple lanes — one tap = one lane only.

---

### Controls

**Tap Left:** Switch one lane left. If already in leftmost lane: nothing (a small tail-wiggle animation, no cost).
**Tap Right:** Switch one lane right. If already in rightmost lane: nothing (same wiggle).
**Hold (any finger, anywhere):** Charges waterfall leap.
- **Minimum hold:** 300ms — below this, Gary makes an aborted lunge (small jump animation, loses 0.5 seconds of forward progress, lands back in same lane — no damage but wastes time)
- **Optimal window:** 800ms–1000ms — PERFECT LEAP. Gary clears the waterfall with a graceful arc; +500 score bonus; airborne shimmer SFX plays.
- **Maximum hold:** 1200ms — Gary has been holding too long; he releases automatically with a startled animation (eyes wide, flops slightly to one side) — still clears the waterfall but with a chaotic "belly flop" animation and a comedic splat sound on landing. No damage, but it looks undignified.
- **Charge Indicator:** A small semicircular meter under Gary, `#F0A500` (amber), fills clockwise. At optimal window it turns `#7EC49A` (green). At over-charge it flashes.

---

### Obstacles

**Boulder:**
- Appears in all 3 lanes, distributed randomly
- Minimum 1 lane always clear at any boulder spawn
- Size: fills ~40% of lane width, protrudes 30% above waterline (visible rocks, not submerged)
- Spawn rate: See difficulty table
- Boulder clusters (2 boulders same row, 2 different lanes): unlocked at Level 2+
- Boulder slides: 3+ boulders in staggered offset rows: unlocked at Level 4+
- Visual telegraph: A slight "upstream ripple" appears 0.8 seconds before the boulder enters the visible play area — white foam V-shape pointing upstream from the rock's future position

**Bear Paw:**
- Single bear paw swipes across 1–2 lanes from the right side
- Telegraph: Bear roars (animation + sound) 1.2 seconds before paw strikes. A large dark shadow precedes the paw by 0.3 seconds (amber warning glow on shadow edge).
- Animation: Paw enters from right edge, sweeps left across target lane(s) in 0.4 seconds, retracts in 0.3 seconds.
- After swipe: 2.5-second cooldown before next paw (bear is resetting)
- Lane targeting: Paw targets the lane Gary is currently occupying at the moment of the roar. If Gary moves after the roar, the paw still hits the original lane — dodgeable by switching at any point during the 1.2-second window.
- Paw hits 1 lane (Level 3), can extend to 2 adjacent lanes (Level 4+)

**Fishing Line:**
- Appears as a near-invisible monofilament stretched horizontally across 2 of the 3 lanes simultaneously, at mid-body height (crosses Gary at his dorsal fin line)
- A small lure/spinner dangles from the line — `#E8C84A` yellow, gently oscillating — this is the only visible marker of the line's position
- **Dodge mechanic:** Gary must be in the clear lane. There is always exactly 1 safe lane per fishing line obstacle.
- The lure oscillates slowly (±15px, 1.2s period) — the safe lane is always on the side *without* the lure overhang
- Spawn rate: Level 4+. At Level 5, two fishing lines can appear in sequence with a 1.8-second gap.
- Visual telegraph: A faint glint of `#D4D0C8` shimmer appears at screen right edge 1.0 seconds before the line crosses the play area

---

### Waterfall Events

- **Frequency:** Every 180–240 meters of river distance (randomized within that range). First waterfall: always at 240m (giving player time to learn). Level 5: waterfalls every 140–180m (waterfall gauntlet).
- **Telegraph:** 3 seconds before the waterfall edge appears, water surface particles begin flowing downward (a visual river "drain" effect). A low rumble sound begins. At 1.5 seconds out, a mist line appears at the right side of the screen, growing. Camera pulls back very slightly (1.0 → 0.97 scale over 1.5 seconds — barely perceptible).
- **The Waterfall Edge:** A horizontal ledge across the full play width. Gary must leap it or die (instant death — no HP — waterfalls are not survivable without a leap).
- **Clearing Time:** Gary must be fully airborne when passing the edge. The leap window (when Gary is above ledge height) lasts approximately 0.8 seconds. If the leap is not charged enough, Gary hits the top of the falls and is swept back — treated as an obstacle hit (loses 1 HP, position resets 20m back).
- **Post-leap:** Gary lands with a splash animation (3-frame impact, brief deceleration). Normal gameplay resumes.

---

### Difficulty Per Level

| Level | Scroll Speed (px/s at 1920px canvas) | Boulder Spawn Rate | Bear Paw Active | Fishing Lines | Notes |
|---|---|---|---|---|---|
| 1 | 280 | 1 boulder every 3.5s | No | No | One boulder at a time; always 2 clear lanes |
| 2 | 320 | 1 boulder every 2.8s; clusters from 60s | No | No | Introduce clusters; slightly tighter windows |
| 3 | 360 | 1 boulder every 2.2s; clusters common | Yes (1 lane swipe) | No | Bear appears at right edge always; paw frequency: 1 per 8s |
| 4 | 400 | 1 boulder every 1.8s | Yes (1–2 lane swipe) | Yes (1 lane, 1 per 12s) | Bear paw can hit 2 lanes; fishing lines begin |
| 5 | 460 | 1 boulder every 1.4s; slides common | Yes (2 lane swipe) | Yes (1 per 8s, pairs possible) | Waterfall gauntlet; bear and fishing lines overlap; final 30s obstacle density spikes |

---

### Win / Lose Conditions

**Win:** Reach the spawning grounds (end of Level 5). A specific visual event: the river narrows into a shallow gravel bed, the music swells, Gary reaches a pool of salmon. Cutscene: Gary arrives. He looks at the camera. He nods once, slightly out of breath. End.

**Lose:** 3 HP system (three red salmon-heart icons in HUD). Each obstacle hit: −1 HP, brief invincibility window of 1.2 seconds. Waterfalls: instant death regardless of HP (swept away). At 0 HP: die animation, restart from beginning of current level.

**Restart:** No shame. One button. The piccolo death wheeze plays, screen fades, the start screen reappears with Gary swimming in place. No lengthy death screens. Gary doesn't brood.

---

### Scoring

| Event | Points |
|---|---|
| Per meter traveled | +1 point |
| Obstacle dodged (boulder) | +10 |
| Bear paw evaded | +25 |
| Fishing line cleared | +20 |
| Waterfall cleared (any) | +100 |
| Waterfall PERFECT LEAP (800–1000ms) | +500 (replaces the +100) |
| Level completed | +1000 bonus |
| Full run with no deaths | +5000 end bonus |

Score displays in top-right corner. No combo multiplier (Gary is not a combo type of fish). At level complete: score tallied with each event type itemized briefly on screen.

---

## LEVEL DESIGN

### Level 1: The Shallows (Intro)
**Name:** "First Current"
**Distance:** 800m
**Vibe:** A gentle introduction. The river is wide, the water is relatively calm, the light is warm. A tutorial moment, but never condescending — just a river that is slightly less hostile than the ones ahead.
**Obstacles:** Boulders only. One at a time. Always 2 of 3 lanes clear. Spawn rate: 1 per 3.5 seconds.
**Introduction:** First 15 seconds: zero obstacles. The river scrolls, Gary swims, the music begins. The player has time to feel the rhythm before anything demands a reaction. First boulder appears at 15 seconds, dead center lane (middle) — easiest possible dodge in either direction.
**Waterfall:** One waterfall at 600m. Very telegraphed. Post-waterfall, a brief calm stretch (10 seconds, no obstacles) before Level 1 ends.
**Gary Note:** Gary's swimming animation at this stage is slightly tentative — pectoral fins moving rapidly, eyes wide. He knows this is going to get harder.

---

### Level 2: Rocky Rapids
**Name:** "The Narrows"
**Distance:** 900m
**Vibe:** The river narrows. Water moves faster. Boulders appear in pairs (2 different lanes simultaneously), forcing commitment to the one clear lane. The forest walls close in on both sides.
**New Obstacle:** Boulder Clusters — two boulders in adjacent lanes, requiring Gary to be in the third lane. They telegraph with two upstream ripples appearing simultaneously.
**Obstacles:** Boulders (solo + clusters). Cluster frequency: 1 per 6 seconds from 30 seconds in.
**Waterfalls:** Two waterfalls (at 400m and 750m). Second waterfall arrives with shorter telegraph (2.5 seconds instead of 3).
**Scroll Speed:** 320px/s
**Gary Note:** By mid-Level 2, Gary's animation shifts — his strokes are stronger, more confident. He's getting into his rhythm.

---

### Level 3: The Bear
**Name:** "Grizzly Bend"
**Distance:** 950m
**Vibe:** The bear. The grizzly has been waiting at a bend in the river where salmon run thick. He is patient. He is large. He is not interested in being dramatic about it.
**New Obstacle:** Bear paw. The roar animation plays for the first time — the entire background momentarily darkens as the bear's shadow falls. The paw sweeps one lane. Players who switch quickly survive. Players who freeze do not.
**First Bear Encounter:** At 200m into the level. One paw, targeting the center lane (where Gary likely is). Generous 1.2-second window. After the miss, the bear looks at Gary. Gary does not look at the bear.
**Obstacles:** Boulders (solo + clusters) + bear paw (every 8 seconds, 1 lane)
**Waterfalls:** Two waterfalls.
**Scroll Speed:** 360px/s
**Gary Note:** The music shifts to the near-bear danger state on first roar. When Gary survives the paw swipe, the music returns to the full arrangement, and the horn plays the Gary Motif — a little triumphant pat on the back.

---

### Level 4: Fisherman Doug
**Name:** "The Bridge Pool"
**Distance:** 1000m
**Vibe:** An old wooden bridge crosses the river overhead (visible in the background — a dark horizontal silhouette). Fisherman Doug stands on it, dropping lines. Doug is unseen except for his boots and fishing rod tip visible at the top of the screen. The lines appear. They shimmer.
**New Obstacle:** Fishing lines — monofilament stretched across 2 lanes, only 1 safe lane, identified by the position of the dangling lure. Lines move slowly downstream as Gary approaches, requiring mid-approach course correction.
**Obstacles:** Boulders + bear paw (can now hit 2 lanes) + fishing lines (1 per 12 seconds)
**Combined Threat:** From 600m: a boulder cluster can appear immediately followed by a fishing line 1.8 seconds later — no rest.
**Waterfalls:** Three waterfalls.
**Scroll Speed:** 400px/s
**Gary Note:** The first time a fishing line appears, it should feel genuinely alarming — that shimmer, so thin, so easy to miss. Then Gary passes below it and you feel the fishing line snap SFX and exhale.

---

### Level 5: The Great Falls
**Name:** "The Great Falls"
**Distance:** 1100m
**Vibe:** The river rises toward its headwaters. The landscape changes: more exposed rock, lower forest, mist hanging everywhere. The river is fastest here. The falls are tallest here. Everything comes at once.
**Waterfall Gauntlet:** Waterfalls every 140–180m (5–6 total). This is the entire level's identity. Everything else — boulders, bear, fishing lines — is pressure between waterfalls.
**Obstacle Density:** Peaks at 70% of the level. From 800m: 10 seconds of continuous obstacle field (boulders + lines + bear paw simultaneously active, overlapping threat windows). This is the gauntlet.
**Final 50m:** A single clear run — no obstacles. Just Gary swimming. The river calms. The music holds on the dominant chord. Then the gravel shallows appear. The music resolves to the major tonic and the Gary Motif plays one final time, slowly, in full ensemble. Gary stops swimming. He has arrived.
**Scroll Speed:** 460px/s

---

## THE MOMENT

It is Level 3, at the first bear encounter. Gary is in the middle lane. The roar sounds — the background darkens, the danger music kicks in, a massive shadow crosses the screen. Gary has 1.2 seconds. The player (slightly panicked) taps right — Gary's tail slaps and he slides into the right lane at the exact moment the paw crashes down into the middle lane, sending a wall of water splashing up. The camera push-in fires (80ms, 1.04 zoom). The bear misses by maybe 15 pixels of margin. The music crashes back into the full arrangement, the French horn plays the Gary Motif — and Gary, without even glancing at the bear, keeps swimming upstream. He doesn't have time for this. He has a spawning ground to reach.

This is the moment. A small, slightly derpy salmon nearly killed by a grizzly bear, saved by your reflexes, celebrated by an orchestra.

---

## EMOTIONAL ARC

**First 30 seconds:**
The music begins quietly on the title screen. Gary appears, swimming in place, straining. Something about the sincerity of it — the little fish against the current — makes you feel a pull. You tap start. The current rushes. The first boulder appears in the center lane. You dodge it. The horn plays a small motif. *Oh*, you think. *This is charming.*

**After 2 minutes:**
You are in Level 2 or early Level 3. You have died once or twice — always instantly restarted, no bitterness. The music has lodged itself in your brain. You're anticipating the boulder clusters now. The rhythm of the game has become muscle memory. You notice Gary's animation — the way his fins move, the slight lean when he switches lanes. You are invested in this fish.

**Near the Win:**
Level 5. The waterfall gauntlet has beaten you twice. On the third attempt you string together three perfect leaps and the music swells each time. The final 50 meters has no obstacles. Gary is swimming, the river is calm, and you realize — you're going to make it. Not Gary. *You.* The Gary Motif swells in full ensemble. Gary arrives at the gravel shallows. He nods at the camera. You feel something. Maybe you feel everything, for a fish.

---

## IDENTITY IN ONE LINE

"This is the game where you play a completely ordinary salmon who will absolutely not give up, and the orchestra agrees."

---

## START SCREEN

### Gary's Idle Animation

Gary swims in place at the center of the screen, positioned at 28% from left edge, vertically centered. The river background scrolls right-to-left at 60% of normal gameplay speed.

**Gary's Motion Parameters:**
- Body S-curve: 12 frames, loops continuously, peak tail angle ±22°, head movement ±4° opposite phase
- Pectoral fins: cycle at 8 frames, independent of tail
- Slight vertical oscillation: Gary bobs ±6px on a 2.2-second sine cycle (current fighting)
- Expression: forward-facing, determined. Eyes slightly narrowed.

**The Boulder:**
- A single boulder appears at the right edge (80% of screen width) and scrolls left toward Gary
- Scroll speed: 1.2× background scroll speed
- Boulder reaches Gary's X position at approximately 4 seconds
- When it reaches Gary: instead of a collision, Gary "phases through" it (boulder slides behind Gary's sprite layer) and the boulder continues to the left edge and vanishes
- After vanishing: a new boulder spawns at the right edge. Loop is seamless.
- Boulder never triggers any collision logic or sound effects on the start screen — purely visual

**The Bear:**
- Grizzly silhouette stands at the far right of the screen, knee-deep in water, at 88% of screen width
- At rest: a gentle weight-shift animation — bear rocks slightly left–right on a 3.5-second cycle, 4° total lean. Both parameters: cycle period 3.5s, peak angle ±2° from center, ease-in-out.
- Every 8 seconds: the bear turns its head toward the camera (20° head rotation toward viewer, 0.4-second ease-in, holds 1.2 seconds, returns over 0.4 seconds). The bear's eye (a small, dark, square shape) makes eye contact with the player.
- The bear never roars, never swipes, never moves from position on the start screen. It just... watches.

---

### SVG Overlay

**Option A — Glowing Title (Required)**

Text: **SALMON RUN**

- **Font:** All-caps, serif with slightly compressed letterforms — think *National Geographic* meets adventure movie poster. Weight: Bold/Black. Tracking: +0.08em (slightly spaced). Approximate: Playfair Display Black, or Libre Baskerville Bold at 120% tracking.
- **Color:** `#F5EDD6` (warm parchment) base fill
- **Glow:** Two-layer SVG `<feGaussianBlur>` filter composite:
  - Inner glow: blur stdDeviation 3, `#F0A500` (amber), opacity 0.9 — sits tight to letterforms
  - Outer glow: blur stdDeviation 12, `#3D7A52` (river green), opacity 0.5 — diffuse ambient light from the water below
- **Animation:** The title breathes. CSS `opacity` animates on the outer glow layer: 0.3 → 0.6 → 0.3, period 3 seconds, ease-in-out. The inner glow pulses on a slightly different period: 2.4 seconds. The two pulses drift in and out of phase, creating a living shimmer that suggests water-reflected light.
- **Position:** Horizontally centered, vertically at 22% from top.
- **Tagline below:** *"He Was Not Built For This. He Will Do It Anyway."* — same font, weight Regular, `#F5EDD6` at 70% opacity, no glow, tracking +0.12em. Positioned at 32% from top.

**Option B — Salmon Silhouette Icon (SVG, 6 Primitives, above title)**

A simplified salmon head-and-body silhouette in deep red `#C0392B`, positioned at 14% from top, centered.

```svg
<g id="gary-icon" fill="#C0392B">
  <!-- Body: elongated ellipse, slightly asymmetric -->
  <ellipse cx="50" cy="40" rx="38" ry="14" />
  <!-- Head bump: smaller ellipse at left -->
  <ellipse cx="16" cy="38" rx="12" ry="10" />
  <!-- Kype jaw: small rotated rect at far left -->
  <rect x="4" y="41" width="10" height="5" rx="2" transform="rotate(-8, 9, 43)" />
  <!-- Tail: forked path at right -->
  <path d="M 85 32 L 100 22 L 96 40 L 100 58 L 85 48 Z" />
  <!-- Dorsal fin: small triangle on top -->
  <polygon points="45,26 55,26 50,18" />
  <!-- Eye: small circle, dark -->
  <circle cx="20" cy="36" r="3" fill="#2C1A0E" />
</g>
```

The icon scales to approximately 80px wide on mobile, 100px on desktop. It casts a very faint drop shadow (SVG `feDropShadow`, dx=0, dy=2, stdDeviation=3, color `#1C3520`, opacity 0.4).

---

## SUMMARY QUICK-REF

| Parameter | Value |
|---|---|
| Canvas background | `#3D7A52` |
| Gary body | `#C0392B` |
| Gary belly | `#E8B4A0` |
| Rock base | `#5C5248` |
| BPM | 132 |
| Bar / loop length | 4/4 / 16 bars |
| Lane width | Equal thirds (640px @ 1920px) |
| Lane switch time | 180ms animated |
| Charge minimum | 300ms |
| Charge optimal | 800–1000ms |
| Charge maximum | 1200ms |
| Bloom strength | 0.4 |
| Bloom threshold | 0.72 |
| Gary HP | 3 |
| Levels | 5 |
| Core loop | Tap to dodge, hold to leap |

END_DESIGN_DOC
