---
title: Designdateiformat
description: In diesem Dokument wird das Format von Designdateien (.theme) erläutert. Eine DESIGN-Datei ist eine .ini-Textdatei, die in Abschnitte unterteilt ist, die visuelle Elemente angeben, die auf einem Windows werden. Abschnittsnamen werden in Klammern (\ \ ) in der .ini umschlossen.
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584e6d9785cf7660e017cadfb2a39d6bce6c2a87
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886634"
---
# <a name="theme-file-format"></a>Designdateiformat

In diesem Dokument wird das Format von Designdateien (.theme) erläutert. Eine DESIGN-Datei ist eine .ini-Textdatei, die in Abschnitte unterteilt ist, die visuelle Elemente angeben, die auf einem Windows werden. Abschnittsnamen werden in Klammern \[ \] () in der .ini umschlossen.

Das neue Dateiformat .themepack wurde mit Version 7 Windows, um Benutzern das Freigeben von Designs zu ermöglichen. Designs können im Personalisierungs-Systemsteuerung nur in Windows 7 Home Premium oder höher oder nur auf Windows Server 2008 R2 ausgewählt werden, wenn die Desktopkomponente installiert ist.

Die folgenden Themen werden in diesem Artikel erläutert.

-   [Erstellen einer Designdatei](#creating-a-theme-file)
-   [Beschreibung einer Designdatei](#description-of-a-theme-file)
    -   [\[\]Designabschnitt](#theme-section)
    -   [\[Systemsteuerung \\ Abschnitt \] "Farben"](#control-panelcolors-section)
    -   [\[Systemsteuerung \\ Cursorabschnitt \]](#control-panelcursors-section)
    -   [\[abschnitt Systemsteuerung \\ Desktop \]](#control-paneldesktop-section)
    -   [\[Abschnitt \] "Slideshow"](#slideshow-section)
    -   [\[Abschnitt \] "Metriken"](#metrics-section)
    -   [\[Abschnitt "Visuelle \] Stile"](#visual-styles-section)
    -   [\[Abschnitte \] \[ "Sounds" und \] "AppEvents" (Sounds)](#sounds-and-appevents-sections-sounds)
    -   [\[\]Startabschnitt](#boot-section)
    -   [\[MasterThemeSelector-Abschnitt \]](#masterthemeselector-section)
-   [Beispiel für eine Designdatei](#example-of-a-theme-file)
-   [Installieren von Designdateien](#installing-theme-files)
-   [Theme Packs](#theme-packs)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-theme-file"></a>Erstellen einer Designdatei

Mit einer DESIGN-Datei können Sie die Darstellung bestimmter Desktopelemente ändern. Sie können eine DESIGN-Datei auf zwei Arten erstellen oder ändern:

-   Ändern Sie die Personalisierungs- oder Anzeigeeinstellungen in Systemsteuerung, und speichern Sie die Einstellungen als DESIGN-Datei. Anweisungen finden Windows Hilfe zu Ihrem Computer.
-   Erstellen Sie manuell eine DESIGN-Datei, um mehr Kontrolle über die Details Ihres Designs zu erhalten.

Um Ihr Design für andere Benutzer verfügbar zu machen, müssen Sie ihre DESIGN-Datei sowie die Hintergrundbild-, Bildschirmschoner- und Symboldateien zur Verfügung stellen. Sie können dies mit einem [Designpaket tun.](#theme-packs)

## <a name="description-of-a-theme-file"></a>Beschreibung einer Designdatei

Designdateien verfügen über eine Reihe von erforderlichen und optionalen Abschnitten. Im Folgenden werden die Abschnitte der DESIGN-Dateien beschrieben und Beispiele zum Angeben von Änderungen für die verschiedenen Elemente angegeben.

### <a name="theme-section"></a>\[\]Designabschnitt

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die DESIGN-Datei ein-/ausdingen, verwendet das System Standardeinstellungen.

 

Der Abschnitt Design identifiziert den Namen Ihres benutzerdefinierten Designs und gibt das Markenlogo und die \[ \] Desktopsymbole Ihres Designs an.

Der erste Teil des \[ Abschnitts Design \] enthält die folgenden beiden Elemente:



| Element                                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName=name<br/> oder<br/> DisplayName= @module ,-stringId<br/> Beispiel: DisplayName= @themeui.dll ,-2013 | DisplayName ist der Designname, der in der Personalisierungsdatei Systemsteuerung. Dies kann eine Zeichenfolge oder ein Verweis auf einen lokalisierten Namen sein.<br/> Dieses Feld ist optional. Wenn er fehlt, wird der Designdateiname als Designname verwendet.<br/>                                                                                                                                                                                                                                         |
| BrandImage=Pfad zum Bild<br/> Beispiel: BrandImage=c: \\ \\ Fabrikam-brand.png<br/>                                 | **Windows 7 und höher** BrandImage gibt den Pfad zu einer Grafikdatei mit Marken an, die in der Designvorschau im Personalisierungsfenster Systemsteuerung.<br/> Die Symbolgrafik muss eine PNG-Datei sein. Die Grafik wird auf 80 x 240 Pixel skaliert, daher wird empfohlen, ein Bild dieser Größe zur Verfügung zu stellen. Der Designkatalog beachtet die transparenten Regionen Ihres Markensymbols.<br/> Dieses Feld ist optional. Wenn es fehlt, wird kein Logo als Designsymbol angezeigt.<br/> |



 

Im restlichen Abschnitt Design werden benutzerdefinierte Symbole für Desktopfunktionen wie \[ \] Computer, Eigene Dokumente, Netzwerk und Papierkorb. Wenn Sie keine benutzerdefinierten Desktopsymbole angeben, zeigt der Desktop die Standarddesktopsymbole des Systems an.

Im Folgenden finden Sie zwei Beispiele dafür, wie eine THEME-Datei das **Computersymbol** fest legt.


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



Im Folgenden finden Sie Werte für die Standarddesktopsymbole in Windows 7.


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



### <a name="control-panelcolors-section"></a>\[Systemsteuerung Abschnitt \\ \] "Farben"

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die DESIGN-Datei ein-/ausdingen, verwendet das System Standardeinstellungen. Wenn Ihr Design den visuellen Stil Von Visuals verwendet, sollten Sie das Überschreiben der Standardwerte in diesem Abschnitt vermeiden.

 

Die Farbe von Elementen, z. B. Scrollleisten, Text und Schaltflächen, kann angepasst werden. Die THEME-Datei gibt die RGB-Werte an, die für diese Elemente geändert werden. Die Werte überschreiben die Standardwerte des visuellen Stils und werden verwendet, wenn Ihr Design auf Windows klassischen, Windows 7 Basic- oder hoher Kontrast basiert.

Im Folgenden finden Sie ein Beispiel dafür, wie Farben festgelegt werden.


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



### <a name="control-panelcursors-section"></a>\[Systemsteuerung \\ Cursorabschnitt \]

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die DESIGN-Datei einordnen, verwendet das System Standardcursor.

 

Ein Design kann auch die Darstellung von Cursorn ändern. Dazu erstellen Sie CUR-Dateien, um die Standardcursor Windows ersetzen. Das folgende Beispiel ist aus einer THEME-Datei, die die Cursor für ein Design namens *Sports definiert.*


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



### <a name="control-paneldesktop-section"></a>\[abschnitt Systemsteuerung \\ Desktop \]

> [!Note]  
> Dieser Abschnitt ist ein Pflichtabschnitt. Wenn Sie diesen Abschnitt nicht in die DESIGN-Datei ein include, ignoriert das System Ihr Design und zeigt das Design nicht in Systemsteuerung.

 

Sie können einen benutzerdefinierten Desktophintergrund erstellen und einen Pfad zur Bilddatei angeben. Das folgende Beispiel zeigt, wie Sie die Desktop-Darstellung ändern.


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



### <a name="slideshow-section"></a>\[Abschnitt \] "Slideshow"

**Windows 7 und höher.**

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die DESIGN-Datei ein-/ausdingen, verwendet das System das Desktophintergrundbild, das im Abschnitt Desktop Systemsteuerung \[ \\ \] ist. Wenn Sie diesen Abschnitt angeben, müssen Sie hier Einstellungen für die Bildschirmpräsentation angeben.

 

Der Hintergrund Ihres Designs kann eine Diashow von lokal gespeicherten Bildern oder von Bildern sein, die von einem RSS-Feed verarbeitet werden. Der \[ Abschnitt Slideshow \] der Datei enthält die folgenden Attribute:




| attribute | Beschreibung | 
|-----------|-------------|
| Interval=Anzahl von Millisekunden | Erforderlich. Interval ist eine Zahl, die bestimmt, wie oft sich der Hintergrund ändert. Sie wird in Millisekunden gemessen. | 
| Shuffle=0 oder 1 | Erforderlich. Shuffle identifiziert, ob der Hintergrund gemischt wird.<br /> 0 = Deaktiviert<br /> 1 = Aktiviert<br /> | 
| RSSFeed=URL zum RSS-Feed | Erforderlich, wenn ImagesRootPath nicht angegeben ist. RSSFeed gibt einen RSS-Feed an, der als Hintergrundfolie verwendet werden soll. Damit der Feed funktioniert, müssen Sie auf bilder mit hoher Auflösung verweisen, die dem Standard "Gehäuse" entsprechen, der von der <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">RSS-Plattform</a>Windows wird. Aufgrund dieser Einschränkung müssen DESIGN-Dateien, die einen RSS-Feed enthalten, manuell erstellt werden. <br /><blockquote>[!Note]<br />Sie können nicht sowohl einen RSSFeed- als auch einen ImagesRootPath angeben.</blockquote><br /><br /> | 
| ImagesRootPath=pfad zum Ordner image | Erforderlich, wenn RSSFeed nicht angegeben ist. ImagesRootPath gibt einen Pfad zu einer Gruppe von Bildern an, die Sie als Hintergrundfolie verwenden möchten. Bilder in Unterordnern sind nicht in der Bildschirmpräsentation enthalten.<br /> ImagesRootPath unterstützt Ersetzungen von Umgebungsvariablen im Pfad.<br /><blockquote>[!Note]<br />Sie können nicht sowohl einen RSSFeed- als auch einen ImagesRootPath angeben.</blockquote><br /><br /> | 
| Item N Path=path(s) to specific image(s) (Element<em>N</em>Pfad=Pfad(e) zu bestimmten Bildern) | Für die Verwendung mit ImagesRootPath. <br /> Element<em>N</em>Pfad gibt Pfade zu bestimmten Bildern an, sodass Sie die Bildschirmpräsentation auf bestimmte Bilder anstatt auf alle Bilder in einem Ordner beschränken können. Wenn keine Pfade angegeben werden, werden alle Bilder im Pfad ImagesRootPath in der Bildschirmpräsentation verwendet, einschließlich der Images, die nach dem Erstellen und Installieren des Designs hinzugefügt wurden.<br /> Item<em>N</em>Path unterstützt Ersetzungen von Umgebungsvariablen im Pfad. <em>N</em> ist 0, 1, 2 und so weiter. <br /> | 




 

In den folgenden Beispielen wird gezeigt, wie eine DESIGN-Datei die Bildschirmpräsentation so angibt, dass sie eine Gruppe von lokal gespeicherten Bildern enthält.


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



Das folgende Beispiel ist eine Vorlage für eine THEME-Datei, die eine Desktophintergrund-Bildschirmpräsentation mit Bildern aus einem RSS-Feed erstellt. Führen Sie die folgenden Schritte aus, um die Vorlage anzupassen:

1.  Kopieren Sie das folgende Beispiel, und fügen Sie es in einen Text-Editor ein.
2.  Ersetzen Sie {themename} durch den Namen, der im Katalog für Personalisierungsdesigns Systemsteuerung werden soll.
3.  Ersetzen Sie {rssfeedurl} durch den vollständigen Pfad zu einem kompatiblen RSS-Feed.
4.  Speichern Sie die Änderungen als Datei mit der Erweiterung ".theme".


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



### <a name="metrics-section"></a>\[Abschnitt \] "Metriken"

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die DESIGN-Datei ein-/ausdingen, verwendet das System standardeinstellungen für visuelle Stile.

 

Sie können Systemmetriken in einer DESIGN-Datei angeben. Systemmetriken sind die Abmessungen verschiedener Anzeigeelemente, z. B. die Breite des Fensterrahmens, die Symbolhöhe oder die Breite der Bildlaufleiste. Die Werte NonclientMetrics und IconMetrics sind binäre Strukturen, die von NONCLIENTMETRICS und ICONMETRICS in winuser.h definiert werden. Im Folgenden finden Sie ein Beispiel für das Ändern von Systemmetriken.


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



### <a name="visual-styles-section"></a>\[Abschnitt "Visuelle \] Stile"

> [!Note]  
> Dieser Abschnitt ist ein Pflichtabschnitt. Wenn Sie diesen Abschnitt nicht in die DESIGN-Datei ein-/ausdingen, ignoriert das System Ihr Design und zeigt das Design nicht in der Systemsteuerung.

 

Sie können spezifische Informationen zur Größe und Farbe von Desktopelementen in MSSTYLES-Dateien liefern. Die Farb- und Größenabschnitte von DESIGN-Dateien können durch MSSTYLES-Dateien ersetzt werden, mit denen Sie Desktopelemente ausführlicher ändern können. Diese Dateien werden im Abschnitt visuelle Stile einer DESIGN-Datei angegeben. Im Folgenden finden Sie ein Beispiel für einen Abschnitt mit visuellen Stilen.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



Das Hinzufügen eines Path-Elements zu einer MSSTYLES-Datei ist optional. Wenn Sie einen Pfad geben, sollten Sie die Metriken und Farbabschnitte aus der DESIGN-Datei entfernen. Wenn diese Abschnitte entfernt werden, stammen die Farben, Schriftarten und Größen für ein Design aus der MSSTYLES-Datei und passen zur Absicht des Msstyles-Autors. Wenn sie die Abschnitte "Metrik" und "Farbe" nicht entfernen, kann dies dazu führen, dass Windows oder Anwendungen Zeichnungsprobleme haben.

**Windows Vista/Windows 7:** Wenn der Pfad auf "Path.msstyles" zeigt, können Sie die gewünschte Glass Color angeben, wie im folgenden Beispiel gezeigt.

**Windows 7:** Wenn der Pfad auf "Path.msstyles" zeigt, können Sie auch den gewünschten Transparenzwert angeben, wie im folgenden Beispiel gezeigt.


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



Wenn die Werte ColorizationColor und Transparency genau mit einer Systemfarbe übereinstimmen, zeigt der Personalisierungs-Systemsteuerung den Systemnamen für die Farbe an. Andernfalls wird die Farbe als "Benutzerdefiniert" bezeichnet.

Das folgende Beispiel zeigt einen VisualStyles-Abschnitt für das Windows 7 Basic-Design.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



Das folgende Beispiel zeigt einen VisualStyles-Abschnitt für Windows klassisches Design.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



Das folgende Beispiel zeigt einen VisualStyles-Abschnitt für ein hoher Kontrast Black-Design.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a>\[Abschnitte \] \[ "Sounds" und \] "AppEvents" (Sounds)

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die DESIGN-Datei ein-/ausdingen, verwendet das System die Standardklangeinstellungen.

 

Der Benutzer kann das **Soundsymbol** in der Systemsteuerung, um Sounds Ereignissen in Anwendungen zu zuordnen. Beispielsweise kann eine WAV-Datei beim Öffnen einer Anwendung wieder verwendet werden. Eine THEME-Datei kann WAV-Dateien angeben, um die Standarddateien zu ersetzen. Das folgende Beispiel zeigt die erforderliche Vorgehensweise.


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



**Windows 7 und höher:** Ein Name des Soundschemas kann angegeben werden, anstatt jeden Sound separat auflisten zu müssen.


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



Der SchemeName-Wert gibt den Namen des Soundschemas oder des lokalisierten Soundschemanamens an, wie im obigen Beispiel gezeigt.

### <a name="boot-section"></a>\[\]Startabschnitt

> [!Note]  
> **Bildschirmschoner sind im Windows 10 Anniversary Update und darüber hinaus veraltet.**

 

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die DESIGN-Datei ein-/ausdingen, wird kein Bildschirmschoner verwendet.

 

In der DESIGN-Datei können Sie den Bildschirmschoner angeben, der von Windows werden soll. Im folgenden Beispiel wird dies veranschaulicht.


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a>\[MasterThemeSelector-Abschnitt \]

> [!Note]  
> Dieser Abschnitt ist ein Pflichtabschnitt. Wenn Sie diesen Abschnitt nicht in die DESIGN-Datei ein-/ausdingen, ignoriert das System Ihr Design und zeigt das Design nicht in der Systemsteuerung.

 

Der Abschnitt master theme selector der DESIGN-Datei sollte immer als Tag enthalten sein, das angibt, dass die Datei gültig ist. Sie haben keine Auswahl von Werten für diesen Parameter. Dies wird im Folgenden veranschaulicht.


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a>Beispiel für eine Designdatei

Das folgende Beispiel zeigt eine vollständige DESIGN-Datei.


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



## <a name="installing-theme-files"></a>Installieren von Designdateien

Wenn Windows initialisiert wird, enumeriert das Betriebssystem die Unterverzeichnisse der ersten Ebene von %WinDir% Resources, um verfügbare Designs \\ \\ zu identifizieren. Die Standarddesigndateien des Systems befinden sich unter %WinDir% \\ \\ Ressourcendesigns. Die Benutzerdesigndateien werden unter %WinDir% \\ \\ &lt; Benutzerbenutzername &gt; \\ AppData \\ Local Microsoft Windows Themes \\ \\ \\ gespeichert.

Eine DESIGN-Datei verfügt über Dateizuordnungen. Daher können Designinstallationsprogrammanwendungen [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) für eine DESIGN-Datei aufrufen, um das Personalisierungsfenster in Systemsteuerung design zu öffnen. 

## <a name="theme-packs"></a>Theme Packs

**Windows 7 und höher.** Ein Designpaket ist eine .cab-Datei, die nicht nur die THEME-Datei enthält, sondern auch die Dateien, die zum Implementieren des Designs auf einem anderen Computer erforderlich sind, z. B. Sounddateien und Bilder. Benutzer können Designpakete über die Personalisierungs-Systemsteuerung.

Folgende Dateitypen werden unterstützt:



| Dateityp    | Durchwahl                           |
|--------------|-------------------------------------|
| Design        | .theme                              |
| Image        | .jpg, .jpeg, .bmp, .dib, .tif, .png |
| Sound        | WAV                                |
| Mauszeiger | .cur, .ani                          |
| Desktopsymbol | .ico                                |
| Markenlogo   | .png                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über visuelle Stile](visual-styles-overview.md)
</dt> </dl>

