https://docs.google.com/document/d/1gBFaGOI3lLB_xCjMvg1LZI8W7LIN7X5g6yRNOOQqMiI/edit
This file is the same as the google doc file listed above.


Render Pipeline: High Definition RP
The Render Pipeline we are planning on using is High Definition RP, as we want to deliver the best quality of visuals. We are also using this pipeline to produce PBR shaders and lighting techniques. The limitation of the HD pipeline is ignored as they don’t apply to the current project delivery or guidelines.
Baked and Realtime Lights
We will be using mixed lightning. Primarily with baked lights for static content, while applying real-time lights based on shots requirements. We believe that we should be able to still use lights to complement the story without needing to have them be animated, and thus be able to optimize rendering time and therefore the budget for the scene.
There are two lighting ideas we are currently pursuing. One is a classic game approach with saturated colors and bright lighting. The other is mood-based lighting. Mood Based lighting will be implemented on few shots depending on primarily on time. But, for the overall theme we have a currently working game-based approach that is up and running.





Maya To Unity Instruction:
Basic Maya Setting (unit and animation)
 
Export To FBX
	Launch Maya.
Select File > Export All, or File > Export Selection. The Export All, or Export Selectiondialog box appears.
Select FBX from File of Type menu.
Note: if you do not see the FBX file extension in the File of Type menu, activate fbxmaya.mll in Maya's Plug-in Manager.
How to import and update static (non-animating meshes):
	Export FBX (mesh only) to Unity/Assets/Model
How to import and update animating meshes:
	Export FBX with animation to Unity/Assets/Model
	Extra animations in Unity/Assets/Anim	
How to import and update textures:
Create materials in Unity/Assets/Materials, while storing textures in Unity/Assets/Textures. 
Naming convention:
Since we only have few meshes, short and meaningful names are used.
Collaboration plans:
Our team is planning on using a multi-prefab workflow, as we feel that it will allow us to improve efficiency. The division of labor will be equal throughout regarding the number of shots animated, documentation, and/or importing asset duties.
We have already and will continue to meet up in person to discuss the project and collaborate in real time on making decisions and progress. We feel that this will be the most effective as we can have a product that we are all satisfied with. 
For primary communication we will be using Messenger and all project files will be stored on a GitHub repository (https://github.com/SharanyaSudhakar/MouseTrap-RealTime.git)
Material Pipeline Outline
Our materials will be developed in a Metal/Roughness Workflow
Albedo - this is our base color input. sRGB ranges 30 – 240 (avg)
Micro surface – Not Used. At this point is our project microscopic details of roughness are not apparent enough to warrant this inclusion. 
Reflectivity – reflectivity values based on F0 (Fresnel values for dielectrics) and metal surfaces. Except for the light saber handles nothing else is metallic in the scene.
Metalness-map - a black and white map that indicated metal in the material. White denotes metal, while black is dielectric. All gray values in between are a blend of the two. All our materials will have a black metalness map, except for the saber handle.
Smoothness map - controls how smooth a material is. Again with no metal values in the project this value is not used.
Normal Map: The normal direction as each pixel is stored in this map. This creates the illusion of detail. 
This map will be used more in the saber handle where details where not created in the mesh creation process. 
We will make use of this map for the mousetrap environment, where not all details were sculpted into the mesh. 
We will also be using the normal maps to for the characters to emphasize their clothing details.
Ambient Occlusion: This map affects the diffuse or base color contribution which is initially lighter toned. Ambient Occlusion maps enable darker details made by light apparent.
Bent Normal Maps: Not Used. Project doesn’t need one.
Height Maps: These maps store pixel displacement information and is used in conjunction with the normal maps. This enables meshes to be really simple at creation.
