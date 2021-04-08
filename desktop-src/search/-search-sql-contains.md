---
description: Das enthält-Prädikat ist Teil der WHERE-Klausel und unterstützt das Suchen nach Wörtern und Ausdrücken in Textspalten.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: Enthält Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908f4c67d5c1d5bcf00c60bd8cb271928682a907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862155"
---
# <a name="contains-predicate"></a>Enthält Prädikat

Das enthält-Prädikat ist Teil der WHERE-Klausel und unterstützt das Suchen nach Wörtern und Ausdrücken in Textspalten. Das enthält ein Prädikat, das über Features für übereinstimmende Wörter, die Übereinstimmung von Flexions Formen von Wörtern, das Suchen mithilfe von Platzhalter Zeichen und die Suche mithilfe von Near verfügt Sie können auch Gewichtungen in einem enthält-Prädikat anwenden, um die Wichtigkeit der Spalten festzulegen, in denen der Suchbegriff gefunden wurde. Das enthält-Prädikat eignet sich besser für exakte Übereinstimmungen (im Gegensatz zum frei [Text](-search-sql-freetext.md) Prädikat), das sich besser für die Suche nach Dokumenten eignet, die Kombinationen der in der Spalte verteilten Suchwörter enthalten. Bei Suchvorgängen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Im folgenden finden Sie die grundlegende Syntax des enthält-Prädikats:

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

Der voll Text \_ Spalten Verweis ist optional. Damit können Sie die Suche auf eine einzelne Spalte oder eine Spalten Gruppe beschränken, für die das Prädikat "enthält" getestet wird. Wenn die voll Text Spalte als "All" oder "" angegeben wird \* , werden alle indizierten Texteigenschaften durchsucht. Obwohl es sich bei der Spalte nicht um eine Text Eigenschaft handeln muss, können die Ergebnisse bedeutungslos sein, wenn es sich bei der Spalte um einen anderen Datentyp handelt. Der Spaltenname kann entweder ein regulärer oder ein Begrenzungs [Bezeichner](-search-sql-identifiers.md)sein, und Sie müssen ihn durch ein Komma von der Bedingung trennen. Wenn keine voll Text Spalte angegeben ist, wird die Spalte "System. search. Content" verwendet, die den Hauptteil des Dokuments enthält.

Der LCID-Teil des Prädikats gibt das Suchgebiets Schema an. Dies weist das Such Modul an, die entsprechende Wörter Trennung und die Flexions Formen für die Suchabfrage zu verwenden. Um das Gebiets Schema anzugeben, geben Sie den Windows-Standard Sprachcode Bezeichner (LCID) an. Beispielsweise ist 1033 die LCID für USA-Englisch. Platzieren Sie die LCID als letztes Element innerhalb der Klammern der enthaltene Klausel. Wichtige Informationen zum Suchen von und Sprachen finden [Sie unter Verwenden lokalisierter Such](-search-sql-usinglocsearches.md)Vorgänge.

> [!NOTE]  
> Das Standard Gebiets Schema für die Suche ist das Standard Gebiets Schema des Systems.

Der enthält Bedingungs \_ Teil muss in einfache Anführungszeichen eingeschlossen werden, um einzelne Wörter oder doppelte Anführungszeichen für Ausdrücke zu verwenden, und besteht aus einem oder mehreren Inhalts Suchbegriffen, die mithilfe der logischen Operatoren **and** oder **or** kombiniert werden. Sie können den optionalen unären Operator **nicht** hinter einem **and-** Operator verwenden, um den logischen Wert eines Inhalts Suchbegriffs zu negieren.

> [!NOTE]  
> Der **Not** -Operator kann nur nach **und** auftreten. Der **Not** -Operator kann nicht verwendet werden, wenn es nur eine Übereinstimmungs Bedingung gibt oder nach dem **or** -Operator.

Mit Klammern können Sie Inhalts Suchbegriffe gruppieren und Schachteln. In der folgenden Tabelle wird die Rangfolge der logischen Operatoren beschrieben.

