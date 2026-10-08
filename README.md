# Cycling Race Portal

A Java back end for managing multi-stage cycling races. It handles races, stages,
checkpoints, teams and riders. It records checkpoint times and calculates results,
points and classifications.

> Built for the **ECM1410** object-oriented programming module at the University of Exeter
> (pair coursework, 2024). The module supplied the `CyclingPortal` / `MiniCyclingPortal`
> interfaces and exception classes. The implementation and domain model are ours.

## Features

- Create and remove races, stages (flat, medium mountain, high mountain, time trial) and checkpoints
  (intermediate sprints and categorised climbs)
- Manage teams and riders, and register each rider's checkpoint times per stage
- **Stage results:** rider rankings and adjusted elapsed times. Riders who finish within a
  second of the rider ahead are grouped together.
- **Points and mountain points** per stage, plus overall race totals
- **General, points and mountain classifications** across a whole race
- Save and load the whole portal with Java serialization

## Structure

| Path | Contents |
|---|---|
| `src/cycling/CyclingPortalImpl.java` | Portal implementation and all results and classification logic |
| `src/cycling/{Race,Stage,Checkpoint,Team,Rider}.java` | Domain model |
| `TestSystem/CyclingPortalTestApp.java` | Test harness that exercises the portal |
| `doc/` | Generated Javadoc |
| `res/` | UML class diagram and test checklist |

## Running

```bash
javac -d out src/cycling/*.java TestSystem/CyclingPortalTestApp.java
java -cp out CyclingPortalTestApp
```

## Team

Pair project by [Edward Pratt](https://github.com/Edward-Pratt) and
[CliffHanger201](https://github.com/CliffHanger201).
Edward wrote most of `CyclingPortalImpl`, including the results, points and classification
logic. CliffHanger201 wrote most of the domain classes.
