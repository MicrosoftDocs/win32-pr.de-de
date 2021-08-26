---
title: Designdateiformat
description: In diesem Dokument wird das Format von Designdateien (.theme) erläutert. Eine DESIGN-Datei ist eine .ini Textdatei, die in Abschnitte unterteilt ist, die visuelle Elemente angeben, die auf einem Windows Desktop angezeigt werden. Abschnittsnamen werden in Klammern (\ \ ) in der .ini-Datei umschlossen.
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67fc2d73e54e4f9c319108c2b29ed62fb58266f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472305"
---
# <a name="theme-file-format"></a>Designdateiformat

In diesem Dokument wird das Format von Designdateien (.theme) erläutert. Eine DESIGN-Datei ist eine .ini Textdatei, die in Abschnitte unterteilt ist, die visuelle Elemente angeben, die auf einem Windows Desktop angezeigt werden. Abschnittsnamen werden in Klammern ( \[ \] ) in der .ini-Datei umschlossen.

Das neue Dateiformat .themepack wurde mit Windows 7 eingeführt, um Benutzern das Freigeben von Designs zu erleichtern. Designs können in der Personalisierungs-Systemsteuerung nur in Windows 7 Home Premium oder höher oder nur auf Windows Server 2008 R2 ausgewählt werden, wenn die Desktopkomponente installiert ist.

Die folgenden Themen werden in diesem Artikel erläutert.

