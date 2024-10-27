## Resize ([ghostscript](https://github.com/ArtifexSoftware/ghostpdl-downloads/releases))
Medium Resolution
```powershell
gswin64c.exe -sDEVICE=pdfwrite -dNOPAUSE -dBATCH -dPDFSETTINGS=/ebook -sOutputFile="compressed.pdf" "input.pdf"
```
Low Resolution
```powershell
gswin64c.exe -sDEVICE=pdfwrite -dNOPAUSE -dBATCH -dPDFSETTINGS=/screen -sOutputFile="compressed.pdf" "input.pdf"
```
Finer Controls
```powershell
gswin64c.exe -sDEVICE=pdfwrite -dNOPAUSE -dBATCH -dPDFSETTINGS=/default -dCompatibilityLevel="1.4" -dDownsampleColorImages=true -dColorImageResolution=125 -dGrayImageResolution=125 -dMonoImageResolution=150 -sOutputFile="compressed.pdf" "input.pdf"
```
