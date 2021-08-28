---
description: Der NEAR-Begriff wird verwendet, um anzugeben, dass zwei Inhaltssuchbegriffe relativ nah beieinander liegen müssen, um als Übereinstimmung für das CONTAINS-Prädikat erkannt zu werden.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: NEAR Term
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad155d49638c33d3bc22c03ae8ce13e44c21478a3efabe987d4164081f8faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094881"
---
# <a name="near-term"></a>NEAR Term

Der NEAR-Begriff wird verwendet, um anzugeben, dass zwei Inhaltssuchbegriffe relativ nah beieinander liegen müssen, um als Übereinstimmung für das [CONTAINS-Prädikat](-search-sql-contains.md) erkannt zu werden.

Die Syntax für den NEAR-Begriff lautet:


```
<content_search_term> NEAR | ~ <content_search_term>
```



Der NEAR-Begriff kann durch das Schlüsselwort "NEAR" oder durch eine Tilde (~) dargestellt werden.

Wenn die wörter, die mit NEAR in der Abfrage verknüpft sind, innerhalb von ca. 50 Wörtern voneinander innerhalb der spalte gefunden werden, die durchsucht wird, gibt der NEAR-Begriff eine Übereinstimmung zurück. Je näher die beiden Wörter liegen, desto höher ist der berechnete Rang für den NEAR-Begriff. Je weiter die beiden Wörter voneinander entfernt sind, desto niedriger ist der Rang.

> [!Note]  
> Die Anzahl der Wörter zwischen gefundenen Suchbegriffen ist ungefähr und hängt von der Darstellung von Füllwörtern wie "a" oder "the" ab und davon, wie Wordbreaker Text tokenisieren. Er kann kleiner als 50 sein.

 


In der folgenden Tabelle werden Inhaltssuchbegriffstypen beschrieben, die mit einem NEAR-Begriff in einem CONTAINS-Prädikat verwendet werden können.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>type</th>
<th>BESCHREIBUNG</th>
<th>Beispiele</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Word</td>
<td>Ein einzelnes Wort ohne Leerzeichen oder andere Interpunktion. Doppelte Anführungszeichen sind nicht erforderlich.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;computer NEAR software)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Ausdruck</td>
<td>Mehrere Wörter oder eingeschlossene Leerzeichen.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;computer software&quot; NEAR hardware)&#39;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Platzhalter</td>
<td>Wörter oder Ausdrücke mit dem Sternchen (*) werden am Ende hinzugefügt. Weitere Informationen finden Sie unter <a href="-search-sql-wildcards.md">Verwenden von Platzhaltern im CONTAINS-Prädikat</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;compu*&quot; NEAR &quot;soft*&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>

> [!Note]  
> Wenn die mit dem NEAR-Begriff angegebenen Übereinstimmungswörter beide in der zu durchsuchenden Spalte gefunden werden, aber weiter entfernt als 50 Wörter liegen, wird das Ergebnis weiterhin zurückgegeben, hat aber den [Rang](-search-sql-understandingrelevancevalues.md) 0.

 

### <a name="example"></a>Beispiel

Das folgende Beispiel zeigt die Verkettung von NEAR-Begriffen, wobei sowohl die kurz- als auch die lange Form des Begriffs verwendet wird:


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Volltextprädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Verwenden von Platzhaltern im CONTAINS-Prädikat](-search-sql-wildcards.md)
</dt> </dl>

 

 



