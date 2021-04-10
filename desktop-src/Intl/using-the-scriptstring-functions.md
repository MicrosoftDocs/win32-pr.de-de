---
description: Für eine Anwendung, die unformatierten Text behandelt, stellt uniscridie scriptstring- \* Funktionen bereit.
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: Verwenden der scriptstring-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a2df5e7515bd605ad48cc7a246941e9b6f08f2
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039800"
---
# <a name="using-the-scriptstring-functions"></a>Verwenden der scriptstring-Funktionen

Für eine Anwendung, die unformatierten Text behandelt, stellt uniscridie **scriptstring \*** -Funktionen bereit. Diese Funktionen ähneln " [**exttextout**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)", "DrawText" und " [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent)", bieten jedoch eine vollständige komplexe Skriptunterstützung, einschließlich der Platzierung von [**Caretzeichen**](/windows/win32/api/winuser/nf-winuser-drawtext). Diese Funktionen ähneln den anderen uniscriefunktionen, sind aber auf die einfacheren Anforderungen der nur-Text-Verarbeitung zugeschnitten.

In der folgenden Tabelle werden die **scriptstring \*** -Funktionen und alle Entsprechungen in den anderen uniscriefunktionen ausführlich erläutert.



<table>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>Scriptstringanalyse</strong></a></td>
<td>Analysiert nur-Text. Diese Funktion entspricht den folgenden Funktionen:<br/> <dl><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>Scriptitemize</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>Scriptshape</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>Scriptplace</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>Scriptbreak</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>Scriptgetcmap</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>Scriptrecht</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>Scriptlayout</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>Scriptstringcptox</strong></a></td>
<td>Ruft die x-Koordinate für eine Zeichenposition ab. Diese Funktion entspricht <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>scriptcptox</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>Scriptstringfree</strong></a></td>
<td>Gibt eine <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> Struktur frei.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>Scriptstringgetlogicalbreiten</strong></a></td>
<td>Konvertiert visuelle breiten in logische breiten. Diese Funktion entspricht <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>scriptgetlogicalbreiten</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>Scriptstringgetor</strong></a></td>
<td>Ordnet Zeichen Symbol Positionen auf ähnliche Weise wie <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">getcharakteriplacement</a>zu, nur für ältere Verwendung. Diese Funktion funktioniert nicht gut mit Skripts, die mehrere Symbole pro Codepunkt generieren.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>Scriptstringout</strong></a></td>
<td>Zeigt nur-Text an. Diese Funktion entspricht <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>scripttextout</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></td>
<td>Gibt einen Zeiger auf die Länge einer abgeschnittenen nur-Text-Zeichenfolge zurück.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></td>
<td>Gibt einen Zeiger auf den logischen Attribut Puffer für eine analysierte nur-Text-Zeichenfolge zurück.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></td>
<td>Gibt einen Zeiger auf die Größe (Breite und Höhe) für eine analysierte nur-Text-Zeichenfolge zurück.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>Scriptstringvalidate</strong></a></td>
<td>Identifiziert Code Punkt Sequenzen, die im angegebenen Skript nicht gültig sind. Diese Funktion unterscheidet sich von <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>scriptgetcmap</strong></a>, wodurch Code Punkte identifiziert werden, die nicht in einer Schriftart vorhanden sind.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>Scriptstringxtcp</strong></a></td>
<td>Konvertiert eine x-Koordinate in eine Zeichenposition. Diese Funktion entspricht <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>scriptxtcp</strong></a>.</td>
</tr>
</tbody>
</table>

Um nur nur-Text ohne Änderungen anzuzeigen, sollte eine Anwendung [**scriptstringanalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**scriptstringout**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)und dann [**scriptstringfree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)aufrufen. Die anderen Funktionen werden verwendet, um den nur-Text vor der Anzeige zu ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von uniscri](using-uniscribe.md)
</dt> </dl>

 

 
