# Create Scene file from Openstreetmap data for Sionna Ray Tracing
This is a utility project which generates [Mitsuba](https://www.mitsuba-renderer.org/) compatible 3D scene file along with 3D objects of buildings, Ground and Roads using [Openstreetmap](https://www.openstreetmap.org/#map=5/21.843/82.795) data. Files generated using [OSM_to_Sionna](./OSM_to_Sionna.ipynb) can be directly used as input to [Sionna](https://github.com/NVlabs/sionna) Ray tracing applications.

![Figure 1](img/SionnaScene1.png) 
### Process Overview
It performs following tasks ...
- Presents an interactive map to let user select an area of interst.
- Creates ground, roads and buildings by fetching geo data from openstreetmap using [Osmnx](https://osmnx.readthedocs.io/en/stable/) library.
- Creates triangulated 3D mesh objects for ground, roads and buildings using [PyVista](https://docs.pyvista.org/version/stable/) and [Open3D](https://www.open3d.org/docs/release/introduction.html) libraries
- Finally it creates a Mitsuba 3 format XML scene file by adding materials, colors, light source, Camera etc. 
### Prerequisite modules
ipyleaflet, IPython.display, ipyvolume.pylab, pyproj, shapely, shapely, math, pyvista, numpy, osmnx, Transformer, open3d, xml.etree.ElementTree, xml.dom.minidom
