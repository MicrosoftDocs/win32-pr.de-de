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
# <a name="theme-file-format"></a>Designdatei Format

In diesem Dokument wird das Format der Designdateien (. Theme) erläutert. Bei einer. Theme-Datei handelt es sich um eine ini-Textdatei, die in Abschnitte unterteilt ist, die visuelle Elemente angeben, die auf einem Windows-Desktop angezeigt werden Abschnittsnamen werden in eckige Klammern ( \[ \] ) in der INI-Datei eingeschlossen.

Ein neues Dateiformat (...) wurde mit Windows 7 eingeführt, um Benutzern die gemeinsame Nutzung von Designs zu erleichtern. Designs können in der Personalisierungs-Systemsteuerung nur in Windows 7 Home Premium oder höher oder nur unter Windows Server 2008 R2 ausgewählt werden, wenn die Desktop Komponente installiert ist.

Die folgenden Themen werden in diesem Artikel erläutert.

-   [Erstellen einer Designdatei](#creating-a-theme-file)
-   [Beschreibung einer Designdatei](#description-of-a-theme-file)
    -   [\[Design \] Abschnitt](#theme-section)
    -   [\[Bereich mit den Farben der Systemsteuerung \\ \]](#control-panelcolors-section)
    -   [\[Abschnitt "System Steuerungs \\ Cursor" \]](#control-panelcursors-section)
    -   [\[Bereich "Desktop" der Systemsteuerung \\ \]](#control-paneldesktop-section)
    -   [\[Abschnitt "Diashow" \]](#slideshow-section)
    -   [\[\]Metrikabschnitt](#metrics-section)
    -   [\[Visueller Stile ( \] Abschnitt)](#visual-styles-section)
    -   [\[Abschnitte "Sounds" \] und " \[ appevents" \] (Sounds)](#sounds-and-appevents-sections-sounds)
    -   [\[Start \] Abschnitt](#boot-section)
    -   [\[Masterthemeselector ( \] Abschnitt)](#masterthemeselector-section)
-   [Beispiel für eine Designdatei](#example-of-a-theme-file)
-   [Designdateien werden installiert.](#installing-theme-files)
-   [Designpakete](#theme-packs)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-theme-file"></a>Erstellen einer Designdatei

Eine. Design-Datei ermöglicht es Ihnen, die Darstellung bestimmter Desktop Elemente zu ändern. Sie können eine. Theme-Datei auf zwei Arten erstellen oder ändern:

-   Ändern Sie die Personalisierungs-oder Anzeigeeinstellungen in der Systemsteuerung, und speichern Sie die Einstellungen als Designdatei. Anweisungen hierzu finden Sie in der Windows-Hilfe.
-   Erstellen Sie manuell eine. Design-Datei, um ein höheres Maß an Kontrolle über die Details Ihres Designs zu erhalten.

Um das Design für andere Benutzer verfügbar zu machen, müssen Sie die. Theme-Datei sowie die Hintergrundbild-, Bildschirmschoner-und Symbol Dateien angeben. Hierfür können Sie ein Design [Pack](#theme-packs)verwenden.

## <a name="description-of-a-theme-file"></a>Beschreibung einer Designdatei

Designdateien sind einige erforderliche und optionale Abschnitte. Im folgenden werden die Abschnitte der Designdateien beschrieben und Beispiele zum Angeben von Änderungen für die verschiedenen Elemente bereitgestellt.

### <a name="theme-section"></a>\[Design \] Abschnitt

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, verwendet das System Standardeinstellungen.

 

Der Abschnitt "Design" \[ \] gibt den Namen des benutzerdefinierten Designs an und gibt das Markenlogo und die Desktop Symbole Ihres Designs an.

Der erste Teil des Design \[ \] Abschnitts enthält die folgenden beiden Elemente:



| Element                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Display Name = Name<br/> oder<br/> Display Name = @module ,-stringID<br/> Beispiel: Display Name = @themeui.dll ,-2013 | Display Name ist der Design Name, der in der Personalisierungs-Systemsteuerung angezeigt wird. Dabei kann es sich um eine Zeichenfolge oder einen Verweis auf einen lokalisierten Namen handeln.<br/> Dieses Feld ist optional. Wenn Sie nicht vorhanden ist, wird der Design Dateiname als Design Name verwendet.<br/>                                                                                                                                                                                                                                         |
| Brandimage = Pfad zum Bild<br/> Beispiel: Brandimage = c: \\ Fabrikam \\brand.png<br/>                                 | **Windows 7 und** höher Brandimage gibt den Pfad zu einer Branding-Grafikdatei an, die in der Design Vorschau in der Personalisierungs-Systemsteuerung enthalten ist.<br/> Die Symbol Grafik muss eine PNG-Datei sein. Die Grafik wird auf 80 x 240 Pixel skaliert. es wird daher empfohlen, ein Bild dieser Größe bereitzustellen. Der Design Katalog respektiert die transparenten Bereiche Ihres Marken Symbols.<br/> Dieses Feld ist optional. Wenn Sie nicht vorhanden ist, wird kein Logo als symbolsymbol angezeigt.<br/> |



 

Im restlichen Abschnitt des \[ Themas Theme werden \] benutzerdefinierte Symbole für Desktop Features wie Computer, eigene Dokumente, Netzwerk und Papierkorb angegeben. Wenn Sie keine benutzerdefinierten Desktop Symbole angeben, zeigt der Desktop die standardmäßigen Desktop Symbole des Systems an.

Im folgenden finden Sie zwei Beispiele dafür, wie eine. Theme-Datei das **Computer** Symbol festlegt.


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



Im folgenden sind die Werte für die Standard Desktop Symbole in Windows 7 dargestellt.


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



### <a name="control-panelcolors-section"></a>\[Bereich mit den Farben der Systemsteuerung \\ \]

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, verwendet das System Standardeinstellungen. Wenn Ihr Design den visuellen Aero-Stil verwendet, sollten Sie das Überschreiben der Standardwerte in diesem Abschnitt vermeiden.

 

Die Farbe von Elementen, z. b. Scrollleisten, Text und Schaltflächen, ist anpassbar. Die. Theme-Datei gibt die RGB-Werte an, die für diese Elemente geändert werden müssen. Die Werte überschreiben die Standardwerte des visuellen Stils und werden verwendet, wenn Ihr Design auf Windows Classic, Windows 7 Basic oder hoher Kontrast Designs basiert.

Im folgenden finden Sie ein Beispiel für die Festlegung von Farben.


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



### <a name="control-panelcursors-section"></a>\[Abschnitt "System Steuerungs \\ Cursor" \]

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die. Theme-Datei einschließen, verwendet das System standardcursorn.

 

Ein Design kann auch die Darstellung von Cursorn ändern. Zu diesem Zweck erstellen Sie cur-Dateien, um die standardmäßigen Windows-Cursor zu ersetzen. Das folgende Beispiel zeigt eine. Design-Datei, die die Cursor für ein Design mit dem Namen " *Sports*" definiert.


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



### <a name="control-paneldesktop-section"></a>\[Bereich "Desktop" der Systemsteuerung \\ \]

> [!Note]  
> Dieser Abschnitt ist ein Pflichtabschnitt. Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, ignoriert das System das Design und zeigt das Design in der Systemsteuerung nicht an.

 

Sie können einen benutzerdefinierten Desktop Hintergrund erstellen und einen Pfad zur Bilddatei angeben. Im folgenden Beispiel wird gezeigt, wie die Desktop Darstellung geändert wird.


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



### <a name="slideshow-section"></a>\[Abschnitt "Diashow" \]

**Windows 7 und höher.**

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, verwendet das System das Desktop Hintergrundbild, das im \[ Abschnitt Desktop der Systemsteuerung angegeben ist \\ \] . Wenn Sie diesen Abschnitt einschließen, müssen Sie hier die Einstellungen für "Folie anzeigen" angeben.

 

Der Hintergrund des Designs kann eine Folie darstellen, die entweder lokal oder von Bildern gespeichert ist, die von einem RSS-Feed bedient werden. Der \[ Abschnitt "Diashow" \] der Datei enthält die folgenden Attribute:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Intervall = Anzahl der Millisekunden</td>
<td>Erforderlich. Interval ist eine Zahl, die bestimmt, wie oft der Hintergrund geändert wird. Der Wert wird in Millisekunden gemessen.</td>
</tr>
<tr class="even">
<td>Shuffle = 0 oder 1</td>
<td>Erforderlich. Shuffle gibt an, ob der Hintergrund heruntergefahren wird.<br/> 0 = Deaktiviert<br/> 1 = Aktiviert<br/></td>
</tr>
<tr class="odd">
<td>RSSFeed = URL zum RSS-Feed</td>
<td>Erforderlich, wenn imagesrootpath nicht angegeben ist. RSSFeed gibt einen RSS-Feed an, der als Hintergrund Bildschirm Anzeige verwendet werden soll. Damit der Feed funktioniert, müssen Sie auf hochauflösende Images verweisen, die dem &quot; Gehäuse &quot; Standard entsprechen, der von der <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS-Plattform</a>verwendet wird. Aufgrund dieser Einschränkung müssen Designdateien, die einen RSS-Feed enthalten, manuell erstellt werden. <br/>
<blockquote>
[!Note]<br />
RSSFeed und imagesrootpath können nicht gleichzeitig angegeben werden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>Imagesrootpath = Pfad zum Bildordner</td>
<td>Erforderlich, wenn RSSFeed nicht angegeben ist. Imagesrootpath gibt einen Pfad zu einem Satz von Bildern an, den Sie als Hintergrund Bildschirm Anzeige verwenden möchten. Bilder in Unterordnern sind nicht in der Folien Anzeige enthalten.<br/> Imagesrootpath unterstützt die Ersetzung von Umgebungsvariablen im Pfad.<br/>
<blockquote>
[!Note]<br />
RSSFeed und imagesrootpath können nicht gleichzeitig angegeben werden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>Element<em>N</em>Pfad = Pfad (e) zu bestimmten Bildern</td>
<td>Zur Verwendung mit imagesrootpath. <br/> Element<em>N</em>Pfad gibt Pfade zu bestimmten Bildern an, sodass Sie die Folien Anzeige auf bestimmte Bilder anstatt auf alle Bilder in einem Ordner beschränken können. Wenn keine Pfade angegeben werden, werden alle Bilder im imagesrootpath-Pfad in der Folien Anzeige verwendet, einschließlich der Bilder, die nach dem Erstellen und Installieren des Designs hinzugefügt wurden.<br/> Element<em>N</em>Path unterstützt die Ersetzung von Umgebungsvariablen im Pfad. <em>N</em> ist 0, 1, 2 usw. <br/></td>
</tr>
</tbody>
</table>



 

In den folgenden Beispielen wird veranschaulicht, wie eine. Theme-Datei die Bildschirm Anzeige angibt, um einen lokal gespeicherten Satz von Bildern einzuschließen.


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



Das folgende Beispiel ist eine Vorlage für eine. Design-Datei, mit der eine Desktop-Hintergrund Folie mit Bildern aus einem RSS-Feed erstellt wird. Führen Sie die folgenden Schritte aus, um die Vorlage anzupassen:

1.  Kopieren Sie das folgende Beispiel, und fügen Sie es in einen Text-Editor ein.
2.  Ersetzen Sie {ThemeName} durch den Namen, der in der Personalisierungs-Systemsteuerung in der Design-Galerie angezeigt werden soll.
3.  Ersetzen Sie {rssfeedurl} durch den vollständigen Pfad zu einem kompatiblen RSS-Feed.
4.  Speichern Sie die Änderungen als Datei mit der Erweiterung ". Theme".


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



### <a name="metrics-section"></a>\[\]Metrikabschnitt

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, verwendet das System Standardeinstellungen des visuellen Stils.

 

Sie können Systemmetriken in einer. Theme-Datei angeben. Systemmetriken sind die Dimensionen verschiedener Anzeigeelemente, wie z. b. die Rahmenbreite des Fensters, die Symbol Höhe oder die Breite der Bild Lauf Leiste. Die nonclientmetrics-und iconmetrics-Werte sind binäre Strukturen, die von nonclientmetrics und iconmetrics in winuser. h definiert werden. Im folgenden finden Sie ein Beispiel für das Ändern von Systemmetriken.


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



### <a name="visual-styles-section"></a>\[Visueller Stile ( \] Abschnitt)

> [!Note]  
> Dieser Abschnitt ist ein Pflichtabschnitt. Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, ignoriert das System das Design und zeigt das Design in der Systemsteuerung nicht an.

 

Sie können spezifische Informationen zur Größe und Farbe der Desktop Elemente in msstyles-Dateien angeben. Die Farb-und Größen Abschnitte von. Design-Dateien können durch msstyles-Dateien ersetzt werden, die es Ihnen ermöglichen, Desktop Elemente ausführlicher zu ändern. Diese Dateien werden im Abschnitt visuelle Stile einer. Theme-Datei angegeben. Im folgenden finden Sie ein Beispiel für einen Abschnitt mit visuellen Stilen.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



Das Hinzufügen eines Path-Elements zu einer. msstyles-Datei ist optional. Wenn Sie einen Pfad angeben, sollten Sie die Metriken und farbabschnitte aus der. Theme-Datei entfernen. Wenn diese Abschnitte entfernt werden, stammen die Farben, Schriftarten und Größen für ein Design aus der msstyles-Datei und stimmen mit der Absicht des Autors von msstyles. Wenn Sie die Metrik-und farbabschnitte nicht entfernen, können Windows-Anwendungen oder Anwendungen Zeichnungs Probleme verursachen.

**Windows Vista/Windows 7:** Wenn der Pfad auf Aero. msstyles zeigt, können Sie die gewünschte Glasfarbe angeben, wie im folgenden Beispiel gezeigt.

**Windows 7:** Wenn der Pfad auf Aero. msstyles zeigt, können Sie auch den gewünschten Transparenz Wert angeben, wie im folgenden Beispiel gezeigt.


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



Wenn die Werte colorizationcolor und Transparenz exakt mit einer System Farbe übereinstimmen, wird in der Personalisierungs-Systemsteuerung der Systemname der Farbe angezeigt. Andernfalls ist die Farbe "Custom".

Das folgende Beispiel zeigt einen VisualStyles-Abschnitt für das grundlegende Design von Windows 7.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



Das folgende Beispiel zeigt einen VisualStyles-Abschnitt für das klassische Windows-Design.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



Das folgende Beispiel zeigt einen VisualStyles-Abschnitt für ein hoher Kontrast schwarzes Design.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a>\[Abschnitte "Sounds" \] und " \[ appevents" \] (Sounds)

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, verwendet das System standardmäßige Soundeinstellungen.

 

Der Benutzer kann das **Sound** Symbol in der Systemsteuerung auswählen, um Sounds Ereignisse zuzuordnen, die in-Anwendungen auftreten. Eine WAV-Datei kann z. b. abgespielt werden, wenn eine Anwendung geöffnet wird. In einer. Design-Datei können WAV-Dateien angegeben werden, um die Standardwerte zu ersetzen. Das folgende Beispiel zeigt die erforderliche Vorgehensweise.


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



**Windows 7 und höher:** Sie können einen Sound Schema Namen angeben, anstatt jeden Sound separat aufzulisten.


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



Der schemeName-Wert gibt den Namen des Audioschemas oder des lokalisierten Sound Schemas an, wie im obigen Beispiel gezeigt.

### <a name="boot-section"></a>\[Start \] Abschnitt

> [!Note]  
> **Bildschirmschoner sind in Windows 10 Anniversary Update und höher veraltet.**

 

> [!Note]  
> Dieser Abschnitt ist optional. Wenn Sie diesen Abschnitt nicht in die. Theme-Datei einschließen, wird kein Bildschirmschoner verwendet.

 

In der. Theme-Datei können Sie den Bildschirmschoner angeben, der von Windows verwendet werden soll. Im folgenden Beispiel wird dies veranschaulicht.


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a>\[Masterthemeselector ( \] Abschnitt)

> [!Note]  
> Dieser Abschnitt ist ein Pflichtabschnitt. Wenn Sie diesen Abschnitt nicht in die Datei ". Theme" einschließen, ignoriert das System das Design und zeigt das Design in der Systemsteuerung nicht an.

 

Der Abschnitt "Master Design Selector" der. Theme-Datei sollte immer als ein Tag eingeschlossen werden, das angibt, dass die Datei gültig ist. Sie haben keine Auswahl von Werten für diesen Parameter. Dies wird in der folgenden Abbildung veranschaulicht.


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a>Beispiel für eine Designdatei

Das folgende Beispiel zeigt eine komplette Designdatei.


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



## <a name="installing-theme-files"></a>Designdateien werden installiert.

Beim Initialisieren von Windows listet das Betriebssystem die Unterverzeichnisse der ersten Ebene von% windir%- \\ Ressourcen auf, \\ um verfügbare Designs zu identifizieren. Die standardmäßigen Systemdateien befinden sich unter% windir% \\ Resources Designs \\ . Die Benutzer Designdateien werden unter "% windir% \\ Users \\ <username> \\ AppData \\ local \\ Microsoft \\ Windows \\ Themes" gespeichert.

Eine. Design-Datei weist Dateizuordnungen auf. Daher können Theme Installer-Anwendungen [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) für eine. Theme-Datei aufzurufen, um das **Personalisierungs** Fenster in der Systemsteuerung für das angegebene Design zu öffnen.

## <a name="theme-packs"></a>Designpakete

**Windows 7 und höher.** Ein Design Pack ist eine CAB-Datei, die nicht nur die. Theme-Datei, sondern auch die Dateien enthält, die zum Implementieren des Designs auf einem anderen Computer erforderlich sind, wie z. b. Audiodateien und Bilder. Benutzer können Designpakete über die Personalisierungs-Systemsteuerung erstellen.

Folgende Dateitypen werden unterstützt:



| Dateityp    | Durchwahl                           |
|--------------|-------------------------------------|
| Design        | .theme                              |
| Image        | . jpg,. JPEG,. BMP,. DIB,. TIF,. png |
| Sound        | WAV                                |
| Mauszeiger | . cur,. ani                          |
| Desktop Symbol | .ico                                |
| Markenlogo   | .png                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über visuelle Stile](visual-styles-overview.md)
</dt> </dl>

