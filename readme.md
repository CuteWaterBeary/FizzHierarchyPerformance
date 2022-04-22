# Nara's Unity Tools

Place for some of the tools I wrote for Unity.
Specifically for the creation of avatars for VRChat and ChilloutVR.

## Installation

Download or clone this project and copy the `Nara` folder into your `Assets` folder in your Unity project.
`Dynamic Bones` is **required**. I'm too lazy to add a fallback.

## Hierarchy improvements & context menus

Gives a small icon in the hierarchy on gameobjects that contain dynamic bones (white/gray) or dynamic bone colliders (blue).

![Screenshot of the hierarchy](.Media/hierarchy_screenshot.png)

Also adds a few other context menu items.
Mainly oriented around selecting and setting up dynamic bones.
You can right click in the hierarchy to quickly select and filter down to dynamic bone components so you can easily edit multiple items.
Right-clicking a dynamic bone component also allows you to quickly set it's root transform to the component's game object.

![Demo of the right menu contexts](.Media/context_demo.gif)

## Animator Tools

Tool that allows the editing of multiple transitions.
This includes conditions and transition timings. Find  the window in `Window > Nara > Animator Tools`.

![Screenshot of AT](.Media/at_screenshot.png)

## Dynamic Bone Constraints

[**>>> Tutorial <<<**](dbc_tutorial.md)

Instead of having 50 dynamic bone transformations hogging up the whole main thread it's better to have just a single chain of dynamic bones and have all other bones be move similarly to the single chain.
This can be done via rotation constraints which are significantly cheaper to compute and they also can be computed on other threads!

![Screenshot of DBC](.Media/dbc_screenshot.png)

The tool is pretty simple to use.
Open the window in `Window > Nara > Dynamic Bone Constraints`.
Select the objects you want to constrain and click the `From selection` button.
If you already have a chain of bones you want to bind these objects to, then use that as the `Constraint source root`.
`Modify source constraint` will modify (and if needed add) children of the root.
In most cases you can leave the `Constraint source root` empty and just click the magical `Setup constraints` button.
[You can have your dynamic bones on your avatar setup in 30 seconds!](https://youtu.be/byvG2FgJEhU)

## Help Me, I'm Stuck

For small questions you can tag me (Nara#0001) in the official VRChat Discord. Don't try to DM me, they are closed.
