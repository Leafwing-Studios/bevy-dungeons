# Global Metadata

## Constraints
- [required] Can be imported as a barebones library for use in other bevy projects (this library contains just the generation logic)
- [required] Has an associated executable that you can run on your local machine to generate maps without any additional code
- [required] User can choose square or hex grid for generation
- [required] Supports "gutter walls", where the walls are on the edges instead of the grid spaces
- [required] Use bevy as a dependency
- [required] Users can set size of dungeon and "connectivity"
- [required] Individual features (to be generated in the dungeon) can be toggled on/off by the user
- [various] Dungeons will be generated with the following features
  - [required] Walls/floors
  - [required] Passageways and rooms (not distinguished programmatically, but has those emergent shapes)
  - [required] Doors
  - [expected] Stairs + multiple levels
  - [expected] Locks and Keys
  - [expected] Warp points
  - [desired] Traps
  - [desired] Room fluff descriptions
  - [desired] Terrain at different heights using height tiers
  - [desired] Loot
  - [desired] Encounters (going from "there is an encounter here" to "these specific monsters")
- [expected] Semantic and stylistic elements of the final dungeon should be decoupled
  - Modular stylistic elements (swap out styles easily for a dungeon)
- [expected] Leverages bevy tilemap library
- [desired] Users can swap out different high level "layout algorithms" easily (ex: locks and keys generation, evolutionary generation)
- [desired] Can add in extra "modules" that provide additional generator functionality (ex: plot, loot generation, etc.)
- [desired] Users can pass in criteria for acceptable dungeons through some API. The system will generate dungeons that fit within (start with rejection sampling)

## Tolerances
- Does not need to be efficient
- Exact file formats are flexible
- Need not be compatible with other systems

## Uncertainties
- How should we decouple semantics and stylistic elements?