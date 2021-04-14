---
description: Eine Aggregatfunktion führt eine Berechnung für einen Satz von Werten aus und gibt einen Wert zurück. Dies ermöglicht es, zusammenfassende Statistiken für Gruppen mit mehreren Ebenen mit geringem mehr Aufwand zu generieren.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Aggregatfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da68ad1104c93e8ae04f7ec37cbbde5020109336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564806"
---
# <a name="aggregate-functions"></a>Aggregatfunktionen

Eine Aggregatfunktion führt eine Berechnung für einen Satz von Werten aus und gibt einen Wert zurück. Dies ermöglicht es, zusammenfassende Statistiken für Gruppen mit mehreren Ebenen mit geringem mehr Aufwand zu generieren.

## <a name="about-aggregate-functions"></a>Informationen zu Aggregatfunktionen

Aggregatfunktionen in Windows Search Structured Query Language (SQL) weisen die folgende Syntax auf:


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



Der Funktionsteil kann eine der folgenden Funktionen und Syntax einschließen:



| Funktion                                                              | BESCHREIBUNG                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AVG ( <column> )                                                   | Gibt den Mittelwert der Werte in einer Gruppe zurück. Gilt nur für Zahlen.                                                                                                                                      |
| Byfrequency ( <column> , <N> )                                | Gibt die häufigsten N Spaltenwerte aus den Ergebnissen in der Gruppe zurück. Umfasst außerdem die Anzahl der Vorkommen der einzelnen Werte und Dokument Bezeichner für Ergebnisse, die jeden zurückgegebenen Wert enthalten. |
| ChildCount ()                                                          | Gibt die Anzahl der Elemente in einer Gruppe zurück (ausgenommen Untergruppen). Wenn mehrere Gruppierungs Ebenen vorhanden sind, wird die Anzahl der unmittelbaren untergeordneten Gruppen zurückgegeben.                                                  |
| COUNT ()                                                               | Gibt die Anzahl der Elemente in einer Gruppe und alle Untergruppen zurück.                                                                                                                                                   |
| DateRange ( <column> )                                             | Gibt die unteren und oberen Begrenzungen der Spaltenwerte zurück, die in der Gruppen Ergebnis Gruppe gefunden wurden. Gilt nur für FILETIME-Eigenschaften.                                                                               |
| First ( <column> , <N> )                                      | Gibt die ersten N Spaltenwerte aus den in einer Gruppe gefundenen Blatt Ergebnissen zurück.                                                                                                                                       |
| Max ( <column> )                                                   | Gibt den größten Wert im Ausdruck zurück. Gilt nur für Zahlen oder Datumsangaben.                                                                                                                              |
| MIN ( <column> )                                                   | Gibt den kleinsten Wert im Ausdruck zurück. Gilt nur für Zahlen oder Datumsangaben.                                                                                                                              |
| Representativeof ( <column> , <idRepresentative> , <N> ) | Gibt N idrepresentative-Werte zurück, die jeweils aus einer der Ergebnis Teilmengen mit einem eindeutigen Spaltenwert ausgewählt wurden. Jeder Wert wird auch mit einem Dokument Bezeichner mit dem idrepresentative-Wert zurückgegeben. |
| Sum ( <column> )                                                   | Gibt die Summe der Werte in einer Gruppe zurück. Gilt nur für Zahlen.                                                                                                                                          |



 

 

> [!Note]  
> Aggregate werden als einzelne Spalten zurückgegeben. Sie sind größtenteils einfache Typen mit Ausnahme von byfrequency, First, DateRange und representativeof, die als Verbund Typen zurückgegeben werden.

 

Sie können eine beliebige numerische oder Datums Spalte für Aggregationen verwenden, und nicht nur diejenigen, die in der SELECT-Klausel enthalten sind. Sie können jedoch keine Gruppierung von Aggregaten durchführt. Ein Syntax Fehler wird zurückgegeben, wenn das über gegebene Spalten Argument weder ein numerischer noch ein Date-Typ ist.

Der Bezeichnungs Teil ist optional und bietet einen besser lesbaren Alias für die Bezeichnung. Wenn Sie keine Alias Bezeichnung einschließen, transformiert Windows Search den Funktions-und Spaltennamen in eine Bezeichnung. Beispiel: Max (System.DocAnzahl. WordCount) wird zu Max \_ systemdocumentwordcount.

## <a name="multi-level-groups-and-counting"></a>Gruppen und zählen auf mehreren Ebenen

Aggregate werden über Blätter definiert und dupliziert. Ein Aggregat übernimmt als Eingabe die Blätter der Gruppe, die es definiert (Dokumente), anstatt die untergeordneten Gruppen seiner untergeordneten Elemente. Diese Funktion wird als Gruppierung mit mehreren Ebenen bezeichnet.

Zusätzlich zu den Aggregaten, die über Blätter definiert und dupliziert werden, werden Sie nur einmal gezählt. Obwohl das gleiche Dokument mehrmals unter einer Gruppe dargestellt werden kann, wird es von Aggregaten nur einmal berücksichtigt. Dieses Konzept wird in der folgenden Abbildung veranschaulicht.

![Diagramm, das anzeigt, dass Aggregate über Blätter definiert und dupliziert werden und nur einmal gezählt werden](images/aggregates.png)

## <a name="aggregate-examples"></a>Aggregat Beispiele

Im folgenden finden Sie Beispiele für Aggregatfunktionen innerhalb der Group on-Klausel:


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist eine Variante, die im Rowset als benutzerdefinierte Eigenschaft gefunden wird, entweder als angegebene Aliase oder als "Aggregate", wenn keine Alias Bezeichnung angegeben wird.

 

 



