---
description: LOCALE \_ idigitsubstitution
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128117"
---
# <a name="locale_idigitsubstitution"></a>LOCALE \_ idigitsubstitution

**Windows 2000:** Die Form der Ziffern. Beispielsweise haben arabische, thailändische und indic-Ziffern klassische Formen, die sich von den europäischen Ziffern unterscheiden. Für Gebiets Schemas mit Gebiets [ \_ Schema-snativedigits](locale-snative-constants.md) , die als andere Werte als ASCII 0-9 angegeben werden, gibt dieser Wert an, ob die anderen Ziffern zu Anzeige Zwecken bevorzugt angegeben werden sollen. Wenn z. b. der Wert 2 ausgewählt wird, werden die von locale \_ snativedigits angegebenen Ziffern immer verwendet. Wenn 1 ausgewählt wird, werden die ASCII 0-9-Ziffern immer verwendet. Wenn 0 ausgewählt wird, wird in einigen Fällen ASCII verwendet, und die durch \_ das Gebiets Schema (snativedigits) angegebenen Ziffern werden je nach Kontext in anderen verwendet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Kontextbasierte Ersetzung. Ziffern werden basierend auf dem vorherigen Text in der gleichen Ausgabe angezeigt. Europäische Ziffern folgen lateinischen Skripts, Arabic-Indic Ziffern auf arabischen Text, und andere nationale Ziffern folgen dem Text, der in verschiedenen anderen Skripts geschrieben wurde. Wenn kein vorheriger Text vorhanden ist, bestimmen das Gebiets Schema und die angezeigte Lesereihenfolge die Ziffern Ersetzung, wie in der folgenden Tabelle dargestellt.
<table>
<thead>
<tr class="header">
<th>Gebietsschema</th>
<th>Lesereihenfolge</th>
<th>Verwendete Ziffern</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Arabisch</td>
<td>Von rechts nach links</td>
<td>Arabic-Indic</td>
</tr>
<tr class="even">
<td>Thailändisch</td>
<td>Von links nach rechts</td>
<td>Thailändische Ziffern</td>
</tr>
<tr class="odd">
<td>Alle anderen</td>
<td>Any</td>
<td>Keine Ersetzung verwendet</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>1</td>
<td>Es wurde keine Ersetzung verwendet. Vollständige Unicode-Kompatibilität.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Native Ziffern Ersetzung. Nationale Formen werden nach LOCALE_SNATIVEDIGITS angezeigt.</td>
</tr>
</tbody>
</table>



 

 

 



