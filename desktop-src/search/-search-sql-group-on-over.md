---
description: Die GROUP ON...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: GROUP ON ... ÜBER... Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df21bb53babd25ae3e407032c6cf9d3774323e85
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882015"
---
# <a name="group-on--over--statement"></a>GROUP ON ... ÜBER... Anweisung

Die GROUP ON... ÜBER... -Anweisung gibt ein hierarchisches Rowset zurück, in dem Suchergebnisse basierend auf einer angegebenen Spalte und optionalen Gruppierungsbereichen in Gruppen unterteilt werden. Wenn Sie nach der [Spalte System.Kind](../properties/props-system-kind.md) gruppieren, wird das Ergebnisset in mehrere Gruppen unterteilt: eine für Dokumente, eine für die Kommunikation und so weiter. Wenn Sie [system.size und](../properties/props-system-size.md) den Gruppenbereich 100 KB gruppiert haben, wird das Ergebnisset in drei Gruppen unterteilt: Elemente der Größe < 100 KB, Elemente der Größe >= 100 KB und Elemente ohne Größenwert. Sie können Auch Gruppierungen mit Funktionen aggregieren.

In diesem Thema werden die folgenden Themen behandelt:

-   [Syntax](#syntax)
-   [Gruppenbereiche](#group-ranges)
-   [Bezeichnungsgruppen](#labeling-groups)
-   [Reihenfolge von Gruppen](#ordering-groups)
-   [Schachteln von Gruppen](#nesting-groups)
-   [Gruppieren nach Vektoreigenschaften](#grouping-on-vector-properties)
-   [Weitere Beispiele](#more-examples)
-   [Zugehörige Themen](#related-topics)

## <a name="syntax"></a>Syntax

Die GROUP ON ... ÜBER... -Anweisung hat die folgende Syntax:


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



Dabei werden Gruppierungsbereiche wie folgt definiert:


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



Die GROUP ON-Spalte kann ein regulärer oder durch Trennzeichen getrennter &lt; &gt; [Bezeichner](-search-sql-identifiers.md) für eine Eigenschaft im Eigenschaftenspeicher sein.

Optional ist eine Liste mit einem oder mehreren Werten (Zahl, Datum oder Zeichenfolge), die zum Aufteilen der Ergebnisse <group ranges> in Gruppen verwendet werden. Identifiziert einen Divisionspunkt im zurückgegebenen Resultset, und identifiziert eine <range limit> <label> benutzerfreundliche Bezeichnung für eine Gruppe. Sie können das Ergebnisset in so viele Gruppen unterteilen, wie Sie benötigen.

Die erste Gruppe von Ergebnissen enthält Elemente mit dem minimal möglichen Wert für die angegebene Eigenschaft bis einschließlich des grenzwerts für den ersten Bereich. Auf diese Gruppe kann mit dem MINVALUE-Schlüsselwort verwiesen werden. Auf die zweite Gruppe kann mit dem Bereichsbegrenzungsspezifizierer selbst verwiesen werden und enthält Elemente, deren Wert für die angegebene Eigenschaft gleich oder größer als der Bereichsgrenzwert ist. Alle Elemente, die keinen Wert für die angegebene Eigenschaft haben, werden zuletzt zurückgegeben und können mit dem **NULL-Schlüsselwort darauf verwiesen** werden.

Ein Bereichslimit von "2006-01-01" für die [System.DateCreated-Eigenschaft](../properties/props-system-datecreated.md) unterteilt das Ergebnisset beispielsweise in Elemente mit Datumsangaben vor dem 01.01.2006 (MINVALUE-Gruppe), Elementen mit Datumsangaben am oder nach dem 01.01.2006 (Gruppe 2006-01-01) und Elementen ohne Datum (**NULL-Gruppe).**

Innerhalb jeder Gruppe werden die Ergebnisse standardmäßig nach den Werten in der GROUP ON-Spalte sortiert. Die [optionale ORDER BY-Klausel](-search-sql-orderby.md) kann einen Richtungsspezifizierer von ASC für aufsteigend (niedrig bis hoch) oder DESC für absteigend (hoch bis niedrig) enthalten, und die [ORDER IN GROUP BY-Klausel](-search-sql-orderingroup.md) kann jede Gruppe mit unterschiedlichen Regeln reihenfolgen. Weitere Informationen [finden Sie weiter](#ordering-groups) unten im Abschnitt Bestellgruppen.

## <a name="group-ranges"></a>Gruppenbereiche

In der folgenden Tabelle wird veranschaulicht, wie Die Ergebnisse basierend auf den Bereichsgrenzwerten in Gruppen unterteilt werden:



| Beispiel ( &lt; &gt; \[ Spaltengruppenbereiche \] )        | Ergebnis                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System.Size \[ 1000, 5000\]                       | Die Ergebnisse werden in vier Buckets eingekreist: **MINVALUE**: < 1000<br/> **1000:** 1000 <= Größe < 5000<br/> **5000:** Größe >= 5000<br/> **NULL:** Kein Wert für Größe<br/>                                                                      |
| System.Author \[ BEFORE('m'),AFTER('r')\]         | Die Ergebnisse werden in vier Buckets eingekreist: **MINVALUE:** Author < character before "m"<br/> **m:** Zeichen vor "m" <= < Zeichen nach "r" erstellen<br/> **r: Zeichen** nach "r" <= Author<br/> **NULL:** Kein Wert für Autor<br/>      |
| System.Author \[ MINVALUE/'a to l',"m"/'m to z'\] | Die Ergebnisse werden in drei Buckets eingekreist: **a bis l:** Author < "m"<br/> **m bis z:** "m" <= Author <br/> **NULL:** Kein Wert für Autor<br/>                                                                                                               |
| System.DateCreated \[ '2005-1-01','2006-6-01'\]   | Die Ergebnisse werden in vier Buckets eingekreist:<br/> **MINVALUE:** DateCreated < 01.05.2005<br/> **2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01<br/> **2006-1-01:** DateCreated >= 2006-6-01<br/> **NULL:** Kein Wert für DateCreated<br/> |



 

 

> [!IMPORTANT]
>
> Falsche: `GROUP ON System.Author['m','z','a']`
>
> Richtig: `GROUP ON System.Author['a','m','z']`

 

 

## <a name="labeling-groups"></a>Bezeichnungsgruppen

Um die Lesbarkeit zu verbessern, können Sie Gruppen mit der folgenden Syntax beschriften:


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



Die Bezeichnung ist durch einen Schrägstrich vom Bereichsgrenzwert getrennt und in einfache Anführungszeichen eingeschlossen. Wenn Sie keine Bezeichnung angeben, ist der Gruppenname die Bereichsbegrenzungszeichenfolge.

Im Folgenden finden Sie ein Beispiel für Bezeichnungsgruppen:


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



In Windows 7 oder höher können Sie auch eine generische OTHER-Bezeichnung verwenden, um \[ \] mehrere Gruppierungsbereiche zu kombinieren. Ergebnisse aus allen Gruppen, die mit dieser Bezeichnung identifiziert werden, werden in einer Gruppe mit dieser Bezeichnung kombiniert. Diese Gruppe von Ergebnissen wird nach allen anderen Gruppen mit Ausnahme der **NULL-Gruppe** zurückgegeben. Die **NULL-Gruppe** enthält Ergebnisse für Elemente, die keinen Wert für die angegebene Eigenschaft haben. Vor Windows 7 wird die \[ Bezeichnung OTHER wie jede andere \] Gruppenbezeichnung behandelt.

Der folgende Code ist ein Beispiel für die Verwendung der Bezeichnung OTHER für Gruppen, die in Windows 7 oder \[ \] höher erstellt werden:


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



In der folgenden Tabelle sind die Gruppen aufgeführt, die durch den vorangehenden Gruppierungscode in Windows 7 oder höher erstellt werden.



| Group     | System.Author | System.FileName |
|-----------|---------------|-----------------|
| 0         | 1Bill         | Lorem.docx      |
| Q         | Königin         | Ipsum.docx      |
|           | Robin         | dolor.docx      |
| J         | Zara          | amet.docx       |
| \[ANDERE\] | Abner         | nonummy.docx    |
|           | Bob           | laoreet.docx    |
|           | Xaria         | magna.docx      |
| **NULL**  |               | aliquam.docx    |



 

## <a name="ordering-groups"></a>Reihenfolge von Gruppen

Es gibt drei Möglichkeiten, Elemente in Gruppen zu bestellen:

-   Standard reihenfolge: Wenn Sie andernfalls nicht angeben, werden die Ergebnisse nach den Werten in der GROUP ON -Spalte in aufsteigender Reihenfolge geordnet.
-   ORDER BY: Sie können eine absteigende Reihenfolge in einer ORDER BY-Klausel angeben. Sie müssen die Ergebnisse nach der GROUP ON-Spalte sortieren.
-   ORDER IN GROUP BY: Sie können für jede Gruppe eine andere Reihenfolge angeben. Wenn Sie nach [System.Kind](../properties/props-system-kind.md)gruppieren, können Sie Dokumente nach [System.Author und](../properties/props-system-author.md) music nach [System.Musik. Interpret](../properties/props-system-music-artist.md).

Weitere Informationen zum Reihenfolgen von Ergebnissen finden Sie auf den Referenzseiten [zur ORDER BY-Klausel](-search-sql-orderby.md) und [zur ORDER IN GROUP-Klausel.](-search-sql-orderingroup.md)

## <a name="nesting-groups"></a>Schachteln von Gruppen

Sie können Gruppen mit mehreren GROUP ON-Klauseln schachteln. Die in der Abfrage angegebene Reihenfolge wird direkt in der Ausgabegruppenhierarchie widergespiegelt, wie im folgenden Beispiel gezeigt.


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| System.Kind    | System.Author | System.DateCreated |
|----------------|---------------|--------------------|
| Dokumente      | Willa         | 2006-01-02         |
|                |               | 2006-01-05         |
|                | Zara          | 2007-06-02         |
|                |               | 2007-09-10         |
| Kommunikation | Abner         | 2006-04-16         |
|                | Jean          | 2007-02-20         |
|                | Willa         | 2006-10-15         |
|                | Zara          | 2008-01-02         |



 

 

## <a name="grouping-on-vector-properties"></a>Gruppieren nach Vektoreigenschaften

Die Gruppierung nach Vektoreigenschaften, Eigenschaften, die einen oder mehrere Werte gleichzeitig enthalten können, vergleicht die Vektorwerte standardmäßig einzeln. Wenn es z. B. ein Dokument gibt, Lorem.docx, mit der System.Author-Eigenschaft "Theresa; Zara" und ein weiteres Dokument, Ipsum.docx, mit der System.Author-Eigenschaft "Zara", gibt die Abfrage das Ergebnisset in zwei Gruppen zurück, wie hier gezeigt:


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| System.Author | System.FileName |
|---------------|-----------------|
| Theresa       | Lorem.docx      |
| Zara          | Lorem.docx      |
|               | Ipsum.docx      |



 

Wie Sie sehen können, gibt die Gruppierung nach Vektoreigenschaften doppelte Zeilen zurück. Lorem.docx wird zweimal angezeigt, da sie über zwei Autoren verfügt.

 

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

[ORDER BY-Klausel](-search-sql-orderby.md)
</dt> <dt>

[ORDER IN GROUP-Klausel](-search-sql-orderingroup.md)
</dt> </dl>

 

 
