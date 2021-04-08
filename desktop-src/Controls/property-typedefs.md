---
title: Eigenschafts Bezeichner (Windows-Steuerelemente)
description: Dieses Thema enthält Informationen zu definierten Werten, die zum Abrufen von Eigenschaften von visuellen Stilen verwendet werden. Die Definitionen finden Sie in Vssym32. h.
ms.assetid: b0e22022-fea9-43d1-8ef0-7a1c518760f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0869ac80332a5dbdb146ee255f5c9e73f4a812
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739280"
---
# <a name="property-identifiers-windows-controls"></a>Eigenschafts Bezeichner (Windows-Steuerelemente)

Dieses Thema enthält Informationen zu definierten Werten, die zum Abrufen von Eigenschaften von visuellen Stilen verwendet werden. Die Definitionen finden Sie in Vssym32. h.

## <a name="property-types"></a>Eigenschaftentypen

In der folgenden Tabelle sind die primitiven Eigenschafts Typen aufgeführt. Die Werte in der ersten Spalte werden normalerweise nicht von Anwendungen verwendet, bieten aber die Möglichkeit, Eigenschaften Bezeichner zu klassifiziert.



| Datentyp       | BESCHREIBUNG                              | Zurückgegebener Typ                          | Abruf Funktion                                                                                                     |
|-----------------|------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| TMT \_ bool       | **True** oder **false**                    | Boolean                                | [**Getdermebool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebool), [ **getthemesysbool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool)                                       |
| TMT- \_ Farbe      | RGB-Farbwert                          | [**COLORREF**](/windows/desktop/gdi/colorref) -Struktur | [**Gettemecolor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor), [ **getthemesyscolor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesyscolor)                                   |
| TMT \_ diskstream | Datenträger Datenstrom                              | **HINSTANCE**                          | [**Gettemestream**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestream)                                                                               |
| TMT-Aufzählung \_       | Enumerationswert                         | Enumeration                            | [**Gettemeenumvalue**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeenumvalue).                                                                        |
| TMT \_ Dateiname   | Dateiname relativ zum Design Verzeichnis | **WCHAR** -Array                        | [**Getmefilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename)                                                                           |
| TMT- \_ Schriftart       | Schriftart Beschreibung                         | [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur   | [**Getdermefont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefont), [ **getthemesysfont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysfont)                                       |
| TMT \_ hBitmap    | Bitmap                                   | **HBitmap** -handle                     | [**Getdermebitmap**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebitmap)                                                                               |
| TMT \_ int        | Signierte Zahl                            | Integer                                | [**Getthemeint**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeint), [**getthemesysint**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysint), [**getdermemetric**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememetric) |
| TMT- \_ intlist    | Liste mit ganzen Zahlen                         | [**Intlist**](/windows/desktop/api/UxTheme/ns-uxtheme-intlist) -Struktur   | [**Getthemin List**](/windows/desktop/api/UxTheme/nf-uxtheme-getthemeintlist)                                                                             |
| TMT- \_ Ränder    | Ränder: Links, oben, rechts und unten    | [**Margin**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) -Struktur   | [**Getdermemargin**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememargins)                                                                             |
| TMT- \_ Position   | Speicherort eines Elements                      | [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur       | [**Getdermeposition**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeposition)                                                                           |
| TMT- \_ Rect       | Größe und Position eines Rechtecks         | [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur         | [**Getthemup**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemerect)                                                                                   |
| TMT- \_ Größe       | Größe eines Elements                          | [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur         | [**Gettemepartsize**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemepartsize)                                                                           |
| TMT- \_ Zeichenfolge     | Unicode-Zeichenfolge                           | **WCHAR** -Array                        | [**Getdermestring**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestring), [ **getthemesysstring**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)                               |



 

## <a name="property-ids"></a>Eigenschaften-IDs

Im folgenden finden Sie die definierten Werte für Design Eigenschaften, gruppiert nach Datentyp.

**TMT \_ bool**



| id                        | Notizen                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ alwaysshowsizingbar  | **True** , wenn die dem Teil und dem Zustand zugeordnete Größenänderung immer angezeigt werden soll.                                                                                                                           |
| TMT \_ AutoSize             | **True** , wenn der dem Teil und dem Zustand zugeordnete nicht-Client Beschriftungs Bereich mit der Text Breite variiert.                                                                                                                 |
| TMT- \_ bgfill               | **True** , wenn die mit dem Teil und dem Zustand verknüpften Bilder in der Größe des Hintergrunds gezeichnet werden sollen.                                                                                                        |
| TMT \_ borderonly           | **True** , wenn das Bild, das dem Teil und dem Zustand zugeordnet ist, nur seinen Rahmen gezeichnet werden soll.                                                                                                                     |
| TMT \_ zusammengesetzt           | **True** , wenn das Steuerelement, das mit dem Part und State verknüpft ist, seine eigene Komposition von Bildern behandelt.                                                                                                           |
| TMT \_ compositedopaque     |                                                                                                                                                                                                                 |
| TMT- \_ drawrahmens          |                                                                                                                                                                                                                 |
| TMT- \_ flatmenüs            | Weitere Informationen finden Sie unter [**getthemesysbool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool).                                                                                                                                                                 |
| TMT- \_ glyphonly            | **True** , wenn das Symbol, das dem Teil und dem Zustand zugeordnet ist, ohne Hintergrund gezeichnet werden soll.                                                                                                                  |
| TMT \_ glyphtransparent     | **True** , wenn das Symbol, das dem Teil und dem Zustand zugeordnet ist, über transparente Bereiche verfügt. Die Definition des TMT-glyphcolor-Werts, der die transparente Farbe definiert, finden Sie unter [**gettemecolor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor) \_ . |
| TMT \_ integralsizing       | **True** , wenn das truesize-Bild oder der Rahmen, das dem Teil und dem Zustand zugeordnet ist, auf den Faktor 2 festgelegt werden muss.                                                                                                     |
| TMT \_ localizedmirrorimage |                                                                                                                                                                                                                 |
| TMT \_ mirrorimage          | **True** , wenn das Bild, das dem Teil und dem Zustand zugeordnet ist, gekippt werden soll, wenn das Fenster im Lesemodus von rechts nach links angezeigt wird.                                                                         |
| TMT \_ noetchedebug       |                                                                                                                                                                                                                 |
| TMT \_ scaledbackground     |                                                                                                                                                                                                                 |
| TMT \_ sourcegrow           | **True** , wenn das dem Teil und dem Status zugeordnete Bild bei Bedarf vergrößert werden soll.                                                                                                                |
| TMT \_ sourceshrink         | **True** , wenn das dem Teil und dem Status zugeordnete Bild bei Bedarf kleiner skaliert werden soll.                                                                                                               |
| TMT \_ textapplyoverlay     |                                                                                                                                                                                                                 |
| TMT- \_ textglanz             |                                                                                                                                                                                                                 |
| TMT \_ textitalic           |                                                                                                                                                                                                                 |
| TMT \_ transparent          |                                                                                                                                                                                                                 |
| TMT- \_ Dimensionierung        | **True** , wenn das dem Teil und dem Zustand zugeordnete Bild die gleiche Höhe und Breite aufweisen muss.                                                                                                                      |
| TMT- \_ Benutzer Bild          | **True** , wenn das dem Teil und dem Status zugeordnete Bild auf dem aktuellen Benutzer basiert.                                                                                                                          |



 

**TMT- \_ Farbe**



| id                           | Notizen                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ accentcolorhint         | Die Farbe, die als Akzent-Farb Hinweis für benutzerdefinierte Steuerelemente verwendet wird.                                                                                                                                    |
| TMT \_ ActiveBorder            |                                                                                                                                                                                                |
| TMT \_ ActiveCaption           |                                                                                                                                                                                                |
| TMT \_ AppWorkspace            |                                                                                                                                                                                                |
| TMT- \_ Hintergrund              |                                                                                                                                                                                                |
| TMT \_ blendcolor              | Die Farbe, die als Blend-Farbe verwendet wird.                                                                                                                                                               |
| TMT \_ bodytextcolor           |                                                                                                                                                                                                |
| TMT- \_ BorderColor             | Die Farbe des Rahmens, der dem Teil und dem Zustand zugeordnet ist.                                                                                                                                    |
| TMT \_ bordercolorhint         | Die Farbe, die als Rahmen Farb Hinweis für benutzerdefinierte Steuerelemente verwendet wird.                                                                                                                                     |
| TMT- \_ btnface                 |                                                                                                                                                                                                |
| TMT \_ btnhervorhebung            |                                                                                                                                                                                                |
| TMT \_ btnshadow               |                                                                                                                                                                                                |
| TMT \_ btntext                 |                                                                                                                                                                                                |
| TMT \_ buttonalternative     |                                                                                                                                                                                                |
| TMT \_ CaptionText             |                                                                                                                                                                                                |
| TMT \_ DKSHADOW3D              |                                                                                                                                                                                                |
| TMT \_ edgedkshadowcolor       | Die dunkle Schatten Farbe des Edge, der diesem Teil und Zustand zugeordnet ist.                                                                                                                         |
| TMT \_ edgefillcolor           | Die Füllfarbe des Edge, der diesem Teil und Zustand zugeordnet ist.                                                                                                                                |
| TMT \_ edgehighlightcolor      | Die Hervorhebungs Farbe des Edge, der diesem Teil und Zustand zugeordnet ist.                                                                                                                           |
| TMT \_ edgelightcolor          | Die helle Farbe des Edge, der diesem Teil und Zustand zugeordnet ist.                                                                                                                               |
| TMT \_ edgeshadowcolor         | Die Schatten Farbe des Edge, der diesem Teil und Zustand zugeordnet ist.                                                                                                                              |
| TMT \_ FillColor               | Die Farbe der Hintergrund Füllung, die dem Teil und dem Zustand zugeordnet ist.                                                                                                                           |
| TMT \_ fillcolorhint           | Die Farbe, die als Füll Farb Hinweis für benutzerdefinierte Steuerelemente verwendet wird.                                                                                                                                       |
| TMT \_ FROMCOLOR1              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR2              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR3              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR4              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR5              |                                                                                                                                                                                                |
| TMT- \_ GlowColor               | Die Farbe des Leucht Effekts, der durch Aufrufen von [**drawthemeicon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon) mithilfe dieses Teils und Zustands erzeugt wird.                                                                                    |
| TMT \_ glyphtextcolor          | Die Farbe, mit der das Schriftart basierte Symbol, das diesem Teil und Zustand zugeordnet ist, verwendet wird.                                                                                                              |
| TMT \_ glyphtransparentcolor   | Die transparente Symbol Farbe, die diesem Teil und Zustand zugeordnet ist. Wenn der TMT \_ -glyphtransparent-Wert für diesen Teil und State **true** ist, werden Teile des Symbols, die diese Farbe verwenden, nicht gezeichnet. |
| TMT \_ GradientActiveCaption   |                                                                                                                                                                                                |
| TMT \_ GRADIENTCOLOR1          | Die erste Farbe des Farbverlaufs, der diesem Teil und Zustand zugeordnet ist.                                                                                                                           |
| TMT \_ GRADIENTCOLOR2          | Die zweite Farbe des Farbverlaufs.                                                                                                                                                              |
| TMT \_ GRADIENTCOLOR3          | Die dritte Farbe des Farbverlaufs.                                                                                                                                                               |
| TMT \_ GRADIENTCOLOR4          | Die vierte Farbe des Farbverlaufs.                                                                                                                                                              |
| TMT \_ GRADIENTCOLOR5          | Die fünfte Farbe des Farbverlaufs.                                                                                                                                                               |
| TMT \_ GradientInactiveCaption |                                                                                                                                                                                                |
| TMT- \_ GrayText                |                                                                                                                                                                                                |
| TMT \_ HEADING1TEXTCOLOR       |                                                                                                                                                                                                |
| TMT \_ HEADING2TEXTCOLOR       |                                                                                                                                                                                                |
| TMT- \_ Hervorhebung               |                                                                                                                                                                                                |
| TMT \_ HighlightText           |                                                                                                                                                                                                |
| TMT- \_ HotTracking             |                                                                                                                                                                                                |
| TMT \_ inactiveborder          |                                                                                                                                                                                                |
| TMT \_ InactiveCaption         |                                                                                                                                                                                                |
| TMT \_ InactiveCaptionText     |                                                                                                                                                                                                |
| TMT- \_ infobk                  |                                                                                                                                                                                                |
| TMT- \_ Infotext                |                                                                                                                                                                                                |
| TMT \_ LIGHT3D                 |                                                                                                                                                                                                |
| TMT- \_ Menü                    |                                                                                                                                                                                                |
| TMT- \_ Menüleiste                 |                                                                                                                                                                                                |
| TMT \_ menuhilight             |                                                                                                                                                                                                |
| TMT- \_ MenuText                |                                                                                                                                                                                                |
| TMT- \_ Scrollleiste               |                                                                                                                                                                                                |
| TMT \_ ShadowColor             | Die Farbe des Schattens, der unterhalb des Texts gezeichnet wird, der diesem Teil und Zustand zugeordnet ist.                                                                                                             |
| TMT \_ textbordercolor         | Die Farbe des Textrahmens, der diesem Teil und Zustand zugeordnet ist.                                                                                                                              |
| TMT- \_ Textfarbe               | Die Farbe des Texts, der diesem Teil und Zustand zugeordnet ist.                                                                                                                                     |
| TMT- \_ textcolorhint           |                                                                                                                                                                                                |
| TMT \_ textShadowColor         | Die Farbe des Text Schattens, der diesem Teil und Zustand zugeordnet ist.                                                                                                                              |
| TMT- \_ TransparentColor        | Die transparente Farbe, die diesem Teil und Zustand zugeordnet ist. Wenn der transparente TMT \_ -Wert für diesen Teil und State **true** ist, werden Teile der Grafik, die diese Farbe verwenden, nicht gezeichnet.          |
| TMT- \_ Fenster                  |                                                                                                                                                                                                |
| TMT- \_ WindowFrame             |                                                                                                                                                                                                |
| TMT- \_ WindowText              |                                                                                                                                                                                                |



 

**TMT \_ diskstream**



| id              | Notizen |
|-----------------|-------|
| TMT \_ atlasimage |       |



 

**TMT-Aufzählung \_**



| Enumeration         | Eigenschaftswerte                                                                                                                                                                                                                                            | Notizen                                                                                                                                                |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bgtype              | BT \_ ImageFile, BT \_ borderfill                                                                                                                                                                                                                              | Der grundlegende Zeichentyp für diesen Teil.                                                                                                                |
| Den BorderType          | BT \_ Rect, BT \_ roundRect, BT \_ Ellipse                                                                                                                                                                                                                       | Der Typ des Rahmens, der gezeichnet wird, wenn dieser Teil eine Rahmenfüllung ist.                                                                                              |
| CONTENTALIGNMENT    | ca \_ left, ca \_ Center, ca \_ right                                                                                                                                                                                                                            | Die Textausrichtung in der Beschriftung, die diesem Teil zugeordnet ist.                                                                                      |
| FILLTYPE            | FT \_ Solid, ft \_ vertgradient, ft \_ horzgradient, ft \_ radialGradient, ft \_ tileimage                                                                                                                                                                           | Der Typ der Füll Form, der gezeichnet wird, wenn dieser Teil eine Rahmenfüllung ist.                                                                                          |
| GlyphType           | gt \_ None, gt \_ imageglyph, gt \_ fontglyph                                                                                                                                                                                                                    | Der Typ des Symbols, das für diesen Teil gezeichnet wird.                                                                                                                |
| GlyphFontSizingType | gfst \_ None, gfst \_ size, gfst \_ dpi                                                                                                                                                                                                                          | Der Typ der Methode, die verwendet wird, um zwischen verschiedenen Symbolen auszuwählen.                                                                                    |
| Halign              | hochverfügbarkeitzentriert \_ , ha \_ Center, ha \_ right                                                                                                                                                                                                                            | Die horizontale Ausrichtung, wenn dieser Teil ein Bild mit der Größe true verwendet.                                                                                        |
| IconEffect          | Ice \_ None, Ice \_ Glüh, Ice \_ Shadow, Ice \_ Pulse, Ice \_ Alpha                                                                                                                                                                                                  | Der Typ des Effekts, der angezeigt werden soll, wenn dieser Teil mithilfe von [**drawthemeicon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon)gezeichnet wird.                                             |
| Image Layout         | Il \_ Vertikal, Il \_ Horizontal                                                                                                                                                                                                                               | Der Typ der Ausrichtung, der verwendet wird, wenn mehrere Bilder gezeichnet werden.                                                                                           |
| ImageSelectType     | ist \_ None, ist \_ size, ist \_ dpi                                                                                                                                                                                                                             | Der Typ der Methode, die verwendet wird, um zwischen Bildern für diesen Teil auszuwählen. Weitere Informationen finden Sie unter TMT \_ IMAGEFILE1-Wert von [**gettemefilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename). |
| OffsetType          | OT \_ TopLeft, OT \_ TopRight, OT \_ topmiddle, OT \_ BottomLeft, OT \_ BottomRight, OT \_ bottommiddle, OT \_ Mittel dleleft, OT \_ Mittel dleright, OT Left \_ fcaption, OT \_ Righto fcaption, OT Left \_ flastbutton, OT \_ righumflastbutton, OT \_ abovelastbutton, OT \_ belowlastbutton | Die Ausrichtung dieses Teils im Fenster.                                                                                                            |
| SizingType          | St \_ truesize, St \_ Stretch, St \_ Tile, St \_ tilehorz, St \_ tilevert, St \_ tilecenter                                                                                                                                                                            | Die Methode, die zum Anpassen eines Bilds verwendet wird, wenn in diesem Teil eine Bilddatei verwendet wird.                                                                                    |
| TextShadowType      | TST \_ None, TST \_ Single, TST \_ Continuous                                                                                                                                                                                                                    | Der Typ des Schatten Effekts, der hinter dem diesem Teil zugeordneten Text gezeichnet werden soll.                                                                             |
| TrueSizeScalingType | Zst \_ None, St \_ size, Zst \_ dpi                                                                                                                                                                                                                          | Der Typ der Skalierung, der verwendet wird, wenn in diesem Teil ein Image der Größe true verwendet wird.                                                                                       |
| Wird überprüft              | VA \_ oben, VA \_ Center, VA \_ unten                                                                                                                                                                                                                            | Die vertikale Ausrichtung, wenn dieser Teil ein Bild mit der Größe true verwendet.                                                                                          |



 

**TMT \_ Dateiname**



| id                  | Notizen                                                                                                                                        |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ glyphimagefile | Der Dateiname für das Symbolbild, das diesem Teil und Zustand zugeordnet ist.                                                                        |
| TMT- \_ ImageFile      | Der Dateiname des Bilds, das diesem Teil und Zustand zugeordnet ist, oder der Basis Dateiname für mehrere Abbilder, die diesem Teil und Zustand zugeordnet sind. |
| TMT \_ IMAGEFILE1     | Der Dateiname des ersten skalierten Bilds, das diesem Teil und Zustand zugeordnet ist, für die Unterstützung unterschiedlicher Auflösungen.                            |
| TMT \_ IMAGEFILE2     | Der Dateiname des zweiten skalierten Bilds.                                                                                                     |
| TMT \_ IMAGEFILE3     | Der Dateiname des dritten skalierten Bilds.                                                                                                      |
| TMT \_ IMAGEFILE4     | Der Dateiname des vierten skalierten Bilds.                                                                                                     |
| TMT \_ IMAGEFILE5     | Der Dateiname des fünften skalierten Bilds.                                                                                                      |



 

**TMT- \_ Schriftart**



| id                    | Notizen                                                                                                |
|-----------------------|------------------------------------------------------------------------------------------------------|
| TMT- \_ bodyfont         |                                                                                                      |
| TMT \_ CaptionFont      |                                                                                                      |
| TMT- \_ glyphfont        | Die Schriftart, mit der das diesem Teil zugeordnete Symbol gezeichnet wird, wenn Schriftart basierte Symbole verwendet werden. |
| TMT \_ HEADING1FONT     |                                                                                                      |
| TMT \_ HEADING2FONT     |                                                                                                      |
| TMT \_ IconTitleFont    |                                                                                                      |
| TMT- \_ menufont         |                                                                                                      |
| TMT \_ msgboxfont       |                                                                                                      |
| TMT \_ SmallCaptionFont |                                                                                                      |
| TMT- \_ Status Schriftart       |                                                                                                      |



 

**TMT \_ int**



| id                       | Notizen                                                                                                                                                                                                            |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ alphalevel          | Der Alpha-Wert (0-255), der für [**drawthemeicon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon)verwendet wird.                                                                                                                                         |
| TMT \_ AlphaThreshold      | Der minimale Alpha-Wert (0-255), der von einem Pixel als nicht transparent angesehen werden muss.                                                                                                                                  |
| TMT \_ animationdelay      |                                                                                                                                                                                                                  |
| TMT \_ animationduration   |                                                                                                                                                                                                                  |
| TMT- \_ BorderSize          | Die Stärke des Rahmens, der gezeichnet wird, wenn in diesem Teil eine Rahmenfüllung verwendet wird.                                                                                                                                               |
| TMT-Zeichen \_ Satz             |                                                                                                                                                                                                                  |
| TMT \_ colorizationcolor   |                                                                                                                                                                                                                  |
| TMT \_ colorizationopacity |                                                                                                                                                                                                                  |
| TMT- \_ framesPerSecond     |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE1            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE2            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE3            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE4            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE5            |                                                                                                                                                                                                                  |
| TMT- \_ glowintensity       |                                                                                                                                                                                                                  |
| TMT- \_ Glyphindex          | Der Zeichen Index in die ausgewählte Schriftart, die für das Symbol verwendet wird, wenn der Teil ein Schriftart basiertes Symbol verwendet.                                                                                                 |
| TMT \_ GRADIENTRATIO1      | Die Menge der ersten Farbverlaufs Farbe (TMT \_ GRADIENTCOLOR1), die beim Zeichnen des Teils verwendet werden soll. Dieser Wert kann zwischen 0 und 255 liegen, aber dieser Wert und die Werte der einzelnen GradientRatio-Werte müssen bis zu 255 addieren. |
| TMT \_ GRADIENTRATIO2      | Die Menge der zweiten Farbverlaufs Farbe (TMT \_ GRADIENTCOLOR2), die beim Zeichnen des Teils verwendet werden soll.                                                                                                                        |
| TMT \_ GRADIENTRATIO3      | Die Menge der dritten Farbverlaufs Farbe (TMT \_ GRADIENTCOLOR3), die beim Zeichnen des Teils verwendet werden soll.                                                                                                                         |
| TMT \_ GRADIENTRATIO4      | Die Menge der vierten Farbverlaufs Farbe (TMT \_ GRADIENTCOLOR4), die beim Zeichnen des Teils verwendet werden soll.                                                                                                                        |
| TMT \_ GRADIENTRATIO5      | Die Menge der fünften Farbverlaufs Farbe (TMT \_ GRADIENTCOLOR5), die beim Zeichnen des Teils verwendet werden soll.                                                                                                                         |
| TMT- \_ Höhe              | Die Höhe des Teils.                                                                                                                                                                                          |
| TMT- \_ imagecount          | Die Anzahl von Zustands Bildern, die in einer Bilddatei vorhanden sind.                                                                                                                                                             |
| TMT \_ mincolortiefe       |                                                                                                                                                                                                                  |
| TMT \_ MINDPI1             | Die minimale Anzahl von Punkten pro Zoll (dpi), für die die erste Bilddatei entworfen wurde.                                                                                                                                      |
| TMT \_ MINDPI2             | Der minimale dpi-Wert, für den die zweite Bilddatei entworfen wurde.                                                                                                                                                     |
| TMT \_ MINDPI3             | Der minimale dpi-Wert, für den die dritte Bilddatei entworfen wurde.                                                                                                                                                      |
| TMT \_ MINDPI4             | Der minimale dpi-Wert, für den die vierte Bilddatei entworfen wurde.                                                                                                                                                     |
| TMT \_ MINDPI5             | Der minimale dpi-Wert, für den die fünfte Bilddatei entworfen wurde.                                                                                                                                                      |
| TMT- \_ Deckkraft             |                                                                                                                                                                                                                  |
| TMT \_ pixelsperframe      |                                                                                                                                                                                                                  |
| TMT \_ progresschunksize   | Die Größe der "Block"-Formen des Status Steuer Elements, die definieren, wie weit ein Vorgang fortgeschritten ist.                                                                                                                 |
| TMT \_ progressspacesize   | Die Gesamtgröße aller "Blöcke" der Fortschritts Steuerung.                                                                                                                                                          |
| TMT \_ roundcornerheight   | Die Rundheit (0 bis 100 Prozent) der Ecken des Teils.                                                                                                                                                          |
| TMT \_ roundcornerwidth    | Die Rundheit (0 bis 100 Prozent) der Ecken des Teils.                                                                                                                                                          |
| TMT- \_ Sättigung          | Der Umfang der Sättigung (0-255), der auf ein Symbol angewendet werden soll, das mit [**drawthemeicon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon)gezeichnet wird.                                                                                                         |
| TMT \_ textbordersize      | Die Stärke des Rahmens, der um Textzeichen gezeichnet wird.                                                                                                                                                        |
| TMT \_ textglowsize        |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR1            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR2            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR3            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR4            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR5            |                                                                                                                                                                                                                  |
| TMT \_ TOHUE1              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE2              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE3              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE4              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE5              |                                                                                                                                                                                                                  |
| TMT \_ truesizestretchmark | Der Prozentsatz der ursprünglichen Größe eines Bilds, bei dem das Bild gestreckt wird.                                                                                                                        |
| TMT- \_ Breite               | Die Breite des Teils.                                                                                                                                                                                           |



 

**TMT- \_ intlist**



| id                       | Notizen |
|--------------------------|-------|
| TMT \_ transitiondurations |       |



 

**TMT- \_ Ränder**



| id                  | Notizen                                                                   |
|---------------------|-------------------------------------------------------------------------|
| TMT- \_ beschriften Ränder | Die Ränder, die definieren, wo der Beschriftungs Text in einem Teil platziert werden kann. |
| TMT- \_ Inhalts Ränder | Die Ränder, die definieren, wo der Inhalt in einem Teil platziert werden kann.      |
| TMT- \_ sizingränder  | Die Ränder, die zur Größenanpassung eines Bilds verwendet werden, das keine echte Größe ist.                      |



 

**TMT- \_ Position**



| id                    | Notizen                                                                                                        |
|-----------------------|--------------------------------------------------------------------------------------------------------------|
| TMT \_ MinSize          | Die minimale Größe, die für die normale Bilddatei verwendet werden kann, bevor die nächste kleinste Bilddatei verschoben wird.   |
| TMT \_ MINSIZE1         | Die minimale Größe, für die die erste kleine Bilddatei verwendet werden kann.                                            |
| TMT \_ MINSIZE2         | Die minimale Größe, für die die zweite kleine Bilddatei verwendet werden kann.                                           |
| TMT \_ MINSIZE3         | Die minimale Größe, für die die dritte kleine Bilddatei verwendet werden kann.                                            |
| TMT \_ MINSIZE4         | Die minimale Größe, für die die vierte kleine Bilddatei verwendet werden kann.                                           |
| TMT \_ MINSIZE5         | Die minimale Größe, für die die fünfte kleine Bilddatei verwendet werden kann.                                            |
| TMT \_ Normalgröße       | Die Größe des diesem Teil zugeordneten normalen Bilds.                                                      |
| TMT- \_ Offset           | Der Positions Offset von der Ausrichtung für diesen Teil. Die Ausrichtung wird durch den TMT \_ OffsetType-Wert definiert. |
| TMT \_ textshadowoffset | Der Offset des Texts, bei dem Text Schatten gezeichnet werden.                                                    |



 

**TMT- \_ Rect**



| id                       | Notizen                         |
|--------------------------|-------------------------------|
| TMT \_ animationbuttonrect |                               |
| TMT \_ atlasrect           |                               |
| TMT \_ customsplitrect     |                               |
| TMT \_ defaultpanesize     | Die Standardgröße des Teils. |



 

**TMT- \_ Größe**



| id                      | Notizen                     |
|-------------------------|---------------------------|
| TMT \_ captionbarheight   | Höhe der Beschriftungs Leiste.       |
| TMT \_ captionbarwidth    | Breite der Beschriftungs Leiste.        |
| TMT \_ MenuBarHeight      | Höhe der Menüleiste.          |
| TMT \_ menubarwidth       | Menüleisten Breite.           |
| TMT \_ paddädborderwidth  | Breite des aufgefüllten Rahmens.      |
| TMT \_ scrollbarheight    | Die Höhe der Scrollleiste.        |
| TMT \_ scrollbarwidth     | Breite der Scrollleiste.         |
| TMT \_ SizingBorderWidth  | Breite eines Größen Anpassungs Rahmens. |
| TMT \_ smcaptionbarheight | Höhe der Beschriftungs Leiste.       |
| TMT \_ smcaptionbarwidth  | Breite der Beschriftungs Leiste.        |



 

**TMT- \_ Zeichenfolge**



| id                   | Notizen                                               |
|----------------------|-----------------------------------------------------|
| TMT- \_ Alias           |                                                     |
| TMT \_ atlasinputimage |                                                     |
| TMT- \_ Autor          |                                                     |
| TMT \_ classicvalue    |                                                     |
| TMT \_ colorschemas    |                                                     |
| TMT- \_ Unternehmen         |                                                     |
| TMT- \_ Copyright       |                                                     |
| TMT \_ cssname         | Siehe " [**getthemesysstring**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)". |
| TMT- \_ Beschreibung     |                                                     |
| TMT- \_ Display Name     |                                                     |
| TMT \_ lastupveraltet     |                                                     |
| TMT- \_ Größen           |                                                     |
| TMT- \_ Text            | Der vom Teil angezeigte Text.                     |
| TMT-QuickInfo \_         |                                                     |
| TMT- \_ URL             |                                                     |
| TMT- \_ Version         |                                                     |
| TMT- \_ XMLName         | Siehe " [**getthemesysstring**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)". |
| TMT- \_ Name            |                                                     |



 

 

 
