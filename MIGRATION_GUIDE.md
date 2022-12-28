## Migration Guide (for future marlin versions)

1. temperature settings 
    1. set HEATER_0_MAXTEMP to 255
    2. set HOTEND_OVERSHOOT to 10

    HEATER_MAXTEMP - HOTEND_OVERSHOOT = MAXTEMP <br>
    MAXTEMP should be around 230-245C depending on the quality of ptfe tube, check for delamination after printing at MAXTEMP

    3. set EXTRUDE_MINTEMP to 180

2. filament runout settings
    1. set FILAMENT_RUNOUT_DISTANCE_MM to 5
    
    TODO see how if it works correctly after false positive and after runout
    
3. preheat profiles
    1. add new profile or change ABS profile
        ``` 
            #define PREHEAT_2_LABEL       "PET-G"
            #define PREHEAT_2_TEMP_HOTEND 235
            #define PREHEAT_2_TEMP_BED    70
            #define PREHEAT_2_TEMP_CHAMBER 35
            #define PREHEAT_2_FAN_SPEED     0 // Value from 0 to 255
        ```