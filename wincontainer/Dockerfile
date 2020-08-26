#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see https://aka.ms/containercompat


FROM mcr.microsoft.com/dotnet/framework/runtime:4.7.2-windowsservercore-ltsc2019
 
COPY /fonts/Chilanka-Regular.ttf  /Windows/Fonts/
WORKDIR /Windows/Fonts
RUN REG ADD "HKLM\Software\Microsoft\Windows NT\CurrentVersion\Fonts" /v "Chilanka" /t REG_SZ /d "Chilanka-Regular.ttf"
 
RUN powershell.exe Get-ItemProperty 'HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts'

