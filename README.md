# Indoor-Localization-Using-Smartphone-Sensor-Data
Dataset- https://www.kaggle.com/c/indoor-location-navigation/data
The dataset used was provided by Microsoft Research in partnership with XYZ10 and includes around 30,000 timestamped traces 
from over 200 buildings in Chinese cities. Each trace was collected by walking in a straight line from one point to another 
and includes ground truth (waypoint coordinates in meters) and the data from IMU (accelerometer, gyroscope), geomagnetic field (magnetometer) readings,
Wi-Fi and Bluetooth iBeacon scanning results, as well as some basic device data such as software version and the brand, maximum range, 
power and resolution of the sensors. In addition to being separated into folders according to site and floor, each trace file has a unique name 
for easy identification. There are also site layouts which can be used to visualize locations.

#Approach
For the classification approach, we have divided the problem into two parts- first we predict the floor number and 
then we predict the location or waypoints on that floor. Currently, we have randomly selected a building to work with. 
It has a total of five floors (including basement). In the first part, our target was to classify sensor traces into five categories or floors;
in the second part, we predicted the location on that floor. But instead of trying to predict the exact waypoint, we divided the floor area into 
uniform grids based on the minimum and maximum waypoint values on the x and y axis. To start with we chose a grid size of 10X10, 
but later we also tried a grid size of 15X15. 
Therefore, our target in the second part was to classify sensor traces into uniform grids (100 to begin with).
