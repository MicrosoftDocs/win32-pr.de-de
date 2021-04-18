---
title: Argument-Element
description: Das Argument-Element enthält einen Teil einer Bedingungs Zeichenfolge.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- Argument Element Windows Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c4adc0b853054d448bc9955f3bd8c64115ac2ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371187"
---
# <a name="argument-element"></a>Argument-Element

Das **Argument** -Element enthält einen Teil einer Bedingungs Zeichenfolge. Eine Bedingungs Zeichenfolge weist in der Regel einen Bedingungs Teil und einen Wertanteil auf. In der Bedingungs Zeichenfolge "Artist ist beispielsweise Joe" ist der Bedingungs Teil "ist" und der Wert Teil "Joe".

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a>Attribute

**Name** (erforderlich)

Der Name eines Teils der Bedingungs Zeichenfolge.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                         |
|-----------|----------------------------------|
| Parent    | [Bruch](fragment-element.md) |
| Untergeordnet     | Keine                             |



 

## <a name="remarks"></a>Bemerkungen

Wenn das **Name** -Attribut eines **Fragment** -Elements ein Medien Element Merkmal ist, z. b. ein Album-Maler oder Genre, muss das **Fragment** -Element zwei **Argument** Elemente enthalten: eines, das eine Bedingung angibt, und ein anderes, das einen Wert angibt. In der folgenden Tabelle werden zwei mögliche Werte für das **Name** -Attribut und die Verwendung von **Argument** Elementen zum Angeben von Bedingungen und Werten angezeigt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Der Inhalt des <strong>Argument</strong> -Elements ist der Bedingungs Teil einer Bedingungs Zeichenfolge. Beispielsweise ist im Bedingungs zeichenfolgenmaler " &quot; Joe" &quot; der Bedingungs &quot; Teil &quot; . Der Bedingungs Teil einer Bedingungs Zeichenfolge muss einer der folgenden sein: ist gleich, ist nicht gleich, enthält, enthält nicht, ist kleiner als, ist größer als, ist, ist nicht, ist vor, ist höher als, ist aktueller als, oberhalb, aufsteigend, aufsteigend, zufällig, ist mindestens, ist nicht größer als.</td>
</tr>
<tr class="even">
<td>Wert</td>
<td>Der Inhalt des <strong>Argument</strong> -Elements ist der Wertteil einer Bedingungs Zeichenfolge. Beispielsweise ist im Bedingungs zeichenfolgenmaler " &quot; Joe" &quot; der Wert Teil Joe &quot; &quot; . Beispiel<br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Wenn das Attribut " **Name** " eines **fragmentelements** "Gesamtgröße begrenzen auf" oder "gesamte Dauer begrenzen auf" festgelegt ist, muss das **Fragment** -Element zwei **Argument** Elemente enthalten: eine, die ein Format angibt, und eine, die eine Zahl angibt. In der folgenden Tabelle werden zwei mögliche Werte für das **Name** -Attribut und die Verwendung von **Argument** Elementen zum Begrenzen der Größe oder Dauer einer Wiedergabeliste angezeigt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributwert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Format</td>
<td>Wenn für das Attribut " <strong>Name</strong> " des <strong>fragmentelements</strong> die &quot; Gesamtgröße auf begrenzt ist &quot; , muss der Inhalt des <strong>Argument</strong> -Elements eines der folgenden sein: Kilobytes, Megabyte oder Gigabyte. Wenn für das <strong>Name</strong> -Attribut des <strong>Fragment</strong> -Elements die &quot; Gesamtdauer der Beschränkung auf begrenzt ist &quot; , muss der Inhalt des <strong>Argument</strong> -Elements eines der folgenden sein: Sekunden, Minuten, Stunden oder Tage.<br/></td>
</tr>
<tr class="even">
<td>Number</td>
<td>Der Inhalt des <strong>Argument</strong> -Elements ist eine Zahl, die die Größe oder Dauer der Wiedergabeliste einschränkt. Beispiele<br/>
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



 

Wenn das **Name** -Attribut eines **Fragment** -Elements "Limit number of Items" lautet, muss das **Fragment** -Element ein **Argument** Element enthalten, das die Anzahl der Elemente angibt. In der folgenden Tabelle wird gezeigt, wie Sie den Number-Wert des **Name** -Attributs verwenden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributwert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Number</td>
<td>Der Inhalt des <strong>Argument</strong> -Elements ist eine Zahl, die die Anzahl der Elemente in einer Wiedergabeliste einschränkt. Beispiel<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Fragment-Element**](fragment-element.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





