# The Dactyl Maximus gaming keyboard
Dactyl Maximus is a DIY split-hand gaming keyboard with interchangeable thumb cluster modules.

<img src="https://raw.githubusercontent.com/adereth/dactyl-cave/master/resources/glamourshot.png"/>

This readme explains *what* the Dactyl Maximus is.
* If you want to learn *how* to build one for yourself, follow the Beginner's Build Guide here: https://wolficefang.github.io/dactyl-maximus-keyboard/
* If you want to customize your Dactyl Maximus or contribute to the project, please peruse the wiki: https://github.com/WolfIcefang/dactyl-maximus-keyboard/wiki
* If you need help or just want to brainstorm, join the Discord server! https://discord.gg/Y8kQEjhf5E
* The latest version of Dactyl Maximus's .stl files can be found in the Releases sidebar to the right. https://github.com/WolfIcefang/dactyl-maximus-keyboard/releases

## First off, what is a Dactyl keyboard?

The Dactyl keyboard is a 3d printed mechanical keyboard. Each half has a "bowl" of keys arranged in a QWERTY grid. The bowl's shape can be set to match your unique hand shape. In place of a space bar, each thumb rests on a "thumb cluster". There have been many forks of the Dactyl's GitHub repository, most famously the Dactyl Manuform, the Tightyl, and the Bastyl.

## How does Dactyl Maximus stand out from the crowd?

The most significant difference between other Dactyl-like keyboards is the shape of their thumb clusters. Rather than try to create another "universal" design, the thumb clusters on the Dactyl Maximus are interchangeable; they are 3D printed independently of the bowls. A standardized "mounting plate" file can be found in **coming soon**, and the wiki has a list of popular cluster designs **coming later**.

Dactyl Maximus should also be easier to print than most Dactyl models. Each bowl is printed in 6 parts: top plate, bottom plate, and four side panels. This allows extensive customization of the keyboard after it has been assembled. Mouse wheels, joysticks, arrow keys, and more can be attached to *any* side. **coming last**

To facilitate swappable components, Dactyl Maximus will officially have one bowl size: 5 rows by 6 columns. Because Dactyl Maximus is based on the same code as the original Dactyl, these parameters can easily be changed. However, doing so will limit your ability to use swappable thumb clusters and other components; I do not recommend it.

## What makes Dactyl Maximus a "gaming" keyboard?

The original Dactyl keyboard was designed by programmers, for programmers, and it shows. The guide for software installation is a few bullet points with tips, and the wiring instructions are, I quote, "A very rough guide for the brave". In contrast, the Dactyl Maximus will inherit the best traits of gaming keyboards: A simple setup experience, reliable operation, convenient software, and of course, 16.8 million colors of per-key RGB backlighting.

To achieve this, a significant amount of effort is being put into the beginner build guide on GitHub Pages. It will list everything, from recommended components, to finding public 3D printers, to learning how to solder. A successful build guide will reflect the success of this repository. I want anyone, provided the build guide, to have a working keyboard within a month. **Coming sooner or later.**

One last thing: Dactyl Maximus is a gam***ing*** keyboard, not an endgame keyboard. It will never hold a candle to enthusiast or group buy products. It also isn't an ergonomic keyboard; I don't feel qualified to make that claim. Regardless, here's hoping that building this keyboard provides as much entertainment as the games it is designed to play.

***The following is the original Dactyl's description. I still need it for a few things, and the video is a good watch.
TODO: Figure out how copyright works, and get it from 2015 to 2021!***

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
