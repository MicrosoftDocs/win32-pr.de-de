---
description: Enthält Titelinformationen über die Journal Notiz.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Title-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351558"
---
# <a name="title-element"></a>Title-Element

Enthält Titelinformationen über die Journal Notiz.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Schreib**](stationery-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**TitleArea**](titlearea-element.md)

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
<th>Mögliche Werte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Stil</strong></td>
<td><strong>xs:string</strong></td>
<td>Erforderlich</td>
<td>Gibt den Typ des Rahmens an, der den Titel des Notiz Rahmens umgibt.</td>
<td><ul>
<li>Keine</li>
<li>Solidsquare</li>
<li>Outlinesquare</li>
<li>"Solidroundrecrect"</li>
<li>Outlineroundrect</li>
<li>"Solidroundrectdottedbaseline"</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>DateStyle</strong></td>
<td><strong>xs:string</strong></td>
<td>Erforderlich</td>
<td>Definiert, ob der Titel ein Datum enthält.</td>
<td><ul>
<li>Keine</li>
<li>Short</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Farbe</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></td>
<td>Optional</td>
<td>Gibt die Hintergrundfarbe an.</td>
<td>Siehe <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Elementinformationen



|              |                                                         |
|--------------|---------------------------------------------------------|
| Elementtyp | ComplexType für [**titletype**](titletype-complex-type.md) |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk              |
| Schemaname  | Journal Leser                                          |



 

 

 



