---
title: Verwenden von Makros für die Fehlerbehandlung
description: COM definiert eine Reihe von Makros, die das Arbeiten mit HRESULT-Werten vereinfachen.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6605ecc05f2d24d3671d28becd770b15d56e1413
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730424"
---
# <a name="using-macros-for-error-handling"></a>Verwenden von Makros für die Fehlerbehandlung

COM definiert eine Reihe von Makros, die das Arbeiten mit **HRESULT** -Werten vereinfachen.

Die Fehler Behandlungs Makros werden in der folgenden Tabelle beschrieben.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Makro</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a><br/></td>
<td>Gibt ein <strong>HRESULT</strong> mit dem angegebenen Schweregrad, dem Betriebs Code und dem Fehlercode zurück, der das <strong>HRESULT</strong>umfasst.<br/>
<blockquote>
[!Note]<br />
Das Aufrufen von <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> für die S_OK Überprüfung führt zu einer Leistungs Einbuße. Sie sollten für erfolgreiche Ergebnisse nicht routinemäßig <strong>MAKE_HRESULT</strong> verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a><br/></td>
<td>Gibt einen <strong>SCODE</strong> mit dem Schweregrad, dem Einrichtungs Code und dem Fehlercode zurück, der den <strong>SCODE</strong>umfasst.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a><br/></td>
<td>Extrahiert den Fehlercode Teil des <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a><br/></td>
<td>Extrahiert den Einrichtungs Code des <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a><br/></td>
<td>Extrahiert den Schweregrad des <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a><br/></td>
<td>Extrahiert den Fehlercode Teil des <strong>scodes</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a><br/></td>
<td>Extrahiert den Einrichtungs Code des <strong>scodes</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a><br/></td>
<td>Extrahiert das Feld "Schweregrad" des <strong>scodes</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>Erfolgreich</strong></a><br/></td>
<td>Testet den Schweregrad von <strong>SCODE</strong> oder <strong>HRESULT</strong>. gibt " <strong>true</strong> " zurück, wenn der Schweregrad 0 (null) und " <strong>false</strong> " ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>Erreicht</strong></a><br/></td>
<td>Testet den Schweregrad von <strong>SCODE</strong> oder <strong>HRESULT</strong>. gibt <strong>true</strong> zurück, wenn der Schweregrad 1 und <strong>false</strong> ist, wenn er NULL ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a><br/></td>
<td>Stellt einen generischen Test Fehler für einen beliebigen Statuswert bereit. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a><br/></td>
<td>Ordnet einen <a href="/windows/desktop/Debug/system-error-codes">Systemfehler Code</a> einem <strong>HRESULT</strong> -Wert zu. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a><br/></td>
<td>Ordnet einen NT-Statuswert einem <strong>HRESULT</strong> -Wert zu.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in com](error-handling-in-com.md)
</dt> </dl>

 

