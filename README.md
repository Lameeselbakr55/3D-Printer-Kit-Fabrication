# 3D-Printer-Kit-Fabrication

The purpose of this project is to implement and congigure my own 3d printer kit 

## Tasks 
1. Mechanical components implementation and chasis 

![chasis](https://user-images.githubusercontent.com/98288035/151264173-06a2ab48-56ea-494c-b4d1-32ac0a57f0bd.jpeg)

2. wiring the hardware circuit due to the attached diagram 
![wiring](https://user-images.githubusercontent.com/98288035/151262292-7b9ea3d8-4d16-41f1-8372-d7bed0ab2231.png)

3. download marlin-1.1x firmware and update configuration.h file according to my 3d printer parameters as  

```
#define MOTHERBOARD BOARD_RAMPS_14_EFB             // Motherboard Name
#define CUSTOM_MACHINE_NAME "ORIGIN FAB"           // Machine name to be displayed in the LCD "Ready" message  (optional)
#define EXTRUDERS 1                                // define number of extruders used 
#define DEFAULT_NOMINAL_FILAMENT_DIA 1.75          // expected filament diameter 

#define TEMP_SENSOR_0 1                            // Select type of bed temperature sensor
#define TEMP_SENSOR_1 0                            // Select type of extruder 1 temperature sensor

#define HEATER_0_MINTEMP 5                         // define heater minimum temperature
#define HEATER_0_MAXTEMP 275                       // define heater  max temperature When temperature exceeds max temp, your heater will be switched off.
#define BED_MINTEMP 5                              // define bed minimum temperature
#define BED_MAXTEMP 200                            // define bed max temperature

#define THERMAL_PROTECTION_HOTENDS                 // comment of enable thermal protection for all extruders
#define THERMAL_PROTECTION_BED                     // comment of enable protection for the heated bed

#define USE_XMIN_PLUG                              // define the used endstops and comment the unused
#define USE_YMIN_PLUG 
#define USE_ZMIN_PLUG
#define USE_XMAX_PLUG
#define USE_YMAX_PLUG
#define USE_ZMAX_PLUG
 

#define X_DRIVER_TYPE  DRV8825                     // define the driver of x , y , z , E motors
#define Y_DRIVER_TYPE  DRV8825
#define Z_DRIVER_TYPE  DRV8825
#define E0_DRIVER_TYPE DRV8825


#define DEFAULT_AXIS_STEPS_PER_UNIT   { 160, 160, 800, 185 }    // Default Axis Steps Per Unit (steps/mm)  for   X, Y, Z, E0 , E1 .. 
#define DEFAULT_MAX_FEEDRATE          { 900, 900, 1000, 1000 }  // Default feedrate mm/s for   X, Y, Z, E0 , E1 .. 
#define DEFAULT_MAX_ACCELERATION      { 500, 500, 300, 10000 }   // Default Max Acceleration (change/s) change = mm/s^2 for   X, Y, Z, E0 , E1 

#define INVERT_X_DIR true                            // set the stepper direction. Change (or reverse the motor connector) if an axis goes the wrong way.
#define INVERT_Y_DIR false
#define INVERT_Z_DIR false

#define X_HOME_DIR -1                              // set the direction of endstops when homing; 1=MAX, -1=MIN
#define Y_HOME_DIR -1
#define Z_HOME_DIR -1

#define X_BED_SIZE 200                           // set the size of the print bed
#define Y_BED_SIZE 200
