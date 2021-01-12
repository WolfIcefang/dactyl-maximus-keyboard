# The Dactyl Maximus gaming keyboard
Dactyl Maximus is a 3d printable split-hand gaming keyboard with interchangeable thumb cluster modules.

<img src="https://raw.githubusercontent.com/adereth/dactyl-cave/master/resources/glamourshot.png"/>

This readme explains *why* I am designing the Dactyl Maximus.
* If you want to learn *how* to build one for yourself, read the GitHub Pages build guide here: **link here**.
* If you want to customize the Dactyl Maximus to match your hand size, or learn how to contribute to the project, please peruse the wiki: **link here**
* If you need help with anything, or just want to brainstorm or chat, join the Discord server! **link here**
* The Dactyl Maximus's stl files can be found in the Releases sidebar to the right. **coming soon**

## Why is the Dactyl Maximus a "gaming" keyboard?

The first real question is, why did I want to build a custom gaming keyboard? Right now, custom keyboards and gaming keyboards are two separate communities. Custom keyboards have many excellent attributes: uncompromising build quality, high-end materials and components, and advanced software. However, gaming keyboards feature different priorities: a simple setup experience, convenient software, and of course, RGB.

I'm not saying the Dactyl Maximus will be as easy to use as a pre-built keyboard, but it should be no more daunting than building a desktop gaming rig. The original Dactyl keyboard was designed by programmers, for programmers, and it shows. The software installation guide is a few bullet points with tips, and the wiring instructions are, I quote, "A very rough guide for the brave". To contrast, a successful build guide will be how I judge the success of Dactyl Maximus as a project. I want anyone, given the build guide, to go from "no prior keyboard knowledge" to "functional masterpiece" within a month.

To round out the "gaming" aspects, Dactyl Maximus has an exposed keyswitch design and, of course per-key RGB backlighting. These don't seriously make sense as gaming features - exposed keyswitches lower a keyboard's durability and RGB effects can be distracting, but they do serve practical purposes here: the former makes 3d printing easier and the latter helps people acclimate to typing with layers. 

Finally, I call the Dactyl Maximus a gaming keyboard to avoid calling it an ergonomic keyboard. The human body is really, *really* complicated; I don't feel qualified to say that this board has real health benefits.


## What else makes the Dactyl Maximus awesome?


There's a talk about the motivation and design of the Dactyl that helps provide context for this repo:

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/uk3A41U0iO4/0.jpg)](https://www.youtube.com/watch?v=uk3A41U0iO4)

## Assembly

### Generating a Design

**Setting up the Clojure environment**
* [Install the Clojure runtime](https://clojure.org)
* [Install the Leiningen project manager](http://leiningen.org/)
* [Install OpenSCAD](http://www.openscad.org/)

**Generating the design**
* Run `lein repl`
* Load the file `(load-file "src/dactyl_keyboard/dactyl.clj")`
* This will regenerate the `things/*.scad` files
* Use OpenSCAD to open a `.scad` file.
* Make changes to design, repeat `load-file`, OpenSCAD will watch for changes and rerender.
* When done, use OpenSCAD to export STL files

**Tips**
* [Some other ways to evaluate the clojure design file](http://stackoverflow.com/a/28213489)
* [Example designing with clojure](http://adereth.github.io/blog/2014/04/09/3d-printing-with-clojure/)


### Printing
Pregenerated STL files are available in the [things/](things/) directory.

### Wiring
Masks for the flexible PCBs I used are available for the [left](resources/pcb-left.svg) and [right](resources/pcb-right.svg) side.

A [very rough guide for the brave is here](guide/README.org#wiring) - It will be improved over time (**TODO**)!

## License

Copyright © 2015 Matthew Adereth

The source code for generating the models (everything excluding the [things/](things/) and [resources/](resources/) directories) is distributed under the [GNU AFFERO GENERAL PUBLIC LICENSE Version 3](LICENSE).  The generated models and PCB designs are distributed under the [Creative Commons Attribution-ShareAlike License Version 4.0](LICENSE-models).
