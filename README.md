# Unity-Stochastic-Shadergraph
Shadergraph package for stochastic texture manipulation for Unity HDRP

- [Original Design works](https://www.reddit.com/r/Unity3D/comments/dhr5g2/i_made_a_stochastic_texture_sampling_shader/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button)


> [!IMPORTANT]
> This shadergraph was created using Unity 6 HDRP, thus a caveat is 
> **_I am unsure of it's compatibility with previous versions of Unity/Shadergraph and other non-HDRP pipelines._**

# Modernized Functionality
### This shader offers standard functionality of the HDRP/Lit shader such as

- Diffuse, Normal & Mask map texture output.
- Tiling and Offsets
- Remapping of Normal strength, Smoothness & Metallic channels of the mask map.
> [!NOTE]
> A default value of `0.1` Metallic and `0.1` Smoothness will provide similar results as the `HDRP/Lit` default shader values.

![Stoch Shader Vals](https://github.com/user-attachments/assets/a610dc6c-5062-4ea2-9d51-70188f3ef7fb)


# Example Use
Diffuse, Normal and Mask map textures across two adjacent planes, where the left is the default `HDRP/Lit` Shader material and the right is the `Stochastic` Shader. 

### 1x1 tiling Similarity Comparison.
![BaseTileNoS](https://github.com/user-attachments/assets/db1199f8-335c-4ad7-8aec-b3100caac75f)

### 6x6 Tiling - Stochastic Disabled
![6x6 No Stoch](https://github.com/user-attachments/assets/8bdb7363-61e7-4c9c-89cd-c9f744ca6b60)

### 6x6 Tiling - Stochastic Enabled
![6x6 Stoch On](https://github.com/user-attachments/assets/9f2cdc07-c7e2-444d-904c-789a7b5204aa)


## Closer Stochastic Allocated Plane Comparison
### Stochastic Disabled
![Big Off](https://github.com/user-attachments/assets/f683fa2f-d04c-46dd-9ee5-0f0bb285d6dc)

### Stochastic Enabled
![Big On](https://github.com/user-attachments/assets/84b9acea-d8b4-4b16-ba4e-3dccd33cd60b)

# Further Information
## Non-Ideal Texture For Stochastic Calculations
> [!CAUTION]
> As outlined in the original Reddit post linked above, this shader's approach is not ideal for textures reliant on pronounced patterns and defined details. See the below example.

### 5x5 Tile Stochastic Disabled
![BrickOff](https://github.com/user-attachments/assets/594c4c51-5b2a-4d25-aac2-a994e59c5c2c)

### 5x5 Tile Stochastic Enabled
![Brick On](https://github.com/user-attachments/assets/58701653-8328-4fd6-84b5-398da49a4c30)
