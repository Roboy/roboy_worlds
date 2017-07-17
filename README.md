# roboy_worlds
This repo contains various environments for roboy_simulation and RoboyVR


New worlds can be created for example from Gazebo. Models in the world are used for physics Simulation and are pulled from Unity for visualization in Virtual Environment.



## Requirements for creating a new model
Due to the multifold use of the models, please consider common requirements for model generation:



Files:
- .STL and additional .DAE file extensions for the modelparts plus a .SDF model file to determine the joints, etc.
- put the original not reduced CAD files into the meshes/CAD folder

Component Naming:
- destinct, for example it should be avoided to name parts like thigh1/ 2, they rather should be thigh_left/ _right.
- simple and intuitive (no special characters!), for example no left_hand1v(0.2)1, but rahter left_hand.

Model Size:
- Due to simulation performance try to decrease the model size of the individual models as much as possible, e.g. by using Blender's Polygon reduction tools

Collisions:
- there must be collision meshes for every model in the collision subfolder

Description:
- Add a proper description into the model.config file, that especially describes the purpose and usage of the model as well as applied modification techniques. Also add your author name to allow further questions and a thumbnail file thats shows the robot.
- The despriction must contain: Are the collision models equal to the visual meshes or a simplified version (how?)? What details have been neglected for simplification? etc..

Folder Structure:
- /world_name
  -  world_name.world<br />
  - thumbnail.png<br />
- /models
  - /model_name
    - model.sdf<br />
    - model.config<br />
	 - /meshes<br />
         - visual
           - VIS_linkX.dae<br />
	       - ...<br />
	   - /collision<br />
	     - COL_linkX.dae<br />
	     - ...<br />
	   - /CAD
