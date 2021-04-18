---
description: Die Ergebnisse einer Abfrage enthalten sowohl die von der Abfrage zurückgegebenen Zeilen als auch einen Rangwert für jede Zeile, wenn die Rang Spalte in der SELECT-Klausel enthalten ist.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: Rank by-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de7f7a63e33f43ba6387cbcea44a5f5b5ae8f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214457"
---
# <a name="rank-by-clause"></a>Rank by-Klausel

Die Ergebnisse einer Abfrage enthalten sowohl die von der Abfrage zurückgegebenen Zeilen als auch einen Rangwert für jede Zeile, wenn die Rang Spalte in der SELECT-Klausel enthalten ist. Die Rang Werte werden von der Suchmaschine berechnet und als ganze Zahlen im Bereich von 0 bis 1000 zurückgegeben. Damit die Rang Ergebnisse aussagekräftiger werden, kann die Abfrage steuern, wie rohrang Werte in der Rank by-Klausel berechnet werden.

Dieses Thema ist wie folgt organisiert:

-   [Rank by-Klausel](#rank-by-clause)
-   [Weight-Funktion](#weight-function)
-   [Umwandlungs Funktion](#coercion-function)

## <a name="rank-by-clause"></a>Rank by-Klausel

Die Syntax für die Rank by-Klausel lautet wie folgt:


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



Die Rank by-Klausel wird auf die \_ unmittelbar vorhergehende Such Bedingung angewendet. dabei wird ein niedrigerer oder höherer Rang für Zeilen angegeben, die von dieser Such Bedingung zurückgegeben werden, als von einer anderen Such Bedingung zurückgegebene Zeilen. Die Klammern, die die Such Bedingung umgeben, \_ sind erforderlich. Die Klammern, die die Rang Spezifikation umgeben, sind optional.

Auf eine einzelne Bedingung können mehr als eine Rang by-Klausel angewendet werden. Sie können zusätzliche Rank by-Klauseln nacheinander mithilfe von Klammern einschließen.

> [!Note]  
> Volltext-Prädikate geben Rang Werte im Bereich von 0 bis 1000 zurück. Rang Werte für alle Dokumente, die mit einem nicht-voll Text Prädikat übereinstimmen, sind 1000. Bei Änderungen an den Rang Werten sollten diese Informationen berücksichtigt werden.

 

Der Rang \_ Spezifikations Teil der rankby-Klausel identifiziert mindestens eine Funktion, die auf die Rang Werte angewendet werden soll. Die Weight-Funktion wendet einen Multiplikator auf den unformatierten Rangwert für eine zurückgegebene Zeile an. Je kleiner der Multiplikator, desto niedriger ist der resultierende Rangwert. Die Umwandlungs Funktion kann verwendet werden, um einen bestimmten Rangwert für eine zurückgegebene Zeile zu multiplizieren, zu addieren oder festzulegen. Jede Rang Spezifikation kann entweder NULL oder eine Gewichtungsfunktion und NULL oder mehr koerationsfunktionen enthalten. Wenn sowohl Gewichtungs-als auch dekoerationsfunktionen in eine Rank by-Klausel eingeschlossen werden, muss die Gewichtungsfunktion zuerst sein.

## <a name="weight-function"></a>Weight-Funktion

Die Syntax der Gewichtungsfunktion lautet wie folgt:


```
WEIGHT ( <weight_multipler> ) 
```



Der Multiplikator muss ein Dezimalwert zwischen 0,001 und 1,000 sein. Der vom Such Bedingungs Prädikat zurückgegebene rohrangwert wird mit dem Gewichtungs Multiplikator multipliziert, um einen neuen Rangwert festzulegen.

Im folgenden Beispiel gibt die Weight-Funktion Dokumente mit dem Wort "Theresia" im System.Doc-Umschlag. Lastauthor-Feld halber der Rangwert von Dokumenten mit "Theresa" im Feld "System. Author":


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> Die Spalten Gewichtungs Features "enthält" und "frei Text Prädikat" unterstützen eine Kurzform mit einem Doppelpunkt zwischen dem Suchbegriff und dem Multiplikator ("Software": 0,25). Die Rang-nach-Klausel unterstützt das gekürzte Formular nicht.

 

Bei der Verwendung von Rang nach Gewichtung gibt es eine Einschränkung: es funktioniert nicht mit Klauseln, die boolesche Bedingungen verwenden; Das folgende Beispiel ist beispielsweise nicht zulässig:


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a>Umwandlungs Funktion

Die Rang Umwandlungs Funktion kann verwendet werden, um den zurückgegebenen Rangwert durch Hinzufügen oder Multiplikation oder durch Zuweisen eines bestimmten Werts zu ändern.

Die Syntax der erumwandlungs Funktion lautet wie folgt:


```
COERCION ( <coercion_operation> , <coercion_value> )
```



Der koerationswert ist ein ganzzahliger Wert.

In der folgenden Tabelle werden die verfügbaren Umwandlungs Vorgangs Einstellungen beschrieben.



| Umwandlungs Vorgang | BESCHREIBUNG                                                                                    | Wertebereich  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| ABSOLUTE           | Der zurückgegebene Rangwert ist der Wert, der im koerationswert angegeben wird.                          | 0 bis 1000    |
| ADD                | Der zurückgegebene Rangwert ist die Summe des rohrang Werts und des angegebenen koerationswerts.     | 0,001 bis 1,0 |
| MULTIPLIZIEREN           | Der zurückgegebene Rangwert ist das Produkt des rohrang Werts und des angegebenen koerationswerts. | 0,001 bis 1,0 |



 

 

> [!IMPORTANT]
> Die Suche kann Rang Werte nur im Bereich von 0 bis 1000 zurückgeben.

 

 

Im folgenden Beispiel wird die Erteilungs Funktion verwendet, um alle Dokumente mit dem Titel "Computer" im Titel auf einen Rang von 1000 festzulegen, während der Rang der Dokumente, die im Titel "Computer" und "Software" enthalten, um ein Quartal reduziert wird.


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



