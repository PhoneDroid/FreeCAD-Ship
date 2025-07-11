# FreeCAD Ship Workbench

![Ship Workbench Logo](freecad/ship/resources/icons/Ship_Logo.svg)

**Welcome to FreeCAD-Ship!**

## Introduction
FreeCAD-Ship is a free module for [FreeCAD] oriented to aid naval ship design by providing several tools commonly used in naval architecture, seakeeping and ship resistance.

## Contents
- [Features](#features)
  - [Areas curve](#areas-curve)
  - [Hydrostatics](#hydrostatics)
  - [Load conditions definition](#load-conditions-definition)
  - [Tank capacity curve](#tank-capacity-curve)
  - [Static sink and trim](#static-sink-and-trim)
  - [GZ curve](#gz-curve)
  - [RAOs](#raos)
- [Install](#install)
- [Usage](#usage)
- [Tutorials](#tutorials)
- [Roadmap](#roadmap)
- [Discussion/Feedback](#discussionfeedback)
- [Bugs/Enhancements](#bugsenhancements)
- [Authors](#authors)

## Features
It currently offers the following tools:

### Areas curve

![Ship_AreaCurve Icon](freecad/ship/resources/icons/Ship_AreaCurve.svg)

![image](https://user-images.githubusercontent.com/4140247/128526169-e2575abd-cadf-4694-bdc7-d59530db1fed.png)

This tool computes the area of each transversal section of the ship, plotting it and providing a spreadsheet with the very same results. The transversal areas curve offers really valuable information in the first stages of a ship's design, as it gives an idea of the shape and volume distribution of the ship.

### Hydrostatics

![Ship_Hydrostatics Icon](freecad/ship/resources/icons/Ship_Hydrostatics.svg)

![image](https://user-images.githubusercontent.com/4140247/128526205-447f70aa-bbee-4631-9914-320ceab0c1b4.png)

The most common hydrostatics can be easily computed with this tool. The hydrostatics are divided in 3 main groups:

 - Volume
   - Wetted area (WSA), heavily related with the ship dynamics.
   - Moment to trim the ship 1 cm (MTC), of critical relevance at the time of planning load conditions.
   - Longitudinal position of the bouyance center (XCB).
 - Stability
   - Floating Area/Waterplane Area (WP), related with the ship waves generation, and thus with the ship resistance.
   - Distance between the keel and bouyance center (KBt), which is related with the transversal stability.
   - Distance between the bouyance center and the metacenter (BMt), which is related with the transversal stability.
 - Coefficients
   - Block coefficient (Cb), heavily related with the ship resistance.
   - Floating Coefficient (Cf), heavily related with the ship resistance due to the waves generation.
   - Main section Coefficient (Cm), related with the ship transversal stability, as well as the ship dynamics.

On top of that, the Displacement-Draft curve is depicted in all the plots. The tool is also providing you a spreadsheet for further computations.

### Load conditions definition

![Ship_Weight Icon](freecad/ship/resources/icons/Ship_Weight.svg) ![Ship_Tank Icon](freecad/ship/resources/icons/Ship_Tank.svg) ![Ship_LoadCondition Icon](freecad/ship/resources/icons/Ship_LoadCondition.svg)

In FreeCAD-Ship you can define as many weights and tanks as required. Then you can combine them all together in a load condition. At the time of defining weights, you can define:

 - Punctual masses, providing their masses.
 - Line elements, providing their linear densities (i.e. the area of the transversal section multiplied by the material density).
 - Surface elements, providing their surface densities (i.e. the width of the element multiplied by the material density).
 - Solid elements, providing their densities.

### Tank capacity curve

![Ship_CapacityCurve Icon](freecad/ship/resources/icons/Ship_CapacityCurve.svg)

![capacity](https://user-images.githubusercontent.com/1668392/137370687-677a027d-c692-4227-a01f-b889406827b0.png)

In FreeCAD-Ship you can easily plot the Filling volume-level ratio of any tank. Of course the tool is providing you a spreadsheet with the information about filling level percentage, filling level height and resulting volume.

### Static sink and trim

![Ship_SinkAndTrim Icon](freecad/ship/resources/icons/Ship_SinkAndTrim.svg)

![sinkandtrim](https://user-images.githubusercontent.com/1668392/137372659-60cf9224-db07-4a1b-82f4-590f5416fa8e.png)

Get a visual hint on the equilibrium draft and trim angle for a certain load condition. You can choose between the representation in the upright ship position, or setting the free-surface as the z=0 plane.

### GZ curve

![Ship_GZ Icon](freecad/ship/resources/icons/Ship_GZ.svg)

![gz](https://user-images.githubusercontent.com/1668392/137374233-5ed5bd86-8675-4e3d-813c-7f78adab1503.png)

The main transversal stability indicator, it is unsurprisingly required by the vast majority of the classification societies to certify a ship. This tool is computing that for you, providing a plot and the associated spreadsheet.

### RAOs

![Seakeeping_SetMesh Icon](freecad/ship/resources/icons/Seakeeping_SetMesh.svg)
![Seakeeping_RAOs Icon](freecad/ship/resources/icons/Seakeeping_RAOs.svg)

![RAOs](https://user-images.githubusercontent.com/1668392/140480149-88bbd2e4-a255-4f9d-893a-c325356d4263.png)

With FreeCAD you can easily compute the Response Amplitude Operators (RAOs), considering the widely validated frequency domain code [Nemoh], and more specifially its Python wrapper [Capytaine].

## Install

This workbench is available for download via the FreeCAD [Addon Manager][Addon-Manager]

## Usage

Documentation for this workbench is available on the [Ship Workbench wiki page][Wiki]

## Tutorials

* Official Ship Workbench Tutorial [Part 1][Tutorial-1]
* Official Ship Workbench Tutorial [Part 2][Tutorial-2]

## Roadmap

There are many tools and features which will be implemented in this module:

 - Wiki documentation
 - Tutorials
 - Seakeeping
   - Added masses
   - Time domain solver
 - Deterministic damaged stability
 - Probabilistic damaged stability
 - Ship resistance

## Discussion/Feedback

Discuss bugs, feedback, thoughts etc.. on the official [FreeCAD forum thread][Forum]

## Bugs/Enhancements

Please open tickets in the [issue queue][Issues]

## Authors

 - Jose Luis Cercós Pita <jlcercos@gmail.com>
 - Juan Manuel Muñoz-Godin (Ship resistance Holtrop and Amadeo tools)
 - Antonio Souto-Iglesias (Advisor of Juan Manuel Muñoz-Godin)


<!----------------------------------------------------------------------------->

[Addon-Manager]: https://github.com/FreeCAD/AddonManager
[Tutorial-1]: https://wiki.freecad.org/FreeCAD-Ship_s60_tutorial
[Tutorial-2]: https://wiki.freecad.org/FreeCAD-Ship_s60_tutorial_(II)
[Capytaine]: https://github.com/mancellin/capytaine
[FreeCAD]: https://freecad.org
[Issues]: https://github.com/FreeCAD/freecad.ship/issues
[Nemoh]: https://lheea.ec-nantes.fr/logiciels-et-brevets/nemoh-presentation-192863.kjsp
[Forum]: https://forum.freecad.org/viewtopic.php?f=8&t=60885
[Wiki]: https://wiki.freecad.org/Ship_Workbench