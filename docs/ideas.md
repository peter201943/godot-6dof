

# Ideas


## Folder Management
```
RES://
├── Misc        # `*` messy/loose files -- too few to categorize
├── Class       # `cs` with HEAVY reuse
├── Place       # `tscn` with `Person` and `Item` instances
├── Item        # `tscn` with effects, carried by `Person`
├── Person      # `tscn` with narrative, inventory, ai
├── Sound       # `ogg` for short listening
├── Music       # `ogg` for long listening
├── Texture     # `png` 
├── Model       # `dae` 
├── Animation   # `gltf` 
└── Resource    # `tres` with HEAVY reuse -- fonts, for example
```

### Why not subfolder?
 - (why flat?)
 - Easier to navigate
 - Emphasis is _not_ on finding files via the file explorer, but instead through the _scenes_ (`tscn`)
 - The scenes are multimedia objects, and as such should be the _only_ occurrence of organization according to topic, as opposed to matter
 - Example:
   - **1:**
     - File: "charles_day.uv.png"
     - Topic: "Charles"
     - Matter: "Texture"
   - **2:**
     - File: "charles_walk.gltf"
     - Topic: "Charles"
     - Matter: "Animation"
   - **3:**
     - File: "train_1.gltf"
     - Topic: "Train"
     - Matter: "Animation"
 - The idea is, that instead of grouping "Charles"'s files together, we keep them with all the other files of the same _matter_.
 - There would then exist some "Charles" _scene_, where all his resources are gathered together
   - Even if the resources are not active at all times, eg, a day/night costume - we still put this on his _object_ rather than on his _folder_.


## Further
 - [Godot Best Practices](https://docs.godotengine.org/en/stable/getting_started/workflow/best_practices/index.html)