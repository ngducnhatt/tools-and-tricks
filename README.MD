# Tricks

## I. Turn off ms-gaming overlay

-   Press Windows+R, type regedit.
-   Go to
    `HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\GameDVR`
-   Open `AppCaptureEnabled` change `1` to `0`, change base to `Decimal`.

Or you can run it on Powershell :
```
Set-ItemProperty -Path "HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\GameDVR" -Name "AppCaptureEnabled" -Value 0
```

## II. Network speed up

-   Press `Windows`+`R`, type `gpedit.msc`.
-   Go to `Local Group Policy Editor -> Computer Configuration -> Administrative Templates -> Network -> QoS Packet Scheduler`
-   Open `Timit reservable bandwidt`h choose `Enabled` change `80` to `0`.

Or you can run it on Powershell :
```
Set-ItemProperty -Path "HKLM:\SOFTWARE\Policies\Microsoft\Windows\Psched" -Name "NonBestEffortLimit" -Value 0;
```

## III. Turn on res 4:3

-   Press `Windows`+`R`, type `regedit`.
-   Go to `Computer\HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\GraphicsDrivers\Configuration`
-   Change `Scaling`: `4` to `3`.

Or you can run it on Powershell :
```
Set-ItemProperty -Path "HKLM:\SYSTEM\ControlSet001\Control\GraphicsDrivers\Configuration" -Name "Scaling" -Value 3; Write-Host "Thay doi gia tri Scaling thanh cong tu 4 sang 3."
```

## IV. Max speed download in Chrome

-   Go to 
```
chrome://flags
```
-   Press `Ctrl` + `F` search `Parallel downloading` choose `Enabled`

## V. Config windows

-   Go to https://christitus.com/debloat-windows-10-2020/
-   Open PowerShell type 
```
iwr -useb https://christitus.com/win | iex
```

## V. Create High Performance plan

-   You can run it on Powershell : 
```
powercfg -duplicatescheme 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c
```

## VI. Install choco

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Or you can run :
```
iwr -useb https://github.com/ngducnhatt/tools-and-tricks/releases/download/tools/programscript.bat -OutFile programscript.bat
Start-Process programscript.bat
```

# Support and contact

<a href="https://bit.ly/3ykbdSS?r=lp"><img src="https://img.shields.io/badge/Facebook-1877F2?style=flat-square&logo=facebook&logoColor=white"></a>
<a href="https://github.com/ngnducnhat"><img src="https://img.shields.io/badge/GitHub-100000?style=flat-square&logo=github&logoColor=white"></a>
<a href="mailto:contactwithme.isme@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=flat-square&logo=gmail&logoColor=white"></a>
<a href="https://bit.ly/m/perlescent_1"><img src="https://img.shields.io/badge/website-000000?style=flat-square&logo=About.me&logoColor=white"></a>
