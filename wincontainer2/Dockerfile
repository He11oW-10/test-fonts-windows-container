#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see https://aka.ms/containercompat


FROM mcr.microsoft.com/dotnet/core/aspnet:3.1
 
COPY /fonts/Chilanka-Regular.ttf  /Windows/Fonts/
WORKDIR /Windows/Fonts
RUN REG query "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts"

USER ContainerAdministrator
RUN REG ADD "HKLM\Software\Microsoft\Windows NT\CurrentVersion\Fonts" /v "Chilanka" /t REG_SZ /d "Chilanka-Regular.ttf"
USER ContainerUser

RUN REG query "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts"

