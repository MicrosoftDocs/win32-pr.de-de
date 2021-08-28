---
title: argument-Element
description: Das Argumentelement enthält einen Teil einer Bedingungszeichenfolge.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- argument-Windows Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29b0c234d2410d512e2f034f92cbc4a2d6ad7449
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880269"
---
# <a name="argument-element"></a>argument-Element

Das **Argumentelement** enthält einen Teil einer Bedingungszeichenfolge. Eine Bedingungszeichenfolge verfügt in der Regel über einen Bedingungsteil und einen Wertteil. Beispielsweise ist in der Bedingungszeichenfolge "Interpret Equals Joe" der Bedingungsteil "Equals" und der Wertteil "Joe".

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a>Attribute

**name** (erforderlich)

Der Name eines Teils der Bedingungszeichenfolge.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy | Elemente                         |
|-----------|----------------------------------|
| Parent    | [Fragment](fragment-element.md) |
| Untergeordnet     | Keine                             |



 

## <a name="remarks"></a>Bemerkungen

Wenn das **Name-Attribut** eines Fragmentelements ein Medienelement-Merkmal wie  Album Interpret  oder Genre ist, muss das Fragmentelement zwei Argumentelemente enthalten: eines, das eine Bedingung angibt, und ein anderes, das einen Wert angibt.  Die folgende Tabelle zeigt zwei mögliche Werte für das **Name-Attribut** und **wie** Argumentelemente verwendet werden, um Bedingungen und Werte anzugeben.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attributwert</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bedingung</td>
<td>Der Inhalt des <strong>Argumentelements</strong> ist der Bedingungsteil einer Bedingungszeichenfolge. In der Bedingungszeichenfolge &quot; "Interpret Equals Joe" &quot; ist der Bedingungsteil beispielsweise Gleich &quot; &quot; . Der Bedingungsteil einer Bedingungszeichenfolge muss einer der folgenden sein: Equals, Does Not Equal, Contains, Does Not Contain, Is Less Than, Is Greater Than, Is, Is Not, Is Before, Is Later Than, Is More Recent Than, Above, Below, Ascending, Descending, Random, Is At Least, Is No More Than.</td>
</tr>
<tr class="even">
<td>Wert</td>
<td>Der Inhalt des <strong>Argumentelements</strong> ist der Wertteil einer Bedingungszeichenfolge. In der Bedingungszeichenfolge &quot; "Interpret Equals Joe" &quot; ist der Wertteil beispielsweise Joe &quot; &quot; . Beispiel:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals&lt;/argument&gt;
  <argument name = &quot;Value&quot;>Joe&lt;/argument&gt;
&lt;/fragment&gt;</code></pre></td>
</tr>
</tbody>
</table>



 

Wenn das **Name-Attribut** eines Fragmentelements "Limit Total Size To"  oder "Limit  Total Duration To" lautet, muss das Fragmentelement zwei Argumentelemente enthalten: ein Element, das ein Format angibt, und eins, das eine Zahl angibt.  Die folgende Tabelle zeigt zwei mögliche Werte  für das **Name-Attribut** und wie Argumentelemente verwendet werden, um die Größe oder Dauer einer Wiedergabeliste zu begrenzen.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attributwert</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Format</td>
<td>Wenn <strong></strong> das Name-Attribut des Fragmentelements Limit Total Size To lautet, muss der Inhalt des Argumentelements einer der folgenden <strong></strong> &quot; &quot; sein: <strong></strong> Kilobytes, Megabytes oder Gigabytes. <strong></strong> <strong></strong> Wenn das Name-Attribut des Fragmentelements Limit Total Duration To ist, muss der Inhalt des Argumentelements einer der folgenden &quot; &quot; sein: Sekunden, Minuten, Stunden oder Tage. <strong></strong><br/></td>
</tr>
<tr class="even">
<td>Number</td>
<td>Der Inhalt des <strong>Argumentelements</strong> ist eine Zahl, die die Größe oder Dauer der Wiedergabeliste einschränkt. Beispiele:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes&lt;/argument&gt;
  <argument name = &quot;Number&quot;>5&lt;/argument&gt;
&lt;/fragment&gt;

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes&lt;/argument&gt;
  <argument name = &quot;Number&quot;>20&lt;/argument&gt;
&lt;/fragment&gt;</code></pre></td>
</tr>
</tbody>
</table>



 

Wenn das **Name-Attribut** eines  **Fragmentelements** "Limit Number of Items" ist, muss das **Fragmentelement** ein Argumentelement enthalten, das die Anzahl der Elemente angibt. In der folgenden Tabelle wird die Verwendung des Number-Werts des **Namensattributs** veranschaulicht.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attributwert</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Number</td>
<td>Der Inhalt des <strong>Argumentelements</strong> ist eine Zahl, die die Anzahl der Elemente in einer Wiedergabeliste einschränkt. Beispiel:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15&lt;/argument&gt;
&lt;/fragment&gt;</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**fragment-Element**](fragment-element.md)
</dt> <dt>

[**Windows Referenz zu Medienwiedergabelistenelementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





