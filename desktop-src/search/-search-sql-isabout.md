---
description: Der ISABOUT-Begriff vergleicht Spalten mit einer Gruppe von mindestens einem Suchbegriff.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: ISABOUT-Begriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f79fc2fa4a56b3ca6b3b412141f096b282e3aa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750384"
---
# <a name="isabout-term"></a>ISABOUT-Begriff

**Veraltet**

Diese Funktion wurde ab Windows 8 entfernt. Wenn Sie neue Anwendungen schreiben, sollten Sie diese veraltete Funktion nicht verwenden. Wenn Sie vorhandene Anwendungen ändern, wird dringend empfohlen, jegliche Abhängigkeit von dieser Funktion zu entfernen.

Der ISABOUT-Begriff vergleicht Spalten mit einer Gruppe von mindestens einem Suchbegriff. Es weist die folgende Syntax auf:


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



Der optionale RankMethod-Begriff gibt die Berechnungsmethode an, mit der die mit einer oder mehreren Komponenten abgeglichen Dokumente eingestuft werden. Wenn keine RankMethod angegeben ist, wird die standardmäßige Jaccard-Koeffizienten-Rang Folge Methode verwendet.

Der ISABOUT-Begriff kann über eine oder mehrere Komponenten verfügen. Die im-Prädikat [enthalten](-search-sql-contains.md) angegebenen Spalten werden für jede Komponente getestet. Das Dokument ist in den Ergebnissen enthalten, wenn mindestens eine der Komponenten übereinstimmt. Kommas trennen mehrere Komponenten.

Der Komponenten Teil weist die folgende Syntax auf:


```
<match_term> [<weight_term>]
```



Sie können den optionalen Gewichtungs Begriff verwenden, um die relative Wichtigkeit der einzelnen Begriffe innerhalb des ISABOUT-Begriffs zu ändern. Wenn kein Gewichtungs Begriff angewendet wird, wird die Standard Gewichtung 1,0 impliziert.

In der folgenden Tabelle werden mögliche Übereinstimmungs Typen beschrieben.



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
<td>Ein einzelnes Wort ohne Leerzeichen oder ein anderes Interpunktions Zeichen.</td>
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
 (&#39;ISABOUT (&quot;computer software&quot;,&quot;hardware&quot;)&#39;)</code></pre></td>
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



 

## <a name="isabout-column-weighting"></a>ISABOUT-Spalten Gewichtung

Der ISABOUT-Begriff ordnet den übereinstimmenden Dokumenten zu, je nachdem, wie genau jedes Dokument mit den übereinstimmenden Begriffen in der Abfrage übereinstimmt. Mit der Spalten Gewichtung können Sie eine größere Wichtigkeit beim Vergleichen einiger Vergleichs Begriffe als andere verwenden. Für jeden Vergleichs Begriff im ISABOUT-Begriff kann ein Gewichtungswert angewendet werden. Die Gewichtung wird auf einen einzelnen Übereinstimmungs Begriff angewendet und wird durch das Schlüsselwort "Weight" angegeben. Der Gewichtungs Begriff verfügt über zwei alternative Syntaxen:


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



Der Gewichtungswert muss zwischen 0 und 1,0 liegen und darf nicht mehr als drei Dezimalstellen aufweisen. Wenn ein Gewichtungswert außerhalb dieses Bereichs angegeben wird, führt dies zu einer Fehlermeldung. Der nicht gewichtete Rang Folge Wert für einen Begriff wird mit dem Gewichtungswert für den Begriff multipliziert.

Wenn für einen Übereinstimmungs Begriff keine Gewichtung angegeben wird, wird der Standardwert 1,0 impliziert.

### <a name="example"></a>Beispiel

Im folgenden Beispiel werden Gewichtungen auf die zwei ISABOUT-Übereinstimmungs Bedingungen angewendet, wobei die Long-und Short-Syntax für Gewichtungswerte verwendet wird.


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Frei Text Prädikat](-search-sql-freetext.md)
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> </dl>

 

 