-   [Erstellen einer Designdatei](#creating-a-theme-file)
-   [Beschreibung einer Designdatei](#description-of-a-theme-file)
    -   [\[\]Abschnitt "Design"](#theme-section)
    -   [\[abschnitt "Systemsteuerung \\ \] Colors"](#control-panelcolors-section)
    -   [\[\\Systemsteuerung-Abschnitt "Cursor" \]](#control-panelcursors-section)
    -   [\[abschnitt "Systemsteuerung \\ \] Desktop"](#control-paneldesktop-section)
    -   [\[Abschnitt \] "Diashow"](#slideshow-section)
    -   [\[Abschnitt \] "Metriken"](#metrics-section)
    -   [\[Abschnitt "Visuelle \] Stile"](#visual-styles-section)
    -   [\[\]Abschnitte "Sounds" und \[ "AppEvents" \] (Sounds)](#sounds-and-appevents-sections-sounds)
    -   [\[Abschnitt \] "Start"](#boot-section)
    -   [\[\]MasterThemeSelector-Abschnitt](#masterthemeselector-section)
-   [Beispiel für eine Designdatei](#example-of-a-theme-file)
-   [Installieren von Designdateien](#installing-theme-files)
-   [Designpakete](#theme-packs)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-theme-file"></a>Erstellen einer Designdatei

Mit einer THEME-Datei können Sie die Darstellung bestimmter Desktopelemente ändern. Sie können eine THEME-Datei auf zwei Arten erstellen oder ändern:

-   Ändern Sie die Personalisierungs- oder Anzeigeeinstellungen in Systemsteuerung, und speichern Sie die Einstellungen als THEME-Datei. Anweisungen finden Sie in der Windows-Hilfe.
-   Erstellen Sie manuell eine DESIGN-Datei, um eine bessere Kontrolle über die Details Ihres Designs zu erhalten.

Um Ihr Design anderen Benutzern zur Verfügung zu stellen, müssen Sie Ihre THEME-Datei sowie die Hintergrundbild-, Bildschirmschoner- und Symboldateien bereitstellen. Dazu können Sie ein [Designpaket erstellen.](#theme-packs)

## <a name="description-of-a-theme-file"></a>Beschreibung einer Designdatei

Designdateien verfügen über eine Reihe von erforderlichen und optionalen Abschnitten. Im Folgenden werden die Abschnitte von THEME-Dateien beschrieben und Beispiele zum Angeben von Änderungen für die verschiedenen Elemente angegeben.

### <a name="theme-section"></a>\[\]Abschnitt "Design"

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in Ihre DESIGN-Datei einschließen, verwendet das System Standardeinstellungen.

 

Der \[ Abschnitt Design identifiziert den Namen Ihres \] benutzerdefinierten Designs und gibt das Markenlogo und die Desktopsymbole Ihres Designs an.

Der erste Teil des \[ Abschnitts Design \] enthält die folgenden beiden Elemente:



| Element                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName=name<br/> oder<br/> DisplayName= @module ,-stringId<br/> Beispiel: DisplayName= @themeui.dll ,-2013 | DisplayName ist der Designname, der in der Personalisierungs-Systemsteuerung angezeigt wird. Dies kann eine Zeichenfolge oder ein Verweis auf einen lokalisierten Namen sein.<br/> Dieses Feld ist optional. Wenn er fehlt, wird der Designdateiname als Designname verwendet.<br/>                                                                                                                                                                                                                                         |
| BrandImage=Pfad zum Bild<br/> Beispiel: BrandImage=c: \\ Fabrikam \\brand.png<br/>                                 | **Windows 7 und höher** BrandImage gibt den Pfad zu einer Markengrafikdatei an, die in der Designvorschau im Personalisierungs-Systemsteuerung enthalten ist.<br/> Die Symbolgrafik muss eine PNG-Datei sein. Die Grafik wird auf 80 x 240 Pixel skaliert, daher wird empfohlen, ein Bild dieser Größe bereitzustellen. Der Designkatalog beachtet die transparenten Bereiche Ihres Markensymbols.<br/> Dieses Feld ist optional. Wenn es fehlt, wird kein Logo als Designsymbol angezeigt.<br/> |



 

Im restlichen \[ Abschnitt Design \] werden benutzerdefinierte Symbole für Desktopfeatures wie Computer, Eigene Dokumente, Network und Papierkorb angegeben. Wenn Sie keine benutzerdefinierten Desktopsymbole angeben, zeigt der Desktop die Standarddesktopsymbole des Systems an.

Im Folgenden sind zwei Beispiele dafür aufgeführt, wie eine THEME-Datei das **Computersymbol** festlegt.


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



Im Folgenden sind Werte für die Standarddesktopsymbole in Windows 7 angegeben.


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



### <a name="control-panelcolors-section"></a>\[abschnitt "Systemsteuerung \\ \] Colors"

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in Ihre DESIGN-Datei einschließen, verwendet das System Standardeinstellungen. Wenn Ihr Design den visuellen Stil Von Styles verwendet, sollten Sie vermeiden, die Standardwerte in diesem Abschnitt zu überschreiben.

 

Die Farbe von Elementen wie Bildlaufleisten, Text und Schaltflächen kann angepasst werden. Die THEME-Datei gibt die RGB-Werte an, die für diese Elemente geändert werden sollen. Die Werte überschreiben die Standardwerte des visuellen Stils und werden verwendet, wenn Ihr Design auf Windows klassischen, Windows 7 Basic- oder hoher Kontrast Designs basiert.

Im Folgenden wird veranschaulicht, wie Farben festgelegt werden.


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



### <a name="control-panelcursors-section"></a>\[\\Systemsteuerung-Abschnitt "Cursor" \]

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in ihre DESIGN-Datei einschließen, verwendet das System Standardcursor.

 

Ein Design kann auch die Darstellung von Cursorn ändern. Hierzu erstellen Sie CUR-Dateien, um die Standard-Windows Cursor zu ersetzen. Das folgende Beispiel stammt aus einer THEME-Datei, die die Cursor für ein Design namens *Sport* definiert.


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



### <a name="control-paneldesktop-section"></a>\[abschnitt "Systemsteuerung \\ \] Desktop"

> [!Note]  
> Dieser Abschnitt ist ein Pflichtabschnitt. Wenn Sie diesen Abschnitt nicht in Ihre DESIGN-Datei einschließen, ignoriert das System Ihr Design und zeigt das Design nicht in Systemsteuerung an.

 

Sie können einen benutzerdefinierten Desktophintergrund erstellen und einen Pfad zur Bilddatei angeben. Das folgende Beispiel zeigt, wie Sie die Desktopdarstellung ändern.


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



### <a name="slideshow-section"></a>\[Abschnitt \] "Diashow"

**Windows 7 und höher.**

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in Die DESIGN-Datei einschließen, verwendet das System das Desktophintergrundbild, das im Abschnitt Systemsteuerung Desktop angegeben \[ \\ \] ist. Wenn Sie diesen Abschnitt einschließen, müssen Sie hier Einstellungen für die Bildschirmpräsentation angeben.

 

Der Hintergrund Ihres Designs kann eine Diashow von lokal gespeicherten Bildern oder von Bildern sein, die von einem RSS-Feed bedient werden. Der \[ Abschnitt Slideshow \] der Datei enthält die folgenden Attribute:




| attribute | BESCHREIBUNG | 
|-----------|-------------|
| Interval=Anzahl von Millisekunden | Erforderlich. Interval ist eine Zahl, die bestimmt, wie oft sich der Hintergrund ändert. Sie wird in Millisekunden gemessen. | 
| Shuffle=0 oder 1 | Erforderlich. Shuffle gibt an, ob der Hintergrund gemischt wird.<br /> 0 = Deaktiviert<br /> 1 = Aktiviert<br /> | 
| RSSFeed=URL zum RSS-Feed | Erforderlich, wenn ImagesRootPath nicht angegeben ist. RSSFeed gibt einen RSS-Feed an, der als Hintergrundpräsentation verwendet werden soll. Damit der Feed funktioniert, müssen Sie auf bilder mit hoher Auflösung verweisen, die dem "Gehäuse"-Standard entsprechen, der vom <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS-Plattform</a>verwendet wird. Aufgrund dieser Einschränkung müssen THEME-Dateien, die einen RSS-Feed enthalten, manuell erstellt werden. <br /><blockquote>[!Note]<br />Sie können weder RSSFeed noch ImagesRootPath angeben.</blockquote><br /><br /> | 
| ImagesRootPath=Pfad zum Imageordner | Erforderlich, wenn RSSFeed nicht angegeben ist. ImagesRootPath gibt einen Pfad zu einer Gruppe von Bildern an, die Sie als Hintergrundpräsentation verwenden möchten. Bilder in Unterordnern sind in der Bildschirmpräsentation nicht enthalten.<br /> ImagesRootPath unterstützt Umgebungsvariablenersetzungen im Pfad.<br /><blockquote>[!Note]<br />Sie können weder RSSFeed noch ImagesRootPath angeben.</blockquote><br /><br /> | 
| Element<em>N</em>Pfad=Pfad(e) zu bestimmten Bildern | Zur Verwendung mit ImagesRootPath. <br /> Element<em>N</em>Pfad gibt Pfade zu bestimmten Bildern an, sodass Sie die Bildschirmpräsentation auf bestimmte Bilder anstatt auf alle Bilder in einem Ordner beschränken können. Wenn keine Pfade angegeben werden, werden alle Bilder im Pfad ImagesRootPath in der Bildschirmpräsentation verwendet, einschließlich der Bilder, die nach dem Erstellen und Installieren des Designs hinzugefügt wurden.<br /> Element<em>N</em>Pfad unterstützt Umgebungsvariablenersetzungen im Pfad. <em>N</em> ist 0, 1, 2 usw. <br /> | 




 

Die folgenden Beispiele zeigen, wie eine THEME-Datei die Bildschirmpräsentation angibt, um eine Gruppe von lokal gespeicherten Bildern einzublenden.


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



Das folgende Beispiel ist eine Vorlage für eine THEME-Datei, die eine Desktophintergrund-Bildschirmpräsentation mitHilfe von Bildern aus einem RSS-Feed erstellt. Führen Sie die folgenden Schritte aus, um die Vorlage anzupassen:

1.  Kopieren Sie das folgende Beispiel, und fügen Sie es in einen Text-Editor ein.
2.  Ersetzen Sie {themename} durch den Namen, den Sie im Katalog Personalisierung Systemsteuerung Designs anzeigen möchten.
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
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in Ihre DESIGN-Datei einschließen, verwendet das System standardmäßige visuelle Stileinstellungen.

 

Sie können Systemmetriken in einer DESIGN-Datei angeben. Systemmetriken sind die Dimensionen verschiedener Anzeigeelemente, z. B. Fensterrahmenbreite, Symbolhöhe oder Bildlaufleistenbreite. Die Werte NonclientMetrics und IconMetrics sind binäre Strukturen, die von NONCLIENTMETRICS und ICONMETRICS in winuser.h definiert werden. Es folgt ein Beispiel für das Ändern von Systemmetriken.


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
> Dieser Abschnitt ist ein Pflichtabschnitt. Wenn Sie diesen Abschnitt nicht in Ihre DESIGN-Datei einschließen, ignoriert das System Ihr Design und zeigt das Design nicht in Systemsteuerung an.

 

Sie können spezifische Informationen zur Größe und Farbe von Desktopelementen in MSSTYLES-Dateien bereitstellen. Die Farb- und Größenabschnitte von THEME-Dateien können durch MSSTYLES-Dateien ersetzt werden, mit denen Sie Desktopelemente ausführlicher ändern können. Diese Dateien werden im Abschnitt visuelle Stile einer THEME-Datei angegeben. Im Folgenden finden Sie ein Beispiel für einen Abschnitt mit visuellen Stilen.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



Das Hinzufügen eines Path-Elements zu einer MSSTYLES-Datei ist optional. Wenn Sie einen Pfad bereitstellen, sollten Sie die Metriken und Farbabschnitte aus der THEME-Datei entfernen. Wenn diese Abschnitte entfernt werden, stammen die Farben, Schriftarten und Größen für ein Design aus der MSSTYLES-Datei und entsprechen der Absicht des MSSTYLES-Autors. Wenn die Metrik- und Farbabschnitte nicht entfernt werden, kann dies dazu führen, dass Windows oder Anwendungen Zeichnungsprobleme haben.

**Windows Vista/Windows 7:** Wenn der Pfad auf Soll.msstyles zeigt, können Sie die gewünschte Glass Color angeben, wie im folgenden Beispiel gezeigt.

**Windows 7:** Wenn der Pfad auf Alias.msstyles zeigt, können Sie auch den gewünschten Transparenzwert angeben, wie im folgenden Beispiel gezeigt.


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



Wenn die ColorizationColor- und Transparency-Werte genau mit einer Systemfarbe übereinstimmen, zeigt die Personalisierung Systemsteuerung den Systemnamen für die Farbe an. Andernfalls wird die Farbe mit "Benutzerdefiniert" bezeichnet.

Im Folgenden finden Sie einen VisualStyles-Abschnitt für das Design Windows 7 Basic.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



Im Folgenden wird ein VisualStyles-Abschnitt für das design Windows Classic gezeigt.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



Im Folgenden wird ein VisualStyles-Abschnitt für ein hoher Kontrast Black-Design gezeigt.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a>\[\]Abschnitte "Sounds" und \[ "AppEvents" \] (Sounds)

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in Ihre DESIGN-Datei einschließen, verwendet das System Standard-Soundeinstellungen.

 

Der Benutzer kann das **Soundsymbol** in Systemsteuerung auswählen, um Sounds Ereignissen zuzuordnen, die in Anwendungen auftreten. Beispielsweise kann eine WAV-Datei wiedergegeben werden, wenn eine Anwendung geöffnet wird. Eine THEME-Datei kann WAV-Dateien angeben, um die Standarddateien zu ersetzen. Das folgende Beispiel zeigt die erforderliche Vorgehensweise.


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



**Windows 7 und höher:** Ein Soundschemaname kann angegeben werden, anstatt jeden Sound separat aufzulisten.


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



Der SchemeName-Wert gibt den Namen des Soundschemas oder den namen des lokalisierten Soundschemas an, wie im obigen Beispiel gezeigt.

### <a name="boot-section"></a>\[\]Abschnitt "Start"

> [!Note]  
> **Bildschirmschoner sind im Windows 10 Anniversary Update und darüber hinaus veraltet.**

 

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in Ihre DESIGN-Datei einschließen, wird kein Bildschirmschoner verwendet.

 

In der THEME-Datei können Sie den Bildschirmschoner für Windows angeben. Im folgenden Beispiel wird dies veranschaulicht.


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a>\[\]MasterThemeSelector-Abschnitt

> [!Note]  
> Dieser Abschnitt ist ein Pflichtabschnitt. Wenn Sie diesen Abschnitt nicht in Ihre DESIGN-Datei einschließen, ignoriert das System Ihr Design und zeigt das Design nicht in Systemsteuerung an.

 

Der Abschnitt master theme selector der THEME-Datei sollte immer als Tag enthalten sein, das angibt, dass die Datei gültig ist. Sie haben keine Auswahl von Werten für diesen Parameter. Dies wird im Folgenden veranschaulicht.


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a>Beispiel für eine Designdatei

Das folgende Beispiel zeigt eine vollständige THEME-Datei.


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

Wenn Windows initialisiert wird, listet das Betriebssystem die Unterverzeichnisse der ersten Ebene von %WinDir% \\ Resources \\ auf, um verfügbare Designs zu identifizieren. Die Standarddesigndateien des Systems befinden sich unter %WinDir% \\ \\ Ressourcendesigns. Die Benutzerdesigndateien werden in %WinDir% \\ Users \\ <username> \\ AppData \\ Local Microsoft Windows Themes \\ \\ \\ gespeichert.

Eine THEME-Datei weist Dateizuordnungen auf. Daher können Designinstallationsprogrammanwendungen [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) für eine THEME-Datei aufrufen, um das **Personalisierungsfenster** in Systemsteuerung zum angegebenen Design zu öffnen.

## <a name="theme-packs"></a>Designpakete

**Windows 7 und höher.** Ein Designpaket ist eine .cab-Datei, die nicht nur die THEME-Datei enthält, sondern auch die Dateien, die zum Implementieren des Designs auf einem anderen Computer erforderlich sind, z. B. Sounddateien und Bilder. Benutzer können Designpakete über die Personalisierungs-Systemsteuerung erstellen.

Folgende Dateitypen werden unterstützt:



| Dateityp    | Durchwahl                           |
|--------------|-------------------------------------|
| Design        | .theme                              |
| Image        | .jpg, JPEG, .bmp, DIB, TIF, .png |
| Sound        | WAV                                |
| Mauscursor | .cur, .ani                          |
| Desktopsymbol | .ico                                |
| Markenlogo   | .png                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über visuelle Stile](visual-styles-overview.md)
</dt> </dl>

