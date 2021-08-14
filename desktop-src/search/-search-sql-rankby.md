---
description: Die Ergebnisse einer Abfrage enthalten sowohl die von der Abfrage zurückgegebenen Zeilen als auch einen Rangwert für jede Zeile, wenn die Rangfolgespalte in der SELECT-Klausel enthalten ist.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: RANK BY-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33daf4865b0f7f08689802822d8c0d5b4d38702a1cb1f813563564e001811a6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462439"
---
# <a name="rank-by-clause"></a>RANK BY-Klausel

Die Ergebnisse einer Abfrage enthalten sowohl die von der Abfrage zurückgegebenen Zeilen als auch einen Rangwert für jede Zeile, wenn die Rangfolgespalte in der SELECT-Klausel enthalten ist. Die Rangwerte werden von der Suchmaschine berechnet und als ganze Zahlen im Bereich 0 bis 1000 zurückgegeben. Um die Rangfolgeergebnisse aussagekräftiger zu gestalten, kann die Abfrage steuern, wie unformatierte Rangwerte in der RANK BY-Klausel berechnet werden.

Dieses Thema ist wie folgt organisiert:

-   [RANK BY-Klausel](#rank-by-clause)
-   [WEIGHT-Funktion](#weight-function)
-   [COERCION-Funktion](#coercion-function)

## <a name="rank-by-clause"></a>RANK BY-Klausel

Die Syntax für die RANK BY-Klausel lautet wie folgt:


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



Die RANK BY-Klausel wird auf die unmittelbar vorausgehende Suchbedingung angewendet und gibt effektiv einen niedrigeren oder höheren Rang für Zeilen an, die von dieser Suchbedingung zurückgegeben werden, als Zeilen, die von einer anderen Suchbedingung \_ zurückgegeben werden. Die Klammern um die \_ Suchbedingung sind erforderlich. Die Klammern um die Rangangabe sind optional.

Mehrere RANK BY-Klauseln können auf eine einzelne Bedingung angewendet werden. Sie können mithilfe von Klammern nacheinander zusätzliche RANK BY-Klauseln verwenden.

> [!Note]  
> Volltext-Prädikate geben Rangwerte im Bereich von 0 bis 1000 zurück. Rangwerte für alle Dokumente, die mit einem Nicht-Volltext-Prädikat übereinstimmen, sind 1000. Änderungen an den Rangwerten sollten diese Informationen berücksichtigen.

 

Der \_ Rangspezifikationsteil der RANKBY-Klausel identifiziert eine oder mehrere Funktionen, die auf die Rangwerte angewendet werden. Die WEIGHT-Funktion wendet einen Multiplikator auf den rohen Rangwert für eine zurückgegebene Zeile an. Je kleiner der Multiplikator, desto niedriger der resultierende Rangwert. Mit der COERCION-Funktion kann ein bestimmter Rangwert für eine zurückgegebene Zeile multipliziert, hinzugefügt oder festgelegt werden. Jede Rangfolgespezifikation kann entweder null oder eine WEIGHT-Funktion und null oder mehr COERCION-Funktionen enthalten. Wenn sowohl die WEIGHT- als auch die COERCION-Funktion in einer RANK BY-Klausel enthalten sind, muss die WEIGHT-Funktion an erster Stelle stehen.

## <a name="weight-function"></a>WEIGHT-Funktion

Die Syntax der WEIGHT-Funktion ist:


```
WEIGHT ( <weight_multipler> ) 
```



Der Multiplikator muss eine Dezimalzahl von 0,001 bis 1,000 sein. Der unformatierte Rangwert, der vom Suchbedingungs-Prädikat zurückgegeben wird, wird mit dem Gewichtungsmultiplikator multipliziert, um einen neuen Rangwert zu setzen.

Im folgenden Beispiel enthält die WEIGHT-Funktion Dokumente mit dem Wort "Theresa" im System.Document. LastAuthor-Feld zur Hälfte des Rangwerts von Dokumenten mit "Theresa" im Feld System.Author:


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> Die Spaltengewichtungsfeatures CONTAINS und FREETEXT unterstützen ein Kurzformat mit einem Doppelpunkt zwischen dem Suchbegriff und dem Multiplikator ("software":0.25). Die RANK BY-Klausel unterstützt die verkürzte Form nicht.

 

Es gibt eine Einschränkung bei der Verwendung von RANK BY WEIGHT: Es funktioniert nicht mit CONTAINS-Klauseln, die boolesche Bedingungen verwenden. Das folgende Beispiel ist beispielsweise nicht zulässig:


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a>COERCION-Funktion

Die Rangkoercion-Funktion kann verwendet werden, um den zurückgegebenen Rangwert durch Addition oder Multiplikation oder durch Zuweisen eines bestimmten Werts zu ändern.

Die Syntax der COERCION-Funktion ist:


```
COERCION ( <coercion_operation> , <coercion_value> )
```



Der Koercion-Wert ist ein ganzzahliger Wert.

In der folgenden Tabelle werden die verfügbaren Einstellungen für den Koercion-Vorgang beschrieben.



| Koercion-Vorgang | BESCHREIBUNG                                                                                    | Wertebereich  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| ABSOLUTE           | Der zurückgegebene Rangwert ist der im Koercion-Wert angegebene Wert.                          | 0 bis 1000    |
| ADD                | Der zurückgegebene Rangwert ist die Summe aus dem rohen Rangwert und dem angegebenen Koercion-Wert.     | 0,001 bis 1,0 |
| MULTIPLIZIEREN           | Der zurückgegebene Rangwert ist das Produkt des rohen Rangwerts und des angegebenen Koercion-Werts. | 0,001 bis 1,0 |



 

 

> [!IMPORTANT]
> Die Suche kann Rangwerte nur im Bereich von 0 bis 1000 zurückgeben.

 

 

Im folgenden Beispiel wird die COERCION-Funktion verwendet, um alle Dokumente mit "computer" im Titel auf einen Rang von 1000 zu setzen, während der Rang der Dokumente, die sowohl "computer" als auch "software" im Titel enthalten, um ein Quartal reduziert wird.


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



