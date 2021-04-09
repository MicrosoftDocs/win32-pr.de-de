---
title: Designdatei Format
description: In diesem Dokument wird das Format der Designdateien (. Theme) erläutert. Bei einer. Theme-Datei handelt es sich um eine ini-Textdatei, die in Abschnitte unterteilt ist, die visuelle Elemente angeben, die auf einem Windows-Desktop angezeigt werden Abschnittsnamen werden in eckige Klammern (\ \) in der INI-Datei eingeschlossen.
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61ba97172fc5aaddb912183130941337a149536
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "103858534"
---
# <a name="theme-file-format"></a><span data-ttu-id="daa66-105">Designdatei Format</span><span class="sxs-lookup"><span data-stu-id="daa66-105">Theme File Format</span></span>

<span data-ttu-id="daa66-106">In diesem Dokument wird das Format der Designdateien (. Theme) erläutert.</span><span class="sxs-lookup"><span data-stu-id="daa66-106">This document discusses the format of Theme (.theme) files.</span></span> <span data-ttu-id="daa66-107">Bei einer. Theme-Datei handelt es sich um eine ini-Textdatei, die in Abschnitte unterteilt ist, die visuelle Elemente angeben, die auf einem Windows-Desktop angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="daa66-107">A .theme file is a .ini text file that is divided into sections, which specify visual elements that appear on a Windows desktop.</span></span> <span data-ttu-id="daa66-108">Abschnittsnamen werden in eckige Klammern ( \[ \] ) in der INI-Datei eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="daa66-108">Section names are wrapped in brackets (\[\]) in the .ini file.</span></span>

<span data-ttu-id="daa66-109">Ein neues Dateiformat (...) wurde mit Windows 7 eingeführt, um Benutzern die gemeinsame Nutzung von Designs zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="daa66-109">A new file format, .themepack, was introduced with Windows 7 to help users share themes.</span></span> <span data-ttu-id="daa66-110">Designs können in der Personalisierungs-Systemsteuerung nur in Windows 7 Home Premium oder höher oder nur unter Windows Server 2008 R2 ausgewählt werden, wenn die Desktop Komponente installiert ist.</span><span class="sxs-lookup"><span data-stu-id="daa66-110">Themes can be selected in the Personalization Control Panel only in Windows 7 Home Premium or higher, or only on Windows Server 2008 R2 when the Desktop component is installed.</span></span>

<span data-ttu-id="daa66-111">Die folgenden Themen werden in diesem Artikel erläutert.</span><span class="sxs-lookup"><span data-stu-id="daa66-111">The following topics are discussed in this article.</span></span>

