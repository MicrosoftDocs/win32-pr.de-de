---
description: Der Near-Begriff wird verwendet, um anzugeben, dass zwei Inhalts Suchbegriffe relativ nah beieinander liegen müssen, um als Übereinstimmung für das enthält-Prädikat erkannt zu werden.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: Near-Term
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4676ec8af80f674ca0b8124d8b4f941d0d6f4936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342958"
---
# <a name="near-term"></a>Near-Term

Der Near-Begriff wird verwendet, um anzugeben, dass zwei Inhalts Suchbegriffe relativ nah beieinander liegen müssen, um als Übereinstimmung für das [enthält](-search-sql-contains.md) -Prädikat erkannt zu werden.

Die Syntax für den NEAR-Begriff lautet wie folgt:


```
<content_search_term> NEAR | ~ <content_search_term>
```



Der Near-Begriff kann durch das Schlüsselwort "Near" oder durch eine Tilde (~) dargestellt werden.

Wenn die mit Near in der Abfrage verbundenen Wörter innerhalb der Spalte, die durchsucht wird, innerhalb von ungefähr 50 Wörtern zueinander gefunden werden, gibt der Near-Begriff eine Übereinstimmung zurück. Je näher die beiden Wörter sind, desto höher ist der berechnete Rang für den NEAR-Begriff. Je weiter auseinander die beiden Wörter liegen, desto niedriger ist der Rang.

> [!Note]  
> Die Anzahl von Wörtern zwischen gefundenen Suchbegriffen ist ungefähre Werte und hängt von der Darstellung von Füll Wörtern ab, wie z. b. "a" oder "The" und der Art und Weise, wie Wörter Trennungen Text mit Token versehen. Der Wert ist möglicherweise kleiner als 50.

 


In der folgenden Tabelle werden die Typen der Inhalts Suchbegriffe beschrieben, die mit einem NEAR-Begriff in einem enthält-Prädikat verwendet werden können.



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
<td>Ein einzelnes Wort ohne Leerzeichen oder ein anderes Interpunktions Zeichen. Doppelte Anführungszeichen sind nicht erforderlich.</td>
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
<td>Mehrere Wörter oder enthaltene Leerzeichen.</td>
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
<td>Wörter oder Ausdrücke mit dem Sternchen (*) am Ende hinzugefügt. Weitere Informationen finden Sie unter Verwenden von Platzhaltern <a href="-search-sql-wildcards.md">im enthält-Prädikat</a>.</td>
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
> Wenn die mit dem NEAR-Begriff angegebenen Übereinstimmungs Wörter in der Spalte gefunden werden, die durchsucht wird, die aber weiter auseinander liegen als 50 Wörter, wird das Ergebnis trotzdem zurückgegeben, aber hat den [Rang](-search-sql-understandingrelevancevalues.md) 0.

 

### <a name="example"></a>Beispiel

Im folgenden Beispiel wird die Verkettung von Near-Begriffen mithilfe der kurzen und langen Formen der Laufzeit veranschaulicht:


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Voll Text Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Verwenden von Platzhaltern im enthält-Prädikat](-search-sql-wildcards.md)
</dt> </dl>

 

 



