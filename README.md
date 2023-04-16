
# CG-3
This project depicts the scene of an abandoned postapocalyptic road in the nature. 


 **Element** | **depicts** |  **Node**  | **External** |
|:-----|:------:|:--------:|:------:|
| Broken Road  | Old road eroded by time | Road : Image map shader, mask, fractal power shader | Image: Road.jpg |
| Pond / lake | Cracked hole in the floor filled with water  | Lake Mask (hole mask, redirect fractal + displacement mask) + Water object  |
| Abandoned car | Rusty red car implemented with obj reader + PBR materials | Singular object with textures : car:25.obj --> Car Parts Shader 01 | ugly_yellow_car\car_25.obj, Material _25_Base_Color.png, Material_25_(Roughness/Metallic/Height).png  |
Grass | Wild vegetation outgrowing the infrastructures due to time | Population with fractal displacement | Grass Terragen Object |
|Fog | Ambiental fog very near to the floor but not very opaque | Atomosphere node |

## Instructions to Possible Errors

:warning:

Please be aware that errors may arise with the usage of objects not natives of Terragens library. 


Possible errors and methodology to correct them: 

1. Image map does not load the image -> Correct the absolute path in the node 
a.In the road
        
        Node: Road Image map shader 01. 
        Path: "/Road.jpg"

2. Objects do not load -> Correct the absolute path in the corresponding node. Ie. Car errors
  
  2.1. Not possible to load the obj
        
        Node: car_25.obj 
        Path: "\ugly_yellow_car\car_25.obj"

  2.2. Not shown the Materials of the obj
        
        Node: Car Parts shader 01 > Material shader
        Paths: Corresponding with the necessary textures such as: 
            - Base color: Material _25_Base_Color.png
            - Roughness : Material _25_Roughness.png
            - Specular/Metalness : Material _25_Metallic.png
            - Displacement: Material _25_Height.png

## Acknowledgements
 - [Crown Vic 1987 Low Poly](https://skfb.ly/oEVqs) by abass20 is licensed under :copyright: [Creative Commons Attribution](http://creativecommons.org/licenses/by/4.0/).
 - [Abandoned street lights pack](https://skfb.ly/oFDUU) by sergeilihandristov is licensed under :copyright: [Creative Commons Attribution](http://creativecommons.org/licenses/by/4.0/).
 
## Authors
- [Lucía Ferrer ](100429154@alumnos.uc3m.es)
- [Javier Montero](1004@alumnos.uc3m.es)

