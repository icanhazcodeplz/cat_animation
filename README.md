# Blender Animation Project: Cat Showdown

**Goal:** Two cats walk towards each other on a sidewalk, glare at each other, and one pulls out a rocket launcher.

---

## Week 1: Blender & Python Fundamentals

**Objectives:**
- Install Blender and get comfortable with the interface
- Learn navigation: orbiting, panning, zooming in the 3D viewport
- Understand objects, edit mode vs object mode, and basic transformations (grab, rotate, scale)
- Run your first Python script in Blender's scripting workspace (`bpy.ops.mesh.primitive_cube_add()`)

**Deliverable:** A simple scene with a few primitive shapes (cubes, spheres) arranged and colored using both the GUI and Python scripting.

**Blender Tutorials**
 - [Blender Donut Tutorial Part 1 (2026)](https://youtu.be/-tbSCMbJA6o?si=jO6r8BKQ5SBn6W_X)
 - [Beginner Python Exercise in Blender: Simple cube location animation](https://youtu.be/nmJqIaSZlRs?si=AWXLPIpg91sutQVL)
 - [Blender Python Tutorial : An Introduction to Scripting](https://www.youtube.com/watch?v=cyt0O7saU4Q)

**Python Tutorial**
 - [Codecademy Python 3](https://www.codecademy.com/learn/learn-python-3)
   - Get through "Hello World" section

---

## Week 2: Basic Modeling — The Cats

**Objectives:**
- Learn basic mesh modeling: extrude, loop cut, subdivide, mirror modifier
- Model a simple low-poly cat (body, head, ears, tail, legs) — keep it stylized and simple
- Duplicate and slightly modify the second cat so they look distinct (different proportions or ear shapes)

**Tips:**
- Start from a cube for the body, extrude the legs and head
- Use the mirror modifier to only model half the cat, then mirror it
- Don't worry about realism — a blocky/cute style is fine and much easier

**Deliverable:** Two distinct low-poly cat models saved in your .blend file.

---

## Week 3: Materials, Textures & the Sidewalk Scene

**Objectives:**
- Learn Blender's material system: base color, roughness, simple node setups
- Assign different materials/colors to each cat (e.g., orange tabby vs gray cat)
- Model the sidewalk background: a flat plane with sidewalk texture or procedural cracks
- Add basic lighting (sun lamp + ambient) and a simple camera angle

**Tips:**
- Use procedural textures (Noise + ColorRamp) for a concrete sidewalk look
- Add a subtle plane or boxes in the background for context (fence, wall, etc.)

**Deliverable:** A fully textured scene with both cats placed on the sidewalk, looking decent in a render.

---

## Week 4: Rigging — Making the Cats Move

**Objectives:**
- Learn armature basics: adding bones, parenting mesh to armature with automatic weights
- Create a simple rig for each cat: spine, legs (4), head, jaw, tail
- Test the rig by posing the cats in a few positions
- Introduction to inverse kinematics (IK) for the legs if comfortable

**Tips:**
- Keep the rig simple — 15-20 bones per cat is plenty
- Name your bones clearly (e.g., `front_leg_L`, `tail_01`, `head`)
- You can rig one cat and duplicate the armature for the second

**Deliverable:** Both cats rigged and poseable. Screenshot showing 2-3 test poses.

---

## Week 5: Animation Basics — The Walk Cycle

**Objectives:**
- Learn keyframe animation: inserting keyframes, using the timeline and dope sheet
- Create a walk cycle for the cats (4-8 keyframes looped)
- Animate both cats walking towards each other from opposite ends of the sidewalk
- Learn the Graph Editor for smoothing motion curves

**Tips:**
- Start with the body bobbing up and down, then add leg movement
- Use reference videos of cats walking
- Keep it to ~4 key poses: contact, down, passing, up

**Deliverable:** Both cats walking towards each other and stopping near the center of the sidewalk. ~3-5 seconds of animation.

---

## Week 6: Acting Animation — The Glare & Rocket Launcher

**Objectives:**
- Animate the "acting" sequence: cats stop, square up, and glare
- Model a simple rocket launcher (cylinder + cone + handle)
- Animate one cat reaching behind and pulling out the rocket launcher
- Use keyframe visibility or a separate collection to make the launcher "appear"

**Tips:**
- Exaggerate the glare: lean heads forward, squint eyes (scale eye bones), puff up the body slightly
- For the rocket launcher reveal, you can animate its scale from 0 to 1 or move it from behind the cat
- Hold the glare for 1-2 seconds before the reveal for comedic timing

**Deliverable:** Full animation sequence rough pass — walk, stop, glare, rocket launcher pull.

---

## Week 7: Polish, Camera Work & Python Automation

**Objectives:**
- Add camera movement: start wide, push in as cats approach, dramatic zoom on the rocket launcher
- Polish animation timing and spacing — adjust curves in the Graph Editor
- Write Python scripts to automate repetitive tasks:
  - Batch rename objects
  - Set up render settings programmatically
  - Auto-insert keyframes at intervals
- Add simple sound effects or markers for where audio would go

**Tips:**
- Use Blender's camera constraints (Track To) for smooth following shots
- A slight camera shake on the rocket launcher reveal adds impact
- Python example for render setup:
  ```python
  import bpy
  scene = bpy.context.scene
  scene.render.resolution_x = 1920
  scene.render.resolution_y = 1080
  scene.render.fps = 24
  scene.frame_start = 1
  scene.frame_end = 240
  ```

**Deliverable:** Polished animation with camera work. At least 2 Python scripts that automate parts of your workflow.

---

## Week 8: Final Render & Presentation

**Objectives:**
- Do a final review of the entire animation sequence
- Set up render settings: resolution (1080p), frame rate (24fps), output format (FFmpeg/MP4)
- Render the full animation (use Eevee for speed or Cycles for quality)
- Compile the final video, add titles or credits if desired
- Write a brief project summary: what you learned, challenges faced, what you'd improve

**Tips:**
- Do a low-resolution test render first to catch issues
- Eevee renders much faster than Cycles and looks great for stylized work
- If render times are long, consider reducing samples or using denoising

**Deliverable:** Final rendered MP4 animation (10-15 seconds), project summary document.

---

**Resources:**
- [Blender Fundamentals (official)](https://www.youtube.com/playlist?list=PLa1F2ddGya_-UvuAqHAksYnB0qL9yWDO6)
- [Blender Python API docs](https://docs.blender.org/api/current/)
- [Blender Guru — Beginner tutorials](https://www.youtube.com/@blenderguru)
- [Royal Skies LLC — Quick Blender tips](https://www.youtube.com/@RoyalSkiesLLC)
