---
description: LOCALE \_ IDIGITSUBS UNTERTITEL
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5fe8adf06cbca11bd5d262edf299b0f043286d4494c36172f9f7a461e17eeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948721"
---
# <a name="locale_idigitsubstitution"></a>LOCALE \_ IDIGITSUBS UNTERTITEL

**Windows 2000:** Die Form der Ziffern. Beispielsweise haben arabische, thailische und indische Ziffern klassische Formen, die sich von europäischen Ziffern unterscheiden. Für Locales mit [LOCALE \_ SNATIVEDIGITS,](locale-snative-constants.md) die als andere Werte als ASCII 0-9 angegeben sind, gibt dieser Wert an, ob diese anderen Ziffern zu Anzeigezwecken bevorzugt werden sollen. Wenn beispielsweise der Wert 2 ausgewählt wird, werden immer die von LOCALE \_ SNATIVEDIGITS angegebenen Ziffern verwendet. Wenn eine 1 ausgewählt wird, werden immer die ASCII-Ziffern 0-9 verwendet. Wenn 0 ausgewählt wird, wird ASCII in einigen Fällen verwendet, und die von LOCALE SNATIVEDIGITS angegebenen Ziffern werden in anderen Zeichen verwendet, je nach \_ Kontext.



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
<td>Kontextbasierte Ersetzung. Ziffern werden basierend auf dem vorherigen Text in derselben Ausgabe angezeigt. Europäische Ziffern folgen lateinischen Skripts, Arabic-Indic Ziffern folgen arabischem Text, und andere nationale Ziffern folgen Text, der in verschiedenen anderen Skripts geschrieben wurde. Wenn es keinen vorangehenden Text gibt, bestimmen das -Locale und die angezeigte Lesefolge die Ziffernersetzung, wie in der folgenden Tabelle gezeigt.
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
<td>Thailändisch Ziffern</td>
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
<td>Es wird keine Ersetzung verwendet. Vollständige Unicode-Kompatibilität.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Native Ziffernersetzung. Nationale Formen werden entsprechend der LOCALE_SNATIVEDIGITS.</td>
</tr>
</tbody>
</table>



 

 

 



