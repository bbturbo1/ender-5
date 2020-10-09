# ender-5
Marlin bugfix- 2.0.x personal edit
all changes made to original Marlin code;
IN PLATFROMIO.INI;
line 21: change Mega2560 to STM32f103RET6

IN CONFIGURATION.H;
line 106: change 0 to 1
line 112: change -1 to 3
line 130: change BOARD_MELZE_CREALITY to BOARD_CREALITY_V427
line 2073: #if ENABLED(CR10_STOCKDISPLAY) 
line 2074: #define RET6_12864_LCD  //RET6 specific to this board
line 2075: #endif

BL_TOUCH SPECIFIC
[
IN CONFIGURATION.H
line 840: uncomment
line 898: uncomment
line 985: change bracket from { 10, 10, 0} to { -45, -7, 0}
line: 1233: uncomment
line 1384: uncomment
line 1393: chnage (4*60) to (8*60)

IN CONFIGURATION_ADV.H
line 1599: uncomment
]

BTT SMART FILAMENT RUNOUT SENSOR SPECIFIC
[
IN CONFIGURATION.H
line 1168: uncomment
line 1172: change LOW to HIGH   //LOW = open with M119, HIGH = TRIGGERED with M119
line 1189: uncomment and change 25 to 7 // currently set at 100 for experimental testing
line 1522: uncomment

IN CONFIGURATION_ADV.H
line 2059: uncomment
]

AFTER FIRST RUN STEPPERS ALL RAN IN REVERSE
FIXED WITH:
line 1085: change true to false    // X-axsis
line 1086: change true to false    // Y-axsis 
line 1087: change true to false    // Z-axsis
line 1092: change true to false    // Extruder
