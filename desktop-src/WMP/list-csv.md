---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player,list.csv
- Onlineshops,list.csv
- Geben Sie 1 Onlineshops ein, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e754f7985fbf59c23cccae5fd9780ff4b4579205ceaf3ef3cc8f74c768d4e71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135343"
---
# <a name="listcsv"></a>list.csv

Diese Datei enthält einen Eintrag für jede der Listen, die der Katalog enthält. Listen können Listen von Titeln, Albums, Genre, Genre, Untergenres oder Radiofeeds sein. oder sie können Listen anderer Listen sein. Jeder Listeneintrag ist eine Zeile, die aus den Feldern besteht, die durch Tabstopps getrennt sind, die in der folgenden Tabelle beschrieben sind. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

Die Spalte Format in der folgenden Tabelle beschreibt die Formatierung der einzelnen Unicode-Textfelder. Er bezieht sich nicht auf den Datentyp des Inhalts. Wenn beispielsweise Integer in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen ganzen Zahl darstellt.



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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ListID</td>
<td>Ja</td>
<td>Nicht negative ganze Zahl.</td>
<td>Listenbezeichner, eindeutig innerhalb list.csv. Muss nicht negativ und kleiner als 2^32 sein. <strong>Anzeigen eines Listenknotens im Strukturansicht-Steuerelement:</strong> Wenn die ListID 0, 1, 2, 3, 4, 5, 6 oder 7 ist, wird die Liste als benutzerdefinierter Knoten unter dem Knoten der obersten Ebene Ihres Onlineshops im Strukturansicht-Steuerelement des Players angezeigt. Benutzerdefinierte Knoten werden vor den Standardknoten unter dem Knoten der obersten Ebene des Onlineshops angezeigt und nach ListID in aufsteigender Reihenfolge positioniert. Wenn es z. B. drei benutzerdefinierte Knoten mit ListIDs von 1, 3 und 5 gibt, werden sie zuerst, zweitens und drittens unter dem Knoten der obersten Ebene des Onlineshops angezeigt.<br/></td>
</tr>
<tr class="even">
<td>ListTitle</td>
<td>Nein</td>
<td>Unicode-Zeichenfolge. Beispiel: Top 10 Treffer<br/></td>
<td>Listentitel.</td>
</tr>
<tr class="odd">
<td>ListSubtitle</td>
<td>Nein</td>
<td>Unicode-Zeichenfolge</td>
<td>Listet einen alternativen Titel auf, der in der zweiten Zeile der Kachelansicht angezeigt wird.</td>
</tr>
<tr class="even">
<td>ListDescription</td>
<td>Ja</td>
<td>Unicode-Zeichenfolge</td>
<td>Auflisten von anzeigefreundlichem Anzeigetext (auf Eigenschaftenseiten angezeigt).</td>
</tr>
<tr class="odd">
<td>Linked_ItemType</td>
<td>Ja</td>
<td>Unicode-Zeichenfolge. Format: [T| P| A| L|G| S| R]<br/> Beispiel: T<br/></td>
<td>Gibt den Typ der verknüpften Elemente an.
<ul>
<li>T= Track</li>
<li>P = Performer</li>
<li>A = Album</li>
<li>L = List</li>
<li>G = Genre</li>
<li>S = Subgenre</li>
<li>R = Radio</li>
</ul></td>
</tr>
<tr class="even">
<td>ListPrice</td>
<td>Ja</td>
<td>Unicode-Zeichenfolge. Beispiel: 9,99 USD<br/></td>
<td>Preis der Liste. Das Währungssymbol sollte enthalten sein. Eine Null bedeutet, dass die Liste frei ist. Kein Wert bedeutet, dass der Preis unbekannt ist. Ein Bindestrich bedeutet, dass die Liste nicht erworben werden kann.<br/></td>
</tr>
<tr class="odd">
<td>Beliebtheit</td>
<td>Ja</td>
<td>Ganzzahliger oder Dezimalwert. Beispiel: 1259.3<br/></td>
<td>Gibt die Beliebtheitsrangfolge an, wenn diese Liste in anderen Listen angezeigt wird. Kann 0 (null) sein, falls nicht zutreffend.</td>
</tr>
<tr class="even">
<td>IsRecentlyAdded</td>
<td>Ja</td>
<td>Boolean.Format: [0|1]<br/> Beispiel: 0<br/></td>
<td>Gibt an, ob die Liste vor Kurzem hinzugefügt wurde.</td>
</tr>
<tr class="odd">
<td>IsFeatured</td>
<td>Ja</td>
<td>Boolean.Format: [0|1]<br/> Beispiel: 0<br/></td>
<td>Gibt an, ob die Liste als Feature angezeigt wird. Kann zum Bestimmen der Sortierreihenfolge verwendet werden.</td>
</tr>
<tr class="even">
<td>EditorialGlyph</td>
<td>Ja</td>
<td>Nicht negative ganze Zahl. Muss 0 sein.</td>
<td>Wird in dieser Version nicht verwendet. Muss 0 sein.</td>
</tr>
<tr class="odd">
<td>ViewType</td>
<td>Ja</td>
<td>Unicode-Zeichenfolge. Format: [I|T| R| L|O]Beispiel: T<br/></td>
<td>Gibt den Ansichtstyp an, der für die Liste verwendet werden soll.
<ul>
<li>I = Symbol</li>
<li>T = Kachel</li>
<li>R = Bericht</li>
<li>L = List</li>
<li>O = Geordnete Liste</li>
</ul></td>
</tr>
<tr class="even">
<td>ViewImageSize</td>
<td>Ja</td>
<td>Nicht negative ganze Zahl. Beispiel: 180<br/></td>
<td>Die Größe, mit der das Listenbild angezeigt wird. Bei 0 wird die Größe automatisch bestimmt.</td>
</tr>
<tr class="odd">
<td>GroupBy</td>
<td>Ja</td>
<td>Unicode-Zeichenfolge. Format: [-| P| A| C|R| D]<br/> Beispiel: P<br/></td>
<td>Gibt an, welches Feld zum Gruppen der Elemente in der Liste verwendet wird.
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
<td>ListItemsAreDynamic</td>
<td>Ja</td>
<td>Boolesch. Kann 0 oder 1 sein.</td>
<td>Gibt an, ob die Liste dynamisch generiert wird. Dynamische Listen enthalten keine Elemente in listitem.csv. Wenn eine Liste als dynamisch markiert ist, werden ihre Elemente von <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a> bereitgestellt.</td>
</tr>
</tbody>
</table>



 

 

 





