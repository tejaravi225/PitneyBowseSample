Robot functionality has been divided into the following general subsections.  Each subsection may correspond to one or more classes in the actual code.  Each experienced programmer is responsible for at least one subsection.

Subsection leaders, please update the descriptions below as relationships between each section change and as you add or remove classes to your section.

### Robot Main:  Ben Bray & Steven Ploog
Code to manage overall robot functionality.  Determines which logic system (AUTON LOGIC or TELEOP LOGIC) currently has control of the robot.

* RobotMain.java

### Sensors:  Curtis Fenner
Code to handle sensor input  Includes FancySensor.  All subsystems make calls to classes under this category. 

* RobotSensors.java

### Robot Drive (Chassis):  Tyler Del Rose
Code to control drive motors.  Both TELEOP LOGIC and AUTON LOGIC will make calls to ROBOT DRIVE to maneuver the robot.

* RobotDrive.java
* PIDLogic.java

### Disc Shooting (Disc Shooter):  Nathan Fenner
Code to shoot discs.  Includes velocity/angle calculations.  Does not include targeting logic.  Responsible for adjusting shooter rotation and controlling shooter motor speeds. Will retrieve information about goals (distance, etc.) from IMAGE PROCESSING.  

* RobotShoot.java

### Disc Manipulation (Disc Pickup):  Ben Bray
Code to pick up discs off the ground, accept discs from the human player, and deliver discs to the shooting mechanism.  Does not take into account period (auton/telop) or user input; both AUTON LOGIC and TELEOP LOGIC will make calls to this section.

* RobotPickup.java

### Climbing Logic (Climbing Mechanism):  Ben Bray
Code to initiate climbing and control the robot while it climbs.  Will be treated like a third “Phase” of robot behavior, along with AUTON LOGIC and TELEOP LOGIC.

* ClimbLogic.java
* RobotClimb.java

### Dashboard:  Steven Ploog
Code to send information from the robot to the dashboard, and code to display information from the robot on the dashboard.  Includes pretty charts and graphs (allow charts/graphs/data/settings from a session to be saved for later?)  Will use SmartDashboard to do so.  Closely related to DATA LOGGING / FILE IO.

### Joysticks & Magic Box:  Steven Ploog
Code to handle XBOX input as well as magic box input. Includes FancyJoysitck.
Teleop Logic:  Steven Ploog
Code to manage the robot during teleop.  Makes calls to ROBOT DRIVE, DISC SHOOTING, DISC MANIPULATION, DASHBOARD & DRIVER STATION, and CLIMBING LOGIC.  

* FancyJoystick.java

### Autonomous Logic:  Ben Bray
Code to manage the robot during autonomous.  Makes calls to ROBOT DRIVE, DISC SHOOTING, DISC MANIPULATION, DASHBOARD & DRIVER STATION, and potentially CLIMBING LOGIC.  

* AutonLogic.java

### Image Processing:  Curtis Fenner
Code to retrieve images from the camera and process them.  Should calculate values necessary for calculations made by DISC SHOOTING, such as distance and angle.  

* RobotCamera.java

### Data Logging / File IO:  Jonathan Zarger
Code to save data to the robot while it operates and code to read in settings from a text file or table at the start of a match.  Includes code to handle saving images from the camera.  Closely related to DASHBOARD & DRIVER STATION.