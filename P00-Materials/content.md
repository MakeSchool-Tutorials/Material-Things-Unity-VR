---
title: "Material Things"
slug: material-things-unity
---

In this tutorial we will work together to create a very realistic scene.  This scene will teach us about Materials and how they work within Unity.

Our scene is going to be an outdoor park scene, with a small metal sculpture, bushes, and a fountain in the middle.  You can see the final scene here:
![Final image](assets/image_7.png)

We will use Glass, Stone, Brick, Bushes, Grass, Metal, and learn about each one and how they work.

>[action]
>Before you begin, import the Forest Grounds Texture Pack from the Asset Store:

![Forest Grounds Texture Pack](assets/forest.png)

<!-- this should probably be a plane rather than a cube -->

>[action]
>Make a cube at 0,0,0 and set it’s scale to 15,0.5,15.

![Ground](assets/image_0.png)

Next let’s add a texture to the ground to make it look like rocky dirt.

>[action]
>Please find "Dry Dirt Small Rocks - bump" in the texture library and drag add it to the cube. After you drag it to the cube, please change the shader to Standard.  The Shader is currently a **Legacy** shader, legacy shaders were used before Unity 5 to draw effects that required a separate shader for each effect.  Now you can use the Standard Shader to draw almost any effect.  We will go into detail on the various properties and maps available on this shader in a moment.

![Textured ground](assets/Animation1.gif)

A good tip to find the texture, by the way, is to click the little circle next to first element in "Materials" and find the material by name.

![Materials by name](assets/circle.png)

![Set by circle](assets/search.png)

To explain the Standard Shader in a little more depth, here is a diagram that explains every single property, one by one:

![Standard Shader](assets/image_2.png)

Most of these maps can be exported by 3d applications when making your model, but you can make your own maps if you want these effects in your scenes.  Now let’s continue on our scene.

>[action]
>Let’s make 5 cubes, and put them all at 0,0,0.  We are going to use a little trick to make a staircase in the middle of the scene.  Set each cube to be 0.5 higher in the Y than the previous one, and 1 larger in the X and Z.  if we start at the bottom we should have 8,1,8, then 7,1.5,7, 6,2,6, and so on.  Put a sphere on the top and texture each stair however you like.

![Pyramid](assets/image_3.png)

Now let’s make our sphere really reflective to give a neat centerpiece effect.

>[action]
>First create a Reflection Probe (GameObject->Light->Reflection Probe) and put it at 0,5,0. This probe will give reflective materials true reflective properties.  Change it’s reflection Type from baked to **realtime.**

![Reflection Probes](assets/refl.png)

>[action]
>Next, create a new material and call it "Mirror.""  Then apply it to the sphere and set the properties as shown below (Shader set to Standard (Specular setup), Specular set to white, and Smoothness set to 0.777).

![Mirror Material](assets/image_4.png)

Now you will have a semi reflective sphere that hovers over your staircase.  Let’s continue.

>[action]
>Now let’s make 4 bushes that align with each of the staircases.  We will need to create some more cubes and apply a grassy texture, like Grass Long Thing, to them.  We will need to also change the grassy texture to use the standard shader and update it’s tiling mode so that it looks good.  You can change these properties by expanding the Shader section at the bottom.

![Textured Bushes](assets/Capture1.png)

Note that how you built the bushes affects how tiling looks on them.  Are they all scaled the same way but rotated, or are they all rotate the same way but scaled differently?

Next let’s add a few trees to the scene to make it look nice in our little park.

>[action]
>Import the Standard Unity Environment package and drag in a some Broadleaf_Mobile Prefabs from the Standard Assets/Environment/SpeedTree/Broadleaf folder.  Set their scales to whatever you'd like.

![Tree Time](assets/Capture2.png)

It is good to use the mobile tree, because these tree assets use fewer triangles than the desktop analogues.

>[action]
>Finally let’s import SteamVR and add a CameraRig, like we have in the past, and put it into our park.  Add a skybox for a finishing touch, if you didn't already have one.  (Just create a new Material and select the SkyBox shader, use procedural and drag it to the sky.)  Also, be sure to remove the default Main Camera if you'd like to view this in VR!

![Woo in VR](assets/image_7.png)

There now we have a pretty park scene to woo at in VR.
