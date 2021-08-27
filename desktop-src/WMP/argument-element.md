---
title: argument-Element
description: Das Argumentelement enthält einen Teil einer Bedingungszeichenfolge.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- argument-Element Windows Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f5a689b74bd18138361d9377358ddee5cf5979f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630191"
---
# <a name="argument-element"></a>argument-Element

Das **Argumentelement** enthält einen Teil einer Bedingungszeichenfolge. Eine Bedingungszeichenfolge verfügt in der Regel über einen Bedingungsteil und einen Wertteil. In der Bedingungszeichenfolge "Interpret Equals Joe" lautet der Bedingungsteil beispielsweise "Equals" und der Wertteil "Joe".

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

Wenn  das Namensattribut eines **Fragmentelements** ein Medienelementmerkmal wie AlbumArtist oder Genre ist, muss das **Fragmentelement** zwei **Argumentelemente** enthalten: eines, das eine Bedingung angibt, und ein anderes, das einen Wert angibt. Die folgende Tabelle zeigt zwei mögliche Werte für das **name-Attribut** und die Verwendung von **Argumentelementen** zum Angeben von Bedingungen und Werten.



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
<td>Der Inhalt des <strong>Argumentelements</strong> ist der Bedingungsteil einer Bedingungszeichenfolge. In der &quot; Bedingungszeichenfolge Interpret Equals Joe lautet der Bedingungsteil z. &quot; &quot; B. Gleich &quot; . Der Bedingungsteil einer Bedingungszeichenfolge muss einer der folgenden Sein: Equals, Does Not Equal, Contains, Does Not Contain, is Less Than, Is Greater Than, Is, Is, Is Before, Is Later Than, Is More Recent Than, Above, Below, Ascending, Descending, Random, Is Least, Is No More Than.</td>
</tr>
<tr class="even">
<td>Wert</td>
<td>Der Inhalt des <strong>Argumentelements</strong> ist der Wertteil einer Bedingungszeichenfolge. In der &quot; Bedingungszeichenfolge Interpret Equals Joe lautet der Wertteil beispielsweise &quot; Joe &quot; &quot; . Beispiel:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Wenn  das Namensattribut eines **Fragmentelements** "Limit Total Size To" oder "Limit Total Duration To" ist, muss das **Fragmentelement** zwei **Argumentelemente** enthalten: eines, das ein Format angibt, und eines, das eine Zahl angibt. Die folgende Tabelle zeigt zwei mögliche Werte für das **Name-Attribut** und wie **Argumentelemente** verwendet werden, um die Größe oder Dauer einer Wiedergabeliste zu begrenzen.



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
<td>Wenn das <strong>Name-Attribut</strong> des <strong>Fragmentelements</strong> &quot; Limit Total Size To &quot; ist, muss der Inhalt des <strong>Argumentelements</strong> eines der folgenden sein: Kilobytes, Megabytes oder Gigabytes. Wenn das <strong>Name-Attribut</strong> des <strong>Fragmentelements</strong> Limit Total Duration &quot; To &quot; ist, muss der Inhalt des <strong>Argumentelements</strong> einer der folgenden sein: Seconds, Minutes, Hours oder Days.<br/></td>
</tr>
<tr class="even">
<td>Number</td>
<td>Der Inhalt des <strong>Argumentelements</strong> ist eine Zahl, die die Größe oder Dauer der Wiedergabeliste einschränkt. Beispiele:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Wenn  das Namensattribut eines **Fragmentelements** "Limit Number of Items" ist, muss das **Fragmentelement** ein **Argumentelement** enthalten, das die Anzahl der Elemente angibt. Die folgende Tabelle zeigt, wie Sie  den Number-Wert des Name-Attributs verwenden.



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
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**fragment-Element**](fragment-element.md)
</dt> <dt>

[**Windows Referenz zu Medienwiedergabelistenelementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





