# TerminalServerCore

## Description
Dotnet Core service that set terminal order and idle states regarding to workplace states.

## Additional information
* ready to run in docker (linux and windows service also available)
* no need to restart when new device is added/removed
* no need to restart when new device_port is added/removed
* checking database availability w/ email when unavailable
* using JSON config file for even better configurability
* creates order when none exists and production is set
* creates idle when none exists and idle is set
* closes order and idle when offline is set
* closes idle when some exists and production is set


    

### Versions  
* Latest    
    * Colorcoding log for Powershell, Bash and Docker
    * Option: SQL Server
* 2018.4
    * Fully working version, Docker based


## Windows installation
1. Install dotnetcore runtime from https://www.microsoft.com/net/download/Windows/run
2. Extract zip file to c:\Zapsi\TerminalServerCore
3. Run powershell ad administrator
4. Navigate to directory c:\Zapsi\TerminalServerCore
5. Run nssm.exe install TerminalServerCore
6. Set up nssm
    * Path is path to dotnet installation (C:\Program Files\dotnet\dotnet.exe)
    * Startup directory is alarm server directory (C:\Zapsi\TerminalServerCore)
    * Arguments are just the name of the dll (terminalServerCore.dll)
    * Service name is the name of the service (terminalServerCore)
7. Click install

# Additional information for using powershell
* Get-Service zapsiServerCore: information about the service
* Start-Service zapsiServerCore: start the service
* Stop-Service zapsiServerCore: stop the service
* Restart-Service zapsiServerCore: restart the service
* Get-Content 'logfile.txt' -Last 20 -Wait | sls "err"
  * Show last 20 lines from logfile.txt
  * Wait fot another lines
  * Show only lines containing err
  
www.zapsi.eu © 2018
