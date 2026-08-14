# STL Suite JK

A lightweight browser-based toolkit for working with STL geometry, combining an **STL Fuzer** with an interactive **3D Viewer** in a single application.

Built to make workflows involving large sets of separate STL files faster and easier to inspect and organize.

## Features

### Fuzer

The **Fuzer** combines multiple ASCII STL files into a single STL.

* Drag and drop multiple STL files
* Reorder components before combining
* Rename individual `solid` sections
* Choose the output filename
* Preview generated ASCII STL data
* Automatically remove existing outer `solid` / `endsolid` wrappers
* Preserve facet geometry
* Reject binary STL files to avoid accidental corruption
* Generate the combined STL directly in the browser

### Viewer

The **Viewer** provides an interactive 3D preview of STL geometry.

* Drag and drop multiple STL files
* Automatically creates **one plate per STL**
* Quickly switch between individual models
* Automatically synchronized with STLs loaded into the Fuzer
* **Appended STL Preview** shows all loaded geometry together
* Appended preview is highlighted in green for easy identification
* Fit-to-view and isometric camera controls
* Toggleable wireframe
* Toggleable reference grid
* Orientation indicator

### Mouse Controls

* **Left Mouse** Rotate
* **Right Mouse** Pan
* **Mouse wheel:** Zoom

The controls differ slightly from SolidWorks while retaining a familiar, intuitive workflow for CAD users.

## Privacy

STL processing is performed locally in the browser.

The application does not intentionally upload STL geometry to a server or external service. STL files are read and processed by browser-side JavaScript.

The 3D Viewer currently loads its Three.js viewer libraries from jsDelivr, so an internet connection may be required to initialize the Viewer.

## Usage

1. Open `STL_Suite_JK_v2.html` in a modern web browser.
2. Open the **Fuzer** page.
3. Drag and drop the desired ASCII STL files.
4. Rename or reorder components as needed.
5. Switch to **Viewer** to inspect each imported STL on its automatically generated plate.
6. Select **Appended STL Preview** to inspect the combined geometry.
7. Return to **Fuzer** and select **Combine & Download STL** when ready.

No installation is required.

## Input / Output

The Fuzer currently operates on **ASCII STL** files.

Each component in the combined output is structured as:

```text
solid component_name
    ...
endsolid
```

Existing top-level `solid` and `endsolid` wrappers are removed before each component is wrapped with its selected name.

## Project Structure

`STL_Suite_JK_v2.html` — Current STL Suite containing the Fuzer and 3D Viewer.

`STL_Fuze_v2.html` — Earlier standalone version of the STL Fuzer.

## Technology

STL Suite JK is built primarily with:

* HTML
* CSS
* JavaScript
* Three.js
* STLLoader

No installation, build process, or desktop application is required.

## Project Status

**Active development / experimental engineering utility**

Features and interface may continue to change as the workflow is refined.

## Disclaimer

Always verify generated and combined geometry before using it for engineering analysis, CFD, manufacturing, or other production purposes.
