---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player Onlineshops,list.csv
- Onlineshops,list.csv
- Geben Sie 1 Onlineshops ein, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7237afb37b30ccf8c96ddac95f0e81e148703d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480786"
---
# <a name="listcsv"></a>list.csv

Diese Datei enthält einen Eintrag für jede liste, die der Katalog enthält. Listen können Listen mit Titeln, Alben, Interpreten, Genres, Untergenres oder Radiofeeds sein. oder sie können Listen mit anderen Listen sein. Jeder Listeneintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben sind. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird. Sie verweist nicht auf den Datentyp des Inhalts. Wenn beispielsweise Integer in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert darstellt, anstatt eine tatsächliche ganze Zahl.




| Feld | Erforderlich | Format | BESCHREIBUNG | 
|-------|----------|--------|-------------|
| ListID | Ja | Nicht negative ganze Zahl. | Listenbezeichner, innerhalb list.csv eindeutig. Muss nicht negativ und kleiner als 2^32 sein. <strong>Anzeigen eines Listenknotens im Strukturansichtssteuerelement:</strong> Wenn die ListID 0, 1, 2, 3, 4, 5, 6 oder 7 ist, wird die Liste als benutzerdefinierter Knoten unter dem Knoten der obersten Ebene Ihres Onlineshops im Strukturansichtssteuerelement des Players angezeigt. Benutzerdefinierte Knoten werden vor den Standardknoten unter dem Knoten der obersten Ebene des Onlineshops angezeigt und nach ListID in aufsteigender Reihenfolge positioniert. Wenn beispielsweise drei benutzerdefinierte Knoten mit ListIDs von 1, 3 und 5 vorhanden sind, werden sie zuerst, zweiten und dritten Knoten unter dem Knoten der obersten Ebene des Onlineshops angezeigt.<br /> | 
| ListTitle | Nein | Unicode-Zeichenfolge. Beispiel: Top Ten Hits<br /> | Listentitel. | 
| ListSubtitle | Nein | Unicode-Zeichenfolge | Listen Sie den alternativen Titel auf, der in der zweiten Zeile der Kachelansicht angezeigt wird. | 
| ListDescription | Ja | Unicode-Zeichenfolge | Auflisten des anzeigefreundlichen Anzeigetexts (wird auf Eigenschaftenseiten angezeigt). | 
| Linked_ItemType | Ja | Unicode-Zeichenfolge. Format: [T|P|Ein|L|G|E|R]<br /> Beispiel: T<br /> | Gibt den Typ der verknüpften Elemente an.<ul><li>T= Track</li><li>P = Performer</li><li>A = Album</li><li>L = Liste</li><li>G = Genre</li><li>S = Subgenre</li><li>R = Radio</li></ul> | 
| ListPrice | Ja | Unicode-Zeichenfolge. Beispiel: 9,99 USD<br /> | Preis der Liste. Das Währungssymbol sollte enthalten sein. Eine Null bedeutet, dass die Liste kostenlos ist. Kein Wert bedeutet, dass der Preis unbekannt ist. Ein Bindestrich bedeutet, dass die Liste nicht erworben werden kann.<br /> | 
| Beliebtheit | Ja | Ganzzahliger oder Dezimalwert. Beispiel: 1259.3<br /> | Gibt die Beliebtheitsrangfolge an, wenn diese Liste in anderen Listen angezeigt wird. Kann 0 (null) sein, falls nicht zutreffend. | 
| IsRecentlyAdded | Ja | Boolean.Format: [0|1]<br /> Beispiel: 0<br /> | Gibt an, ob die Liste kürzlich hinzugefügt wurde. | 
| IsFeatured | Ja | Boolean.Format: [0|1]<br /> Beispiel: 0<br /> | Gibt an, ob die Liste angezeigt wird. Kann zum Bestimmen der Sortierreihenfolge verwendet werden. | 
| EditorialGlyph | Ja | Nicht negative ganze Zahl. Muss 0 sein. | Wird in dieser Version nicht verwendet. Muss 0 sein. | 
| ViewType | Ja | Unicode-Zeichenfolge. Format: [I|T|R|L|O]Beispiel: T<br /> | Gibt den Ansichtstyp an, der für die Liste verwendet werden soll.<ul><li>I = Symbol</li><li>T = Kachel</li><li>R = Bericht</li><li>L = Liste</li><li>O = Sortierte Liste</li></ul> | 
| ViewImageSize | Ja | Nicht negative ganze Zahl. Beispiel: 180<br /> | Die Größe, mit der das Listenbild angezeigt wird. Bei 0 wird die Größe automatisch bestimmt. | 
| GroupBy | Ja | Unicode-Zeichenfolge. Format: [-|P|Ein|C|R|D]<br /> Beispiel: P<br /> | Gibt an, welches Feld zum Gruppen der Elemente in der Liste verwendet wird.<ul><li>- = Automatisch</li><li>P = Performer</li><li>A = Album</li><li>C = Composer</li><li>R = Bewertung</li><li>D = Datum</li></ul> | 
| ListItemsAreDynamic | Ja | Boolesch. Kann 0 oder 1 sein. | Gibt an, ob die Liste dynamisch generiert wird. Dynamische Listen enthalten keine Elemente in listitem.csv. Wenn eine Liste als dynamisch markiert ist, werden ihre Elemente von <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents bereitgestellt.</a> | 




 

 

 





