

# Plan


### Level of Skill
 - How much do I really know about Godot?
   - I Barely understand the physics and general workflow
 - What do I want to know?
   - C# Binds?
   - Scene Management?
   - Physics?
 - What interests me?
   - Godot - Recursive Environments reminescent of Plan9
   - Haskell - Domain Specific Languages and Functional Programming
   - Wave Function Collapse - Procedural Generation and AI


### Areas of Consideration
 - Files
   - How to Organize resources within Folders?
 - Scenes
   - How to Organize elements within a Scene?
 - Scripts
   - How to Organize/Separate functions/functionalities?
 - Naming Conventions
   - Projects - executable, metadata
   - Folders - `Misc` or `misc` or `MISCELLANIOUS`?
   - Files - `a_file` or `AFile` or `aFile` or `a_file` or `a file`?
   - Functions - `_a_func` or `a_func` or `aFunc` or `AFunc`?
   - Variables - _see above_
 - Documentation
   - On Git
     - Wiki?
   - On Site
     - Jekyll + Markdown?
   - In Script
     - Comments?
     - Names?
   - In Editor
     - Fields?
   - In Game
     - Popups/Tooltips?
     - Indications?
 - Programming
   - Single File
   - Object Oriented
   - Component
   - Signalled
   - Actor/Agent
   - By Input
   - By Layer
   - Functional
   - Test Driven
 - Language
   - GDScript
   - C#
   - F#
   - Haskell


### Single File
 - Nasty, Fast
 - Gets all the functionality down quick

### Object Oriented
 - Dedicated File for Each "Verb"
   - "Ship" has "Controls", "Thrusters", and "Settings"

### Component
 - Dedicated Instances for each "Thing"
   - "Up" Thruster, "Down" Thruster, "Steering" Controls, "Power" Generator, "Up" Input, "Down" Input
   - Allows individual items to fail

### Layer
 - View each thing as occupying a layer, from Human -> Interface -> Game World -> Ship -> Thrusters -> Script -> Silicon
   - "WorldInput" Layer - `*`
   - "ShipInput" Layer - `wasdqe^_`
   - "ThrusterInput" Layer - `on`/`off`

### Functional
 - `MoveShip()` accepts a `Vector3` and generates a `void` (calls the physics system)
 - `DecodeInput()` accepts a `KeyStroke` and generates a `Vector3`

### Test Driven
 - Write a simple test for each and every function
   - Both in script and in game
 - Write tests for tests
 - Write full integration tests
 - Write test generators


## True Complexity
 - Moving a ship around is fine and all, but the true trouble comes from all the _side effects_
 - Consider, a real airplane, and just the _noise_:
   - Pilot Breathing
   - Button Flicking
   - Wind Rushing
   - Metal Creaking
   - Computer Chirping
   - Hydraulics Flowing
   - Engines Whining
   - Rockets Firing
 - How do we coordinate and control these sounds?
 - There are all manner of other effects as well, such as:
   - Lighting
     - Display
     - Weapons
     - Thrusters
   - AI Messaging
     - Environment
     - Enemies
     - Ship
   - Physics
     - Backblast
     - Inertia
   - Radar Messaging
   - HUD Messaging
 - How do we group all these effects together?
 - How do we control these effects through game rules?
   - Eg, suppose only low velocity thrusters can be used in the fuel depot
     - How do we decribe this rule?
     - Feedback?
     - etc?
 - And more importantly, how does each paradigm address talking about these effects?
   - OOP: "Effects" Object
   - FUNC: "Effects" Datatype and Transformers
   - LAYER: "Effects" Layer
 - Now, how do we handle different effects firing at different times?
   - How do we handle some effects interrupting other effects?
   - What about effects calling _other_ effects?
   - How do we mediate these interactions?