-   [<span data-ttu-id="daa66-112">Erstellen einer Designdatei</span><span class="sxs-lookup"><span data-stu-id="daa66-112">Creating a Theme File</span></span>](#creating-a-theme-file)
-   [<span data-ttu-id="daa66-113">Beschreibung einer Designdatei</span><span class="sxs-lookup"><span data-stu-id="daa66-113">Description of a Theme File</span></span>](#description-of-a-theme-file)
    -   <span data-ttu-id="daa66-114">[\[Design \] Abschnitt](#theme-section)</span><span class="sxs-lookup"><span data-stu-id="daa66-114">[\[Theme\] Section](#theme-section)</span></span>
    -   <span data-ttu-id="daa66-115">[\[Bereich mit den Farben der Systemsteuerung \\ \]](#control-panelcolors-section)</span><span class="sxs-lookup"><span data-stu-id="daa66-115">[\[Control Panel\\Colors\] Section](#control-panelcolors-section)</span></span>
    -   <span data-ttu-id="daa66-116">[\[Abschnitt "System Steuerungs \\ Cursor" \]](#control-panelcursors-section)</span><span class="sxs-lookup"><span data-stu-id="daa66-116">[\[Control Panel\\Cursors\] Section](#control-panelcursors-section)</span></span>
    -   <span data-ttu-id="daa66-117">[\[Bereich "Desktop" der Systemsteuerung \\ \]](#control-paneldesktop-section)</span><span class="sxs-lookup"><span data-stu-id="daa66-117">[\[Control Panel\\Desktop\] Section](#control-paneldesktop-section)</span></span>
    -   <span data-ttu-id="daa66-118">[\[Abschnitt "Diashow" \]](#slideshow-section)</span><span class="sxs-lookup"><span data-stu-id="daa66-118">[\[Slideshow\] Section](#slideshow-section)</span></span>
    -   <span data-ttu-id="daa66-119">[\[\]Metrikabschnitt](#metrics-section)</span><span class="sxs-lookup"><span data-stu-id="daa66-119">[\[Metrics\] Section](#metrics-section)</span></span>
    -   <span data-ttu-id="daa66-120">[\[Visueller Stile ( \] Abschnitt)](#visual-styles-section)</span><span class="sxs-lookup"><span data-stu-id="daa66-120">[\[Visual Styles\] Section](#visual-styles-section)</span></span>
    -   <span data-ttu-id="daa66-121">[\[Abschnitte "Sounds" \] und " \[ appevents" \] (Sounds)](#sounds-and-appevents-sections-sounds)</span><span class="sxs-lookup"><span data-stu-id="daa66-121">[\[Sounds\] and \[AppEvents\] Sections (Sounds)](#sounds-and-appevents-sections-sounds)</span></span>
    -   <span data-ttu-id="daa66-122">[\[Start \] Abschnitt](#boot-section)</span><span class="sxs-lookup"><span data-stu-id="daa66-122">[\[Boot\] Section](#boot-section)</span></span>
    -   <span data-ttu-id="daa66-123">[\[Masterthemeselector ( \] Abschnitt)](#masterthemeselector-section)</span><span class="sxs-lookup"><span data-stu-id="daa66-123">[\[MasterThemeSelector\] Section](#masterthemeselector-section)</span></span>
-   [<span data-ttu-id="daa66-124">Beispiel für eine Designdatei</span><span class="sxs-lookup"><span data-stu-id="daa66-124">Example of a Theme File</span></span>](#example-of-a-theme-file)
-   [<span data-ttu-id="daa66-125">Designdateien werden installiert.</span><span class="sxs-lookup"><span data-stu-id="daa66-125">Installing Theme Files</span></span>](#installing-theme-files)
-   [<span data-ttu-id="daa66-126">Designpakete</span><span class="sxs-lookup"><span data-stu-id="daa66-126">Theme Packs</span></span>](#theme-packs)
-   [<span data-ttu-id="daa66-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="daa66-127">Related topics</span></span>](#related-topics)

## <a name="creating-a-theme-file"></a><span data-ttu-id="daa66-128">Erstellen einer Designdatei</span><span class="sxs-lookup"><span data-stu-id="daa66-128">Creating a Theme File</span></span>

<span data-ttu-id="daa66-129">Eine. Design-Datei ermöglicht es Ihnen, die Darstellung bestimmter Desktop Elemente zu ändern.</span><span class="sxs-lookup"><span data-stu-id="daa66-129">A .theme file enables you to change the appearance of certain desktop elements.</span></span> <span data-ttu-id="daa66-130">Sie können eine. Theme-Datei auf zwei Arten erstellen oder ändern:</span><span class="sxs-lookup"><span data-stu-id="daa66-130">You can create or modify a .theme file in two ways:</span></span>

-   <span data-ttu-id="daa66-131">Ändern Sie die Personalisierungs-oder Anzeigeeinstellungen in der Systemsteuerung, und speichern Sie die Einstellungen als Designdatei.</span><span class="sxs-lookup"><span data-stu-id="daa66-131">Modify personalization or display settings in Control Panel and save the settings as a .theme file.</span></span> <span data-ttu-id="daa66-132">Anweisungen hierzu finden Sie in der Windows-Hilfe.</span><span class="sxs-lookup"><span data-stu-id="daa66-132">See your Windows Help for instructions.</span></span>
-   <span data-ttu-id="daa66-133">Erstellen Sie manuell eine. Design-Datei, um ein höheres Maß an Kontrolle über die Details Ihres Designs zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="daa66-133">Create a .theme file manually for a greater level of control over the details of your theme.</span></span>

<span data-ttu-id="daa66-134">Um das Design für andere Benutzer verfügbar zu machen, müssen Sie die. Theme-Datei sowie die Hintergrundbild-, Bildschirmschoner-und Symbol Dateien angeben.</span><span class="sxs-lookup"><span data-stu-id="daa66-134">To make your theme available to other users, you must supply your .theme file, as well as the background picture, screen saver, and icons files.</span></span> <span data-ttu-id="daa66-135">Hierfür können Sie ein Design [Pack](#theme-packs)verwenden.</span><span class="sxs-lookup"><span data-stu-id="daa66-135">You can do this with a [theme pack](#theme-packs).</span></span>

## <a name="description-of-a-theme-file"></a><span data-ttu-id="daa66-136">Beschreibung einer Designdatei</span><span class="sxs-lookup"><span data-stu-id="daa66-136">Description of a Theme File</span></span>

<span data-ttu-id="daa66-137">Designdateien sind einige erforderliche und optionale Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="daa66-137">Theme files have a number of required and optional sections.</span></span> <span data-ttu-id="daa66-138">Im folgenden werden die Abschnitte der Designdateien beschrieben und Beispiele zum Angeben von Änderungen für die verschiedenen Elemente bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="daa66-138">The following describe the sections of .theme files and provide examples of how to specify changes for the different elements.</span></span>

### <a name="theme-section"></a><span data-ttu-id="daa66-139">\[Design \] Abschnitt</span><span class="sxs-lookup"><span data-stu-id="daa66-139">\[Theme\] Section</span></span>

> [!Note]  
> <span data-ttu-id="daa66-140">Dieser Abschnitt ist optional.</span><span class="sxs-lookup"><span data-stu-id="daa66-140">This section is optional.</span></span> <span data-ttu-id="daa66-141">Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, verwendet das System Standardeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="daa66-141">If you do not include this section in your .theme file, the system uses default settings.</span></span>

 

<span data-ttu-id="daa66-142">Der Abschnitt "Design" \[ \] gibt den Namen des benutzerdefinierten Designs an und gibt das Markenlogo und die Desktop Symbole Ihres Designs an.</span><span class="sxs-lookup"><span data-stu-id="daa66-142">The \[Theme\] section identifies the name of your custom theme and specifies your theme's brand logo and desktop icons.</span></span>

<span data-ttu-id="daa66-143">Der erste Teil des Design \[ \] Abschnitts enthält die folgenden beiden Elemente:</span><span class="sxs-lookup"><span data-stu-id="daa66-143">The first part of the \[Theme\] section contains the following two elements:</span></span>



| <span data-ttu-id="daa66-144">Element</span><span class="sxs-lookup"><span data-stu-id="daa66-144">Element</span></span>                                                                                                                    | <span data-ttu-id="daa66-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="daa66-145">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daa66-146">Display Name = Name</span><span class="sxs-lookup"><span data-stu-id="daa66-146">DisplayName=name</span></span><br/> <span data-ttu-id="daa66-147">oder</span><span class="sxs-lookup"><span data-stu-id="daa66-147">or</span></span><br/> <span data-ttu-id="daa66-148">Display Name = @module ,-stringID</span><span class="sxs-lookup"><span data-stu-id="daa66-148">DisplayName=@module,-stringId</span></span><br/> <span data-ttu-id="daa66-149">Beispiel: Display Name = @themeui.dll ,-2013</span><span class="sxs-lookup"><span data-stu-id="daa66-149">example: DisplayName=@themeui.dll,-2013</span></span> | <span data-ttu-id="daa66-150">Display Name ist der Design Name, der in der Personalisierungs-Systemsteuerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="daa66-150">DisplayName is the theme name that will show up in the Personalization Control Panel.</span></span> <span data-ttu-id="daa66-151">Dabei kann es sich um eine Zeichenfolge oder einen Verweis auf einen lokalisierten Namen handeln.</span><span class="sxs-lookup"><span data-stu-id="daa66-151">It can be a string or a reference to a localized name.</span></span><br/> <span data-ttu-id="daa66-152">Dieses Feld ist optional.</span><span class="sxs-lookup"><span data-stu-id="daa66-152">This field is optional.</span></span> <span data-ttu-id="daa66-153">Wenn Sie nicht vorhanden ist, wird der Design Dateiname als Design Name verwendet.</span><span class="sxs-lookup"><span data-stu-id="daa66-153">If it is missing, the theme filename is used as the theme name.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="daa66-154">Brandimage = Pfad zum Bild</span><span class="sxs-lookup"><span data-stu-id="daa66-154">BrandImage=path to image</span></span><br/> <span data-ttu-id="daa66-155">Beispiel: Brandimage = c: \\ Fabrikam \\brand.png</span><span class="sxs-lookup"><span data-stu-id="daa66-155">example: BrandImage=c:\\Fabrikam\\brand.png</span></span><br/>                                 | <span data-ttu-id="daa66-156">**Windows 7 und** höher Brandimage gibt den Pfad zu einer Branding-Grafikdatei an, die in der Design Vorschau in der Personalisierungs-Systemsteuerung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="daa66-156">**Windows 7 and later** BrandImage specifies the path to a branded graphic file that is incorporated in the theme preview in the Personalization Control Panel.</span></span><br/> <span data-ttu-id="daa66-157">Die Symbol Grafik muss eine PNG-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="daa66-157">The icon graphic must be a PNG file.</span></span> <span data-ttu-id="daa66-158">Die Grafik wird auf 80 x 240 Pixel skaliert. es wird daher empfohlen, ein Bild dieser Größe bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="daa66-158">The graphic is scaled to 80x240 pixels, so it is recommended that you provide an image of that size.</span></span> <span data-ttu-id="daa66-159">Der Design Katalog respektiert die transparenten Bereiche Ihres Marken Symbols.</span><span class="sxs-lookup"><span data-stu-id="daa66-159">The Theme gallery respects the transparent regions of your brand icon.</span></span><br/> <span data-ttu-id="daa66-160">Dieses Feld ist optional.</span><span class="sxs-lookup"><span data-stu-id="daa66-160">This field is optional.</span></span> <span data-ttu-id="daa66-161">Wenn Sie nicht vorhanden ist, wird kein Logo als symbolsymbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="daa66-161">If it is missing, no logo is displayed as the theme icon.</span></span><br/> |



 

<span data-ttu-id="daa66-162">Im restlichen Abschnitt des \[ Themas Theme werden \] benutzerdefinierte Symbole für Desktop Features wie Computer, eigene Dokumente, Netzwerk und Papierkorb angegeben.</span><span class="sxs-lookup"><span data-stu-id="daa66-162">The rest of the \[Theme\] section specifies custom icons for desktop features like Computer, My Documents, Network, and Recycle Bin.</span></span> <span data-ttu-id="daa66-163">Wenn Sie keine benutzerdefinierten Desktop Symbole angeben, zeigt der Desktop die standardmäßigen Desktop Symbole des Systems an.</span><span class="sxs-lookup"><span data-stu-id="daa66-163">If you do not specify custom desktop icons, the desktop displays the system default desktop icons.</span></span>

<span data-ttu-id="daa66-164">Im folgenden finden Sie zwei Beispiele dafür, wie eine. Theme-Datei das **Computer** Symbol festlegt.</span><span class="sxs-lookup"><span data-stu-id="daa66-164">The following are two examples of how a .theme file sets the **Computer** icon.</span></span>


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



<span data-ttu-id="daa66-165">Im folgenden sind die Werte für die Standard Desktop Symbole in Windows 7 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="daa66-165">The following are values for the default desktop icons in Windows 7.</span></span>


```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55
```



### <a name="control-panelcolors-section"></a><span data-ttu-id="daa66-166">\[Bereich mit den Farben der Systemsteuerung \\ \]</span><span class="sxs-lookup"><span data-stu-id="daa66-166">\[Control Panel\\Colors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="daa66-167">Dieser Abschnitt ist optional.</span><span class="sxs-lookup"><span data-stu-id="daa66-167">This section is optional.</span></span> <span data-ttu-id="daa66-168">Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, verwendet das System Standardeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="daa66-168">If you do not include this section in your .theme file, the system uses default settings.</span></span> <span data-ttu-id="daa66-169">Wenn Ihr Design den visuellen Aero-Stil verwendet, sollten Sie das Überschreiben der Standardwerte in diesem Abschnitt vermeiden.</span><span class="sxs-lookup"><span data-stu-id="daa66-169">If your theme uses the Aero visual style, you should avoid overriding the default values in this section.</span></span>

 

<span data-ttu-id="daa66-170">Die Farbe von Elementen, z. b. Scrollleisten, Text und Schaltflächen, ist anpassbar.</span><span class="sxs-lookup"><span data-stu-id="daa66-170">The color of elements, such as scroll bars, text, and buttons, are customizable.</span></span> <span data-ttu-id="daa66-171">Die. Theme-Datei gibt die RGB-Werte an, die für diese Elemente geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="daa66-171">The .theme file specifies the RGB values to change for these elements.</span></span> <span data-ttu-id="daa66-172">Die Werte überschreiben die Standardwerte des visuellen Stils und werden verwendet, wenn Ihr Design auf Windows Classic, Windows 7 Basic oder hoher Kontrast Designs basiert.</span><span class="sxs-lookup"><span data-stu-id="daa66-172">The values override the default values of the visual style and are used when your theme is based on Windows Classic, Windows 7 Basic, or High Contrast themes.</span></span>

<span data-ttu-id="daa66-173">Im folgenden finden Sie ein Beispiel für die Festlegung von Farben.</span><span class="sxs-lookup"><span data-stu-id="daa66-173">Following is an example of how colors are set.</span></span>


```
[Control Panel\Colors]
ActiveTitle=10 36 106
Background=166 202 240
Hilight=10 36 106
HilightText=255 255 255
TitleText=255 255 255
Window=255 255 255
WindowText=0 0 0
Scrollbar=212 208 200
InactiveTitle=128 128 128
Menu=212 208 200
WindowFrame=0 0 0
MenuText=0 0 0
ActiveBorder=212 208 200
InactiveBorder=212 208 200
AppWorkspace=128 128 128
ButtonFace=212 208 200
ButtonShadow=128 128 128
GrayText=128 128 128
ButtonText=0 0 0
InactiveTitleText=212 208 200
ButtonHilight=255 255 255
ButtonDkShadow=64 64 64
ButtonLight=212 208 200
InfoText=0 0 0
InfoWindow=255 255 225
GradientActiveTitle=166 202 240
GradientInactiveTitle=192 192 192
```



### <a name="control-panelcursors-section"></a><span data-ttu-id="daa66-174">\[Abschnitt "System Steuerungs \\ Cursor" \]</span><span class="sxs-lookup"><span data-stu-id="daa66-174">\[Control Panel\\Cursors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="daa66-175">Dieser Abschnitt ist optional.</span><span class="sxs-lookup"><span data-stu-id="daa66-175">This section is optional.</span></span> <span data-ttu-id="daa66-176">Wenn Sie diesen Abschnitt nicht in die. Theme-Datei einschließen, verwendet das System standardcursorn.</span><span class="sxs-lookup"><span data-stu-id="daa66-176">If you do not include this section in your .theme file, the system uses default cursors.</span></span>

 

<span data-ttu-id="daa66-177">Ein Design kann auch die Darstellung von Cursorn ändern.</span><span class="sxs-lookup"><span data-stu-id="daa66-177">A theme can also change the appearance of cursors.</span></span> <span data-ttu-id="daa66-178">Zu diesem Zweck erstellen Sie cur-Dateien, um die standardmäßigen Windows-Cursor zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="daa66-178">To do so, you create .cur files to replace the default Windows cursors.</span></span> <span data-ttu-id="daa66-179">Das folgende Beispiel zeigt eine. Design-Datei, die die Cursor für ein Design mit dem Namen " *Sports*" definiert.</span><span class="sxs-lookup"><span data-stu-id="daa66-179">The following example is from a .theme file that defines the cursors for a theme called *Sports*.</span></span>


```
[Control Panel\Cursors]
Arrow=%SystemRoot%\sports_arrow.cur
Help=%SystemRoot%\sports_help.cur
AppStarting=%SystemRoot%\sports_wait.ani
Wait=%SystemRoot%\sports_busy.ani
NWPen=%SystemRoot%\sports_pen.cur
No=%SystemRoot%\sports_no.cur
SizeNS=%SystemRoot%\sports_size_ns.cur
SizeWE=%SystemRoot%\sports_size_we.cur
Crosshair=%SystemRoot%\sports_cross.cur
IBeam=%SystemRoot%\sports_beam.cur
SizeNWSE=%SystemRoot%\sports_size_nwse.cur
SizeNESW=%SystemRoot%\sports_size_nesw.cur
SizeAll=%SystemRoot%\sports_move.cur
UpArrow=%SystemRoot%\sports_up.cur
DefaultValue=Windows default
```



### <a name="control-paneldesktop-section"></a><span data-ttu-id="daa66-180">\[Bereich "Desktop" der Systemsteuerung \\ \]</span><span class="sxs-lookup"><span data-stu-id="daa66-180">\[Control Panel\\Desktop\] Section</span></span>

> [!Note]  
> <span data-ttu-id="daa66-181">Dieser Abschnitt ist ein Pflichtabschnitt.</span><span class="sxs-lookup"><span data-stu-id="daa66-181">This section is required.</span></span> <span data-ttu-id="daa66-182">Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, ignoriert das System das Design und zeigt das Design in der Systemsteuerung nicht an.</span><span class="sxs-lookup"><span data-stu-id="daa66-182">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="daa66-183">Sie können einen benutzerdefinierten Desktop Hintergrund erstellen und einen Pfad zur Bilddatei angeben.</span><span class="sxs-lookup"><span data-stu-id="daa66-183">You can create a custom desktop background and specify a path to the image file.</span></span> <span data-ttu-id="daa66-184">Im folgenden Beispiel wird gezeigt, wie die Desktop Darstellung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="daa66-184">The following example shows how to modify the desktop appearance.</span></span>


```
[Control Panel\Desktop]
Wallpaper=%WinDir%\web\wallpaper\Windows\img0.jpg
; The path to the wallpaper picture can point to a 
; .bmp, .gif, .jpg, .png, or .tif file.

TileWallpaper=0
; 0: The wallpaper picture should not be tiled 
; 1: The wallpaper picture should be tiled 

WallpaperStyle=2
; 0:  The image is centered if TileWallpaper=0 or tiled if TileWallpaper=1
; 2:  The image is stretched to fill the screen
; 6:  The image is resized to fit the screen while maintaining the aspect 
      ratio. (Windows 7 and later)
; 10: The image is resized and cropped to fill the screen while maintaining 
      the aspect ratio. (Windows 7 and later)
```



### <a name="slideshow-section"></a><span data-ttu-id="daa66-185">\[Abschnitt "Diashow" \]</span><span class="sxs-lookup"><span data-stu-id="daa66-185">\[Slideshow\] Section</span></span>

<span data-ttu-id="daa66-186">**Windows 7 und höher.**</span><span class="sxs-lookup"><span data-stu-id="daa66-186">**Windows 7 and later.**</span></span>

> [!Note]  
> <span data-ttu-id="daa66-187">Dieser Abschnitt ist optional.</span><span class="sxs-lookup"><span data-stu-id="daa66-187">This section is optional.</span></span> <span data-ttu-id="daa66-188">Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, verwendet das System das Desktop Hintergrundbild, das im \[ Abschnitt Desktop der Systemsteuerung angegeben ist \\ \] .</span><span class="sxs-lookup"><span data-stu-id="daa66-188">If you do not include this section in your .theme file, the system uses the desktop background image specified in the \[Control Panel\\Desktop\] section.</span></span> <span data-ttu-id="daa66-189">Wenn Sie diesen Abschnitt einschließen, müssen Sie hier die Einstellungen für "Folie anzeigen" angeben.</span><span class="sxs-lookup"><span data-stu-id="daa66-189">If you include this section, you must specify slide show settings here.</span></span>

 

<span data-ttu-id="daa66-190">Der Hintergrund des Designs kann eine Folie darstellen, die entweder lokal oder von Bildern gespeichert ist, die von einem RSS-Feed bedient werden.</span><span class="sxs-lookup"><span data-stu-id="daa66-190">Your theme's background can be a slide show either of images stored locally or of images served by an RSS feed.</span></span> <span data-ttu-id="daa66-191">Der \[ Abschnitt "Diashow" \] der Datei enthält die folgenden Attribute:</span><span class="sxs-lookup"><span data-stu-id="daa66-191">The \[Slideshow\] section of the file contains the following attributes:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daa66-192">Attribut</span><span class="sxs-lookup"><span data-stu-id="daa66-192">Attribute</span></span></th>
<th><span data-ttu-id="daa66-193">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="daa66-193">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="daa66-194">Intervall = Anzahl der Millisekunden</span><span class="sxs-lookup"><span data-stu-id="daa66-194">Interval=number of milliseconds</span></span></td>
<td><span data-ttu-id="daa66-195">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="daa66-195">Required.</span></span> <span data-ttu-id="daa66-196">Interval ist eine Zahl, die bestimmt, wie oft der Hintergrund geändert wird.</span><span class="sxs-lookup"><span data-stu-id="daa66-196">Interval is a number that determines how often the background changes.</span></span> <span data-ttu-id="daa66-197">Der Wert wird in Millisekunden gemessen.</span><span class="sxs-lookup"><span data-stu-id="daa66-197">It is measured in milliseconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="daa66-198">Shuffle = 0 oder 1</span><span class="sxs-lookup"><span data-stu-id="daa66-198">Shuffle=0 or 1</span></span></td>
<td><span data-ttu-id="daa66-199">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="daa66-199">Required.</span></span> <span data-ttu-id="daa66-200">Shuffle gibt an, ob der Hintergrund heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="daa66-200">Shuffle identifies whether the background shuffles.</span></span><br/> <span data-ttu-id="daa66-201">0 = Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="daa66-201">0 = Disabled</span></span><br/> <span data-ttu-id="daa66-202">1 = Aktiviert</span><span class="sxs-lookup"><span data-stu-id="daa66-202">1 = Enabled</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="daa66-203">RSSFeed = URL zum RSS-Feed</span><span class="sxs-lookup"><span data-stu-id="daa66-203">RSSFeed=URL to RSS feed</span></span></td>
<td><span data-ttu-id="daa66-204">Erforderlich, wenn imagesrootpath nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="daa66-204">Required if ImagesRootPath is not specified.</span></span> <span data-ttu-id="daa66-205">RSSFeed gibt einen RSS-Feed an, der als Hintergrund Bildschirm Anzeige verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="daa66-205">RSSFeed specifies an RSS feed to use as the background slide show.</span></span> <span data-ttu-id="daa66-206">Damit der Feed funktioniert, müssen Sie auf hochauflösende Images verweisen, die dem &quot; Gehäuse &quot; Standard entsprechen, der von der <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS-Plattform</a>verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="daa66-206">For the feed to work, you need to reference high-resolution images adhering to the &quot;enclosures&quot; standard used by the <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS Platform</a>.</span></span> <span data-ttu-id="daa66-207">Aufgrund dieser Einschränkung müssen Designdateien, die einen RSS-Feed enthalten, manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="daa66-207">Because of this limitation, .theme files that include an RSS feed must be created manually.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="daa66-208">RSSFeed und imagesrootpath können nicht gleichzeitig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="daa66-208">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="daa66-209">Imagesrootpath = Pfad zum Bildordner</span><span class="sxs-lookup"><span data-stu-id="daa66-209">ImagesRootPath=path to image folder</span></span></td>
<td><span data-ttu-id="daa66-210">Erforderlich, wenn RSSFeed nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="daa66-210">Required if RSSFeed is not specified.</span></span> <span data-ttu-id="daa66-211">Imagesrootpath gibt einen Pfad zu einem Satz von Bildern an, den Sie als Hintergrund Bildschirm Anzeige verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="daa66-211">ImagesRootPath specifies a path to a set of images you want to use as the background slide show.</span></span> <span data-ttu-id="daa66-212">Bilder in Unterordnern sind nicht in der Folien Anzeige enthalten.</span><span class="sxs-lookup"><span data-stu-id="daa66-212">Images in subfolders are not included in the slide show.</span></span><br/> <span data-ttu-id="daa66-213">Imagesrootpath unterstützt die Ersetzung von Umgebungsvariablen im Pfad.</span><span class="sxs-lookup"><span data-stu-id="daa66-213">ImagesRootPath supports Environment Variable substitutions in the path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="daa66-214">RSSFeed und imagesrootpath können nicht gleichzeitig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="daa66-214">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="daa66-215">Element<em>N</em>Pfad = Pfad (e) zu bestimmten Bildern</span><span class="sxs-lookup"><span data-stu-id="daa66-215">Item<em>N</em>Path=path(s) to specific image(s)</span></span></td>
<td><span data-ttu-id="daa66-216">Zur Verwendung mit imagesrootpath.</span><span class="sxs-lookup"><span data-stu-id="daa66-216">For use with ImagesRootPath.</span></span> <br/> <span data-ttu-id="daa66-217">Element<em>N</em>Pfad gibt Pfade zu bestimmten Bildern an, sodass Sie die Folien Anzeige auf bestimmte Bilder anstatt auf alle Bilder in einem Ordner beschränken können.</span><span class="sxs-lookup"><span data-stu-id="daa66-217">Item<em>N</em>Path specifies paths to specific images, so that you can limit the slide show to particular images instead of all images in a folder.</span></span> <span data-ttu-id="daa66-218">Wenn keine Pfade angegeben werden, werden alle Bilder im imagesrootpath-Pfad in der Folien Anzeige verwendet, einschließlich der Bilder, die nach dem Erstellen und Installieren des Designs hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="daa66-218">If no paths are specified, all images in the ImagesRootPath path are used in the slide show, including images added after creating and installing the theme.</span></span><br/> <span data-ttu-id="daa66-219">Element<em>N</em>Path unterstützt die Ersetzung von Umgebungsvariablen im Pfad.</span><span class="sxs-lookup"><span data-stu-id="daa66-219">Item<em>N</em>Path supports Environment Variable substitutions in the path.</span></span> <span data-ttu-id="daa66-220"><em>N</em> ist 0, 1, 2 usw.</span><span class="sxs-lookup"><span data-stu-id="daa66-220"><em>N</em> is 0, 1, 2, and so on.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="daa66-221">In den folgenden Beispielen wird veranschaulicht, wie eine. Theme-Datei die Bildschirm Anzeige angibt, um einen lokal gespeicherten Satz von Bildern einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="daa66-221">The following examples show how a .theme file specifies the slide show to include a set of images stored locally.</span></span>


```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%SystemRoot%\Web\Wallpaper
```




```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg
```



<span data-ttu-id="daa66-222">Das folgende Beispiel ist eine Vorlage für eine. Design-Datei, mit der eine Desktop-Hintergrund Folie mit Bildern aus einem RSS-Feed erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="daa66-222">The following example is a template for a .theme file that creates a desktop background slide show using images from an RSS feed.</span></span> <span data-ttu-id="daa66-223">Führen Sie die folgenden Schritte aus, um die Vorlage anzupassen:</span><span class="sxs-lookup"><span data-stu-id="daa66-223">Follow these steps to customize the template:</span></span>

1.  <span data-ttu-id="daa66-224">Kopieren Sie das folgende Beispiel, und fügen Sie es in einen Text-Editor ein.</span><span class="sxs-lookup"><span data-stu-id="daa66-224">Copy the following example and paste it into a text editor.</span></span>
2.  <span data-ttu-id="daa66-225">Ersetzen Sie {ThemeName} durch den Namen, der in der Personalisierungs-Systemsteuerung in der Design-Galerie angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="daa66-225">Replace {themename} with the name you want to appear in the Personalization Control Panel themes gallery.</span></span>
3.  <span data-ttu-id="daa66-226">Ersetzen Sie {rssfeedurl} durch den vollständigen Pfad zu einem kompatiblen RSS-Feed.</span><span class="sxs-lookup"><span data-stu-id="daa66-226">Replace {rssfeedurl} with the full path to a compatible RSS feed.</span></span>
4.  <span data-ttu-id="daa66-227">Speichern Sie die Änderungen als Datei mit der Erweiterung ". Theme".</span><span class="sxs-lookup"><span data-stu-id="daa66-227">Save the changes as a file with the ".theme" extension.</span></span>


```
[Theme]
DisplayName={themename}

[Slideshow]
Interval=1800000
Shuffle=1
RssFeed={rssfeedurl}

[Control Panel\Desktop]
TileWallpaper=0
WallpaperStyle=10
Pattern=

[Control Panel\Cursors]
AppStarting=%SystemRoot%\cursors\aero_working.ani
Arrow=%SystemRoot%\cursors\aero_arrow.cur
Crosshair=
Hand=%SystemRoot%\cursors\aero_link.cur
Help=%SystemRoot%\cursors\aero_helpsel.cur
IBeam=
No=%SystemRoot%\cursors\aero_unavail.cur
NWPen=%SystemRoot%\cursors\aero_pen.cur
SizeAll=%SystemRoot%\cursors\aero_move.cur
SizeNESW=%SystemRoot%\cursors\aero_nesw.cur
SizeNS=%SystemRoot%\cursors\aero_ns.cur
SizeNWSE=%SystemRoot%\cursors\aero_nwse.cur
SizeWE=%SystemRoot%\cursors\aero_ew.cur
UpArrow=%SystemRoot%\cursors\aero_up.cur
Wait=%SystemRoot%\cursors\aero_busy.ani
DefaultValue=Windows Aero
Link=

[VisualStyles]
Path=%SystemRoot%\resources\themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X6B74B8FC
Transparency=1

[MasterThemeSelector]
MTSM=DABJDKT
```



### <a name="metrics-section"></a><span data-ttu-id="daa66-228">\[\]Metrikabschnitt</span><span class="sxs-lookup"><span data-stu-id="daa66-228">\[Metrics\] Section</span></span>

> [!Note]  
> <span data-ttu-id="daa66-229">Dieser Abschnitt ist optional.</span><span class="sxs-lookup"><span data-stu-id="daa66-229">This section is optional.</span></span> <span data-ttu-id="daa66-230">Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, verwendet das System Standardeinstellungen des visuellen Stils.</span><span class="sxs-lookup"><span data-stu-id="daa66-230">If you do not include this section in your .theme file, the system uses default visual style settings.</span></span>

 

<span data-ttu-id="daa66-231">Sie können Systemmetriken in einer. Theme-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="daa66-231">You can specify system metrics in a .theme file.</span></span> <span data-ttu-id="daa66-232">Systemmetriken sind die Dimensionen verschiedener Anzeigeelemente, wie z. b. die Rahmenbreite des Fensters, die Symbol Höhe oder die Breite der Bild Lauf Leiste.</span><span class="sxs-lookup"><span data-stu-id="daa66-232">System metrics are the dimensions of various display elements, such as the window border width, icon height, or scroll bar width.</span></span> <span data-ttu-id="daa66-233">Die nonclientmetrics-und iconmetrics-Werte sind binäre Strukturen, die von nonclientmetrics und iconmetrics in winuser. h definiert werden.</span><span class="sxs-lookup"><span data-stu-id="daa66-233">The NonclientMetrics and IconMetrics values are binary structures defined by NONCLIENTMETRICS and ICONMETRICS in winuser.h.</span></span> <span data-ttu-id="daa66-234">Im folgenden finden Sie ein Beispiel für das Ändern von Systemmetriken.</span><span class="sxs-lookup"><span data-stu-id="daa66-234">Following is an example of how to change system metrics.</span></span>


```
[Control Panel\Desktop\WindowMetrics]

[Metrics]
IconMetrics=76 0 0 0 139 0 0 0 139 0 0 0 1 0 0 0 245
255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0 0 0 0
0 0 0 0 84 97 104 111 109 97 0 119 0 0 7 0 0 0 0 0 216
31 7 0 28 52 1 1 216 31 7 0 176 36 1 1 
NonclientMetrics=84 1 0 0 1 0 0 0 16 0 0 0 16 0 0 0 18
0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
188 2 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 12 0 0 0
15 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 188 2
0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 80 37 11
0 0 0 0 0 140 221 6 0 227 115 247 119 2 40 11 0 7 0 0
0 18 0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0
0 0 0 144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0
0 0 0 0 0 60 222 6 0 50 71 252 119 120 1 7 0 76 73 252
119 8 6 7 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 119 0
0 7 0 120 1 7 0 120 1 7 0 40 37 11 0 120 1 7 0 120 1 7
0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0
0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 92 1 0 0 136 4
0 0 40 37 1 1 0 0 7 0 184 221 6 0 46 75 232 119 
```



### <a name="visual-styles-section"></a><span data-ttu-id="daa66-235">\[Visueller Stile ( \] Abschnitt)</span><span class="sxs-lookup"><span data-stu-id="daa66-235">\[Visual Styles\] Section</span></span>

> [!Note]  
> <span data-ttu-id="daa66-236">Dieser Abschnitt ist ein Pflichtabschnitt.</span><span class="sxs-lookup"><span data-stu-id="daa66-236">This section is required.</span></span> <span data-ttu-id="daa66-237">Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, ignoriert das System das Design und zeigt das Design in der Systemsteuerung nicht an.</span><span class="sxs-lookup"><span data-stu-id="daa66-237">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="daa66-238">Sie können spezifische Informationen zur Größe und Farbe der Desktop Elemente in msstyles-Dateien angeben.</span><span class="sxs-lookup"><span data-stu-id="daa66-238">You can supply specific information concerning the size and color of desktop elements in .msstyles files.</span></span> <span data-ttu-id="daa66-239">Die Farb-und Größen Abschnitte von. Design-Dateien können durch msstyles-Dateien ersetzt werden, die es Ihnen ermöglichen, Desktop Elemente ausführlicher zu ändern.</span><span class="sxs-lookup"><span data-stu-id="daa66-239">The color and size sections of .theme files can be replaced by .msstyles files which enable you to modify desktop elements in more detail.</span></span> <span data-ttu-id="daa66-240">Diese Dateien werden im Abschnitt visuelle Stile einer. Theme-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="daa66-240">These files are specified in the visual styles section of a .theme file.</span></span> <span data-ttu-id="daa66-241">Im folgenden finden Sie ein Beispiel für einen Abschnitt mit visuellen Stilen.</span><span class="sxs-lookup"><span data-stu-id="daa66-241">Following is an example of a visual styles section.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



<span data-ttu-id="daa66-242">Das Hinzufügen eines Path-Elements zu einer. msstyles-Datei ist optional.</span><span class="sxs-lookup"><span data-stu-id="daa66-242">Adding a Path element to a .msstyles file is optional.</span></span> <span data-ttu-id="daa66-243">Wenn Sie einen Pfad angeben, sollten Sie die Metriken und farbabschnitte aus der. Theme-Datei entfernen.</span><span class="sxs-lookup"><span data-stu-id="daa66-243">If you supply a path, you should remove the metrics and color sections from the .theme file.</span></span> <span data-ttu-id="daa66-244">Wenn diese Abschnitte entfernt werden, stammen die Farben, Schriftarten und Größen für ein Design aus der msstyles-Datei und stimmen mit der Absicht des Autors von msstyles.</span><span class="sxs-lookup"><span data-stu-id="daa66-244">When these sections are removed, the colors, fonts, and sizes for a theme come from the .msstyles file and match the .msstyles author's intent.</span></span> <span data-ttu-id="daa66-245">Wenn Sie die Metrik-und farbabschnitte nicht entfernen, können Windows-Anwendungen oder Anwendungen Zeichnungs Probleme verursachen.</span><span class="sxs-lookup"><span data-stu-id="daa66-245">Failing to remove the metric and color sections can cause Windows or applications to have drawing problems.</span></span>

<span data-ttu-id="daa66-246">**Windows Vista/Windows 7:** Wenn der Pfad auf Aero. msstyles zeigt, können Sie die gewünschte Glasfarbe angeben, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="daa66-246">**Windows Vista / Windows 7:** When the path points to Aero.msstyles, you can specify the desired Glass Color, as shown in the following example.</span></span>

<span data-ttu-id="daa66-247">**Windows 7:** Wenn der Pfad auf Aero. msstyles zeigt, können Sie auch den gewünschten Transparenz Wert angeben, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="daa66-247">**Windows 7:** When the path points to Aero.msstyles, you can also specify the desired Transparency value, as shown in the following example.</span></span>


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



<span data-ttu-id="daa66-248">Wenn die Werte colorizationcolor und Transparenz exakt mit einer System Farbe übereinstimmen, wird in der Personalisierungs-Systemsteuerung der Systemname der Farbe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="daa66-248">If the ColorizationColor and Transparency values exactly match a system color, the Personalization Control Panel displays the system name for the color.</span></span> <span data-ttu-id="daa66-249">Andernfalls ist die Farbe "Custom".</span><span class="sxs-lookup"><span data-stu-id="daa66-249">Otherwise, the color is labeled "Custom."</span></span>

<span data-ttu-id="daa66-250">Das folgende Beispiel zeigt einen VisualStyles-Abschnitt für das grundlegende Design von Windows 7.</span><span class="sxs-lookup"><span data-stu-id="daa66-250">The following shows a VisualStyles section for the Windows 7 Basic theme.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



<span data-ttu-id="daa66-251">Das folgende Beispiel zeigt einen VisualStyles-Abschnitt für das klassische Windows-Design.</span><span class="sxs-lookup"><span data-stu-id="daa66-251">The following shows a VisualStyles section for the Windows Classic theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



<span data-ttu-id="daa66-252">Das folgende Beispiel zeigt einen VisualStyles-Abschnitt für ein hoher Kontrast schwarzes Design.</span><span class="sxs-lookup"><span data-stu-id="daa66-252">The following shows a VisualStyles section for a High Contrast Black theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a><span data-ttu-id="daa66-253">\[Abschnitte "Sounds" \] und " \[ appevents" \] (Sounds)</span><span class="sxs-lookup"><span data-stu-id="daa66-253">\[Sounds\] and \[AppEvents\] Sections (Sounds)</span></span>

> [!Note]  
> <span data-ttu-id="daa66-254">Dieser Abschnitt ist optional.</span><span class="sxs-lookup"><span data-stu-id="daa66-254">This section is optional.</span></span> <span data-ttu-id="daa66-255">Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, verwendet das System standardmäßige Soundeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="daa66-255">If you do not include this section in your .theme file, the system uses default sound settings.</span></span>

 

<span data-ttu-id="daa66-256">Der Benutzer kann das **Sound** Symbol in der Systemsteuerung auswählen, um Sounds Ereignisse zuzuordnen, die in-Anwendungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="daa66-256">The user can select the **Sound** icon in Control Panel to associate sounds with events that occur in applications.</span></span> <span data-ttu-id="daa66-257">Eine WAV-Datei kann z. b. abgespielt werden, wenn eine Anwendung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="daa66-257">For example, a .wav file can play when an application is opened.</span></span> <span data-ttu-id="daa66-258">In einer. Design-Datei können WAV-Dateien angegeben werden, um die Standardwerte zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="daa66-258">A .theme file can specify .wav files to replace the default ones.</span></span> <span data-ttu-id="daa66-259">Das folgende Beispiel zeigt die erforderliche Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="daa66-259">The following example shows how to do this.</span></span>


```
[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=%WinDir%\media\tada.wav

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=%WinDir%\media\The Microsoft Sound.wav

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav
```



<span data-ttu-id="daa66-260">**Windows 7 und höher:** Sie können einen Sound Schema Namen angeben, anstatt jeden Sound separat aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="daa66-260">**Windows 7 and later:** A sound scheme name can be specified instead of listing each sound separately.</span></span>


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



<span data-ttu-id="daa66-261">Der schemeName-Wert gibt den Namen des Audioschemas oder des lokalisierten Sound Schemas an, wie im obigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="daa66-261">The SchemeName value specifies the sound scheme name or the localized sound scheme name, as shown in the example above.</span></span>

### <a name="boot-section"></a><span data-ttu-id="daa66-262">\[Start \] Abschnitt</span><span class="sxs-lookup"><span data-stu-id="daa66-262">\[Boot\] Section</span></span>

> [!Note]  
> <span data-ttu-id="daa66-263">**Bildschirmschoner sind in Windows 10 Anniversary Update und höher veraltet.**</span><span class="sxs-lookup"><span data-stu-id="daa66-263">**Screen Savers are deprecated in the Windows 10 Anniversary Update and beyond.**</span></span>

 

> [!Note]  
> <span data-ttu-id="daa66-264">Dieser Abschnitt ist optional.</span><span class="sxs-lookup"><span data-stu-id="daa66-264">This section is optional.</span></span> <span data-ttu-id="daa66-265">Wenn Sie diesen Abschnitt nicht in die. Theme-Datei einschließen, wird kein Bildschirmschoner verwendet.</span><span class="sxs-lookup"><span data-stu-id="daa66-265">If you do not include this section in your .theme file, no screen saver is used.</span></span>

 

<span data-ttu-id="daa66-266">In der. Theme-Datei können Sie den Bildschirmschoner angeben, der von Windows verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="daa66-266">In the .theme file, you can specify the screen saver for Windows to use.</span></span> <span data-ttu-id="daa66-267">Im folgenden Beispiel wird dies veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="daa66-267">The following example shows this.</span></span>


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a><span data-ttu-id="daa66-268">\[Masterthemeselector ( \] Abschnitt)</span><span class="sxs-lookup"><span data-stu-id="daa66-268">\[MasterThemeSelector\] Section</span></span>

> [!Note]  
> <span data-ttu-id="daa66-269">Dieser Abschnitt ist ein Pflichtabschnitt.</span><span class="sxs-lookup"><span data-stu-id="daa66-269">This section is required.</span></span> <span data-ttu-id="daa66-270">Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, ignoriert das System das Design und zeigt das Design in der Systemsteuerung nicht an.</span><span class="sxs-lookup"><span data-stu-id="daa66-270">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="daa66-271">Der Abschnitt "Master Design Selector" der. Theme-Datei sollte immer als ein Tag eingeschlossen werden, das angibt, dass die Datei gültig ist.</span><span class="sxs-lookup"><span data-stu-id="daa66-271">The master theme selector section of the .theme file should always be included as a tag that indicates the file is valid.</span></span> <span data-ttu-id="daa66-272">Sie haben keine Auswahl von Werten für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="daa66-272">You do not have a choice of values for this parameter.</span></span> <span data-ttu-id="daa66-273">Dies wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="daa66-273">The following shows this.</span></span>


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a><span data-ttu-id="daa66-274">Beispiel für eine Designdatei</span><span class="sxs-lookup"><span data-stu-id="daa66-274">Example of a Theme File</span></span>

<span data-ttu-id="daa66-275">Das folgende Beispiel zeigt eine komplette Designdatei.</span><span class="sxs-lookup"><span data-stu-id="daa66-275">The following example shows a complete .theme file.</span></span>


```
[Theme]
DisplayName=My Current Theme
BrandImage=c:\Fabrikam\brand.png

; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55

[Control Panel\Cursors]
Arrow=
Help=
AppStarting=
Wait=
NWPen=
No=
SizeNS=
SizeWE=
Crosshair=
IBeam=
SizeNWSE=
SizeNESW=
SizeAll=
UpArrow=
DefaultValue=Windows default

[Control Panel\Desktop]
Wallpaper=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
TileWallpaper=0
WallpaperStyle=2
Pattern=
ScreenSaveActive=0

[AppEvents\Schemes\Apps\.Default\.Default]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\AppGPFault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Maximize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuCommand]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuPopup]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Minimize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Open]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreDown]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreUp]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RingIn]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Ringout]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemAsterisk]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemDefault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\Close]
DefaultValue=

[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg

[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr

[MasterThemeSelector]
MTSM=DABJDKT
ThemeColorBPP=4

[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x856E3BA1
Transparency=1
```



## <a name="installing-theme-files"></a><span data-ttu-id="daa66-276">Designdateien werden installiert.</span><span class="sxs-lookup"><span data-stu-id="daa66-276">Installing Theme Files</span></span>

<span data-ttu-id="daa66-277">Beim Initialisieren von Windows listet das Betriebssystem die Unterverzeichnisse der ersten Ebene von% windir%- \\ Ressourcen auf, \\ um verfügbare Designs zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="daa66-277">When Windows is initialized, the operating system enumerates the first-level subdirectories of %WinDir%\\Resources\\ to identify available themes.</span></span> <span data-ttu-id="daa66-278">Die standardmäßigen Systemdateien befinden sich unter% windir% \\ Resources Designs \\ .</span><span class="sxs-lookup"><span data-stu-id="daa66-278">The system default theme files are located in %WinDir%\\Resources\\Themes.</span></span> <span data-ttu-id="daa66-279">Die Benutzer Designdateien werden unter "% windir% \\ Users \\ <username> \\ AppData \\ local \\ Microsoft \\ Windows \\ Themes" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="daa66-279">The user theme files are stored in %WinDir%\\Users\\<username>\\AppData\\Local\\Microsoft\\Windows\\Themes.</span></span>

<span data-ttu-id="daa66-280">Eine. Design-Datei weist Dateizuordnungen auf. Daher können Theme Installer-Anwendungen [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) für eine. Theme-Datei aufzurufen, um das **Personalisierungs** Fenster in der Systemsteuerung für das angegebene Design zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="daa66-280">A .theme file has file associations; therefore, theme installer applications can call [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) on a .theme file to open the **Personalization** window in Control Panel to the specified theme.</span></span>

## <a name="theme-packs"></a><span data-ttu-id="daa66-281">Designpakete</span><span class="sxs-lookup"><span data-stu-id="daa66-281">Theme Packs</span></span>

<span data-ttu-id="daa66-282">**Windows 7 und höher.**</span><span class="sxs-lookup"><span data-stu-id="daa66-282">**Windows 7 and later.**</span></span> <span data-ttu-id="daa66-283">Ein Design Pack ist eine CAB-Datei, die nicht nur die. Theme-Datei, sondern auch die Dateien enthält, die zum Implementieren des Designs auf einem anderen Computer erforderlich sind, wie z. b. Audiodateien und Bilder.</span><span class="sxs-lookup"><span data-stu-id="daa66-283">A theme pack is a .cab file that contains not only the .theme file but also the files needed to implement the theme on another computer, such as sound files and images.</span></span> <span data-ttu-id="daa66-284">Benutzer können Designpakete über die Personalisierungs-Systemsteuerung erstellen.</span><span class="sxs-lookup"><span data-stu-id="daa66-284">Users can create theme packs through the Personalization Control Panel.</span></span>

<span data-ttu-id="daa66-285">Folgende Dateitypen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="daa66-285">Supported file types include the following:</span></span>



| <span data-ttu-id="daa66-286">Dateityp</span><span class="sxs-lookup"><span data-stu-id="daa66-286">File type</span></span>    | <span data-ttu-id="daa66-287">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="daa66-287">Extension</span></span>                           |
|--------------|-------------------------------------|
| <span data-ttu-id="daa66-288">Design</span><span class="sxs-lookup"><span data-stu-id="daa66-288">Theme</span></span>        | <span data-ttu-id="daa66-289">.theme</span><span class="sxs-lookup"><span data-stu-id="daa66-289">.theme</span></span>                              |
| <span data-ttu-id="daa66-290">Image</span><span class="sxs-lookup"><span data-stu-id="daa66-290">Image</span></span>        | <span data-ttu-id="daa66-291">. jpg,. JPEG,. BMP,. DIB,. TIF,. png</span><span class="sxs-lookup"><span data-stu-id="daa66-291">.jpg, .jpeg, .bmp, .dib, .tif, .png</span></span> |
| <span data-ttu-id="daa66-292">Sound</span><span class="sxs-lookup"><span data-stu-id="daa66-292">Sound</span></span>        | <span data-ttu-id="daa66-293">WAV</span><span class="sxs-lookup"><span data-stu-id="daa66-293">.wav</span></span>                                |
| <span data-ttu-id="daa66-294">Mauszeiger</span><span class="sxs-lookup"><span data-stu-id="daa66-294">Mouse cursor</span></span> | <span data-ttu-id="daa66-295">. cur,. ani</span><span class="sxs-lookup"><span data-stu-id="daa66-295">.cur, .ani</span></span>                          |
| <span data-ttu-id="daa66-296">Desktop Symbol</span><span class="sxs-lookup"><span data-stu-id="daa66-296">Desktop icon</span></span> | <span data-ttu-id="daa66-297">.ico</span><span class="sxs-lookup"><span data-stu-id="daa66-297">.ico</span></span>                                |
| <span data-ttu-id="daa66-298">Markenlogo</span><span class="sxs-lookup"><span data-stu-id="daa66-298">Brand logo</span></span>   | <span data-ttu-id="daa66-299">.png</span><span class="sxs-lookup"><span data-stu-id="daa66-299">.png</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="daa66-300">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="daa66-300">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daa66-301">Übersicht über visuelle Stile</span><span class="sxs-lookup"><span data-stu-id="daa66-301">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

