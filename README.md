# AIL
AiL (Starter AiL) 


# Getting started

1. Clone or download the project from github
```
git clone https://github.com/m-silliman/AIL
```

2. Run the following code using a powershell command line to verify 
```
Get-ChildItem 'HKLM:\SOFTWARE\Microsoft\NET Framework Setup\NDP' -recurse |
Get-ItemProperty -name Version,Release -EA 0 |
Where { $_.PSChildName -match '^(?!S)\p{L}'} |
Select PSChildName, Version, Release
```
If .NET framework 4.8 or higher does not appear in the list proceed to the links
 to download.
# .NET Framework 4.8 Download
```
[https://www.microsoft.com/en-us/download/details.aspx?id=53344](https://dotnet.microsoft.com/en-us/download/dotnet-framework/net48)
https://tinyurl.com/jncefr5
```
3. Install SQL CE 64 bit runtime included in the git repository.  Look in the folder thirdparty and run "SSCERuntime_x64-ENU.exe"
4. To run the data proxy will require OPC Common Components to be installed from the ThirdParty folder.
5. Install DataProxy using the powershell in administrator mode by typing the following
```
./OpcServerProxy.exe install 
```
6. Configure the Data Proxy using the Setup.Xml to register required tags
