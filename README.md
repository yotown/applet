# Yo.Town 3D Works

Public 3D related files from Yo.Town.

This repository shares selected CAD examples, 3D printing models, source scripts, STEP files, STL files, 3MF files, GLB previews, screenshots, and mechanical animation demos.

The goal is simple:

> Show how product ideas can become real, inspectable, manufacturable 3D assets.

Yo.Town 3D Works is used as a public gallery and technical reference for Yo.Town / YoCAD experiments, maker projects, mechanical demos, and 3D printing workflows.

---

## What is included

This repository may include:

- CadQuery Python source files
- OpenSCAD source files
- STEP files for CAD handoff
- STL files for 3D printing
- 3MF files for 3D printing workflows
- GLB files for web preview
- screenshots and rendered previews
- short animation videos or GIFs
- Onshape import and assembly notes
- mechanical motion examples such as gears, hinges, sliders, grippers, clamps, and linkages

The repository is intended to be practical. Each example should be easy to inspect, download, test, import into CAD software, or use as a reference for future modeling work.

---

## What is not included

This repository does not include proprietary YoCAD engine internals.

Not included:

- YoCAD C++ CAD kernel implementation
- proprietary BRep algorithms
- proprietary provenance or traceback implementation
- private backend services
- private evaluation datasets
- private training or benchmarking infrastructure
- patent-sensitive internal implementation details

The public files here are examples, demos, and exported assets.

---

## Why this repository exists

Modern 3D creation needs more than mesh generation. Real product workflows often require:

- editable source logic
- parametric CAD scripts
- CAD-friendly STEP export
- 3D-printable STL or 3MF files
- web-friendly GLB previews
- mechanical assembly examples
- motion or animation demos
- clear design history and reproducibility

Yo.Town 3D Works is a place to share these outputs publicly.

For Yo.Town, this repository helps demonstrate a practical workflow:

```text
idea / sketch / script
        ↓
CAD source
        ↓
STEP / STL / 3MF / GLB
        ↓
preview / print / assembly / animation
```

---

## Repository structure

The structure may evolve, but the intended layout is:

```text
3dworks/
  README.md
  LICENSE

  cad/
    cadquery/
      geartrain/
      roboticgripper/
      foldablephone/
      toggleclamp/

    openscad/
      brackets/
      boxes/
      connectors/

    yocad/
      examples/
      generated/

  models/
    step/
    stl/
    3mf/
    glb/

  printing/
    testprints/
    slicerprofiles/
    photos/

  animations/
    geartrain/
    roboticgripper/
    foldablephone/
    toggleclamp/

  docs/
    formats.md
    onshape.md
    printing.md
    animation.md

  media/
    previews/
    screenshots/
    videos/
```

---

## File format guide

| Format | Use case |
|---|---|
| `.py` | CadQuery source script |
| `.scad` | OpenSCAD source script |
| `.step` / `.stp` | CAD handoff, Onshape, Fusion, SolidWorks, manufacturing workflows |
| `.stl` | common 3D printing mesh format |
| `.3mf` | modern 3D printing package format with richer print metadata |
| `.glb` | web preview, lightweight sharing, 3D viewers |
| `.png` / `.jpg` | screenshots and preview images |
| `.gif` / `.mp4` | animation preview and motion demo |

---

## Example categories

### 1. CAD source examples

These examples show how a model is created from code.

Typical contents:

```text
example.py
example.step
example.stl
preview.png
README.md
```

Useful for:

- learning CadQuery or OpenSCAD
- testing STEP export
- comparing generated geometry
- reproducing a model from source

---

### 2. Mechanical demos

Mechanical demos show moving or assembled structures.

Examples may include:

- gear train
- slider crank
- robotic gripper
- foldable phone stand
- toggle clamp
- hinge assembly
- linkage mechanism
- simple robot joint

Typical contents:

```text
source.py
parts/
  base.step
  gear1.step
  gear2.step
  arm.step
assembly.step
animation.mp4
preview.png
onshape.md
```

Useful for:

- CAD animation demos
- Onshape assembly testing
- motion visualization
- investor or product demo videos
- mechanical design education

---

### 3. 3D printing models

3D printing models are intended for print testing, maker workflows, and physical validation.

Typical contents:

```text
model.stl
model.3mf
preview.png
print_notes.md
photos/
```

Print notes may include:

- suggested material
- layer height
- support requirements
- print orientation
- scale
- known issues
- tested printer or slicer settings

---

### 4. Web preview assets

GLB assets are useful for browser-based previews and product pages.

Typical contents:

```text
model.glb
preview.png
source.step
README.md
```

Useful for:

- web viewers
- product pages
- maker.yotown.com previews
- lightweight sharing

---

## Recommended example folder format

Each public example should try to follow this structure:

```text
example-name/
  README.md
  source/
    model.py
    model.scad

  output/
    model.step
    model.stl
    model.3mf
    model.glb

  media/
    preview.png
    animation.mp4
    animation.gif

  docs/
    onshape.md
    print_notes.md
```

Not every example needs every file. A simple example may only include source code, one exported model, and one preview image.

---

## Suggested README for each example

Each example folder should include a short `README.md` with:

