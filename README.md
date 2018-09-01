# Guitar 3D Visualizer - Report

## General description
For the realization of the *Product Visualizer*, I kept a simple layout containing only the essencial staff. I was inspired by this [3D demo](https://threekit.com/3d-product-demos/mens-polo-shirt-clothing/).

The chosen model is an [electric guitar](https://sketchfab.com/models/7ab6e59ba93b46bd8afa981fef92f114) in which it is possible modify the type of wood of the body and the metal of some of its components. 

The files used are the following: 
- **index.html**: the main file, it contains the code of the whole project.
- **model**:
	- **scene.gltf**: it contains the model of the electric guitar.
- **libraries**:
	- **GLTFLoader.js**: loader for models in glTF format
	- **TGALoader.js**: loader for textures in TGA format
	- **OrbitControls.js**
	- **three.min.js**
- **textures**:
	- **cubemap**: used as [environment map](http://www.humus.name/index.php?page=Cubemap&item=Yokohama).
	- **materials**: the different types of wood were taken from the site [https://www.gametextures.com](https://www.gametextures.com).

## Design choices
To obtain more realistic materials, I used a cubemap as environment map but, wanting to keep a clean style of the web page, and given the type of model chosen as subject, I kept the white background insead of showing the cubemap used. For this reason, I did not apply IEM because the reflections on the model would have been "wrong".

## Materials
In the *Product Visualizer* only some guitar materials are customazible: 
- body: you can choose the type of *wood* between mahogany, ebony and rosewood;
- metallic parts: they mainly concern mechanics, nut, pickups and bridge; you can choose the type of *metal* between platinum, copper, gold and silver.

For the rest of the guitar I used the following materials: 
- *plastic* for the knobs
- *chrome* for frets
- *nickel* for the strings 
- *black metal* for some parts of the bridge.

The model chosen has an UV mapping only on the front and back of the guitar body. Indeed at the neck and at the edge of the guitar body, I could not apply textures to simulate a complex material; so I decided to use an opaque diffusive material. 

## BRDF
The materials were made using the following techniques:
- wood: diffuse map, specular map, roughness map and normal map
- metal: specular reflection (used environment map and chosen mipmap layer to use based on roughness)
- plastic: combination of Lambertian BRDF and Cook-Torrance BRDF
- lambert: Lambertian BRDF.

## Lighting
I used three `PointLight` arranged in the following way:
1. front light: `(0.0, 0.00, 6.0)`
2. right back light: `(8.0, 4.0, -6.0)`
3. left back light: `(-8.0, 4.0, -6.0)` 

## Project development
The project is developed executing the following steps:
- research and model selection in [Sketchfab](https://sketchfab.com/)
- insertion of the cubemap
- writing shaders for materials
- creation of the form for the personalization of materials 
- added addictional materials selectable via the form
- insertion of lights
- creation of web page layout using [Bootstrap](http://getbootstrap.com)
- correction of materials and position of lights. 

## Result
[Link final result](https://cocuma22.github.io/Product-visualizer/)
![Immagine di default](textures/img/default.png)
![Immagine custom](textures/img/customized.png)
