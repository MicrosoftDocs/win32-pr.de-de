---
title: Rich-Edit-Funktionen
description: Rich-Edit-Funktionen
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99f776b9a08095fa66645713e107a3d66920e80f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106373456"
---
# <a name="rich-edit-functions"></a>Rich-Edit-Funktionen

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
<td><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>Autocorrectproc</em></a><br/></td>
<td>Die <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>autocorrectproc</em></a> -Funktion ist eine Anwendungs definierte Rückruffunktion, die mit der <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> Nachricht verwendet wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>Editstreamcallback</em></a><br/></td>
<td>Die <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>editstreamcallback</em></a> -Funktion ist eine Anwendungs definierte Rückruffunktion, die mit den <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> -und <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> -Nachrichten verwendet wird. Es wird verwendet, um einen Datenstrom in ein oder aus einem Rich-Edit-Steuerelement zu übertragen. Der <strong>editstreamcallback</strong> -Typ definiert einen Zeiger auf diese Rückruffunktion. <em>Editstreamcallback</em> ist ein Platzhalter für den Namen der Anwendungs definierten Funktion. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>Editwordbreakprocex</em></a><br/></td>
<td>Die <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>editwordbreakprocex</em></a> -Funktion ist eine Anwendungs definierte Rückruffunktion, die mit der <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> Nachricht verwendet wird. Er bestimmt den Zeichen Index der Wort Umbruch-oder Zeichenklassen-und Wort Umbruch Kennzeichen der Zeichen im angegebenen Text. Der <strong>editwordbreakprocex</strong> -Typ definiert einen Zeiger auf diese Rückruffunktion. <em>Editwordbreakprocex</em> ist ein Platzhalter für den Namen der Anwendungs definierten Funktion. <br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>Getmathalpha numerisch</strong></a><br/></td>
<td>Ruft das alphanumerische Unicode-Transformations Format (UTF)-32-alphanumerische Zeichen ab, das dem angegebenen grundlegenden Zeichen für die mehrsprachige Ebene (BMP) und dem mathematischen Stil entspricht. <br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>Getmathalpha annumerischer Code</strong></a><br/></td>
<td>Ruft den mathematischen Stil und den Zeichencode der "Upright Basic-mehrsprachige Ebene (BMP)" ab, der dem angegebenen nachfolgenden Byte eines mathematischen Ersatz Zeichen Paars entspricht.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>Hyphenateproc</em></a><br/></td>
<td>Die <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>hyphenateproc</em></a> -Funktion ist eine Anwendungs definierte Rückruffunktion, die mit der <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> Nachricht verwendet wird. Es bestimmt, wie die Bindestriche in einem Rich-Edit-Steuerelement von Microsoft ausgeführt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>Mathbuilddown</strong></a><br/></td>
<td>Übersetzt die integrierten mathematischen, Ruby-und anderen Inline Objekte im angegebenen Bereich in eine lineare Form.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>Mathbuildup</strong></a><br/></td>
<td>Konvertiert die mathematische lineare Formatierung in einem Bereich in ein integriertes Formular oder ändert das aktuelle integrierte Formular. <br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>Mathtranslation</strong></a><br/></td>
<td>Übersetzt die mathematischen Zeichen im angegebenen Bereich.<br/></td>
</tr>
<tr class="even">
<td><a href="reextendedregisterclass.md"><strong>Reextendedregisterclass</strong></a><br/></td>
<td>Registriert die beiden Klassennamen REListBox20W und RECombobox20W, die verwendet werden können, um ein umfangreiches Bearbeitungs Listenfeld oder ComboBox-Fenster zu erstellen. <br/>
<blockquote>
[!Note]<br />
Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen. Diese Funktion wird in zukünftigen Versionen möglicherweise nicht mehr unterstützt.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

