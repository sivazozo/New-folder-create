@echo off
set  counter=0
mkdir "New folder" 2>nul || goto :TryNext
:continue
REM rest of your code

goto :eof
:TryNext
set /a counter+=1
mkdir "New folder (%counter%)" 2>nul || goto :TryNext
goto :continue
