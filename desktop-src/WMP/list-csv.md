---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player Online Stores list.csv
- Online Stores, list.csv
- Geben Sie 1 Online Stores, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f41ed237c5f4a185f01feace8f09b4615e4922b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101238"
---
# <a name="listcsv"></a>list.csv

Diese Datei enthält einen Eintrag für jede der Listen, die im Katalog enthalten sind. Listen können Listen von Spuren, Alben, Künstlern, Genres, unter Genres oder Radio Feeds sein. oder Sie können Listen mit anderen Listen sein. Jeder Listeneintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben werden. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

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
<td>Listen</td>
<td>Ja</td>
<td>Nicht negative ganze Zahl.</td>
<td>Listen Bezeichner, der innerhalb list.csv eindeutig ist. Muss nicht negativ und kleiner als 2 ^ 32 sein. <strong>Anzeigen eines Listen Knotens im Strukturansicht-Steuerelement:</strong> Wenn die ListId 0, 1, 2, 3, 4, 5, 6 oder 7 ist, wird die Liste in dem Strukturansicht-Steuerelement des Players als benutzerdefinierter Knoten unter dem Knoten der obersten Ebene des Online Stores angezeigt. Benutzerdefinierte Knoten werden vor den Standard Knoten unter dem Knoten der obersten Ebene des Online Stores angezeigt, und Sie werden in aufsteigender Reihenfolge nach ListId positioniert. Wenn z. b. drei benutzerdefinierte Knoten mit den listids 1, 3 und 5 vorhanden sind, werden diese zuerst unter dem Knoten der obersten Ebene des Online Stores angezeigt.<br/></td>
</tr>
<tr class="even">
<td>"Listen Titel</td>
<td>Nein</td>
<td>Unicode-Zeichenfolge. Beispiel: Top 10-Treffer<br/></td>
<td>Listen Titel.</td>
</tr>
<tr class="odd">
<td>Listtitel</td>
<td>Nein</td>
<td>Unicode-Zeichenfolge</td>
<td>Listet einen alternativen Titel auf, der in der zweiten Zeile der Kachel Ansicht angezeigt wird.</td>
</tr>
<tr class="even">
<td>Listdescription</td>
<td>Ja</td>
<td>Unicode-Zeichenfolge</td>
<td>Listen Anzeige Text (wird in den Eigenschaften Seiten angezeigt).</td>
</tr>
<tr class="odd">
<td>Linked_ItemType</td>
<td>Ja</td>
<td>Unicode-Zeichenfolge. Format: [T | P | A | L | G | S | R<br/> Beispiel: T<br/></td>
<td>Gibt den Typ der verknüpften Elemente an.
<ul>
<li>T = Nachverfolgung</li>
<li>P = Performer</li>
<li>A = Album</li>
<li>L = Liste</li>
<li>G = Genre</li>
<li>S = Subgenre</li>
<li>R = Radio</li>
</ul></td>
</tr>
<tr class="even">
<td>ListPrice</td>
<td>Ja</td>
<td>Unicode-Zeichenfolge. Beispiel: $9,99<br/></td>
<td>Der Preis der Liste. Das Währungssymbol sollte eingeschlossen werden. NULL bedeutet, dass die Liste kostenlos ist. Kein Wert bedeutet, dass der Preis unbekannt ist. Ein Bindestrich bedeutet, dass die Liste nicht erworben werden kann.<br/></td>
</tr>
<tr class="odd">
<td>Beliebtheit</td>
<td>Ja</td>
<td>Eine Ganzzahl oder ein Dezimalwert. Beispiel: 1259,3<br/></td>
<td>Gibt die rangfolgenrangfolge an, wenn diese Liste in anderen Listen angezeigt wird. Kann NULL sein, wenn nicht zutreffend.</td>
</tr>
<tr class="even">
<td>Isrecentlyadded</td>
<td>Ja</td>
<td>Boolescher Wert. Format: [0 | 1]<br/> Beispiel: 0<br/></td>
<td>Gibt an, ob die Liste kürzlich hinzugefügt wurde.</td>
</tr>
<tr class="odd">
<td>Isfeatured</td>
<td>Ja</td>
<td>Boolescher Wert. Format: [0 | 1]<br/> Beispiel: 0<br/></td>
<td>Gibt an, ob die Liste angezeigt wird. Kann zum Bestimmen der Sortierreihenfolge verwendet werden.</td>
</tr>
<tr class="even">
<td>Editorialglyph</td>
<td>Ja</td>
<td>Nicht negative ganze Zahl. Muss 0 sein.</td>
<td>Wird in dieser Version nicht verwendet. Muss 0 sein.</td>
</tr>
<tr class="odd">
<td>ViewType</td>
<td>Ja</td>
<td>Unicode-Zeichenfolge. Format: [I | T | R | L | O] Beispiel: T<br/></td>
<td>Gibt den Ansichtstyp an, der für die Liste verwendet werden soll.
<ul>
<li>I = Symbol</li>
<li>T = Kachel</li>
<li>R = Bericht</li>
<li>L = Liste</li>
<li>O = geordnete Liste</li>
</ul></td>
</tr>
<tr class="even">
<td>Viewimagesize</td>
<td>Ja</td>
<td>Nicht negative ganze Zahl. Beispiel: 180<br/></td>
<td>Die Größe, in der das Listen Bild angezeigt wird. Wenn der Wert 0 ist, wird die Größe automatisch bestimmt.</td>
</tr>
<tr class="odd">
<td>GroupBy</td>
<td>Ja</td>
<td>Unicode-Zeichenfolge. Format: [-| P | A | C | R | D<br/> Beispiel: P<br/></td>
<td>Gibt an, welches Feld zum Gruppieren der Elemente in der Liste verwendet wird.
<ul>
<li>- = Automatisch</li>
<li>P = Performer</li>
<li>A = Album</li>
<li>C = Composer</li>
<li>R = Bewertung</li>
<li>D = Datum</li>
</ul></td>
</tr>
<tr class="even">
<td>Listitemsaredynamic</td>
<td>Ja</td>
<td>Boolesch. Kann 0 oder 1 sein.</td>
<td>Gibt an, ob die Liste dynamisch generiert wird. Dynamische Listen enthalten keine Elemente in listitem.csv. Wenn eine Liste als dynamisch markiert ist, werden die zugehörigen Elemente von <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">iwmpcontentpartner:: getlistcontents</a> bereitgestellt.</td>
</tr>
</tbody>
</table>



 

 

 





