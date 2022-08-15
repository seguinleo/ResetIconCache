# ResetIconCache
BAT file to reset icon cache on Windows 7/10/11 to avoid white icons.

```batch
taskkill /im explorer.exe /f
cd /d %userprofile%\appdata\local
attrib -h -r -s iconcache.db
del iconcache.db /q
start %windir%\explorer.exe
```
