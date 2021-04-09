---
description: Beschreibt Datumsformate, die für die Verwendung in der WQL WHERE-Klausel unterstützt werden.
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: WQL-Supported Datumsformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01e5741de24943defc4df0e59e7255bc1a37effd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865652"
---
# <a name="wql-supported-date-formats"></a>WQL-Supported Datumsformate

Zusätzlich zum WMI- **DateTime** -Format werden die folgenden Datumsformate für die Verwendung in der WQL- **Where** -Klausel unterstützt.

Das angezeigte Zeitformat unterscheidet sich für verschiedene Gebiets Schemas. Bei Skripts, die eine Verbindung mit Remote Computern herstellen, muss die Zeit in dem für das Gebiets Schema des Ziel Computers geeigneten Format angegeben werden.

Beispielsweise ist das Datums-und Uhrzeit Format von USA mm-dd-yyyy. Wenn ein Skript auf einem US-Computer eine Verbindung mit einem Zielcomputer in einem Gebiets Schema herstellt, bei dem das Format dd-mm-yyyy ist, werden Abfragen auf dem Zielcomputer als dd-mm-yyyy verarbeitet. Um unterschiedliche Ergebnisse zwischen Gebiets Schemas zu vermeiden, verwenden Sie das [**DateTime**](datetime.md) -Format. Weitere Informationen finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).



<table>
<thead>
<tr class="header">
<th>Format</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mon [TH] DD [,] [yy] JJ</td>
<td>Monat (in drei Buchstaben geschrieben oder abgekürzt), Tag, optionales Komma und zwei oder vierstellige Jahres Angabe.<br/> <dl> 21. Januar 1932<br />
21. Januar 32<br />
Jan 21 1932<br />
Jan 21 32<br />
</dl></td>
</tr>
<tr class="even">
<td>Mon [TH] [,] JJJJ</td>
<td>Monat (in drei Buchstaben geschrieben oder abgekürzt), optionales Komma und vierstellige Jahres Angabe.<br/> <dl> 1932. Januar<br />
Jan 1932<br />
</dl></td>
</tr>
<tr class="odd">
<td>Mon [TH] [yy] JJ DD</td>
<td>Monat (in drei Buchstaben geschrieben oder abgekürzt), zwei oder vierstellige Jahres Angabe und Tag.<br/> <dl> 1932 21. Januar<br />
Jan 32 21<br />
</dl></td>
</tr>
<tr class="even">
<td>DD Mon [TH] [,] [] [yy] y</td>
<td>Tag des Monats, Monats (entweder in drei Buchstaben geschrieben oder abgekürzt), optionales Komma, optionaler Bereich und zwei oder vierstellige Jahres Angabe.<br/> <dl> 21. Januar 1932<br />
21 Jan32<br />
</dl></td>
</tr>
<tr class="odd">
<td>DD [jj] yy Mon [TH]</td>
<td>Tag des Monats, zwei-oder vierstellige Jahres Angabe und Monat (entweder in drei Buchstaben ausgeloebener oder abgekürzt).<br/> <dl> 21 1932. Januar<br />
</dl></td>
</tr>
<tr class="even">
<td>[jj] y [TH] DD</td>
<td>Zwei-oder vierstellige Jahres Angabe, Monat (entweder in drei Buchstaben eingeblendet oder abgekürzt) und Tag.<br/> <dl> 1932. Januar 21<br />
</dl></td>
</tr>
<tr class="odd">
<td>JJJJ Mon [TH]</td>
<td>Zwei-oder vierstellige Jahres-und Monats Angabe (in drei Buchstaben geschrieben oder abgekürzt).<br/> <dl> 1932. Januar<br />
</dl></td>
</tr>
<tr class="even">
<td>JJJJ DD Mon [TH]</td>
<td>Zwei-oder vierstellige Jahres Angabe, Tag und Monat (entweder in drei Buchstaben eingeblendet oder abgekürzt).<br/> <dl> 1932 21. Januar<br />
</dl></td>
</tr>
<tr class="odd">
<td>800 M {/-.} DD {/-.} [jj] JJ</td>
<td>Monat, Tag und zwei oder vierstellige Jahres Angabe. Beachten Sie, dass die Trennzeichen identisch sein müssen.<br/></td>
</tr>
<tr class="even">
<td>DD {/-.} 800 M {/-.} [jj] JJ</td>
<td>Tag des Monats, Monats und zwei oder vierstelligen Jahres Angabe. Beachten Sie, dass die Trennzeichen identisch sein müssen.<br/></td>
</tr>
<tr class="odd">
<td>800 M {/-.} [jj] JJ {/-.} benutzen</td>
<td>Monat, zwei oder vierstellige Jahres Angabe und Tag. Beachten Sie, dass die Trennzeichen identisch sein müssen.<br/></td>
</tr>
<tr class="even">
<td>DD {/-.} [jj] JJ {/-.} 800 800</td>
<td>Tag des Monats, zwei oder vierstellige Jahres Angabe und Monat. Beachten Sie, dass die Trennzeichen identisch sein müssen.<br/></td>
</tr>
<tr class="odd">
<td>[jj] JJ {/-.} DD {/-.} 800 800</td>
<td>Zwei oder vierstellige Jahres Angabe, Tag und Monat. Beachten Sie, dass die Trennzeichen identisch sein müssen.<br/></td>
</tr>
<tr class="even">
<td>[jj] JJ {/-.} 800 M {/-.} benutzen</td>
<td>Zwei oder vierstellige Ziffern (Jahr, Monat und Tag). Beachten Sie, dass die Trennzeichen identisch sein müssen.<br/></td>
</tr>
<tr class="odd">
<td>[jj] YYMMDD</td>
<td>Zwei-oder vierstellige Ziffern (Jahr, Monat und Tag) ohne Leerzeichen.<br/></td>
</tr>
<tr class="even">
<td>yyyy [mm [DD]]</td>
<td>Zwei-oder vierstellige Jahres Angabe, optionaler Monat und optionaler Tag ohne Leerzeichen.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WHERE-Klausel](where-clause.md)
</dt> </dl>

 

 




