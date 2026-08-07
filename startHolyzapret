@echo off
net session >nul 2>&1
if %errorLevel% neq 0 (
    powershell -Command "Start-Process '%~f0' -Verb RunAs"
    exit /b
)

call "%~dp0general.bat"

echo waiting 2 seconds...
timeout /t 2 /nobreak > nul

sc stop windivert > nul 2>&1
sc delete windivert > nul 2>&1

pause
