## Requirements
- [ ] [ghostscript](https://github.com/ArtifexSoftware/ghostpdl-downloads/releases)

---

## Merge PDFs
```powershell
gswin64c.exe -sDEVICE=pdfwrite -dCompatibilityLevel="1.4" -dNOPAUSE -dBATCH -sOutputFile="merged.pdf" "input1.pdf" "input2.pdf"
```

## Compress PDF
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
gswin64c.exe -sDEVICE=pdfwrite -dNOPAUSE -dBATCH -dPDFSETTINGS=/default -dProcessColorModel=/DeviceGray -dColorConversionStrategy=/Gray -dOverrideICC -dCompatibilityLevel="1.4" -dDownsampleColorImages=true -dDownsampleGrayImages=true -dDownsampleMonoImages=true -dColorImageResolution=125 -dGrayImageResolution=125 -dMonoImageResolution=125 -sOutputFile="compressed.pdf" "input.pdf"
```
