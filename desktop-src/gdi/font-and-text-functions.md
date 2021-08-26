---
description: Die folgenden Funktionen werden mit Schriftarten und Text verwendet.
ms.assetid: 69c04ed7-52da-4cb6-9fd2-f2a8c044df8b
title: Schriftart- und Textfunktionen (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e243ea92cf8fdcecc159495102caa70f6a9a55128acf6df9c6d83e1c2b84737a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015350"
---
# <a name="font-and-text-functions-windows-gdi"></a>Schriftart- und Textfunktionen (Windows GDI)

Die folgenden Funktionen werden mit Schriftarten und Text verwendet.



| Funktion                                                   | BESCHREIBUNG                                                                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AddFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontmemresourceex)       | Fügt der Schriftarttabelle des Systems eine eingebettete Schriftart hinzu.                                                                      |
| [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)                 | Fügt der Schriftarttabelle des Systems eine Schriftartressource hinzu.                                                                       |
| [**AddFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa)             | Fügt der Systemschriftarttabelle eine private oder nicht aufzählbare Schriftart hinzu.                                                      |
| [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta)                           | Erstellt eine logische Schriftart.                                                                                              |
| [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)           | Erstellt eine logische Schriftart aus einer -Struktur.                                                                             |
| [**CreateFontIndirectEx**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirectexa)       | Erstellt eine logische Schriftart aus einer -Struktur.                                                                             |
| [**Drawtext**](/windows/desktop/api/Winuser/nf-winuser-drawtext)                               | Zeichnet formatierten Text in einem Rechteck.                                                                                 |
| [**DrawTextEx**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)                           | Zeichnet formatierten Text in einem Rechteck.                                                                                   |
| [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85))             | Eine anwendungsdefinierteCallback-Funktion, die mit [**EnumFontFamiliesEx**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa) zum Verarbeiten von Schriftarten verwendet wird. |
| [**EnumFontFamiliesEx**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa)           | Listet alle Schriftarten im System mit bestimmten Merkmalen auf.                                                     |
| [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)                           | Zeichnet eine Zeichenfolge.                                                                                            |
| [**GetAspectRatioFilterEx**](/windows/desktop/api/Wingdi/nf-wingdi-getaspectratiofilterex)   | Ruft die Einstellung für den Seitenverhältnisfilter ab.                                                                        |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)               | Ruft die Breite aufeinanderfolgender Zeichen aus der TrueType-Schriftart ab.                                                    |
| [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata)     | Ruft die Breite aufeinanderfolgender Zeichen aus der aktuellen Schriftart ab.                                                     |
| [**GetCharABCWidthsI**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsi)             | Ruft die Breite aufeinanderfolgender Glyphenindizes oder aus einem Array von Glyphenindizes aus der TrueType-Schriftart ab.               |
| [**GetCharacterPlacement**](/windows/desktop/api/Wingdi/nf-wingdi-getcharacterplacementa)     | Ruft Informationen zu einer Zeichenfolge ab.                                                                           |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)                   | Ruft die Breite aufeinanderfolgender Zeichen aus der aktuellen Schriftart ab.                                                     |
| [**GetCharWidthFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata)             | Ruft die Bruchbreiten aufeinanderfolgender Zeichen aus der aktuellen Schriftart ab.                                          |
| [**GetCharWidthI**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthi)                     | Ruft die Breite aufeinander folgender Glyphenindizes oder ein Array von Glyphenindizes aus der aktuellen Schriftart ab.                     |
| [**GetFontData**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata)                         | Ruft Metrikdaten für eine TrueType-Schriftart ab.                                                                                |
| [**GetFontLanguageInfo**](/windows/desktop/api/Wingdi/nf-wingdi-getfontlanguageinfo)         | Gibt Informationen zur ausgewählten Schriftart für einen Anzeigekontext zurück.                                                   |
| [**GetFontUnicodeRanges**](/windows/desktop/api/Wingdi/nf-wingdi-getfontunicoderanges)       | Gibt an, welche Unicode-Zeichen von einer Schriftart unterstützt werden.                                                              |
| [**GetGlyphIndices**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphindicesa)                 | Übersetzt eine Zeichenfolge in ein Array von Glyphenindizes.                                                                  |
| [**GetGlyphOutline**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea)                 | Ruft die Kontur oder Bitmap für ein Zeichen in der TrueType-Schriftart ab.                                                     |
| [**GetKerningPairs**](/windows/desktop/api/WinGdi/nf-wingdi-getkerningpairsa)                 | Ruft die Zeichenkernpaare für eine Schriftart ab.                                                                         |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)     | Ruft Textmetriken für TrueType-Schriftarten ab.                                                                                |
| [**GetRasterizerCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getrasterizercaps)             | Gibt an, ob TrueType-Schriftarten installiert sind.                                                                          |
| [**GetTabbedTextExtent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta)         | Berechnet die Breite und Höhe einer Zeichenfolge, einschließlich Registerkarten.                                                 |
| [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign)                       | Ruft die Einstellung für die Textausrichtung für einen Gerätekontext ab.                                                                |
| [**GetTextCharacterExtra**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra)     | Ruft den aktuellen Interzeichenabstand für einen Gerätekontext ab.                                                        |
| [**GetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)                       | Ruft die Textfarbe für einen Gerätekontext ab.                                                                            |
| [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa)       | Ruft die Anzahl der Zeichen in einer Zeichenfolge ab, die in ein Leerzeichen passen.                                              |
| [**GetTextExtentExPointI**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointi)     | Ruft die Anzahl der Glyphenindizes ab, die in ein Leerzeichen passen.                                                       |
| [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)       | Berechnet die Breite und Höhe einer Textzeichenfolge.                                                                   |
| [**GetTextExtentPointI**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpointi)         | Berechnet die Breite und Höhe eines Arrays von Glyphenindizes.                                                          |
| [**GetTextFace**](/windows/desktop/api/Wingdi/nf-wingdi-gettextfacea)                         | Ruft den Namen der Schriftart ab, die in einem Gerätekontext ausgewählt ist.                                                    |
| [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics)                   | Füllt einen Puffer mit den Metriken für eine Schriftart aus.                                                                          |
| [**PolyTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)                         | Zeichnet mehrere Zeichenfolgen mithilfe der Schrift- und Textfarben in einem Gerätekontext.                                            |
| [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex) | Entfernt eine Schriftart, deren Quelle in ein Dokument eingebettet wurde, aus der Schriftarttabelle des Systems.                                   |
| [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)           | Entfernt die Schriftarten in einer Datei aus der Schriftarttabelle des Systems.                                                              |
| [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa)       | Entfernt eine private oder nicht aufzählbare Schriftart aus der Schriftarttabelle des Systems.                                                 |
| [**SetMapperFlags**](/windows/desktop/api/Wingdi/nf-wingdi-setmapperflags)                   | Ändert den Algorithmus, der verwendet wird, um logische Schriftarten physischen Schriftarten zuzuordnen.                                                    |
| [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign)                       | Legt die Textausrichtungsflags für einen Gerätekontext fest.                                                                  |
| [**SetTextCharacterExtra**](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra)     | Legt den Abstand des Interzeichens fest.                                                                                     |
| [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)                       | Legt die Textfarbe für einen Gerätekontext fest.                                                                            |
| [**SetTextJustification**](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification)       | Gibt den Speicherplatz an, den das System den Unterbrechungszeichen in einer Zeichenfolge hinzufügen soll.                             |
| [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)                     | Schreibt eine Zeichenfolge an einer Position und erweitert Tabstopps auf angegebene Werte.                                         |
| [**Textout**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)                                 | Schreibt eine Zeichenfolge an einer Position.                                                                             |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Diese Funktionen werden nur zur Kompatibilität mit 16-Bit-Versionen von Windows.

-   [**CreateScalableFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-createscalablefontresourcea)
-   [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)
-   [**EnumFontFamProc**](/previous-versions//dd162621(v=vs.85))
-   [**EnumFonts**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa)
-   [**EnumFontsProc**](/previous-versions//dd162623(v=vs.85))
-   [**GetCharWidth**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidtha)
-   [**GetTextExtentPoint**](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa)

 

 
