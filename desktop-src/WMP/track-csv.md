---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player Online Stores track.csv
- Online Stores, track.csv
- Geben Sie 1 Online Stores, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310371"
---
# <a name="trackcsv"></a>track.csv

Diese Datei enthält einen Eintrag für jede Spur im Katalog. Jeder Eintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben werden. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird. Er verweist nicht auf den Datentyp des Inhalts. Wenn beispielsweise eine ganze Zahl in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen Ganzzahl darstellt.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Feld</th>
<th>Erforderlich</th>
<th>Format</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TrackID</td>
<td>Ja</td>
<td>Nicht negative ganze Zahl. Beispiel: 32789<br/></td>
<td>Vom Inhaltsanbieter bereitgestellter eindeutiger Bezeichner. Muss kleiner als 2 ^ 32 sein. Leistungs Tipp: Wenn die IDs, die den Spuren desselben Albums zugewiesen sind, nacheinander nummeriert werden, ist die Katalog Komprimierung effizienter. Die aufeinanderfolgende Nummerierung von Albumtiteln ist jedoch nicht erforderlich.<br/></td>
</tr>
<tr class="even">
<td>Tracktitle</td>
<td>Ja</td>
<td>Unicode-Zeichenfolge. Beispiel: Raygun Räuber ' Blues</td>
<td>Name der Spur</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Ja</td>
<td>Nicht negative ganze Zahl. Beispiel: 543<br/></td>
<td>Dauer der Spur in Sekunden.</td>
</tr>
<tr class="even">
<td>Tracknumber</td>
<td>Ja</td>
<td>Nicht negative ganze Zahl. Beispiel: 7<br/></td>
<td>Verfolgen Sie die Nummer im Titel des Titels. Nachverfolgen von Zahlen beginnen bei 1 und erhöhen die Anzahl von Festplatten Sätzen. Die Nachverfolgung muss kleiner als 256 sein. Eine Nachverfolgung, die größer oder gleich 256 ist, führt zu unerwartetem Verhalten in Windows Media Player.</td>
</tr>
<tr class="odd">
<td>Trackprice</td>
<td>Ja</td>
<td>Unicode-Zeichenfolge. Beispiel: $0,99.</td>
<td>Preis nachverfolgen. Das Währungssymbol sollte eingeschlossen werden. Die leere Zeichenfolge 0 und-haben eine besondere Bedeutung. Eine leere Zeichenfolge gibt an, dass der Preis unbekannt ist. Ein NULL-Wert in diesem Feld bedeutet, dass der Titel frei ist, und ein Bindestrich (-) gibt an, dass der Track nicht gekauft werden kann.</td>
</tr>
<tr class="even">
<td>Canstream</td>
<td>Ja</td>
<td>Boolesch. Kann 0 oder 1 sein. Beispiel: 0<br/></td>
<td>Gibt an, ob der Track gestreamt werden kann.</td>
</tr>
<tr class="odd">
<td>Kerzen laden</td>
<td>Ja</td>
<td>Boolesch. Kann 0 oder 1 sein. Beispiel: 0<br/></td>
<td>Gibt an, ob der Track heruntergeladen werden kann.</td>
</tr>
<tr class="even">
<td>Haspreviewclip</td>
<td>Ja</td>
<td>Boolesch. Kann 0 oder 1 sein. Beispiel: 0<br/></td>
<td>Gibt an, ob der Titel einen Vorschau Clip aufweist.</td>
</tr>
<tr class="odd">
<td>Hasvideoclip</td>
<td>Ja</td>
<td>Boolesch. Kann 0 oder 1 sein. Beispiel: 0<br/></td>
<td>Gibt an, ob der Track über einen Videoclip verfügt.</td>
</tr>
<tr class="even">
<td>Parametrialbewertung</td>
<td>Ja</td>
<td>Enumeration. Kann n, E oder C sein. Beispiel: n<br/></td>
<td>Gibt die Bewertung des Elternbeirats an. Die Werte N, E und C stehen für "Normal", "explizit" und "Clean".</td>
</tr>
<tr class="odd">
<td>Linkedalbumid</td>
<td>Ja</td>
<td>Nicht negative ganze Zahl. Muss die ID eines-Albums sein. Beispiel: 32423</td>
<td>Die ID des Albums, das diese Spur enthält.
<blockquote>
[!Note]<br />
Jeder Track muss zu einem Album gehören. Das heißt, für jede Spur muss das Feld linkedalbumid gleich einer der Album-IDs in der album.csv-Datei sein.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>LinkedTrackArtist_ArtistIDs</td>
<td>Ja</td>
<td>Liste mit ganzen Zahlen. Die Liste enthält die durch Semikolons getrennten Interpreten-IDs. Beispiel: 41322; 12321; 82123;</td>
<td>Eine Liste von IDs, die den beteiligten Künstlern entsprechen.</td>
</tr>
<tr class="odd">
<td>Composer</td>
<td>Nein</td>
<td>Unicode-Zeichenfolge. Beispiel: Beethoven</td>
<td>Der Ersteller des Titels. Wenn für das Genre des Titels das hascomposer-Feld nicht festgelegt ist, wird der Wert des Felds Composer ignoriert. Wird normalerweise nur für Jazz-oder klassische Titel verwendet.</td>
</tr>
<tr class="even">
<td>Beliebtheit</td>
<td>Ja</td>
<td>Nicht negative ganze Zahl oder float. Beispiel: 1252,6<br/></td>
<td>Bestimmt die Position des Titels in der Liste, wenn nach Beliebtheit sortiert. Eine niedrigere Zahl weist auf eine höhere Beliebtheit hin.</td>
</tr>
<tr class="odd">
<td>Star Rating</td>
<td>Nein</td>
<td>Float. Beispiel: 4,21<br/></td>
<td>Die Stern Bewertung wird von Windows Media Player auf den nächsten 1/4-Stern gerundet, bevor Sie auf der Windows Media Player-Benutzeroberfläche angezeigt wird.</td>
</tr>
</tbody>
</table>



 

 

 





