---
description: Die Gruppe in...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: Gruppieren nach... Über... An
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d7087305f0a5a86f0288ed92ec4bda5b8c882c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128541"
---
# <a name="group-on--over--statement"></a>Gruppieren nach... Über... An

Die Gruppe in... Über... die-Anweisung gibt ein hierarchisches Rowset zurück, in dem Suchergebnisse auf der Grundlage einer angegebenen Spalte und optionaler Gruppierungs Bereiche in Gruppen aufgeteilt werden. Wenn Sie in der Spalte [System. Kind](../properties/props-system-kind.md) gruppieren, ist das Resultset in mehrere Gruppen unterteilt: eine für Dokumente, eine für die Kommunikation usw. Wenn Sie [System. Size](../properties/props-system-size.md) und den Gruppenbereich 100 KB gruppieren, ist das Resultset in drei Gruppen unterteilt: Elemente der Größe < 100 KB, Elemente der Größe >= 100 KB und Elemente ohne Größen Wert. Sie können auch Gruppierungen mit Funktionen aggregieren.

In diesem Thema werden die folgenden Themen behandelt:

-   [Syntax](#syntax)
-   [Gruppen Bereiche](#group-ranges)
-   [Bezeichnen von Gruppen](#labeling-groups)
-   [Anordnen von Gruppen](#ordering-groups)
-   [Schachteln von Gruppen](#nesting-groups)
-   [Gruppieren von Vektor Eigenschaften](#grouping-on-vector-properties)
-   [Weitere Beispiele](#more-examples)
-   [Zugehörige Themen](#related-topics)

## <a name="syntax"></a>Syntax

Die Gruppe in... Über... die-Anweisung weist die folgende Syntax auf:


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



Dabei werden Gruppierungs Bereiche wie folgt definiert:


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



Die Gruppe in <column> kann ein regulärer oder Begrenzungs [Bezeichner](-search-sql-identifiers.md) für eine Eigenschaft im Eigenschaften Speicher sein.

Der optionale <group ranges> ist eine Liste mit einem oder mehreren Werten (Anzahl, Datum oder Zeichenfolge), die zum Aufteilen der Ergebnisse in Gruppen verwendet werden. Der <range limit> identifiziert einen Divisions Punkt im zurückgegebenen Resultset, und der <label> identifiziert eine benutzerfreundliche Bezeichnung für eine Gruppe. Sie können das Resultset in beliebig viele Gruppen aufteilen.

Die erste Gruppe der Ergebnisse umfasst Elemente mit dem minimal möglichen Wert für die angegebene Eigenschaft bis zum ersten Bereichs Limit. Auf diese Gruppe kann mit dem MinValue-Schlüsselwort verwiesen werden. Auf die zweite Gruppe kann mit dem bereichsbeschränkungsspezifizierer selbst verwiesen werden. Sie enthält Elemente, deren Wert für die angegebene Eigenschaft größer oder gleich dem Bereichs Limit ist. Alle Elemente, die nicht über einen Wert für die angegebene Eigenschaft verfügen, werden zuletzt zurückgegeben, und auf Sie kann mit dem **null** -Schlüsselwort verwiesen werden.

Beispielsweise dividiert eine Bereichs Beschränkung von "2006-01-01" für die [System. DateCreated](../properties/props-system-datecreated.md) -Eigenschaft das Resultset in Elemente mit Datumsangaben vor 2006-01-01 (MinValue-Gruppe), Elementen mit Datumsangaben auf oder nach 2006-01-01 (2006-01-01-Gruppe) und Elementen ohne Datum (**null** -Gruppe).

In jeder Gruppe werden die Ergebnisse standardmäßig nach den Werten in der Spalte Gruppieren nach sortiert. Die optionale [Order by](-search-sql-orderby.md) -Klausel kann einen Zugriffsspezifizierer von ASC für aufsteigend (niedrig zu hoch) oder für absteigend (hoch bis niedrig) enthalten, und die [Reihenfolge in der Group by](-search-sql-orderingroup.md) -Klausel kann jede Gruppe mit unterschiedlichen Regeln sortieren. Weitere Informationen finden Sie im nachfolgenden Abschnitt [Bestell Gruppen](#ordering-groups) .

## <a name="group-ranges"></a>Gruppen Bereiche

In der folgenden Tabelle wird veranschaulicht, wie die Ergebnisse in Gruppen unterteilt werden, basierend auf den Bereichs Limits:



| Beispiel ( <column> \[ Gruppen Bereiche \] )        | Ergebnis                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System. size \[ 1000, 5000\]                       | Die Ergebnisse werden in vier Bucket gruppiert: **MinValue**: Size < 1000<br/> **1000:** 1000 <= Größe < 5000<br/> **5000:** Größe >= 5000<br/> **Null:** Kein Wert für Größe<br/>                                                                      |
| System. Author \[ vor ('m '), After (' r ')\]         | Die Ergebnisse werden in vier Bucket gruppiert: **MinValue:** "Autor < Zeichen" vor "m"<br/> **m:** Zeichen vor "m" <= Autor < Zeichen nach "r"<br/> **r:** Zeichen nach "r" <= Autor<br/> **Null:** Kein Wert für Autor<br/>      |
| System. Author \[ MinValue/"a to l", "m"/be to z "\] | Die Ergebnisse werden in drei Bucket gruppiert: **a bis l:** Author < "m"<br/> **m bis z:** "m" <= Autor <br/> **Null:** Kein Wert für Autor<br/>                                                                                                               |
| System. DateCreated \[ "2005-1-01", "2006-6-01"\]   | Die Ergebnisse werden in vier Bucket gruppiert:<br/> **MinValue:** DateCreated-< 2005-1-01<br/> **2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01<br/> **2006-1-01:** DateCreated->= 2006-6-01<br/> **Null:** Kein Wert für DateCreated<br/> |



 

 

> [!IMPORTANT]
>
> Korre `GROUP ON System.Author['m','z','a']`
>
> Richtig: `GROUP ON System.Author['a','m','z']`

 

 

## <a name="labeling-groups"></a>Bezeichnen von Gruppen

Um die Lesbarkeit zu verbessern, können Sie Gruppen mit der folgenden Syntax bezeichnen:


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



Die Bezeichnung ist von der Bereichs Beschränkung mit einem Schrägstrich getrennt und in einfache Anführungszeichen eingeschlossen. Wenn Sie keine Bezeichnung angeben, ist der Gruppenname die Zeichenfolge für das Bereichs Limit.

Im folgenden finden Sie ein Beispiel für die Bezeichnung von Gruppen:


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



In Windows 7 oder höher können Sie auch eine generische \[ andere Bezeichnung verwenden, \] um mehrere Gruppierungs Bereiche zu kombinieren. Ergebnisse aus allen Gruppen, die mit dieser Bezeichnung identifiziert werden, werden mit dieser Bezeichnung zu einer Gruppe zusammengefasst. Diese Ergebnis Gruppe wird nach allen anderen Gruppen außer der **null** -Gruppe zurückgegeben. Die Gruppe **null** enthält Ergebnisse für Elemente, die nicht über einen Wert für die angegebene Eigenschaft verfügen. Vor Windows 7 wird die \[ andere \] Bezeichnung wie jede andere Gruppen Bezeichnung behandelt.

Der folgende Code ist ein Beispiel für die Verwendung der \[ anderen \] Bezeichnung für Gruppen, die in Windows 7 oder höher erstellt werden:


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



In der folgenden Tabelle sind die Gruppen aufgeführt, die durch den vorangehenden Gruppierungs Code in Windows 7 oder höher erstellt werden.



| Gruppieren     | System.Author | System. filename |
|-----------|---------------|-----------------|
| 0         | 1 Rechnung         | Lorem.docx      |
| Q         | Queen         | Ipsum.docx      |
|           | Robin         | dolor.docx      |
| J         | Kette          | amet.docx       |
| \[Außer\] | Abner         | nonummy.docx    |
|           | Bernd           | laoreet.docx    |
|           | Xaria         | magna.docx      |
| **NULL**  |               | aliquam.docx    |



 

## <a name="ordering-groups"></a>Anordnen von Gruppen

Es gibt drei Möglichkeiten, um Elemente in Gruppen zu sortieren:

-   Standardsortierung: Wenn Sie nichts anderes angeben, werden die Ergebnisse nach den Werten in der Spalte Gruppieren in aufsteigender Reihenfolge sortiert.
-   Order by: Sie können eine absteigende Reihenfolge in einer ORDER BY-Klausel angeben. Sie müssen die Ergebnisse nach der Spalte Gruppieren in sortieren.
-   Order in Group by: Sie können für jede Gruppe eine andere Reihenfolge angeben. Wenn Sie [System. Kind](../properties/props-system-kind.md)gruppieren, können Sie Dokumente nach System [. Author](../properties/props-system-author.md) und Musik von [System. Music.](../properties/props-system-music-artist.md)Author anordnen.

Weitere Informationen zum Sortieren von Ergebnissen finden Sie in den Referenzseiten [Order By-Klausel](-search-sql-orderby.md) und [Order in Group-Klausel](-search-sql-orderingroup.md) .

## <a name="nesting-groups"></a>Schachteln von Gruppen

Gruppen können mit mehreren Group on-Klauseln geschachtelt werden. Die in der Abfrage angegebene Reihenfolge wird direkt in der Ausgabe Gruppen Hierarchie reflektiert, wie im folgenden Beispiel gezeigt.


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| System. Kind    | System.Author | System. DateCreated |
|----------------|---------------|--------------------|
| Dokumente      | Willa         | 2006-01-02         |
|                |               | 2006-01-05         |
|                | Kette          | 2007-06-02         |
|                |               | 2007-09-10         |
| Kommunikation | Abner         | 2006-04-16         |
|                | Jean          | 2007-02-20         |
|                | Willa         | 2006-10-15         |
|                | Kette          | 2008-01-02         |



 

 

## <a name="grouping-on-vector-properties"></a>Gruppieren von Vektor Eigenschaften

Gruppieren von Vektor Eigenschaften, Eigenschaften, die einen oder mehrere Werte gleichzeitig enthalten können, vergleicht die Vektor Werte standardmäßig einzeln. Wenn beispielsweise ein Dokument, Lorem.docx, mit der System. Author-Eigenschaft "Theresa;" vorhanden ist. Zara "und ein anderes Dokument, Ipsum.docx, mit der System. Author-Eigenschaft als" Zara ", gibt die Abfrage das Resultset in zwei Gruppen zurück, wie hier gezeigt:


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| System.Author | System. filename |
|---------------|-----------------|
| SIAs       | Lorem.docx      |
| Kette          | Lorem.docx      |
|               | Ipsum.docx      |



 

Wie Sie sehen können, gibt die Gruppierung von Vektor Eigenschaften doppelte Zeilen zurück. Lorem.docx wird zweimal angezeigt, weil es zwei Autoren hat.

 

## <a name="more-examples"></a>Weitere Beispiele


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aggregatfunktionen](-search-sql-aggregates.md)
</dt> <dt>

[Order By-Klausel](-search-sql-orderby.md)
</dt> <dt>

[Order in Group-Klausel](-search-sql-orderingroup.md)
</dt> </dl>

 

 
