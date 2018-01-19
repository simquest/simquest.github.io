---
layout: default
---

# OpenSurgSim Google Summer of Code 2018

Welcome to OSS. Hopefully you are interested in real time physical simulation in general or medical simulation specifically. OSS is a framework to do that. We have various areas that could use improvement, spanning from graphics to scripting or physics. Any help in these areas is always appreciated. Remember that these are just some ideas.

OSS is written in C++11 and supports Windows & Linux. When writing code for OSS you will also be required to write unit test code to make sure things are working ok and document your header files via doxygen.

If you are interested in OSS sign up to the [mailing list](https://groups.google.com/a/simquest.com/forum/#!forum/opensurgsim/join) on google groups.

## Ideas

### Physically based rendering

The current OSS rendering system is based on simple phong shading equation, with the current advances in graphics cards physically based rendering (PBR) is becoming more and more common. You would be working on extending the OSS rendering pipeline to enable PBR, enable high definition range images, writing the appropriate shaders.

- **Proficiencies**: C++, OpenSceneGraph, Computer Graphics, GLSL, Physically based Rendering
- **Difficulty**: Hard
- **Mentors**: Harald Scheirich, Ryan Kornheisl

### OSS Scene Composer

Scenes in OSS can be written in C++ or scripted via YAML. For easier access to OSS it would be great if scenes could be assembled via a tool. We have done some experiments with ImGui and those have shown promise. Our current runtime architecture is not quite suited for a "paused" assembly, this would probably be the biggest hurdle. You would be modifying the core to enable assembly, write the actual "editor" or editing mode and enable change to components parameters through a UI.

- **Proficiencies**: C++, Application Development, ImGUI
- **Difficulty**: Medium
- **Mentors**: Harald Scheirich, Ryan Kornheisl

### Python to OSS scripting

One of our long term goals was always to be accessible from scripting languages, so one could write OSS simulations in a scripting language. While some prerequisites are available (we have untyped infrastructure inside of OSS), the details were never worked out. If you've always wanted to create a script engine this is your chance. A technical hurdle is that we have been building everything as static libraries under Windows this would probably have to change. You would be creating the language binding, any necessary interfaces between Python and OSS, you might have to work with the build system.
If you can make a case for a different scripting language please do so in your proposal.

- **Proficiencies**: C++, Python, Language Binding, SWIG, CMake
- **Difficulty**: Medium
- **Mentors**: Harald Scheirich, Ryan Kornheisl

### OSS to Python scripting

While writing components in C++ is our preferred mode, sometimes it would be helpful if we could write components in a scripting language, the goal is to enable OSS to execute a scripted component. You would need to write a `ScriptableComponent` that can execute a script, you would also need to enable bidrectional access to this components variables through out property system. Access to other components properties should also be available
If you can make a case for a different scripting language please do so in your proposal.

- **Proficiencies**: C++, Python, Language Binding, SWIG
- **Difficulty**: Medium
- **Mentors**: Harald Scheirich, Ryan Kornheisl

### Improve Blender Tools

There is a set of Blender add-ons provided in OSS that aid in generating FEM model files for the physics engine in OSS to use. Presently they do work, although there are limitations or certain special cases that are not supported that would greatly improve their usefulness if implemented. Additionally certain ease-of-use functionalities could bolster the user experience of using the add-ons. You would be modifying our current plugin to improve the UI and add feature to the exporter for example: adding per vertex properties, enabling the editing of finite element model boundary conditions. 

- **Proficiencies**: Python, Blender, 3D Modelling
- **Difficulty**: Easy
- **Mentors**: Ryan Kornheisl, Harald Scheirich

### Physics Speedup

A hard threshold to performance in OSS are physics calculations, in most cases all physics have to be dealt with before a new frame can be started. Haptics feel ok under 250Hz but faster is always better. The human touch runs at a rate of about 1kHz. There are various avenues in OSS that could be pursued, if you are interested in this kind of work talk to us.

- **Proficiencies**: C++, Numerical Mathematics, Physics, Mechanics
- **Difficulty**: Hard
- **Mentors**: Ryan Beasley, Harald Scheirich


## Applying to OSS

In most cases you will need to be conversant with C++11 and should be comfortable with using Boost and google-test. Due to the time constraints we won't be able to teach you C++. If you are interested in working with OSS sign up to the mailing list and send a proposal. While there is no specific format for this please consider the following questions:

- Why do you want to work with OSS ?
- What is your background ? What projects have you worked on ?
- What motivates you ? What keeps you in front of the keyboard ?
- A brief description of your project.
- A more detailed description of your project including goals, maybe a rough timeline, references that you would use, etc.
- Why do you want to do this project ?
- How did you prepare ? Did you prototype your solution ?
- What are the biggest risk factors in this that could prevent you from finishing ?
- How will you schedule your work and allocate your time over the course of the three months ? 
- Contact information

All our mentors are located in the EST Timezone, while working with a time difference of +/- 6-8 hours is feasible anything further away makes communication extremely challenging.
