---
layout: default
---
OpenSurgSim has various areas that could use improvement, spanning from graphics to scripting or physics. Any help in these areas is always appreciated. Here are just a few ideas.  

## Improve OSS redering capabilities

The current OSS rendering system is based on simple phong shading equation, with the current advances in graphics cards physically based rendering (PBR) is becoming more and more common, tasks in this area would be extending the OSS rendering pipeline to enable PBR, enable high definition range images, writing the appropriate shaders. 

## Implement a scene editing composer

Scenes in OSS can be written in C++ or scripted via YAML. For easier access to OSS it would be great if scenes could be assembled via a tool. This will not only require writing this tool but also modifications to some of the core engines of OSS to enable a "paused" assembly of components.

## Scripting (2 ways)

While most components in OSS have a type neutral interface that could be used for scripting, there are no language bindings implemented right now. It is conceivable that scenes could be assembled via scripts (scripting one way). In the other direction it would be quite handy to be able to write OSS behaviors in a scripting language.

