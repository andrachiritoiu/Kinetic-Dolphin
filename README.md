# 🐬 Kinetic Dolphin

> A 3D-printed mechanical sculpture that simulates dolphin swimming using a cam-driven mechanism — no electronics, no motors, no code.

**100% Mechanical** · **4 Cam Offsets** · **PLA / PETG** · **Manual Crank** · **CAD & 3D Printing Final Project**

---

## Description

**Kinetic Dolphin** converts rotational motion into a smooth, sequential wave-like movement of a segmented dolphin body. The user turns a crank, which rotates a central shaft carrying four cams. Each cam is offset by 90°, causing body segments to move one after another — simulating natural swimming.

---

## How It Works

```
Turn the crank
      ↓
Central shaft rotates
      ↓
4 cams push followers at staggered moments
      ↓
Followers move vertically (up/down)
      ↓
Body segments rotate sequentially
      ↓
Wave-like swimming motion
```

---

## Project Goals

- Understand cam-based mechanisms
- Convert rotation into vertical follower motion
- Design articulated body segments
- Create parts suitable for 3D printing
- Assemble a functional mechanical system
- Test tolerances and clearances between printed parts

---

## Main Components

| Part | Qty | Role |
|------|-----|------|
| Crank handle | ×1 | Manual input — rotates the mechanism |
| Central shaft | ×1 | Transfers rotation to all cams |
| Cams | ×4 | Push followers at staggered moments |
| Followers | ×4 | Convert cam rotation into vertical motion |
| Body segments | ×4 | Move sequentially to create the swimming effect |
| Hinge pins (body) | ×3 | Connect segments while allowing rotation |
| Follower pins | ×4 | Connect each follower to its corresponding segment |
| Frame | ×1 | Supports and aligns the full mechanism |
| Base | ×1 | Provides stability for the entire assembly |

---

## Mechanical Design

### Body Segments

The dolphin body is divided into four articulated segments:

1. **Head / front body segment**
2. **Middle body segment 1**
3. **Middle body segment 2**
4. **Tail segment**

Segments are connected with hinge pins, allowing each section to rotate slightly relative to the next.

### Joint Types

| Connection | Joint Type |
|------------|------------|
| Frame to ground | Fixed / grounded |
| Central shaft to frame | Revolute joint |
| Cams to shaft | Rigid connection |
| Followers to frame | Slider joint (vertical only) |
| Segment to segment | Revolute joint (hinge pins) |
| Follower to segment | Revolute joint (follower pins) |
| Cam to follower | Contact surface |

---

## Cam Phase Offsets

Each cam is offset from the previous by 90°, creating a wave that travels from head to tail:

| Cam | Offset | Segment |
|-----|--------|---------|
| Cam 1 | 0° | Head |
| Cam 2 | 90° | Middle 1 |
| Cam 3 | 180° | Middle 2 |
| Cam 4 | 270° | Tail |

```
Cam 1:  0°  →  ●───
Cam 2: 90°  →  ───●
Cam 3: 180° →  ───●
Cam 4: 270° →  ●───
```

---

## Recommended Dimensions

| Element | Value |
|---------|-------|
| Hinge pin diameter | 2.0 mm |
| Hinge hole diameter | 2.4 mm |
| Follower pin diameter | 2.0 mm |
| Follower hole diameter | 2.4 mm |
| Clearance between moving parts | 0.3 – 0.6 mm |
| Space between body segments | 1 – 1.5 mm |
| Follower vertical travel | ~5 – 6 mm |
| Body segment rotation limit | ±12° to ±15° |

> **Note:** Holes are always 0.4 mm larger than pins to allow free movement after 3D printing.

---

## Design Decisions

### Segmented body
Split into 4 separate parts instead of one solid piece — enables the realistic bending motion that simulates swimming.

### Pin-based hinges
Simple, printable, and allows controlled rotation between adjacent segments without complex mechanisms.

### Cam & follower mechanism
Reliable transformation of rotational motion into vertical movement. Offsetting the cams makes the motion sequential rather than simultaneous.

### Individual followers
One follower per segment gives independent, precise control over each body section.

### Manual crank
Fully mechanical, easy to demonstrate, and requires no electronics or batteries.

---

## Implementation Challenges

### 1. Segment alignment
Keeping segments aligned while still allowing rotation. A long rod through the entire body was too rigid — individual hinge pins between segments was the solution.

### 2. Smooth wave motion
If all cams are aligned identically, all followers move at once and the dolphin doesn't appear to swim. Correct 90° offsets travel the motion from head to tail.

### 3. Follower guidance
Followers must move only vertically. Without proper guides they tilt and block movement. Each requires a vertical slider constraint.

### 4. 3D print tolerances
Multiple moving parts make tolerances critical. Holes at 2.4 mm for 2.0 mm pins — the 0.4 mm clearance allows free rotation after printing.

### 5. Avoiding rigid connections
Followers must not be fixed rigidly to body segments. Revolute joints via small pins let each segment rotate naturally through its range.

---

## Assembly Steps

1. Print the frame and base
2. Insert the central shaft through the frame
3. Attach all four cams to the shaft at correct angular offsets
4. Mount the crank handle on one end of the shaft
5. Add the four vertical followers above the cams
6. Assemble the dolphin body segments using hinge pins
7. Connect each follower to its corresponding segment via follower pins
8. Check that all moving parts rotate or slide freely
9. Turn the crank and observe the wave-like swimming motion

---

## Expected Motion

When the crank is turned:

```
Segment 1 (Head)   → moves first
Segment 2 (Mid 1)  → follows
Segment 3 (Mid 2)  → follows
Segment 4 (Tail)   → moves last
```

The result is a mechanical wave travelling through the dolphin body from head to tail.

---

## Materials & Tools

- PLA or PETG filament
- 3D printer
- CAD software
- Small metal or printed pins
- Sandpaper or file for cleaning holes
- Optional lubricant for smoother movement
- Optional metal rod for the central shaft

---

## Current Status

### Completed
- Main frame and base
- Central shaft
- Four cams
- Four followers
- Four dolphin body segments
- Hinge connections between body segments
- Follower-to-segment pin connections

### Next Steps
- [ ] Final tolerance checking
- [ ] Testing follower movement
- [ ] Adjusting cam positions
- [ ] Exporting parts for 3D printing
- [ ] Assembling and testing the physical model

---

## References

- [Save the Whales Kinetic Sculpture](https://www.youtube.com/watch?v=XO6ccPXwV70) — YouTube inspiration
- [Kinetic Whale](https://www.thingiverse.com/thing:3932765) — Thingiverse mechanism reference
- [Save the Whales](https://www.myminifactory.com/object/3d-print-save-the-whales-kinetic-whales-59557) — MyMiniFactory reference
- [Cam Mechanism Examples](https://www.printables.com/model/490289-cam-mechanism-examples) — Printables reference

---

## Pictures

> Final pictures of the printed and assembled mechanism will be added here.

```
images/dolphin.jpg
```

---

## Credits

Designed and built as a final project for the **CAD & 3D Printing** university course.
Inspired by kinetic animal sculptures and cam-driven mechanical models.
