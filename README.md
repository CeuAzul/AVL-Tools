# AVL Tools

AVL Tools is a wrapper around AVL (by Mark Drela - MIT) that allows one to easily modify an AVL configuration file through Python.

## Using

Run "test.py" to analyze the desired aerodynamic surface.

Currently the following aerodynamic surface parameters are available for modification:

- surface_name
- cl_max_airfoil
- airfoil1_name
- airfoil2_name
- airfoil3_name
- LE_x_location
- LE_z_location
- span1
- span2
- chord1
- chord2
- chord3
- twist1
- twist2
- twist3
- incidence

As you can see, by default the library divides the surface on 2 sections, with 3 cross-sections, defined by their Chord, Twist and Airfoil. Each section is defined by it's span.

As VLM doesn't have a stall criteria, you can use the cl_max_airfoil variable to limit the  analysis till it find this value for CL.

## Errors

If you get FileNotFoundError on "coeficients_along_span" file, you are probably inside a folder location that is too deep for Windows to interpret. In this case, move the entire AVL folder to something closer than the drive root (ex.: "C:/").

## Authors

- André Silva Wagner (UFSC)
- Rafael Araujo Lehmkuhl (UFSC)