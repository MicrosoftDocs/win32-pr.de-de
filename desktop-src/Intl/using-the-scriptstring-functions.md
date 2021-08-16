---
description: Für eine Anwendung, die mit unformatiertem Text arbeitet, stellt Uniscribe die ScriptString-Funktionen \* zur Verfügung.
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: Verwenden der ScriptString-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6685af7dad2c9e1b8d0cf460d526155f967a9105e1b107047afb99c18a5124f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389406"
---
# <a name="using-the-scriptstring-functions"></a>Verwenden der ScriptString-Funktionen

Für eine Anwendung, die mit unformatiertem Text arbeitet, stellt Uniscribe die **ScriptString \* _-Funktionen* zur Verfügung. Diese Funktionen ähneln [_ *ExtTextOut,* *](/windows/win32/api/wingdi/nf-wingdi-exttextouta) [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)und [**GetTextExtent,**](/cpp/mfc/reference/cdc-class#gettextextent)bieten jedoch vollständige komplexe Skriptunterstützung, einschließlich caret-Platzierung. Diese Funktionen ähneln den anderen Uniscribe-Funktionen, sind aber auf die einfacheren Anforderungen der Nur-Text-Verarbeitung zugeschnitten.

In der folgenden Tabelle sind die **ScriptString-Funktionen \*** und alle Entsprechungen in den anderen Uniscribe-Funktionen aufgeführt.



<table>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></td>
<td>Analysiert Nur-Text. Diese Funktion entspricht den folgenden Funktionen:<br/> <dl><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></td>
<td>Ruft die x-Koordinate für eine Zeichenposition ab. Diese Funktion entspricht <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></td>
<td>Gibt eine <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> frei.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></td>
<td>Konvertiert visuelle Breiten in logische Breiten. Diese Funktion entspricht <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></td>
<td>Karten Zeichen-Glyphenpositionen auf ähnliche Weise wie <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement,</a>nur zur älteren Verwendung. Diese Funktion funktioniert nicht gut mit Skripts, die mehr als ein Glyphen pro Codepunkt generieren.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></td>
<td>Zeigt Nur-Text an. Diese Funktion entspricht <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></td>
<td>Gibt einen Zeiger auf die Länge einer abgeschnittenen Nur-Text-Zeichenfolge zurück.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></td>
<td>Gibt einen Zeiger auf den Puffer logischer Attribute für eine analysierte Nur-Text-Zeichenfolge zurück.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></td>
<td>Gibt einen Zeiger auf die Größe (Breite und Höhe) für eine analysierte Nur-Text-Zeichenfolge zurück.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></td>
<td>Identifiziert Codepunktsequenzen, die im angegebenen Skript nicht gültig sind. Diese Funktion ist anders als <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap,</strong></a>das Codepunkte identifiziert, die nicht in einer Schriftart vorhanden sind.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></td>
<td>Konvertiert eine x-Koordinate in eine Zeichenposition. Diese Funktion entspricht <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</td>
</tr>
</tbody>
</table>

Um nur Nur-Text ohne Änderungen anzuzeigen, sollte eine Anwendung [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)und [**dann ScriptStringFree aufrufen.**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) Die anderen Funktionen werden verwendet, um den Nur-Text vor der Anzeige zu ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
