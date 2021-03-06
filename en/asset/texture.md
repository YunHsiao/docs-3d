# Texture Map Assets

**Texture mapping** assets are assets used for procedural sampling, such as **textures on models** and the **UI on Sprites**. When the UI or model are rendered, the corresponding texture is sampled, then filled on the model grid, plus a series of processing such as lighting to render the entire scene.

___Texture assets__ can be generated from __ImageAsset__. Some common image formats, including,  `.png`, `.jpeg`, etc. can be used in __ImageAsset__.

## Texture2D

__Texture2D__ is a type of __texture asset__ that is usually used for rendering of __3D models__, such as *reflection maps*, *ambient light mask maps*, etc. in model materials.

__Texture2D__ in __Cocos Creator 3D__:

![Texture2D](texture/Texture2D.jpg)

> **Note**: The texture type is a **Texture2D** asset.

### Adjusting the Properties of a Texture2D

When importing an __ImageAsset__, it will be set to __Texture2D__ by default. At this same time, one or more sub-assets will be generated on the original asset. Click the arrow in front of the original asset to see all the sub-assets. Example: 

![View Sub-assets](texture/SubAssets.gif)

After selecting the generated __Texture2D__ sub-asset, you can see the following panel:

![Texture2D sub-asset](texture/Texture2DPanel.jpg)

#### Sub-Asset Texture2D Properties Panel

![Texture2D Property Panel](texture/Texture2DDetail.jpg)

The following describes the properties of the panel:

| Properties | Explanation |
| --- | --- |
| **anisotropy** | Anisotropy value |
| **minFilter** | Narrowing Filter Algorithm |
| **magFilter** | Magnification Filter Algorithm |
| **mipFilter** | Multi-level texture filtering algorithm |
| **wrapS** | S (U) direction texture addressing mode |
| **wrapT** | T (V) direction texture addressing mode |

### Using Texture2D

__Texture2D__ is a very widely used asset. Any property marked as __Texture2D__ in the __Property Panel__ can be dragged into a __Texture2D__ asset type.

The usage scenario is mainly in the __Editor__ environment and for __dynamic acquisition__:

  - In the __Editor__, just drag the assets in;
  - For __dynamic acquisition__, you need to obtain the __ImageAsset__ asset first, and then instantiate the __Texture2D__ asset based on the obtained __ImageAsset__;

## TextureCube

__TextureCube__ is a cube texture, which can be used to set the scene's [Skybox](../concepts/scene/skybox.md). It can be obtained by setting the __panorama__ __ImageAsset__ to the __TextureCube__ type. It can also be obtained by making __CubeMap__ assets. 

__TextureCube__ obtained from a __panorama__ in __Cocos Creator 3D__:

![Panorama](texture/Panorama.jpg)

__TextureCube__ obtained by making a __CubeMap__ in __Cocos Creator 3D__:

![CubeMap](../concepts/scene/skybox/Cubemap.jpg)

To learn more about the use of **TextureCube** and **CubeMaps**, please refer to the [Sky Box](../scripting/setup.md) documentation.
