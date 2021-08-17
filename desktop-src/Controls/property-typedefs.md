---
title: Eigenschaftenbezeichner (Windows Steuerelemente)
description: Dieses Thema enthält Informationen zu definierten Werten, die zum Abrufen von Eigenschaften visueller Stile verwendet werden. Die Definitionen befinden sich in Vssym32.h.
ms.assetid: b0e22022-fea9-43d1-8ef0-7a1c518760f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf20429d5eb5bd45ea850e3b77c5734ab6b8e0fa0e63fe4c1d2b1c918f837f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078864"
---
# <a name="property-identifiers-windows-controls"></a>Eigenschaftenbezeichner (Windows Steuerelemente)

Dieses Thema enthält Informationen zu definierten Werten, die zum Abrufen von Eigenschaften visueller Stile verwendet werden. Die Definitionen befinden sich in Vssym32.h.

## <a name="property-types"></a>Eigenschaftentypen

In der folgenden Tabelle sind die primitiven Eigenschaftentypen aufgeführt. Die Werte in der ersten Spalte werden normalerweise nicht von Anwendungen verwendet, bieten aber eine Möglichkeit zum Klassifizieren von Eigenschaftenbezeichnern.



| Datentyp       | BESCHREIBUNG                              | Zurückgegebener Typ                          | Abruffunktion                                                                                                     |
|-----------------|------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| TMT \_ BOOL       | **TRUE** oder **FALSE**                    | Boolean                                | [**GetThemeBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebool), [ **GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool)                                       |
| \_TMT-FARBE      | RGB-Farbwert                          | [**COLORREF-Struktur**](/windows/desktop/gdi/colorref) | [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor), [ **GetThemeSysColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesyscolor)                                   |
| TMT \_ DISKSTREAM | Datenträgerstream                              | **Hinstance**                          | [**GetThemeStream**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestream)                                                                               |
| \_TMT-ENUM       | Enumerationswert                         | Enumeration                            | [**GetThemeEnumValue**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeenumvalue).                                                                        |
| TMT \_ FILENAME   | Dateiname relativ zum Designverzeichnis | **WCHAR-Array**                        | [**GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename)                                                                           |
| \_TMT-SCHRIFTART       | Schriftartbeschreibung                         | [**LOGFONT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logfonta)   | [**GetThemeFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefont), [ **GetThemeSysFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysfont)                                       |
| TMT \_ HBITMAP    | Bitmap                                   | **HBITMAP-Handle**                     | [**GetThemeBitmap**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebitmap)                                                                               |
| TMT \_ INT        | Zahl mit Vorzeichen                            | Integer                                | [**GetThemeInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeint), [**GetThemeSysInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysint), [**GetThemeMetric**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememetric) |
| TMT \_ INTLIST    | Liste der ganzen Zahlen                         | [**INTLIST-Struktur**](/windows/desktop/api/UxTheme/ns-uxtheme-intlist)   | [**GetThemeIntList**](/windows/desktop/api/UxTheme/nf-uxtheme-getthemeintlist)                                                                             |
| \_TMT-RÄNDER    | Ränder: links, oben, rechts und unten    | [**MARGINS-Struktur**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins)   | [**GetThemeMargins**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememargins)                                                                             |
| \_TMT-POSITION   | Speicherort eines Elements                      | [**POINT-Struktur**](/previous-versions//dd162805(v=vs.85))       | [**GetThemePosition**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeposition)                                                                           |
| TMT \_ RECT       | Größe und Position eines Rechtecks         | [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85))         | [**GetThemeRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemerect)                                                                                   |
| \_TMT-GRÖßE       | Größe eines Elements                          | [**SIZE-Struktur**](/previous-versions//dd145106(v=vs.85))         | [**GetThemePartSize**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemepartsize)                                                                           |
| TMT \_ STRING     | Unicode-Zeichenfolge                           | **WCHAR-Array**                        | [**GetThemeString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestring), [ **GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)                               |



 

## <a name="property-ids"></a>Eigenschaften-IDs

Im Folgenden finden Sie die definierten Werte für Designeigenschaften, die nach Datentypen gruppiert sind.

**TMT \_ BOOL**



| ID                        | Hinweise                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALWAYSSHOWSIZINGBAR  | **TRUE,** wenn die Größenleiste, die dem Teil und dem Zustand zugeordnet ist, immer angezeigt werden soll.                                                                                                                           |
| TMT \_ AUTOIZE             | **TRUE,** wenn der dem Teil und Zustand zugeordnete Beschriftungsbereich ohne Client mit der Textbreite variiert.                                                                                                                 |
| TMT \_ BGFILL               | **TRUE,** wenn bilder mit der richtigen Größe, die dem Teil und dem Zustand zugeordnet sind, auf der Hintergrundfüllung gezeichnet werden sollen.                                                                                                        |
| TMT \_ BORDERONLY           | **TRUE,** wenn für das dem Teil und Zustand zugeordnete Bild nur der Rahmen gezeichnet werden soll.                                                                                                                     |
| TMT \_ COMPOSITED           | **TRUE,** wenn das steuerelement, das dem Teil und dem Zustand zugeordnet ist, seine eigene Bildkompositing verarbeitet.                                                                                                           |
| TMT \_ COMPOSITEDOPAQUE     |                                                                                                                                                                                                                 |
| TMT \_ DRAWBORDERS          |                                                                                                                                                                                                                 |
| TMT \_ FLATMENUS            | Weitere Informationen [**finden Sie unter GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool).                                                                                                                                                                 |
| TMT \_ GLYPHONELY            | **TRUE,** wenn das dem Teil und zustand zugeordnete Glyph ohne Hintergrund gezeichnet werden soll.                                                                                                                  |
| TMT \_ GLYPHTRANSPARENT     | **TRUE,** wenn das dem Teil und zustand zugeordnete Glyph transparente Bereiche hat. Unter [**GetThemeColor finden**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor) Sie die Definition des TMT \_ GLYPHCOLOR-Werts, der die transparente Farbe definiert. |
| TMT \_ INTEGRALSIZING       | **TRUE,** wenn das Bild oder der Rahmen, das dem Teil und dem Zustand zugeordnet ist, truesize auf den Faktor 2 dimensioniert werden muss.                                                                                                     |
| TMT \_ LOCALIZEDMIRRORIMAGE |                                                                                                                                                                                                                 |
| TMT \_ MIRRORIMAGE          | **TRUE,** wenn das dem Teil und zustand zugeordnete Bild gekippt werden soll, wenn das Fenster im Lesemodus von rechts nach links angezeigt wird.                                                                         |
| TMT \_ NOETCHEDEFFECT       |                                                                                                                                                                                                                 |
| TMT \_ SCALEDBACKGROUND     |                                                                                                                                                                                                                 |
| TMT \_ SOURCEGROW           | **TRUE,** wenn das image, das dem Teil und zustand zugeordnet ist, bei Bedarf größer skaliert wird.                                                                                                                |
| \_TMT-QUELLENHRINK         | **TRUE,** wenn das image, das dem Teil und zustand zugeordnet ist, bei Bedarf kleiner skaliert wird.                                                                                                               |
| TMT \_ TEXTAPPLYOVERLAY     |                                                                                                                                                                                                                 |
| TMT \_ TEXTGLOW             |                                                                                                                                                                                                                 |
| TMT \_ TEXTITALIC           |                                                                                                                                                                                                                 |
| TMT \_ TRANSPARENT          |                                                                                                                                                                                                                 |
| TMT \_ UNIFORMSIZING        | **TRUE,** wenn das dem Teil und dem Zustand zugeordnete Bild die gleiche Höhe und Breite haben muss.                                                                                                                      |
| TMT \_ USERPICTURE          | **TRUE,** wenn das image, das dem Teil und dem Zustand zugeordnet ist, auf dem aktuellen Benutzer basiert.                                                                                                                          |



 

**\_TMT-FARBE**



| ID                           | Hinweise                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ACCENTCOLORHINT         | Die Farbe, die als Akzentfarbhinweis für benutzerdefinierte Steuerelemente verwendet wird.                                                                                                                                    |
| TMT \_ ACTIVEBORDER            |                                                                                                                                                                                                |
| TMT \_ ACTIVECAPTION           |                                                                                                                                                                                                |
| TMT \_ APPWORKSPACE            |                                                                                                                                                                                                |
| TMT \_ BACKGROUND              |                                                                                                                                                                                                |
| TMT \_ BLENDCOLOR              | Die Farbe, die als Mischungsfarbe verwendet wird.                                                                                                                                                               |
| TMT \_ BODYTEXTCOLOR           |                                                                                                                                                                                                |
| TMT \_ BORDERCOLOR             | Die Farbe des Rahmens, der dem Teil und zustand zugeordnet ist.                                                                                                                                    |
| TMT \_ BORDERCOLORHINT         | Die Farbe, die als Rahmenfarbhinweis für benutzerdefinierte Steuerelemente verwendet wird.                                                                                                                                     |
| TMT \_ BTNFACE                 |                                                                                                                                                                                                |
| TMT \_ BTNHIGHLIGHT            |                                                                                                                                                                                                |
| TMT \_ BTNSHADOW               |                                                                                                                                                                                                |
| TMT \_ BTNTEXT                 |                                                                                                                                                                                                |
| TMT \_ BUTTONALTERNATEFACE     |                                                                                                                                                                                                |
| TMT \_ CAPTIONTEXT             |                                                                                                                                                                                                |
| TMT \_ DKSHADOW3D              |                                                                                                                                                                                                |
| TMT \_ EDGEDKSHADOWCOLOR       | Die dunkle Schattenfarbe des Rands, der diesem Teil und Zustand zugeordnet ist.                                                                                                                         |
| TMT \_ EDGEFILLCOLOR           | Die Füllfarbe des Rands, der diesem Teil und Zustand zugeordnet ist.                                                                                                                                |
| TMT \_ EDGEHIGHLIGHTCOLOR      | Die Hervorhebungsfarbe des Rands, der diesem Teil und Zustand zugeordnet ist.                                                                                                                           |
| TMT \_ EDGELIGHTCOLOR          | Die helle Farbe des Rands, der diesem Teil und Zustand zugeordnet ist.                                                                                                                               |
| TMT \_ EDGESHADOWCOLOR         | Die Schattenfarbe des Rands, der diesem Teil und Zustand zugeordnet ist.                                                                                                                              |
| TMT \_ FILLCOLOR               | Die Farbe der Hintergrundfüllung, die dem Teil und zustand zugeordnet ist.                                                                                                                           |
| TMT \_ FILLCOLORHINT           | Die Farbe, die als Füllfarbe für benutzerdefinierte Steuerelemente verwendet wird.                                                                                                                                       |
| TMT \_ FROMCOLOR1              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR2              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR3              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR4              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR5              |                                                                                                                                                                                                |
| TMT \_ GLOWCOLOR               | Die Farbe des Lichts, das durch Aufrufen von [**DrawThemeIcon mithilfe dieses**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon) Teils und Zustands erzeugt wird.                                                                                    |
| TMT \_ GLYPHTEXTCOLOR          | Die Farbe, die das schriftartbasierte Glyph verwendet, das diesem Teil und Zustand zugeordnet ist.                                                                                                              |
| TMT \_ GLYPHTRANSPARENTCOLOR   | Die transparente Glyphenfarbe, die diesem Teil und Zustand zugeordnet ist. Wenn der TMT GLYPHTRANSPARENT-Wert für diesen Teil und Zustand TRUE ist, werden Teile des Symbols, die diese Farbe \_ verwenden, nicht gezeichnet. |
| TMT \_ GRADIENTACTIVECAPTION   |                                                                                                                                                                                                |
| TMT \_ GRADIENTCOLOR1          | Die erste Farbe des Farbverlaufs, die diesem Teil und Zustand zugeordnet ist.                                                                                                                           |
| TMT \_ GRADIENTCOLOR2          | Die zweite Farbe des Farbverlaufs.                                                                                                                                                              |
| TMT \_ GRADIENTCOLOR3          | Die dritte Farbe des Farbverlaufs.                                                                                                                                                               |
| TMT \_ GRADIENTCOLOR4          | Die vierte Farbe des Farbverlaufs.                                                                                                                                                              |
| TMT \_ GRADIENTCOLOR5          | Die fünfte Farbe des Farbverlaufs.                                                                                                                                                               |
| TMT \_ GRADIENTINACTIVECAPTION |                                                                                                                                                                                                |
| TMT \_ GRAYTEXT                |                                                                                                                                                                                                |
| TMT \_ HEADING1TEXTCOLOR       |                                                                                                                                                                                                |
| TMT \_ HEADING2TEXTCOLOR       |                                                                                                                                                                                                |
| TMT \_ HIGHLIGHT               |                                                                                                                                                                                                |
| TMT \_ HIGHLIGHTTEXT           |                                                                                                                                                                                                |
| TMT \_ HOTTRACKING             |                                                                                                                                                                                                |
| TMT \_ INACTIVEBORDER          |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTION         |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTIONTEXT     |                                                                                                                                                                                                |
| TMT \_ INFOBK                  |                                                                                                                                                                                                |
| TMT \_ INFOTEXT                |                                                                                                                                                                                                |
| TMT \_ LIGHT3D                 |                                                                                                                                                                                                |
| \_TMT-MENÜ                    |                                                                                                                                                                                                |
| \_TMT-MENÜLEISTE                 |                                                                                                                                                                                                |
| TMT \_ MENUHILIGHT             |                                                                                                                                                                                                |
| TMT \_ MENUTEXT                |                                                                                                                                                                                                |
| TMT \_ SCROLLBAR               |                                                                                                                                                                                                |
| TMT \_ SHADOWCOLOR             | Die Farbe des Schattens, der unter dem Text gezeichnet wird, der diesem Teil und Zustand zugeordnet ist.                                                                                                             |
| TMT \_ TEXTBORDERCOLOR         | Die Farbe des text-Rahmens, der diesem Teil und Zustand zugeordnet ist.                                                                                                                              |
| TMT \_ TEXTCOLOR               | Die Farbe des Texts, der diesem Teil und Zustand zugeordnet ist.                                                                                                                                     |
| TMT \_ TEXTCOLORHINT           |                                                                                                                                                                                                |
| TMT \_ TEXTSHADOWCOLOR         | Die Farbe des Textschattens, der diesem Teil und Zustand zugeordnet ist.                                                                                                                              |
| TMT \_ TRANSPARENTCOLOR        | Die transparente Farbe, die diesem Teil und Zustand zugeordnet ist. Wenn der TMT TRANSPARENT-Wert für diesen Teil und Zustand TRUE ist, werden Teile der Grafik, die diese Farbe \_ verwenden, nicht gezeichnet.          |
| \_TMT-FENSTER                  |                                                                                                                                                                                                |
| TMT \_ WINDOWFRAME             |                                                                                                                                                                                                |
| TMT \_ WINDOWTEXT              |                                                                                                                                                                                                |



 

**TMT \_ DISKSTREAM**



| ID              | Hinweise |
|-----------------|-------|
| TMT \_ ATLASIMAGE |       |



 

**\_TMT-ENUM**



| Enumeration         | Eigenschaftswerte                                                                                                                                                                                                                                            | Hinweise                                                                                                                                                |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| BGTYPE              | BT \_ IMAGEFILE, BT \_ BORDERFILL                                                                                                                                                                                                                              | Der grundlegende Zeichnungstyp für diesen Teil.                                                                                                                |
| BORDERTYPE          | BT \_ RECT, BT \_ ROUNDRECT, BT \_ ELLIPSE                                                                                                                                                                                                                       | Der Typ des Rahmens, der gezeichnet wird, wenn dieser Teil eine Rahmenfüllung ist.                                                                                              |
| Contentalignment    | CA \_ LEFT, CA \_ CENTER, CA \_ RIGHT                                                                                                                                                                                                                            | Die Ausrichtung des Texts in der Diesem Teil zugeordneten Beschriftung.                                                                                      |
| FILLTYPE            | FT \_ SOLID, FT \_ VERTGRADIENT, FT \_ HORZGRADIENT, FT \_ RADIALGRADIENT, FT \_ TILEIMAGE                                                                                                                                                                           | Der Typ der gezeichneten Füllform, wenn es sich bei diesem Teil um eine Rahmenfüllung handelt.                                                                                          |
| GLYPHTYPE           | GT \_ NONE, GT \_ IMAGEGLYPH, GT \_ FONTGLYPH                                                                                                                                                                                                                    | Der Typ des für diesen Teil gezeichneten Glyphens.                                                                                                                |
| GLYPHFONTSIZINGTYPE | GFST \_ NONE, GFST \_ SIZE, GFST \_ DPI                                                                                                                                                                                                                          | Der Typ der Methode, mit der zwischen Glyphen unterschiedlicher Größe ausgewählt wird.                                                                                    |
| GSIGN              | HA \_ LEFT, HA \_ CENTER, HA \_ RIGHT                                                                                                                                                                                                                            | Die horizontale Ausrichtung, wenn dieser Teil ein Bild der richtigen Größe verwendet.                                                                                        |
| ICONEFFECT          | ICE \_ NONE, ICE \_ GLOW, ICE \_ SHADOW, ICE \_ PULSE, ICE \_ ALPHA                                                                                                                                                                                                  | Der Effekttyp, der angezeigt werden soll, wenn dieser Teil mit [**DrawThemeIcon gezeichnet wird.**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon)                                             |
| Imagelayout         | IL \_ VERTICAL, IL \_ HORIZONTAL                                                                                                                                                                                                                               | Der Typ der Ausrichtung, der verwendet wird, wenn mehrere Bilder gezeichnet werden.                                                                                           |
| IMAGESELECTTYPE     | IST \_ NONE, IST \_ SIZE, IST \_ DPI                                                                                                                                                                                                                             | Der Typ der Methode, die verwendet wird, um für diesen Teil Bilder mit unterschiedlicher Größe auszuwählen. Siehe den TMT \_ IMAGEFILE1-Wert [**von GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename). |
| OFFSETTYPE          | OT \_ TOPLEFT, OT \_ TOPRIGHT, OT \_ TOPMIDDLE, OT \_ BOTTOMLEFT, OT \_ BOTTOMRIGHT, OT \_ BOTTOMMIDDLE, OT \_ MIDDLELEFT, OT \_ MIDDLERIGHT, OT \_ LEFTOFCAPTION, OT \_ RIGHTOFCAPTION, OT \_ LEFTOFLASTBUTTON, OT \_ RIGHTOFLASTBUTTON, OT \_ ABOVELASTBUTTON, OT \_ BELOWLASTBUTTON | Die Ausrichtung dieses Teils im Fenster.                                                                                                            |
| SIZINGTYPE          | ST \_ TRUESIZE, ST \_ STRETCH, ST \_ TILE, ST \_ TILEHORZ, ST \_ TILEVERT, ST \_ TILECENTER                                                                                                                                                                            | Die Methode, die verwendet wird, um die Größe eines Bilds zu vergrößern, wenn dieser Teil eine Bilddatei verwendet.                                                                                    |
| TEXTSHADOWTYPE      | TST \_ NONE, TST \_ SINGLE, TST \_ CONTINUOUS                                                                                                                                                                                                                    | Der Typ des Schatteneffekts, der hinter text ge zeichnen wird, der diesem Teil zugeordnet ist.                                                                             |
| TRUESIZESCALINGTYPE | TSST \_ NONE, TSST \_ SIZE, TSST \_ DPI                                                                                                                                                                                                                          | Der Skalierungstyp, der verwendet wird, wenn dieser Teil ein Bild mit der richtigen Größe verwendet.                                                                                       |
| Valign              | VA \_ TOP, VA \_ CENTER, VA \_ BOTTOM                                                                                                                                                                                                                            | Die vertikale Ausrichtung, wenn dieser Teil ein Bild der richtigen Größe verwendet.                                                                                          |



 

**TMT \_ FILENAME**



| ID                  | Hinweise                                                                                                                                        |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ GLYPHIMAGEFILE | Der Dateiname für das Symbolbild, das diesem Teil und Zustand zugeordnet ist.                                                                        |
| TMT \_ IMAGEFILE      | Der Dateiname des Images, das diesem Teil und Zustand zugeordnet ist, oder der Basisdateiname für mehrere Images, die diesem Teil und Zustand zugeordnet sind. |
| TMT \_ IMAGEFILE1     | Der Dateiname des ersten skalierten Bilds, das diesem Teil und dem Zustand zugeordnet ist, um unterschiedliche Auflösungen zu unterstützen.                            |
| TMT \_ IMAGEFILE2     | Der Dateiname des zweiten skalierten Bilds.                                                                                                     |
| TMT \_ IMAGEFILE3     | Der Dateiname des dritten skalierten Images.                                                                                                      |
| TMT \_ IMAGEFILE4     | Der Dateiname des vierten skalierten Bilds.                                                                                                     |
| TMT \_ IMAGEFILE5     | Der Dateiname des fünften skalierten Bilds.                                                                                                      |



 

**\_TMT-SCHRIFTART**



| ID                    | Hinweise                                                                                                |
|-----------------------|------------------------------------------------------------------------------------------------------|
| TMT \_ BODYFONT         |                                                                                                      |
| TMT \_ CAPTIONFONT      |                                                                                                      |
| TMT \_ GLYPHFONT        | Die Schriftart, mit der das diesem Teil zugeordnete Glyph gezeichnet wird, wenn schriftartbasierte Glyphen verwendet werden. |
| TMT \_ HEADING1FONT     |                                                                                                      |
| TMT \_ HEADING2FONT     |                                                                                                      |
| \_TMT-SYMBOLTITLEFONT    |                                                                                                      |
| TMT \_ MENUFONT         |                                                                                                      |
| TMT \_ MSGBOXFONT       |                                                                                                      |
| TMT \_ SMALLCAPTIONFONT |                                                                                                      |
| TMT \_ STATUSFONT       |                                                                                                      |



 

**TMT \_ INT**



| ID                       | Hinweise                                                                                                                                                                                                            |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALPHALEVEL          | Der alpha-Wert (0-255), der für [**DrawThemeIcon verwendet wird.**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon)                                                                                                                                         |
| TMT \_ ALPHATHRESHOLD      | Der minimale Alphawert (0-255), der für ein Pixel als nicht transparent angesehen werden muss.                                                                                                                                  |
| TMT \_ ANIMATIONDELAY      |                                                                                                                                                                                                                  |
| TMT \_ ANIMATIONDURATION   |                                                                                                                                                                                                                  |
| TMT \_ BORDERSIZE          | Die Stärke des Rahmens, der gezeichnet wird, wenn dieser Teil eine Rahmenfüllung verwendet.                                                                                                                                               |
| TMT \_ CHARSET             |                                                                                                                                                                                                                  |
| TMT \_ COLORIZATIONCOLOR   |                                                                                                                                                                                                                  |
| TMT \_ COLORIZATIONOPACITY |                                                                                                                                                                                                                  |
| TMT \_ FRAMESPERSECOND     |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE1            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE2            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE3            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE4            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE5            |                                                                                                                                                                                                                  |
| \_TMT-LEUCHTINTENSITY       |                                                                                                                                                                                                                  |
| TMT \_ GLYPHINDEX          | Der Zeichenindex in der ausgewählten Schriftart, der für das Glyphe verwendet wird, wenn der Teil ein schriftartbasiertes Glyph verwendet.                                                                                                 |
| TMT \_ GRADIENTRATIO1      | Die Menge der ersten Farbverlaufsfarbe (TMT \_ GRADIENTCOLOR1), die beim Zeichnen des Teils verwendet werden soll. Dieser Wert kann zwischen 0 und 255 sein, aber dieser Wert plus die Werte der einzelnen GRADIENTRATIO-Werte müssen bis zu 255 addieren. |
| TMT \_ GRADIENTRATIO2      | Die Menge der zweiten Farbverlaufsfarbe (TMT \_ GRADIENTCOLOR2), die beim Zeichnen des Teils verwendet werden soll.                                                                                                                        |
| TMT \_ GRADIENTRATIO3      | Die Menge der dritten Farbverlaufsfarbe (TMT \_ GRADIENTCOLOR3), die beim Zeichnen des Teils verwendet werden soll.                                                                                                                         |
| TMT \_ GRADIENTRATIO4      | Die Menge der vierten Farbverlaufsfarbe (TMT \_ GRADIENTCOLOR4), die beim Zeichnen des Teils verwendet werden soll.                                                                                                                        |
| TMT \_ GRADIENTRATIO5      | Die Menge der fünften Farbverlaufsfarbe (TMT \_ GRADIENTCOLOR5), die beim Zeichnen des Teils verwendet werden soll.                                                                                                                         |
| \_TMT-HÖHE              | Die Höhe des Teils.                                                                                                                                                                                          |
| TMT \_ IMAGECOUNT          | Die Anzahl von Zustandsbildern, die in einer Bilddatei vorhanden sind.                                                                                                                                                             |
| TMT \_ MINCOLORDEPTH       |                                                                                                                                                                                                                  |
| TMT \_ MINDPI1             | Die minimalen Punkte pro Zoll (dpi), für die die erste Bilddatei entworfen wurde.                                                                                                                                      |
| TMT \_ MINDPI2             | Die minimale DPI,für die die zweite Bilddatei entworfen wurde.                                                                                                                                                     |
| TMT \_ MINDPI3             | Die minimale DPI, für die die dritte Bilddatei entworfen wurde.                                                                                                                                                      |
| TMT \_ MINDPI4             | Die minimale DPI, für die die vierte Bilddatei entworfen wurde.                                                                                                                                                     |
| TMT \_ MINDPI5             | Die minimale DPI,für die die fünfte Bilddatei entworfen wurde.                                                                                                                                                      |
| TMT \_ OPACITY             |                                                                                                                                                                                                                  |
| TMT \_ PIXELSPERFRAME      |                                                                                                                                                                                                                  |
| TMT \_ PROGRESSCHUNKSIZE   | Die Größe der "Segment"-Formen des Statussteuerelements, die definieren, wie weit ein Vorgang ausgeführt wurde.                                                                                                                 |
| TMT \_ PROGRESSSPACESIZE   | Die Gesamtgröße aller "Blöcke" des Statussteuerelements.                                                                                                                                                          |
| TMT \_ ROUNDCORNERHEIGHT   | Die Rundung (0 bis 100 Prozent) der Ecken des Teils.                                                                                                                                                          |
| TMT \_ ROUNDCORNERWIDTH    | Die Rundung (0 bis 100 Prozent) der Ecken des Teils.                                                                                                                                                          |
| \_TMT-SÄTTIGUNG          | Die Menge der Sättigung (0-255), die auf ein Mit [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon)gezeichnetes Symbol angewendet werden soll.                                                                                                         |
| TMT \_ TEXTBORDERSIZE      | Die Stärke des Rahmens, der um Textzeichen gezeichnet wird.                                                                                                                                                        |
| TMT \_ TEXTGLOWSIZE        |                                                                                                                                                                                                                  |
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
| TMT \_ TRUESIZESTRETCHMARK | Der Prozentsatz der ursprünglichen Größe eines Bilds mit tatsächlicher Größe, bei dem das Bild gestreckt wird.                                                                                                                        |
| \_TMT-BREITE               | Die Breite des Teils.                                                                                                                                                                                           |



 

**TMT \_ INTLIST**



| ID                       | Hinweise |
|--------------------------|-------|
| TMT \_ TRANSITIONDURATIONS |       |



 

**\_TMT-RÄNDER**



| ID                  | Hinweise                                                                   |
|---------------------|-------------------------------------------------------------------------|
| TMT \_ CAPTIONMARGINS | Die Ränder, die definieren, wo Beschriftungstext innerhalb eines Teils platziert werden kann. |
| TMT \_ CONTENTMARGINS | Die Ränder, die definieren, wo Inhalt innerhalb eines Teils platziert werden kann.      |
| TMT \_ SIZINGMARGINS  | Die Ränder, die zum Dimensionieren eines Nicht-True-Size-Bilds verwendet werden.                      |



 

**\_TMT-POSITION**



| ID                    | Hinweise                                                                                                        |
|-----------------------|--------------------------------------------------------------------------------------------------------------|
| TMT \_ MINSIZE          | Die Mindestgröße, für die die normale Bilddatei verwendet werden kann, bevor zur nächsten kleinsten Bilddatei verschoben wird.   |
| TMT \_ MINSIZE1         | Die Mindestgröße, für die die erste kleine Bilddatei verwendet werden kann.                                            |
| TMT \_ MINSIZE2         | Die Mindestgröße, für die die zweite kleine Bilddatei verwendet werden kann.                                           |
| TMT \_ MINSIZE3         | Die Mindestgröße, für die die dritte kleine Bilddatei verwendet werden kann.                                            |
| TMT \_ MINSIZE4         | Die Mindestgröße, für die die vierte kleine Bilddatei verwendet werden kann.                                           |
| TMT \_ MINSIZE5         | Die Mindestgröße, für die die fünfte kleine Bilddatei verwendet werden kann.                                            |
| TMT \_ NORMALSIZE       | Die Größe des normalen Bilds, das diesem Teil zugeordnet ist.                                                      |
| TMT \_ OFFSET           | Der Positionsoffset von der Ausrichtung für diesen Teil. Die Ausrichtung wird durch den TMT \_ OFFSETTYPE-Wert definiert. |
| TMT \_ TEXTSHADOWOFFSET | Der Offset des Texts, an dem Textschatten gezeichnet werden.                                                    |



 

**TMT \_ RECT**



| ID                       | Hinweise                         |
|--------------------------|-------------------------------|
| TMT \_ ANIMATIONBUTTONRECT |                               |
| TMT \_ ATLASRECT           |                               |
| \_TMT-LIKPLITRECT     |                               |
| TMT \_ DEFAULTPANESIZE     | Die Standardgröße des Teils. |



 

**TMT \_ SIZE**



| ID                      | Hinweise                     |
|-------------------------|---------------------------|
| TMT \_ CAPTIONBARHEIGHT   | Höhe der Beschriftungsleiste.       |
| TMT \_ CAPTIONBARWIDTH    | Beschriftungsleistenbreite.        |
| TMT \_ MENUBARHEIGHT      | Höhe der Menüleiste.          |
| TMT \_ MENUBARWIDTH       | Breite der Menüleiste.           |
| TMT \_ PADDEDBORDERWIDTH  | Aufgefüllte Rahmenbreite.      |
| TMT \_ SCROLLBARHEIGHT    | Bildlaufleistenhöhe.        |
| TMT \_ SCROLLBARWIDTH     | Scrollleistenbreite.         |
| TMT \_ SIZINGBORDERWIDTH  | Breite eines Größenrahmens. |
| TMT \_ SMCAPTIONBARHEIGHT | Höhe der Beschriftungsleiste.       |
| TMT \_ SMCAPTIONBARWIDTH  | Beschriftungsleistenbreite.        |



 

**TMT \_ STRING**



| ID                   | Hinweise                                               |
|----------------------|-----------------------------------------------------|
| \_TMT-ALIAS           |                                                     |
| TMT \_ ATLASINPUTIMAGE |                                                     |
| TMT \_ AUTHOR          |                                                     |
| TMT \_ CLASSICVALUE    |                                                     |
| TMT \_ COLORSCHEMES    |                                                     |
| TMT \_ COMPANY         |                                                     |
| TMT \_ COPYRIGHT       |                                                     |
| TMT \_ CSSNAME         | Siehe [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring). |
| \_TMT-BESCHREIBUNG     |                                                     |
| TMT \_ DISPLAYNAME     |                                                     |
| TMT \_ LASTUPDATED     |                                                     |
| \_TMT-GRÖßEN           |                                                     |
| TMT \_ TEXT            | Der vom Teil angezeigte Text.                     |
| \_TMT-QUICKINFO         |                                                     |
| \_TMT-URL             |                                                     |
| \_TMT-VERSION         |                                                     |
| TMT \_ XMLNAME         | Siehe [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring). |
| \_TMT-NAME            |                                                     |



 

 

 
