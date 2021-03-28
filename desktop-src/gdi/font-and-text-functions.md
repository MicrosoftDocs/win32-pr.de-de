---
description: Die folgenden Funktionen werden mit Schriftarten und Text verwendet.
ms.assetid: 69c04ed7-52da-4cb6-9fd2-f2a8c044df8b
title: Schriftart-und Text Funktionen (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a4dd6f000356dfb0e52c34fadef81bd6e8843e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528352"
---
# <a name="font-and-text-functions-windows-gdi"></a>Schriftart-und Text Funktionen (Windows GDI)

Die folgenden Funktionen werden mit Schriftarten und Text verwendet.



| Funktion                                                   | BESCHREIBUNG                                                                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**Addfontmemresourceex**](/windows/desktop/api/Wingdi/nf-wingdi-addfontmemresourceex)       | Fügt der System Schriftart Tabelle eine eingebettete Schriftart hinzu.                                                                      |
| [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)                 | Fügt der System Schriftart Tabelle eine Schriftart Ressource hinzu.                                                                       |
| [**Addfontresourceex**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa)             | Fügt der System Schriftart Tabelle eine private oder nicht Aufzähl Bare Schriftart hinzu.                                                      |
| [**"Kreatefont"**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta)                           | Erstellt eine logische Schriftart.                                                                                              |
| [**"Kreatefontindirekte"**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)           | Erstellt eine logische Schriftart aus einer-Struktur.                                                                             |
| [**"Kreatefontderetex"**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirectexa)       | Erstellt eine logische Schriftart aus einer-Struktur.                                                                             |
| [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)                               | Zeichnet formatierten Text in einem Rechteck.                                                                                 |
| [**Drawtextex**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)                           | Zeichnet formatierten Text im Rechteck.                                                                                   |
| [**Enumfontfamexproc**](/previous-versions//dd162618(v=vs.85))             | Eine Application definedcallback-Funktion, die mit [**enumfontfamiliesex**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa) zum Verarbeiten von Schriftarten verwendet wird. |
| [**Enumfontfamiliesex**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa)           | Listet alle Schriftarten im System mit bestimmten Merkmalen auf.                                                     |
| [**Exttextout**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)                           | Zeichnet eine Zeichenfolge.                                                                                            |
| [**Getaspectratiofilterex**](/windows/desktop/api/Wingdi/nf-wingdi-getaspectratiofilterex)   | Ruft die Einstellung für den Seitenverhältnis Filter ab.                                                                        |
| [**Getcharabcbreiten**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)               | Ruft die Breite der aufeinander folgenden Zeichen aus der TrueType-Schriftart ab.                                                    |
| [**Getcharabcwidthsfloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata)     | Ruft die Breite der aufeinander folgenden Zeichen aus der aktuellen Schriftart ab.                                                     |
| [**Getcharabcwidthsi**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsi)             | Ruft die Breite von aufeinander folgenden Glyphe-Indizes oder aus einem Array von Glyphe-Indizes aus der TrueType-Schriftart ab.               |
| [**GetCharacterPlacement**](/windows/desktop/api/Wingdi/nf-wingdi-getcharacterplacementa)     | Ruft Informationen zu einer Zeichenfolge ab.                                                                           |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)                   | Ruft die Breite der aufeinander folgenden Zeichen aus der aktuellen Schriftart ab.                                                     |
| [**Getcharwidthfloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata)             | Ruft die Bruch Breite von aufeinander folgenden Zeichen aus der aktuellen Schriftart ab.                                          |
| [**Getcharwidthi**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthi)                     | Ruft die Breite von aufeinander folgenden Glyphe-Indizes oder ein Array von Glyphe-Indizes aus der aktuellen Schriftart ab.                     |
| [**Getfontdata**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata)                         | Ruft Metrikdaten für eine TrueType-Schriftart ab.                                                                                |
| [**Getfontlanguageingefo**](/windows/desktop/api/Wingdi/nf-wingdi-getfontlanguageinfo)         | Gibt Informationen über die ausgewählte Schriftart für einen Anzeige Kontext zurück.                                                   |
| [**Getfontunicoderanges**](/windows/desktop/api/Wingdi/nf-wingdi-getfontunicoderanges)       | Gibt an, welche Unicode-Zeichen von einer Schriftart unterstützt werden.                                                              |
| [**Getglyphindices**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphindicesa)                 | Übersetzt eine Zeichenfolge in ein Array von Symbol Indizes.                                                                  |
| [**GetGlyphOutline**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea)                 | Ruft die Kontur oder Bitmap für ein Zeichen in der TrueType-Schriftart ab.                                                     |
| [**Getkerningpairs**](/windows/desktop/api/WinGdi/nf-wingdi-getkerningpairsa)                 | Ruft die Zeichen Nummern Paare für eine Schriftart ab.                                                                         |
| [**Getoutlinetextmetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)     | Ruft textmetriken für TrueType-Schriftarten ab.                                                                                |
| [**Getrasterizercaps**](/windows/desktop/api/Wingdi/nf-wingdi-getrasterizercaps)             | Gibt an, ob TrueType-Schriftarten installiert sind.                                                                          |
| [**Gettabbedtextextent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta)         | Berechnet die Breite und Höhe einer Zeichenfolge, einschließlich der Registerkarten.                                                 |
| [**Gettextalign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign)                       | Ruft die Text Ausrichtungs Einstellung für einen Gerätekontext ab.                                                                |
| [**Gettextcharakteriextra**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra)     | Ruft den aktuellen intercharacter-Abstand für einen Gerätekontext ab.                                                        |
| [**Gettextcolor**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)                       | Ruft die Textfarbe für einen Gerätekontext ab.                                                                            |
| [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa)       | Ruft die Anzahl der Zeichen in einer Zeichenfolge ab, die in ein Leerzeichen passt.                                              |
| [**Gettextextentexpointi**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointi)     | Ruft die Anzahl der Glyphe-Indizes ab, die in ein Leerzeichen passen.                                                       |
| [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)       | Berechnet die Breite und Höhe einer Text Zeichenfolge.                                                                   |
| [**Gettextextentpointi**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpointi)         | Berechnet die Breite und Höhe eines Arrays von Glyphe-Indizes.                                                          |
| [**Gettextface**](/windows/desktop/api/Wingdi/nf-wingdi-gettextfacea)                         | Ruft den Namen der Schriftart ab, die in einem Gerätekontext ausgewählt wird.                                                    |
| [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics)                   | Füllt einen Puffer mit den Metriken für eine Schriftart aus.                                                                          |
| [**Polytextout**](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)                         | Zeichnet mehrere Zeichen folgen mithilfe der Schriftart und der Textfarben in einem Gerätekontext.                                            |
| [**Removefontmemresourceex**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex) | Entfernt eine Schriftart, deren Quelle in ein Dokument eingebettet wurde, aus der Schriftart Tabelle des Systems.                                   |
| [**Removefontresource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)           | Entfernt die Schriftarten in einer Datei aus der Schriftart Tabelle des Systems.                                                              |
| [**Removefontresourceex**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa)       | Entfernt eine private oder nicht Aufzähl Bare Schriftart aus der Schriftart Tabelle des Systems.                                                 |
| [**Setmapperflags**](/windows/desktop/api/Wingdi/nf-wingdi-setmapperflags)                   | Ändert den Algorithmus, der verwendet wird, um logische Schriftarten physischen Schriftarten zuzuordnen.                                                    |
| [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign)                       | Legt die Flags für die Textausrichtung für einen Gerätekontext fest.                                                                  |
| [**Settextcharakteriextra**](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra)     | Legt den Abstand zwischen Zeichen fest.                                                                                     |
| [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)                       | Legt die Textfarbe für einen Gerätekontext fest.                                                                            |
| [**Settextbegrün dung**](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification)       | Gibt den Speicherplatz an, den das System den Break-Zeichen in einer Zeichenfolge hinzufügen soll.                             |
| [**Tabbedtextout**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)                     | Schreibt eine Zeichenfolge an einer Position und erweitert die Registerkarten auf angegebene Werte.                                         |
| [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)                                 | Schreibt eine Zeichenfolge an einem Speicherort.                                                                             |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Diese Funktionen werden nur aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt.

-   [**"Kreatescalablefontresource"**](/windows/desktop/api/Wingdi/nf-wingdi-createscalablefontresourcea)
-   [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)
-   [**Enumfontfamproc**](/previous-versions//dd162621(v=vs.85))
-   [**Enumfonts**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa)
-   [**Enumfontsproc**](/previous-versions//dd162623(v=vs.85))
-   [**Getcharwidth**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidtha)
-   [**GetTextExtentPoint**](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa)

 

 