```markdown
# Example Name

Short description.

## Files

- `source/model.py`: source CAD script
- `output/model.step`: CAD exchange file
- `output/model.stl`: 3D printing mesh
- `output/model.glb`: web preview
- `media/preview.png`: screenshot

## How to use

1. Open the STEP file in Onshape, Fusion, SolidWorks, FreeCAD, or another CAD tool.
2. Open the STL or 3MF file in a slicer for 3D printing.
3. Open the GLB file in a web-based 3D viewer.
4. Review the source script to understand how the model was generated.

## Notes

Any limitations, print settings, or assembly instructions.
```

---

## Using the CadQuery examples

Many examples are written in CadQuery Python.

A typical script can be run with a local CadQuery environment:

```bash
python model.py
```

Depending on the script, it may export files such as:

```text
model.step
model.stl
model.glb
```

Some examples may be generated by YoCAD-compatible workflows and then exported to standard CAD or 3D printing formats.

---

## Using the STEP files

STEP files are intended for CAD handoff.

You can usually import them into:

- Onshape
- Fusion
- SolidWorks
- FreeCAD
- Rhino
- Siemens NX
- PTC Creo
- other CAD systems that support STEP import

For Onshape, a typical workflow is:

1. Create or open an Onshape document.
2. Upload the `.step` file.
3. Translate it into an Onshape Part Studio.
4. Insert parts into an Assembly if needed.
5. Add mates such as revolute, slider, fastened, or gear relations for motion demos.

Some mechanical examples include an `onshape.md` file with recommended assembly setup.

---

## Using STL and 3MF files

STL and 3MF files are intended for 3D printing workflows.

You can open them in slicers such as:

- Bambu Studio
- PrusaSlicer
- Cura
- OrcaSlicer
- Simplify3D

For best results, check the example-specific `print_notes.md` when available.

Important:

- STL files may not contain units or material settings.
- 3MF files may contain richer printing information depending on how they were exported.
- Always check scale before printing.
- Always inspect thin walls, overhangs, and small features before starting a long print.

---

## Using GLB files

GLB files are intended for web preview and lightweight sharing.

They can be used in:

- browser-based 3D viewers
- Three.js projects
- model preview pages
- maker.yotown.com style experiences
- product showcase pages

GLB files are not usually the best format for manufacturing. For CAD handoff, prefer STEP. For 3D printing, prefer STL or 3MF.

---

## Large files

Some 3D assets and videos can become large.

For files larger than normal GitHub-friendly sizes, use Git LFS:

```bash
git lfs install
git lfs track "*.step"
git lfs track "*.stp"
git lfs track "*.stl"
git lfs track "*.3mf"
git lfs track "*.glb"
git lfs track "*.mp4"
git add .gitattributes
```

Then commit files as usual.

---

## Naming conventions

Use lowercase folder names where possible.

Recommended:

```text
geartrain
roboticgripper
foldablephone
toggleclamp
slidercrank
phoneholder
bracket01
connector01
```

Avoid spaces in filenames.

Recommended file names:

```text
model.py
model.scad
model.step
model.stl
model.3mf
model.glb
preview.png
animation.mp4
print_notes.md
onshape.md
```

---

## Quality guidelines

Before publishing an example, try to include:

- source file if available
- at least one exported 3D format
- one preview image
- short description
- clear units
- print or assembly notes if relevant

For mechanical examples, try to include:

- separate STEP parts
- assembly notes
- animation preview
- motion description
- mate recommendations if using Onshape

For 3D printing examples, try to include:

- STL or 3MF
- print orientation notes
- support notes
- tested or recommended material
- photo of physical print if available

---

## Current focus

The current focus of this repository is:

- public CAD examples
- YoCAD-generated or YoCAD-compatible demos
- CadQuery and OpenSCAD source examples
- STEP export tests
- 3D printing assets
- mechanical motion demos
- public proof-of-work for idea-to-model workflows

---

## About YoCAD

YoCAD is a Yo.Town project exploring script-based and AI-assisted CAD workflows.

The long-term direction is to make generated CAD more editable, traceable, and manufacturable.

Public examples in this repository may demonstrate:

- source-driven CAD generation
- parametric modeling
- CAD-to-STEP workflows
- 3D printing handoff
- assembly and motion demos
- mechanical concept visualization

Try YoCAD:

```text
https://maker.yotown.com
```

---

## About Yo.Town

Yo.Town builds tools and workflows for 3D creation, CAD, manufacturing, 3D printing, and maker commerce.

Yo.Town 3D Works is one public place where we share selected 3D results, demos, and files.

Website:

```text
https://maker.yotown.com
```

---

## License

Unless otherwise noted, source code in this repository is provided under the MIT License.

3D model files, images, videos, and exported assets are provided for learning, testing, demonstration, and reference use.

Please check individual example folders for any additional license notes.

---

## Disclaimer

Files in this repository are provided as-is.

Before using any model for production, manufacturing, commercial products, safety-critical parts, or mechanical load-bearing applications, you should independently verify:

- dimensions
- tolerances
- material suitability
- printability
- structural strength
- assembly clearance
- manufacturing process compatibility

Public examples are demos and references, not certified engineering drawings.

---

## Contact

For questions, collaboration, or custom CAD / 3D model / animation requests:

```text
help@yotown.com
https://maker.yotown.com
```

