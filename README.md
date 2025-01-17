# Animaquina v0.0.8 Pre-Alpha for Ufactory Robots
by Luis Pacheco

Animaquina is a robot Integrated Development Environment (IDE) designed for controlling and simulating Robots within Blender. It leverages Blender's powerful 3D capabilities to provide a versatile platform for robot programming and visualization.

## Version Information
- Compatible with Blender 4.2
- Only compatible with Ufactory robots (Xarm6 and 850 tested)
- Requires a startup file for each robot model
- This is a pre-alpha version and may contain bugs or incomplete features.

## Installation

1. **Use Blender Launcher**: It is advised to use Blender Launcher to keep an isolated version of Blender and Python.
2. Open Blender 4.2.
3. Locate your Blender 4.2 Python lib folder. This is typically found in:
   - Windows: `C:\Program Files\Blender Foundation\Blender 4.2\4.2\python\lib`
   - macOS: `/Applications/Blender.app/Contents/Resources/4.2/python/lib`
   - Linux: `/usr/share/blender/4.2/python/lib`
4. Copy both the xarm folder into the Blender Python lib folder.
5. Go to **Edit** > **Preferences** in Blender.
6. Click on the **Add-ons** tab.
7. In the top-right corner of the Add-ons panel, click on **Install**.
8. Navigate to and select the Animaquinauf_0.0.8 pre-alpha ZIP file.
9. Click **Install Add-on**.
10. Locate "Animaquina" in the add-ons list and enable it by checking the box next to its name.

## Usage

1. Select the robot you have from the drop down list this is either ufxarm6_twin, uf850.
2. Set the IP address of your obot in the Animaquina panel.
3. In the target selection dropdown, select the 'tcp_target' .
4. Click the **Connect** button to establish a connection with the robot.
5. Click the **Update Pose** button to synchronize the digital twin's TCP with the selected robot's TCP. This action updates the current joint rotation and TCP position of the digital twin robot.
6. On the info panel, you can view the current joint rotation and TCP position of the digital twin.
7. To move the robot via Blender:
   a. Manipulate the `tcp_target` object in the 3D viewport.
   b. Click the **GoTarget** button to send the command and move the physical robot to the new position.
8. Enable the **RealTime** option to see the digital twin robot moving in sync with the physical robot.
9. To manually manipulate the physical robot:
   a. Click on **Manual Mode** to enable physical manipulation of the robot.
   b. If **RealTime** is enabled, you will see the robot's movements updated in real-time in the 3D viewport.
10. To digitize features in the cell:
   a. Move the robot's TCP to the desired position.
   b. Click the **addMarker** button to save the current TCP position as a marker.
11. To run a toolpath:
    a. Select a mesh object in the 3D viewport.
    b. Click the **Path** button to execute the toolpath.


    **Warning:** The order of vertices in the mesh object matters for the toolpath execution. Ensure the vertices are in the correct order before using this function.

## Features

- IP-based robot connection
- Real-time robot manipulation via Blender's 3D viewport
- Digital twin synchronization with physical robot
- Real-time movement visualization
- Manual mode for physical robot manipulation
- Live update of digital twin in manual mode
- Marker placement for digitizing cell features
- Toolpath execution based on mesh object vertices
- Display of current joint rotation and TCP position in the info panel

## Known Issues and Safety Warnings

⚠️ **IMPORTANT: USE AT YOUR OWN RISK!** ⚠️

The developer is not responsible for any damage to property, personal injury, or death resulting from the use of this software.

- **No collision detection:** The software does not detect or prevent collisions between the robot and its environment.
- **No angle limits:** Joint angle limits are not enforced, which could lead to unexpected or dangerous movements.
- **Real-time mode bug:** In real-time mode, you may need to wiggle the mouse to see the robot updating in the viewport.
- **Limited safety features:** Only speed and acceleration are capped. There are NO comprehensive safety measures programmed.
- **Lack of comprehensive safety protocols:** This pre-alpha version does not include industry-standard safety features typically found in production-ready robotic control software.

## Additional Safety Precautions

1. Always maintain a safe distance from the robot during operation.
2. Use physical safety barriers and emergency stop systems.
3. Thoroughly test all movements in a controlled, safe environment before executing them on the actual robot.
4. Ensure that all users are properly trained in robot safety and operation.
5. Never use this software in production environments or near personnel without proper risk assessment and mitigation strategies.

## Compatibility

- Blender version: 4.2
- Ufactory models only
- tested on windows

## License

GPL License

## Authors

- Luis Pacheco
  

## Support

For support or to report bugs, please [contact our support team/create an issue on our GitHub repository].

## Install
https://youtu.be/NPsnpP_cLk0

**Note:** This is a pre-alpha version intended for development and testing purposes only. It contains significant limitations and safety risks. Do not use in production environments or without expert supervision.

## Acknowledgments

This project builds on the ideas and inspiration from several similar tools in architectural robotics / animation. 
