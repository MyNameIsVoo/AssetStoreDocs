# Support

___

[![Ko-Fi](https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/erochinsam) [![Patreon](https://img.shields.io/badge/Patreon-F96854?style=for-the-badge&logo=patreon&logoColor=white)](https://patreon.com/ErochinSam) [![Boostry](https://img.shields.io/badge/Boosty-F16061?style=for-the-badge&logo=boosty&logoColor=white)](https://boosty.to/erochinsam/donate)
![GitHub Follow](https://img.shields.io/github/followers/MyNameIsVoo?label=MyNameIsVoo&style=social)


# IIGR - InstancedIndirectGrassRenderer

___

The material from this repository was taken as a basis [UnityURP-MobileDrawMeshInstancedIndirectExample](https://github.com/ColinLeung-NiloCat/UnityURP-MobileDrawMeshInstancedIndirectExample/tree/master). More detailed information can be found there. Here I will describe the changes, innovations and improvements.

![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white) ![Unity](https://img.shields.io/badge/unity-%23000000.svg?style=for-the-badge&logo=unity&logoColor=white)

![Start Image](images/IIGR_6.png)

Find the asset on Unity [Asset Store]().

# What's new?

___

## Editor for working with grass

Added many auxiliary elements, such as:

### Grass cell rendering area
![Start Image](images/IIGR_1.png)

### Culling objects
![Start Image](images/IIGR_2.png)

### Culling objects settings
![Start Image](images/IIGR_3.png)

### GUI for changing the settings of the grass in real time

### Buttons for quick access to the necessary functions
![Start Image](images/IIGR_4.png)

## Baking the grass, hiding the grass

___

Grass generation works like this: you pass an array of points and IIGR creates grass at those points. The area can be completely filled with grass and in order not to generate all the grass and not fill the computer's memory with unnecessary, unused data, a grass clipping system was introduced. You specify the area in which the grass should be clipped and then bake it.

![Start Image](images/IIGR_Gif_0.gif)

> Make sure your herb is generated before baking!

Baking works in multi-threaded mode. Also, during baking, the main IIGR functions will be unavailable. You can interrupt baking by simply turning the IIGR component off and on. However, this is not recommended!

## Terrain support

___

![Start Image](images/IIGR_Gif_1.gif)

IIGR supports standard Terrain Unity. Just attach the TerrainGrass component to it and press the Preview button and watch the result. To increase the density of grass, you need to increase the resolution of the terrain in its settings. The default resolution is 1025x1025. At a lower resolution, artifacts in the form of blinking grass may appear.

![Start Image](images/IIGR_5.png)

## Shadows

___

![Start Image](images/IIGR_7.png)

In URP, shadows are controlled in the render settings. The **Cascade Count** parameter is responsible for this. Unfortunately, at higher values ??of this parameter, shadows from objects disappear. Keep this in mind!

![Start Image](images/IIGR_Gif_3.gif)

## Multithreading

___

Most operations are performed in multi-threaded mode. This is done to optimize and speed up data generation.

> ?It is not recommended to perform time-consuming operations in real time or in the Update method!

A good practice is to first generate the grass area, then bake it and then save it to file.

## Saving and loading data

___

Saving and loading data is done from a *.dat file. The binary format was chosen to reduce the file size and increase the speed of reading and writing to it.

> If your scene has a large amount of grass, for example more than 10 million, then the save file will be large (about 200 MB). At the same time, loading the file may take a long time. Keep this in mind!

![Start Image](images/IIGR_Gif_2.gif)

Generating 10 million blades of grass takes about 5 seconds
Cutting three objects with 10 million blades of grass takes about 5 seconds

## Dependencies

___

- [Editor Coroutines](https://docs.unity3d.com/Packages/com.unity.editorcoroutines@1.0/manual/index.html)

# Compatibility

___

![Unity](https://img.shields.io/badge/Tested-Unity2022.3-000.svg) ![Unity](https://img.shields.io/badge/Tested-Unity6-000.svg)
Compatible with the following versions of **Unity**:
- **Unity 2022.3.7f1** or higher
- **Unity 6000.0.22f1**

Render-pipelines:
- ![Unity](https://img.shields.io/badge/URP-000.svg)
- ![Unity](https://img.shields.io/badge/HDRP-000.svg)

> ![Unity](https://img.shields.io/badge/BuildIn-000.svg) not supported!

# Platform

___

![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white) ![Android](https://img.shields.io/badge/Android-0078D6?style=for-the-badge&logo=android&logoColor=white) ![IOs](https://img.shields.io/badge/IOs-0078D6?style=for-the-badge&logo=ios&logoColor=white)

# Contacts

___

[![Facebook](https://img.shields.io/badge/Facebook-%231877F2.svg?style=for-the-badge&logo=Facebook&logoColor=white)](https://www.facebook.com/profile.php?id=100004418195249) [![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=Instagram&logoColor=white)](https://www.instagram.com/sam.eroch/) [![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sam-erochin-927a629b/) [![X](https://img.shields.io/badge/X-%23000000.svg?style=for-the-badge&logo=X&logoColor=white)](https://x.com/VooChannel) [![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://www.youtube.com/@voochannel7151)

E-mail: choco.16mail@mail.ru
My other [ASSETS](https://assetstore.unity.com/publishers/18484)

# Bug-reports

___

If you find a bug or have any suggestions for improvement, please let us know: choco.16mail@mail.ru

![Start Image](images/IIGR_0.png)

# References

___

- [UnityURP-MobileDrawMeshInstancedIndirectExample](https://github.com/ColinLeung-NiloCat/UnityURP-MobileDrawMeshInstancedIndirectExample/tree/master)