# cfd-verification-1


A simple incompressible flow around a sphere computational fluid dynamics model to be exercised with OpenFOAM version 11.  

Work in progress.  Many parameters still need to be tuned.

### Rough Workflow

0. Navigate to inside the `case_directory` folder.
1. `foamCleanCase` to remove all previous runs
2. `blockMesh` to create the initial block mesh
3. `snappyHexMesh` to create the refined mesh with the sphere obstruction
4. `foamRun` to run the simulation
5. `paraFoam -builtin` to view the results in ParaView

The geometry is a 6x3x3 meter box.  The sphere obstruction is centered at (1.5, 1.5, 1.5) with a radius of 0.5 meters.

The `animation.ogv` was created by slicing the 3D volume on the z-plane through the center of the sphere obstruction.

### License:

Copyright 2023 L3Harris Technologies, Inc.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.