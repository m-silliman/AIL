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

If .NET framework 4.6 or higher does not appear in the list proceed to the links
below to download.
# .NET Framework 4.6 Download
```
https://www.microsoft.com/en-us/download/details.aspx?id=53344
https://tinyurl.com/jncefr5
```