| Reihenfolge (Rangfolge) | Logischer Operator |
|--------------------|------------------|
| First (höchste)    | **NOT**          |
| Sekunde             | **AND**          |
| Dritte (niedrigste)     | **OR**           |

Logische Operatoren desselben Typs sind assoziativ, und es ist keine Berechnungs Reihenfolge angegeben. Beispielsweise können (a **und** B) **und** (c **und** d) (b **und** c) **und** (A **und** d) ohne Änderung im logischen Ergebnis berechnet werden.

In der folgenden Tabelle werden die Typen der Inhalts Suchbegriffe beschrieben.

<!-- markdownlint-disable MD033 -->
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
<td><pre><code>...WHERE CONTAINS (&#39;computer&#39;)</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer software&quot;&#39;)

Or, to use a double quote mark:

... WHERE CONTAINS
(&#39;&quot;computer &quot;&quot;science&quot;&quot; &quot;&#39;)</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;compu*&quot;&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;,
&quot;computation&quot;, and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>Voll Text Spalte</td>
<td>Der Name einer Eigenschaften Spalte, mit der die verbleibende Abfrage abgeglichen werden soll.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (System.Author,&#39;&quot;James&quot; OR &quot;Juan&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Boolean</td>
<td>Wörter, Ausdrücke und Platzhalter Zeichenfolgen in Kombination mit den booleschen Operatoren <strong>and</strong>, <strong>or</strong>oder <strong>Not</strong>. Schließen Sie die booleschen Begriffe in doppelte Anführungszeichen ein.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer monitor&quot; AND
  &quot;software program&quot; AND
  &quot;install component&quot;&#39;)

...WHERE CONTAINS
 (&#39; &quot;computer&quot; AND
  &quot;software&quot; AND
  &quot;install&quot; &#39; )

...WHERE CONTAINS
(&#39;&quot;computer software install&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>Near</td>
<td>Wörter, Ausdrücke oder Platzhalter, getrennt durch die-Funktion in der Nähe von. Weitere Informationen finden Sie unter <a href="-search-sql-near.md">near Term</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer&quot; NEAR &quot;software&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>FormsOf</td>
<td>Entspricht einem Wort und den Flexions Versionen dieses Worts. Weitere Informationen finden Sie unter <a href="-search-sql-formsof.md">FORMSOF Term</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;FORMSOF
 (INFLECTIONAL, &quot;happy&quot;))

Matches &quot;happy&quot;, &quot;happier&quot;,
&quot;happiest&quot;, &quot;happily&quot;, and so on.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>IsAbout</td>
<td>Kombiniert übereinstimmende Ergebnisse über mehrere Wort-, Ausdrucks-oder Platzhalter Suchbegriffe. Jeder Suchbegriff kann optional gewichtet werden. Optional können Sie die Rang Berechnungsmethode angeben, mit der Gewichtungen und die Anzahl der Elemente kombiniert werden, mit denen das Dokument übereinstimmt. Weitere Informationen finden Sie unter <a href="-search-sql-isabout.md">ISABOUT Term</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;ISABOUT ( &quot;computer&quot; WEIGHT (0.75) ,
    &quot;software&quot; WEIGHT (0.25) ,
    &quot;development&quot; WEIGHT (0.255)
 ) RANKMETHOD INNER PRODUCT
&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

Dieser Abschnitt schließt folgende Themen ein:

- [Verwenden von Platzhaltern im enthält-Prädikat](-search-sql-wildcards.md)
- [FORMSOF-Begriff](-search-sql-formsof.md)
- [ISABOUT-Begriff](-search-sql-isabout.md)
- [Near-Term](-search-sql-near.md)

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Referenz

[WHERE-Klausel](-search-sql-where.md)

### <a name="conceptual"></a>Konzept

[Voll Text Prädikate](-search-sql-fulltextpredicates.md)

[Nicht-voll Text Prädikate](-search-sql-nonfulltextpredicates.md)
