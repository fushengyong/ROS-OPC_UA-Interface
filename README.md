# ROS-OPC_UA-Interface
Simple Python Script that can communicate with an OPC-Server over ROS-Services

# Installation
1. Install FreeOpcUa Python from github.com/FreeOpcUa/freeopcua/tree/master/python
2. Clone Project into a new Folder and name it "OPCService" in catkin_ws
3. Execute `catkin_make`

# Basic Usage
1. start `roscore`
2. start opc_service_server with `rosrun opc_service opc_service_server.py`

Examples:   
Login: `rosservice call /opc_service "{option: 'login', cps: 's=16145', function: '', variable: '', valueToWrite: '', displayName: 'iiwa-1'}"`  
Add Package: `rosservice call /opc_service "{option: 'addPackage', cps: 'iiwa-1', function: 'F000020', variable: '', valueToWrite: '', displayName: ''}"`  
Add Package: `rosservice call /opc_service "{option: 'addPackage', cps: 's=16145', function: 'F000020', variable: '', valueToWrite: '', displayName: ''}"`  
RemovePackage: `rosservice call /opc_service "{option: 'remPackage', cps: 'iiwa-1', function: 's=16165', variable: '', valueToWrite: '', displayName: ''}"`  
RemovePackage: `rosservice call /opc_service "{option: 'remPackage', cps: 's=16145', function: 's=16165', variable: '', valueToWrite: '', displayName: ''}"`  
Read: `rosservice call /opc_service "{option: 'read', cps: 'iiwa-1', function: 'F000020', variable: 'local', valueToWrite: '', displayName: ''}"`  
Read: `rosservice call /opc_service "{option: 'read', cps: '', function: '', variable: 's=16768.local', valueToWrite: '', displayName: ''}"`  
Write: `rosservice call /opc_service "{option: 'write', cps: 'iiwa-1', function: 'F000020', variable: 'local', valueToWrite: 'true', displayName: ''}"`  
Write: `rosservice call /opc_service "{option: 'write', cps: '', function: '', variable: 's=16768.local', valueToWrite: 'true', displayName: ''}"`  
Subscribe: `rosservice call /opc_service "{option: 'subscribe', cps: 'iiwa-1', function: 'F000020', variable: 'local', valueToWrite: '', displayName: ''}"`  
Subscribe: `rosservice call /opc_service "{option: 'subscribe', cps: '', function: '', variable: 's=16768.local', valueToWrite: '', displayName: ''}"`  
Get available Functions: `rosservice call /opc_service "{option: 'getFunctions', cps: 'iiwa-1', function: '', variable: '', valueToWrite: '', displayName: ''}"`  
Get available Functions: `rosservice call /opc_service "{option: 'getFunctions', cps: 's=16145', function: '', variable: '', valueToWrite: '', displayName: ''}"`  
Logout: `rosservice call /opc_service "{option: 'logout', cps: 'iiwa-1', function: '', variable: '', valueToWrite: '', displayName: ''}"`  
Logout: `rosservice call /opc_service "{option: 'logout', cps: 's=16145', function: '', variable: '', valueToWrite: '', displayName: ''}"`  
Remove CPS: `rosservice call /opc_service "{option: 'remCPS', cps: 's=16145', function: '', variable: '', valueToWrite: '', displayName: ''}"`  
