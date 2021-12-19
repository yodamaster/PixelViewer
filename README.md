# PixelViewer [![](https://img.shields.io/github/release-date-pre/carina-studio/PixelViewer?style=flat-square)](https://github.com/carina-studio/PixelViewer/releases/tag/1.104.0.1123) [![](https://img.shields.io/github/last-commit/carina-studio/PixelViewer?style=flat-square)](https://github.com/carina-studio/PixelViewer/commits/master) [![](https://img.shields.io/github/license/carina-studio/PixelViewer?style=flat-square)](https://github.com/carina-studio/PixelViewer/blob/master/LICENSE.md)

PixelViewer is a [.NET](https://dotnet.microsoft.com/) based cross-platform image viewer written by C# which supports reading raw Luminance/YUV/RGB/ARGB/Bayer pixels data from file and rendering it.

[![Release](https://img.shields.io/github/v/release/carina-studio/PixelViewer?include_prereleases&style=for-the-badge&color=cyan&label=Preview)](https://github.com/carina-studio/PixelViewer/releases/1.104.0.1123)

&nbsp;    | Windows 10/11 | Linux | macOS
:--------:|:-------------:|:-----:|:-----:
Download  |[x64](https://github.com/carina-studio/PixelViewer/releases/download/1.104.0.1123/PixelViewer-1.104.0.1123-win-x64.zip)|[x64](https://github.com/carina-studio/PixelViewer/releases/download/1.104.0.1123/PixelViewer-1.104.0.1123-linux-x64.zip)|[x64](https://github.com/carina-studio/PixelViewer/releases/download/1.104.0.1123/PixelViewer-1.104.0.1123-osx-x64.zip)
Screenshot|<img src="https://github.com/carina-studio/PixelViewer/blob/master/docs/Screenshot_MainWindow_Windows_Thumb.png" alt="Main window (Windows)" width="250"/>|<img src="https://github.com/carina-studio/PixelViewer/blob/master/docs/Screenshot_MainWindow_Ubuntu_Thumb.png" alt="Main window (Ubuntu)" width="250"/>|<img src="https://github.com/carina-studio/PixelViewer/blob/master/docs/Screenshot_MainWindow_macOS_Thumb.png" alt="Main window (macOS)" width="250"/>


[![Release](https://img.shields.io/github/v/release/carina-studio/PixelViewer?include_releases&style=for-the-badge&color=cyan&label=Stable)](https://github.com/carina-studio/PixelViewer/releases/1.0.0.617)

&nbsp;    | Windows 10/11 | Linux
:--------:|:-------------:|:-----:
Download  |[x86](https://github.com/carina-studio/PixelViewer/releases/download/1.0.0.617/PixelViewer-1.0.0.617-win-x86.zip) &#124; [x64](https://github.com/carina-studio/PixelViewer/releases/download/1.0.0.617/PixelViewer-1.0.0.617-win-x64.zip)|[x64](https://github.com/carina-studio/PixelViewer/releases/download/1.104.0.1123/PixelViewer-1.104.0.1123-linux-x64.zip)|[x64](https://github.com/carina-studio/PixelViewer/releases/download/1.0.0.617/PixelViewer-1.0.0.617-linux-x64.zip)
Screenshot|<img src="https://github.com/carina-studio/PixelViewer/blob/master/docs/Screenshot_MainWindow_Windows_Thumb_Old.png" alt="Main window (Windows)" width="250"/>|<img src="https://github.com/carina-studio/PixelViewer/blob/master/docs/Screenshot_MainWindow_Ubuntu_Thumb_Old.png" alt="Main window (Ubuntu)" width="250"/>


## ⭐Supported formats
* Luminance
  * L8
  * L16
* YUV
  * YUV444p
  * P410 (v1.99+)
  * P416 (v1.99+)
  * YUV422p
  * P210 (v1.99+)
  * P216 (v1.99+)
  * UYVY
  * YUVY
  * NV12
  * NV21
  * Y010 (v1.99+)
  * Y016 (v1.99+)
  * I420
  * YV12
  * P010 (v1.99+)
  * P016 (v1.99+)
* RGB
  * BGR_888
  * RGB_565
  * RGB_888
  * BGRX_8888
  * RGBX_8888
  * XBGR_8888
  * XRGB_8888
* ARGB
  * ARGB_8888
  * ABGR_8888
  * BGRA_8888
  * RGBA_8888
* Bayer
  * BGGR_16
  * GBRG_16
  * GRBG_16
  * RGGB_16
  
## ⭐Supported color spaces (v1.104+)
* sRGB
* DCI-P3
* Adobe RGB
* ITU-R BT.601
* ITU-R BT.2020

## ⭐Supported functions
* Rendering image from raw pixel file.
* Evaluate image dimensions according to file name, file size and format.
* Specify pixel-stride and row-stride for each plane.
* Specify data offset to image in file. (v1.99+)
* Specify color space of image and screen. (v1.104+)
* Rotate and scale rendered image.
* Navigate to specific image frame in file. (v1.99+)
* Adjust brightness/contrast and color balance. (v1.104+)
* Show histograms of R/G/B and luminance. (v1.102+)
* Demosaicing for Bayer Pattern formats. (v1.103+)
* Save rendered image as PNG file.

## 💻Installation
Currently PixelViewer is built as portable package, you can just unzip the package and run PixelViewer executable directly without installing .NET runtime environment.

### macOS User
If you want to run PixelViewer on macOS, please do the following steps first:
1. Grant execution permission to PixelViewer. For ex: run command ```chmod 755 PixelViewer``` in terminal.
2. Right click on PixelViewer > ```Open``` > Click ```Open``` on the pop-up window.

You may see that system shows message like ```"XXX.dylib" can't be opened because Apple cannot check it for malicious software``` when you trying to launch PixelViewer. Once you encounter such problem, please follow the steps:
1. Open ```System Preference``` of macOS.
2. Choose ```Security & Privacy``` > ```General``` > Find the blocked library on the bottom and click ```Allow Anyway```.
3. Try launching PixelViewer again.
4. Repeat step 1~3 until all libraries are allowed. 

### Ubuntu user
Some functions of PixelViewer depend on ```libgdiplus``` before v1.99, you may need to install ```libgdiplus``` manually to let PixelViewer runs properly:

```
apt-get install libgdiplus
```

If you want to run PixelViewer on Ubuntu (also for other Linux distributions), please grant execution permission to PixelViewer first. If you want to create an entry on desktop, please follow the steps:
1. Create a file *(name)*.desktop in ~/.local/share/applications. ex, ~/.local/share/applications/pixelviewer.desktop.
2. Open the .desktop file and put the following content:

```
[Desktop Entry]  
Name=PixelViewer  
Comment=  
Exec=(path to executable)
Icon=(path to AppIcon_128px.png in PixelViewer folder)
Terminal=false  
Type=Application
```

3. After saving the file, you should see the entry shown on desktop or application list.

Reference: [How can I edit/create new launcher items in Unity by hand?
](https://askubuntu.com/questions/13758/how-can-i-edit-create-new-launcher-items-in-unity-by-hand)

Currently PixelViewer lacks of ability to detect screen DPI on Linux, so you may find that UI displays too small on Hi-DPI screen. In this case you can open ```Application Options``` of PixelViewer, find ```User interface scale factor``` and change the scale factor to proper value. If you found that scale factor doesn't work on your Linux PC, please install ```xrandr``` tool then check again.

## 📦Upgrade

### v1.99+
PixelViewer checks for update periodically when you are using. It will notify you to upgrade once the update found. Alternatively you can click "Check for update" item in the "Other actions" menu on the right hand side of toolbar to check whether the update is available or not.

PixelViewer supports self updating on Windows and Linux, so you just need to click "Update" button and wait for updating completed. For macOS user, you just need to download and extract new package, override all existing files to upgrade.

### v1.0
PixelViewer has no installation package nor auto updater. To upgrade PixelViewer, you just need to extract new package and override all existing files.

## 🤝Dependencies
* [.NET](https://dotnet.microsoft.com/)
* [AppBase](https://github.com/carina-studio/AppBase)
* [AppSuiteBase](https://github.com/carina-studio/AppSuiteBase)
* [Avalonia](https://github.com/AvaloniaUI/Avalonia)
* [Colourful](https://github.com/tompazourek/Colourful)
* [NLog](https://github.com/NLog/NLog)
* [NUnit](https://github.com/nunit/nunit)
* [ReactiveUI](https://github.com/reactiveui/ReactiveUI)
