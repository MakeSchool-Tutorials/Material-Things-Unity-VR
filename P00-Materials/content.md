---
title: "Material Things"
slug: material-things-unity
---

In this tutorial we will work together to create a very realistic scene.  This scene will teach us about materials and how they work within Unity.  This pack also includes several hand picked texture packs from the Unity Asset store.  These texture packs are all free and you can use them to bolster your own library of texture assets.

Our scene is going to be an outdoor park scene, with a small metal sculpture, bushes, and a fountain in the middle.  You can see the final scene here:

We will use Glass, Stone, Brick, Bushes, Grass, Metal, and learn about each one and how they work.

To get started, let’s make a cube at 0,0,0 and set it’s scale to 15,0.5,15.  It should look like this:

![FirstImage](assets/image_0.png)

Next let’s drag a texture to the ground to make it look like rocky dirt.  Please find Dry Dirt Small Rocks - bump in the texture library and drag it to the cube.  After you drag it to the cube, please change the shader to Standard.  The Shader is currently a **Legacy** shader, legacy shaders were used before Unity 5 to draw effects that required a seperate shader for each effect.  Now you can use the Standard Shader to draw almost any effect.  We will go into detail on the various properties and maps available on this shader in a moment.  Use the next screenshot as a guide:

![image alt text](assets/image_1.png)

Here is a diagram that explains every single property, one by one:

![image alt text](assets/image_2.png)

Most of these maps can be exported by 3d applications when making your model, but you can make your own maps if you want these effects in your scenes.  Now let’s continue on our scene.

Let’s make 5 cubes, and put them all at 0,0,0.  We are going to use a little trick to make a staircase in the middle of the scene.  Set each cube to be 0.5 higher in the Y than the previous one, and 1 larger in the X and Z.  if we start at the bottom we should have 8,1,8, then 7,1.5,7, 6,2,6, and so on.  Put a sphere on the top and texture each stair however you like.  You will end up with a picture that looks something like this:

![image alt text](assets/image_3.png)

Now let’s make our sphere really reflective to give a neat centerpiece effect.  First go to light->reflection probe to create a reflection probe and put it at 0,5,0. This probe will give reflective materials true reflective properties.  Change it’s reflection mode to **realtime.**

Next, create a new material and call it mirror.  Then apply it to the sphere and set the properties as shown below:

![image alt text](assets/image_4.png)

Now you will have a semi reflective sphere that hovers over your staircase.  Let’s continue.

Now let’s make 4 bushes that align with each of the staircases, we will need to create some more cubes and apply a grassy texture to them.  We will need to also change the grassy texture to use the standard shader and update it’s tiling mode so that it looks good.  You can see the result here:

![image alt text](assets/image_5.png)

Next let’s add a few trees to the scene to make it look nice in our little park.  Find the Broadleaf mobile asset, this is a Unity SpeedTree and it is free and included with the standard Unity Environment Pack.

![image alt text](assets/image_6.png)

Drag in 3 trees and position them on the corners, then set their scale to whatever you like.  It is good to use the mobile tree, because these tree assets use a lot of polygons.

Finally let’s import the SteamVR rig like we have in the past and put it into our park.  Let’s all add a skybox for a finishing touch.  Just create a new Material and select the SkyBox shader, use procedural and drag it to the sky.

![image alt text](assets/image_7.png)

There now we have a pretty park scene to woo at in VR.