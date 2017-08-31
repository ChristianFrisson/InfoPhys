# InfoPhys

## Abstract

Information visualisation is the transformation of abstract data into visual, interactive representations. In this paper we present InfoPhys, a device that enables the direct, tangible manipulation of visualisations. InfoPhys makes use of a force-feedback pointing device to simulate haptic feedback while the user explores visualisations projected on top of the device. We present a use case illustrating the trends in ten years of TEI proceedings and how InfoPhys allows users to feel and manipulate these trends. The technical and software aspects of our prototype are presented, and promising improvements and future work opened by InfoPhys are then discussed.

Christian Frisson and Bruno Dumas. 2016. InfoPhys: Direct Manipulation of Information Visualisation through a Force-Feedback Pointing Device. In Proceedings of the TEI '16: Tenth International Conference on Tangible, Embedded, and Embodied Interaction (TEI '16). ACM, New York, NY, USA, 428-433. DOI: https://doi.org/10.1145/2839462.2856545 

## Distribution

[InfoPhys](https://github.com/ChristianFrisson/InfoPhys) requires two tools:
1. a modified visualization of PaperMachines that allows to generate X3D scenes converted from SVG through d3.js.
2. a modified version of H3DViewer that can load X3D scenes converted from SVG through d3.js.

### PaperMachines

We have modified a visualization from [PaperMachines](https://github.com/papermachines/papermachines) to generate X3D scenes converted from SVG through d3.js.

#### Installation
Just load the HTML file under folder `PaperMachines` in a web browser!

Click on button "X3D" to export the visualisation to a file.

#### License

PaperMachines is released under the terms of the [BSD 2-clause "Simplified" License](https://github.com/papermachines/papermachines/blob/master/LICENSE).

The dataset of the visualization has been extracted from the ACM Digital Library using Zotero, but does not provide full texts of proceedings.

### H3DViewer

We have modified H3D components so that H3DViewer can load X3D scenes converted from SVG through d3.js:
- [H3DUtil](https://github.com/ChristianFrisson/H3DUtil): a utility library for the H3D framework. Includes vector and matrix math, image loading functions, thread handling and other common functions. 
- [HAPI](https://github.com/ChristianFrisson/HAPI): a C++ open source cross-platform haptics library 
- [H3DAPI](https://github.com/ChristianFrisson/H3DAPI): a cross-platform, device independent haptics and graphics scenegraph API based on the X3D standard 
- [H3DCore](https://github.com/ChristianFrisson/H3DCore): meta-repository for compiling H3DAPI, H3DUtil and HAPI

#### Installation

InfoPhys H3DViewer has only been tested on macOS so far, and using the MacPorts package manager.

To use the production version, add custom portfiles from [MacPortsCycle](https://github.com/ChristianFrisson/MacPortsCycle) (see repository for instructions) and install H3DViewer:
```sudo port install h3dviewer```
(Warning: some Porfile definitions might be deprecated!)

To compile the development version:
1. update submodules: `git submodule update --init --recursive`
2. point CMake to the source directory `H3DViewer`

#### License

H3DAPI, H3DUtil and HAPI are released under the terms of the [GPLv2](http://www.gnu.org/licenses/gpl-2.0.html) license.

## Authors
 * [Christian Frisson](http://christian.frisson.re) (University of Mons): creator and main developer
 * [Bruno Dumas](https://directory.unamur.be/staff/bdumas) (University of Namur): contributor
