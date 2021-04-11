---
description: Gebiets Schema \_ Rückgabe \* Konstanten
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: LOCALE_RETURN *-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d3e5017a6463457b7bc36358e9956365430c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217804"
---
# <a name="locale_return-constants"></a>Gebiets Schema \_ Rückgabe \* Konstanten

In diesem Thema werden die \_ \* von NLS verwendeten Gebiets Schema Rückgabe Konstanten definiert.



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
<td>LOCALE_RETURN_GENITIVE_NAMES</td>
<td><strong>Windows 7 und höher:</strong> Rufen Sie die Namen von Monaten ab, bei denen es sich um die Namen handelt, die verwendet werden, wenn die Monatsnamen mit anderen Elementen kombiniert werden. Beispielsweise wird in Ukrainisch die Entsprechung von Januar geschrieben, &quot; &quot; Wenn der Monat allein benannt wird. Wenn jedoch der Monats Name in Kombination verwendet wird, z. b. in einem Datum wie dem 5. Januar 2003, wird das Format des Namens verwendet. Im Beispiel "Ukrainisch" wird der Name des "Genitive Month" als &quot; 2003 5 &quot; . Die Liste mit den Namen der Namen des Genies beginnt mit Januar und ist durch Semikolon getrennt. Wenn kein 13. Monat vorhanden ist, verwenden Sie ein Semikolon am Ende der Liste.
<blockquote>
[!Note]<br />
In allen Sprachen sind keine Namen für das audiotive Monats vorhanden.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>LOCALE_RETURN_NUMBER</td>
<td><strong>Windows Me/98, Windows NT 4,0 und höher:</strong> Ruft eine Zahl ab. Diese Konstante bewirkt, dass <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>getlocaleingefo</strong></a> oder <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>getlocaleingefoex</strong></a> einen Wert als Zahl anstelle von als Zeichenfolge abruft. Der Puffer, der den Wert empfängt, muss mindestens die Länge eines DWORD-Werts haben. Diese Konstante kann mit einer beliebigen anderen Konstante mit einem Namen kombiniert werden, der mit &quot; LOCALE_I beginnt &quot; .</td>
</tr>
</tbody>
</table>



 

 

 




