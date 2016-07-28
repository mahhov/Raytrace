manuk hovanesian
tested on windows 7
subbmitted by me

COMPILE:
make sure all java files are in a folder named "raytrace"
then "javac raytrace/*.java" if you are in parent of raytrace folder

RUNNING:
run "java raytrace/Engine input_01" to run with a simple teapot input.
NOTE running without any argument will default to "java raytrace/Engine input_nn", and there should be a correctly formatted file named "input_nn" 
NOTE you can not run from inside raytrace folder, you should be in the parent folder of raytrace.
NOTE input files should be in same folder as raytrace folder is in (i.e., don't place input file inside raytrace folder).

INPUT FILES:
to use custom input files
1) simply create a input file that is correctly formatted,
2) place it in same directory as the raytrace folder,
3) and pass in the name of the file as a command line argument
you can look at file input_01_teapot to see how the file is formatted

OUTPUT:
the output file will be in the same folder as raytrace folder and input files
the output file name and resolution will be specified by the input file
the input files included have simple output file names such as input "input_01" --> output "a_01.png" 
output format will be .png, and cannot be changed from input file

OTHER SHAPES:
the program can draw spheres/cubes and other objects you want if you tell it to do so.
but there is no way to tell it via the input files.
if you run with no command arguemtns ("java raytrace/Engine") it will produce spheres and a rectanglular prism renedered to "a_00.png".
If you want to try out other spheres, you can manually modify the sphere/cube paramters inside the code.

CUBES:
if you want to try out cubes, the constructor of cubes takes 4 vectors as well as the material paramters that spheres takes.
the first vector is the corner of the cube
the next three vectors are the edges of the cube beginning at the corner vertex
the corner should be the bottom left front (i.e., minimum x, y, z) corner otherwise, triangles may have reversed normals and it will draw the cube inside/out.

FEATURES:
read .obj files, (supports n-gons!)
shadows
reflections
axis aligned bounding boxs (not organized into tree, just one bounding box per object)
can change camera vertical/horizontal view angles (see a_001.png)
real time rendering (run "java raytrace/Engine2")
