# Ship-detection
Satellite imagery provides unique insights into various markets like agriculture, energy, finance as well as defense. The aim of this analysis is to address the difficulty in monitoring port activities and detecting locations of large ships, track their movement and can also be applied to detect illegal cross border movements. Automating this process can be applied to many issues including monitoring port activity levels and supply chain analysis.

 The dataset consists of images extracted from Planet satellite imagery collected over the globe. It includes 4000 80x80 RGB images labeled with either a “ship” or “no ship” classification. Images were derived from PlanetScope full-frame  visual scene products, which are orthorectified to a 3-meter pixel size. It is provided in a zipped directory shipsnet.zip that contains the entire dataset as .png images. Each individual filename follows a specific format: {label},{scene id},{longitude},{latitude}.png
label: Valued 1 or 0, representing the "ship" class and "no-ship" class, respectively.
scene id: The unique identifier of the PlanetScope visual scene the image was extracted from. The scene id can be used with the Planet API to discover and download the entire scene.
longitude_latitude: The longitude and latitude coordinates of the image center point, with values separated by a single underscore.
The dataset is also distributed as a JSON formatted text file shipsnet.json. The loaded object contains data, label, scene_ids, and location lists.

The pixel value data for each 80x80 RGB image is stored as a list of 19200 integers within the data list. The first 6400 entries contain the red channel values, the next 6400 the green, and the final 6400 the blue. The image is stored in row-major order so that the first 80 entries of the array are the red channel values of the first row of image.
The list values at index i in labels, scene_ids, and locations each correspond to the i-th image in the data list.

dataset link : https://www.kaggle.com/datasets/rhammell/ships-in-satellite-imagery
