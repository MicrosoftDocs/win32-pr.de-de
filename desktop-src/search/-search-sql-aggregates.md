---
description: Eine Aggregatfunktion führt eine Berechnung für einen Satz von Werten durch und gibt einen Wert zurück. Dadurch können zusammenfassende Statistiken für Gruppen mit mehreren Ebene mit geringem Mehraufwand generiert werden.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Aggregatfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d504a9343116bc23e847728716eeaa79fc2d26d993e962dd81ccd43669e22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094955"
---
# <a name="aggregate-functions"></a>Aggregatfunktionen

Eine Aggregatfunktion führt eine Berechnung für einen Satz von Werten durch und gibt einen Wert zurück. Dadurch können zusammenfassende Statistiken für Gruppen mit mehreren Ebene mit geringem Mehraufwand generiert werden.

## <a name="about-aggregate-functions"></a>Informationen zu Aggregatfunktionen

Aggregatfunktionen in Windows Search strukturierte Abfragesprache (SQL) haben die folgende Syntax:


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



Der Funktionsteil kann eine der folgenden Funktionen und Syntax enthalten:



| Funktion                                                              | Beschreibung                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AVG( <column> )                                                   | Gibt den Mittelwert der Werte in einer Gruppe zurück. Gilt nur für Zahlen.                                                                                                                                      |
| BYFREQUENCY( <column> , <N> )                                | Gibt die häufigsten N Spaltenwerte aus den Ergebnissen in der Gruppe zurück. Enthält auch die Anzahl der Aufgetretenen werte und Dokumentbezeichner für Ergebnisse, die jeden zurückgegebenen Wert enthalten. |
| CHILDCOUNT()                                                          | Gibt die Anzahl der Elemente in einer Gruppe zurück (mit Ausnahme von Untergruppen). Wenn es mehrere Gruppierungsebenen gibt, wird die Anzahl der unmittelbar untergeordneten Gruppen zurückgegeben.                                                  |
| COUNT()                                                               | Gibt die Anzahl der Elemente in einer Gruppe und alle Untergruppen zurück.                                                                                                                                                   |
| DATERANGE( <column> )                                             | Gibt die untere und obere Grenze der Spaltenwerte in der Gruppenergebnisgruppe zurück. Nur für filetime-Eigenschaften gültig.                                                                               |
| FIRST( <column> , <N> )                                      | Gibt die ersten N Spaltenwerte aus Blattergebnissen zurück, die in einer Gruppe gefunden wurden.                                                                                                                                       |
| MAX( <column> )                                                   | Gibt den größten Wert im Ausdruck zurück. Gilt nur für Zahlen oder Datumsangaben.                                                                                                                              |
| MIN( <column> )                                                   | Gibt den kleinsten Wert im Ausdruck zurück. Gilt nur für Zahlen oder Datumsangaben.                                                                                                                              |
| REPRESENTATIVEOF( <column> , <idRepresentative> , <N> ) | Gibt N idRepresentative-Werte zurück, die jeweils aus einer der Ergebnisteilmengen ausgewählt wurden, die über einen eindeutigen Spaltenwert verfügt. Jeder Wert wird auch mit einem Dokumentbezeichner zurückgegeben, der über den idRepresentative-Wert verfügt. |
| SUM( <column> )                                                   | Gibt die Summe der Werte in einer Gruppe zurück. Gilt nur für Zahlen.                                                                                                                                          |



 

 

> [!Note]  
> Aggregate werden als einzelne Spalten zurückgegeben. Sie sind größtenteils einfache Typen mit Ausnahme von ByFrequency, First, DateRange und RepresentativeOf, die als Verbundtypen zurückgegeben werden.

 

Sie können eine beliebige numerische spalte oder datumsspalte für Aggregationen verwenden, nicht nur diejenigen, die in der SELECT-Klausel enthalten sind. Sie können jedoch nicht nach Aggregaten gruppieren. Ein Syntaxfehler wird zurückgegeben, wenn das übergebene Spaltenargument weder ein numerischer Typ noch ein Datumstyp ist.

Der Bezeichnungsteil ist optional und bietet einen besser lesbaren Alias für die Bezeichnung. Wenn Sie keine Aliasbezeichnung angeben, transformiert Windows Search den Funktions- und Spaltennamen in eine Bezeichnung. Beispiel: MAX(System.Document. WordCount) wird zu MAX \_ SystemDocumentWordCount.

## <a name="multi-level-groups-and-counting"></a>Gruppen und Zählen auf mehreren Ebene

Aggregate werden über Blättern definiert und dupliziert. Ein Aggregat verwendet als Eingabe die Blätter der Gruppe, die sie definiert (Dokumente), und nicht die Untergruppen ihrer untergeordneten Gruppen. Diese Funktion wird als Gruppierung mit mehreren Ebene bezeichnet.

Zusätzlich zu Aggregaten, die für Blätter definiert und dupliziert werden, werden sie nur einmal gezählt. Obwohl dasselbe Dokument möglicherweise mehrmals unter einer Gruppe dargestellt wird, wird es von Aggregaten nur einmal betrachtet. Die folgende Grafik veranschaulicht dieses Konzept.

![Diagramm, das zeigt, dass Aggregate für Blätter definiert und dupliziert und nur einmal gezählt werden](images/aggregates.png)

## <a name="aggregate-examples"></a>Aggregatbeispiele

Im Folgenden finden Sie Beispiele für Aggregatfunktionen innerhalb der GROUP ON-Klausel:


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

Der Rückgabewert ist eine Variante, die im Rowset als benutzerdefinierte Eigenschaft gefunden wird, entweder als angegebene Aliase oder als "Aggregates", wenn keine Aliasbezeichnung angegeben ist.

 

 



