---
title: Umfangreiche Bearbeitungsfunktionen
description: Umfangreiche Bearbeitungsfunktionen
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5908bc1767e32fd7631f88b6c1ddf70e5fd22a6b7eb45bfafb6a4f4416b84c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958729"
---
# <a name="rich-edit-functions"></a>Umfangreiche Bearbeitungsfunktionen

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a><br/></td>
<td>Die <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc-Funktion</em></a> ist eine anwendungsdefinierte Rückruffunktion, die mit der EM_SETAUTOCORRECTPROC <a href="em-setautocorrectproc.md"><strong>wird.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a><br/></td>
<td>Die <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback-Funktion</em></a> ist eine anwendungsdefinierte Rückruffunktion, die mit den EM_STREAMIN <a href="em-streamin.md"><strong>und</strong></a> <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> wird. Es wird verwendet, um einen Datenstrom in ein oder aus einem Rich-Edit-Steuerelement zu übertragen. Der <strong>EDITSTREAMCALLBACK-Typ</strong> definiert einen Zeiger auf diese Rückruffunktion. <em>EditStreamCallback</em> ist ein Platzhalter für den anwendungsdefinierten Funktionsnamen. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a><br/></td>
<td>Die <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx-Funktion</em></a> ist eine anwendungsdefinierte Rückruffunktion, die mit der EM_SETWORDBREAKPROCEX <a href="em-setwordbreakprocex.md"><strong>wird.</strong></a> Er bestimmt den Zeichenindex der Wörterpause oder der Zeichenklasse sowie die Wörterbruchflags der Zeichen im angegebenen Text. Der <strong>EDITWORDBREAKPROCEX-Typ</strong> definiert einen Zeiger auf diese Rückruffunktion. <em>EditWordBreakProcEx</em> ist ein Platzhalter für den anwendungsdefinierten Funktionsnamen. <br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMath Alphaumeric</strong></a><br/></td>
<td>Ruft das mathematische alphanumerische Zeichen UTF-32 (Unicode Transformation Format) ab, das dem angegebenen BMP-Zeichen (Basic Multilingual Plane) und mathematischem Stil entspricht. <br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMath AlphaumericCode</strong></a><br/></td>
<td>Ruft den mathematischen Stil und den aufrechten BMP-Zeichencode (Basic Multilingual Plane) ab, der dem angegebenen nachenden Byte eines mathematischen Ersatzzeichenpaars entspricht.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphnateProc</em></a><br/></td>
<td>Die <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphnateProc-Funktion</em></a> ist eine anwendungsdefinierte Rückruffunktion, die mit der EM_SETHYPHENATEINFO <a href="em-sethyphenateinfo.md"><strong>wird.</strong></a> Sie bestimmt, wie Bindestriche in einem Microsoft Rich Edit-Steuerelement erfolgen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a><br/></td>
<td>Übersetzt die integrierten Mathematischen, Ruby- und anderen Inlineobjekte im angegebenen Bereich in lineare Form.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a><br/></td>
<td>Konvertiert die Mathematik im linearen Format in einem Bereich in ein integriertes Formular oder ändert das aktuelle integrierte Formular. <br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a><br/></td>
<td>Übersetzt die mathematischen Zeichen im angegebenen Bereich.<br/></td>
</tr>
<tr class="even">
<td><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a><br/></td>
<td>Registriert zwei Klassennamen, REListBox20W und RECombobox20W, die zum Erstellen von Rich Edit-Listen- oder Kombinationsfeldfenstern verwendet werden können. <br/>
<blockquote>
[!Note]<br />
Für die interne Verwendung vorgesehen; wird nicht für die Verwendung in Anwendungen empfohlen. Diese Funktion wird in zukünftigen Versionen möglicherweise nicht unterstützt.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

