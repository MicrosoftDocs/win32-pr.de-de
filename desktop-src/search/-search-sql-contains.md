---
description: Das CONTAINS-Prädikat ist Teil der WHERE-Klausel und unterstützt die Suche nach Wörtern und Ausdrücken in Textspalten.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: CONTAINS-Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c821431bb5f00319fe47414dcce5240775f2ce78335998c1bb30b84dc9fe17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863713"
---
# <a name="contains-predicate"></a>CONTAINS-Prädikat

Das CONTAINS-Prädikat ist Teil der WHERE-Klausel und unterstützt die Suche nach Wörtern und Ausdrücken in Textspalten. Das CONTAINS-Prädikat verfügt über Funktionen zum Abgleichen von Wörtern, zum Abgleichen von Flexionsformen von Wörtern, zum Suchen mit Platzhalterzeichen und zum Suchen mithilfe von Näherung. Sie können auch Gewichtungen in einem CONTAINS-Prädikat anwenden, um die Wichtigkeit der Spalten festzulegen, in denen der Suchbegriff gefunden wird. Das CONTAINS-Prädikat eignet sich besser für genaue Übereinstimmungen im Gegensatz zum [FREETEXT-Prädikat,](-search-sql-freetext.md) das besser zum Suchen von Dokumenten geeignet ist, die Kombinationen der in der Spalte verteilten Suchbegriffe enthalten. Bei Suchvorgängen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Im Folgenden finden Sie die grundlegende Syntax des CONTAINS-Prädikats:

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

Der \_ Volltextspaltenverweis ist optional. Damit können Sie die Suche auf eine einzelne Spalte oder eine Spaltengruppe beschränken, für die das CONTAINS-Prädikat getestet wird. Wenn die Volltextspalte als "ALL" oder "" angegeben \* wird, werden alle indizierten Texteigenschaften durchsucht. Obwohl die Spalte keine Texteigenschaft sein muss, sind die Ergebnisse möglicherweise bedeutungslos, wenn die Spalte ein anderer Datentyp ist. Der Spaltenname kann entweder ein regulärer oder ein durch Trennzeichen getrennter [Bezeichner](-search-sql-identifiers.md)sein, und Sie müssen ihn durch ein Komma von der Bedingung trennen. Wenn keine Volltextspalte angegeben wird, wird die Spalte System.Search.Contents verwendet, die den Text des Dokuments darstellt.

Der LCID-Teil des Prädikats gibt das Suchschema an. Dadurch wird die Suchmaschine angewiesen, die entsprechende Wörterpause und die entsprechenden Flexionsformen für die Suchabfrage zu verwenden. Um das Gebietsschema anzugeben, geben Sie den Windows LCID (Standard Language Code Identifier) an. Beispielsweise ist 1033 die LCID für USA-Englisch. Platzieren Sie die LCID als letztes Element in den Klammern der CONTAINS-Klausel. Wichtige Informationen zu Suchen und Sprachen finden Sie unter [Verwenden von lokalisierten Suchvorgängen.](-search-sql-usinglocsearches.md)

> [!NOTE]  
> Das Standardsuchschema ist das Standardschema des Systems.

Der \_ Contains-Bedingungsteil muss in einfache Anführungszeichen für einzelne Wörter oder doppelte Anführungszeichen für Ausdrücke eingeschlossen werden und besteht aus einem oder mehreren Inhaltssuchbegriffen, die mit den logischen Operatoren **AND** oder **OR** kombiniert werden. Sie können den optionalen unären Operator **NOT** nach einem **AND-Operator** verwenden, um den logischen Wert eines Inhaltssuchbegriffs zu negieren.

> [!NOTE]  
> Der **NOT-Operator** kann nur nach **AND** auftreten. Sie können den **NOT-Operator** nicht verwenden, wenn nur eine Übereinstimmungsbedingung vorhanden ist, oder nach dem **OR-Operator.**

Sie können Klammern verwenden, um Suchbegriffe für Inhalte zu gruppieren und zu schachteln. In der folgenden Tabelle wird die Rangfolge für die logischen Operatoren beschrieben.

| Reihenfolge (Rangfolge) | Logischer Operator |
|--------------------|------------------|
| Erste (höchste)    | **NOT**          |
| Second             | **AND**          |
| Dritte (niedrigste)     | **OR**           |

Logische Operatoren desselben Typs sind assoziativ, und es gibt keine angegebene Berechnungsreihenfolge. Beispielsweise können (A **UND** B) **AND** (C **UND** D) (B **UND** C) **UND** (A **UND** D) ohne Änderung des logischen Ergebnisses berechnet werden.

In der folgenden Tabelle werden die Typen von Inhaltssuchbegriffen beschrieben.

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Typ</th>
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
<td><pre><code>...WHERE CONTAINS (&#39;computer&#39;)</code></pre></td>
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
<td>Wörter oder Ausdrücke mit dem Sternchen (*) werden am Ende hinzugefügt. Weitere Informationen finden Sie unter <a href="-search-sql-wildcards.md">Verwenden von Platzhaltern im CONTAINS-Prädikat</a>.</td>
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
<td>Volltextspalte</td>
<td>Ein Eigenschaftenspaltenname, mit dem die verbleibende Abfrage übereinstimmt.</td>
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
<td>Boolesch</td>
<td>Wörter, Ausdrücke und Platzhalterzeichenfolgen, kombiniert mit den booleschen Operatoren <strong>AND,</strong> <strong>OR</strong>oder <strong>NOT.</strong> Schließen Sie die booleschen Begriffe in doppelte Anführungszeichen ein.</td>
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
<td>Wörter, Ausdrücke oder Platzhalter, die durch die Near-Funktion getrennt sind. Weitere Informationen finden Sie unter <a href="-search-sql-near.md">NEAR Term</a>.</td>
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
<td>Entspricht einem Wort und den Flexionsversionen dieses Worts. Weitere Informationen finden Sie unter <a href="-search-sql-formsof.md">FORMSOF-Begriff</a>.</td>
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
<td>Kombiniert übereinstimmende Ergebnisse über mehrere Wort-, Ausdrucks- oder Platzhaltersuchbegriffe. Jeder Suchbegriff kann optional gewichtet werden. Sie können optional die Rangfolgeberechnungsmethode angeben, die die Gewichtungen und die Anzahl der Elemente kombiniert, mit denen das Dokument übereinstimmt. Weitere Informationen finden Sie unter <a href="-search-sql-isabout.md">ISABOUT-Begriff.</a></td>
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

- [Verwenden von Platzhaltern im CONTAINS-Prädikat](-search-sql-wildcards.md)
- [FORMSOF-Begriff](-search-sql-formsof.md)
- [ISABOUT-Begriff](-search-sql-isabout.md)
- [NEAR Term](-search-sql-near.md)

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Verweis

[WHERE-Klausel](-search-sql-where.md)

### <a name="conceptual"></a>Konzept

[Volltextprädikate](-search-sql-fulltextpredicates.md)

[Nicht-Volltextprädikate](-search-sql-nonfulltextpredicates.md)
