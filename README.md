# VStancer
|Master|Development|
|:-:|:-:|
|[![Build status](https://ci.appveyor.com/api/projects/status/qialhqew9j0i9528/branch/master?svg=true)](https://ci.appveyor.com/project/neos7/fivem-vstancer/branch/master) |[![Build status](https://ci.appveyor.com/api/projects/status/qialhqew9j0i9528/branch/development?svg=true)](https://ci.appveyor.com/project/neos7/fivem-vstancer/branch/development)|

### Description
An attempt to use the features from ikt's VStancer as resource for FiveM servers to synchronize the edited vehicles with all the players. It is built using FiveM API and FiveM port of NativeUI.

When a client edits a vehicle, it will be automatically synchronized with all the players.
If a vehicle is reset to the default values it will stop from being synchronized.
The synchronization is made using decorators.

The default key to open the menu is F6

### Features
* Edit X Position of the wheels' bones (Track Width)
* Edit Y Rotation of the wheels' bones (Camber)

### Client Commands
`vstancer_preset`
Prints the preset of the current vehicle

`vstancer_decorators`
Prints the info about decorators on the current vehicle

`vstancer_decorators <int>` 
Prints the info about decorators on the vehicle with the specified int as local handle

`vstancer_print`
Prints the list of all the vehicles with any decorator of this script

`vstancer_distance <float>`
Sets the specified float as the maximum distance used to refresh wheels of the vehicles with decorators

`vstancer_debug <bool>`
Enables or disables the logs to be printed in the console

### Config
`toggleMenu=167`
The Control to toggle the Menu, default is 167 which is F6 (check the [controls list](https://docs.fivem.net/game-references/controls/))

`editingFactor=0.01`
The step used to increase and decrease a value

`frontMaxOffset=0.25`
The max value you can increase or decrease the front Track Width

`frontMaxCamber=0.20`
The max value you can increase or decrease the front Camber

`rearMaxOffset=0.25`
The max value you can increase or decrease the rear Track Width

`rearMaxCamber=0.20`
The max value you can increase or decrease the rear Camber

`maxSyncDistance=150.0`
The max distance within which each client refreshes others clients' vehicles

`timer=1000`
The value in milliseconds used by each client to check if its preset requires to be synched again

`debug=false`
Enables the debug mode, which prints some logs in the console

[Source](https://github.com/neos7/fivem-vstancer)
[Download](https://github.com/neos7/fivem-vstancer/releases)
I am open to any kind of feedback. Report suggestions and bugs you find.

### Build
Open the `postbuild.bat` and edit the path of the resource folder. If in Debug configuration, the post build event will copy the following files to the specified path: the script, the `config.ini`, the `__resource.lua` and a copy of a built [NativeUI](https://github.com/citizenfx/NativeUI) script ported to FiveM.

### Credits
* VStancer by ikt: https://github.com/E66666666/GTAVStancer
* FiveM by CitizenFX: https://github.com/citizenfx/fivem
* NativeUI by Guad: https://github.com/Guad/NativeUI
* GTADrifting members: https://gtad.club/
* All the testers
