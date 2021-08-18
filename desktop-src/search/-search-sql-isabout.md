---
description: Der ISABOUT-Begriff gleicht Spalten mit einer Gruppe von einem oder mehreren Suchbegriffen ab.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: ISABOUT-Begriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5665e7bf62da4858cf2e7d68e65d0f42771903d55e3189db12f19cdd5414530d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969609"
---
# <a name="isabout-term"></a>ISABOUT-Begriff

**Veraltet**

Dieses Feature wurde ab Windows 8 entfernt. Wenn Sie neue Anwendungen schreiben, vermeiden Sie die Verwendung dieser veralteten Funktion. Wenn Sie vorhandene Anwendungen ändern, wird dringend empfohlen, alle Abhängigkeiten von diesem Feature zu entfernen.

Der ISABOUT-Begriff gleicht Spalten mit einer Gruppe von einem oder mehreren Suchbegriffen ab. Sie weist die folgende Syntax auf:


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



Der optionale RANKMETHOD-Begriff gibt die Berechnungsmethode an, die zum Bewerten der Dokumente verwendet wird, die einer oder mehreren Komponenten entsprechen. Wenn keine RANKMETHOD angegeben ist, wird die standardmäßige Csv-Koeffizient-Rangfolgemethode verwendet.

Der ISABOUT-Begriff kann eine oder mehrere Komponenten enthalten. Die im [CONTAINS-Prädikat](-search-sql-contains.md) angegebenen Spalten werden für jede Komponente getestet. Das Dokument ist in den Ergebnissen enthalten, wenn mindestens eine der Komponenten übereinstimmt. Kommas trennen mehrere Komponenten.

Der Komponententeil weist die folgende Syntax auf:


```
<match_term> [<weight_term>]
```



Sie können den optionalen WEIGHT-Begriff verwenden, um die relative Wichtigkeit jedes Begriffs innerhalb des ISABOUT-Begriffs zu ändern. Wenn kein Gewichtungsbegriff angewendet wird, wird die Standardgewichtung 1,0 impliziert.

In der folgenden Tabelle werden mögliche Übereinstimmungsbegriffstypen beschrieben.



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
<td>Ein einzelnes Wort ohne Leerzeichen oder andere Interpunktion.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer&quot;,&quot;software&quot;)&#39;)</code></pre></td>
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
 (&#39;ISABOUT (&quot;computer software&quot;,&quot;hardware&quot;)&#39;)</code></pre></td>
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
 (&#39;ISABOUT (&quot;compu*&quot;,&quot;soft*&quot;)&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;, &quot;computation&quot;, 
and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="isabout-column-weighting"></a>ISABOUT-Spaltengewichtung

Der ISABOUT-Begriff bewertet übereinstimmende Dokumente basierend darauf, wie genau jedes Dokument mit dem Satz von Übereinstimmungsbegriffen in der Abfrage übereinstimmt. Sie können die Spaltengewichtung verwenden, um die Übereinstimmung einiger Übereinstimmungsbegriffe wichtiger zu machen als andere. Auf jeden Übereinstimmungsbegriff im ISABOUT-Begriff kann ein Gewichtungswert angewendet werden. Die Gewichtung wird auf einen einzelnen Übereinstimmungsbegriff angewendet und durch das Schlüsselwort "WEIGHT" angegeben. Der WEIGHT-Begriff verfügt über zwei alternative Syntaxen:


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



Der Gewichtungswert muss zwischen 0 und 1,0 und nicht mehr als drei Dezimalstellen sein. Das Angeben eines Gewichtungswerts außerhalb dieses Bereichs führt zu einer Fehlermeldung. Der nicht gewichtete Rangfolgewert für einen Begriff wird mit dem Gewichtungswert für den Begriff multipliziert.

Wenn für einen Übereinstimmungsbegriff keine Gewichtung angegeben ist, wird der Standardwert 1,0 impliziert.

### <a name="example"></a>Beispiel

Im folgenden Beispiel werden Gewichtungen auf die beiden ISABOUT-Übereinstimmungsbegriffe angewendet, wobei sowohl die lange als auch die kurze Syntax für Gewichtungswerte verwendet werden.


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[FREETEXT-Prädikat](-search-sql-freetext.md)
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> </dl>

 

 



