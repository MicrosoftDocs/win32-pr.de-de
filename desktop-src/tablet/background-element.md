---
description: Enthält den Hintergrund für ein journaldocument-Element oder journalpage-Element.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Background-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58a836c7cfd13130779c1cd6b017105bcaa6321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368905"
---
# <a name="background-element"></a>Background-Element

Enthält den Hintergrund für ein [**journaldocument**](journaldocument-element.md) -Element oder [**journalpage**](journalpage-element.md) -Element.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Schreib**](stationery-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**Image**](image-element.md)

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
<td>Gibt die Art des Hintergrunds an.</td>
<td><ul>
<li>Keine</li>
<li>Basis</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Farbe</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</td>
<td>Optional</td>
<td>Gibt die Hintergrundfarbe an.</td>
<td>Siehe <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Elementinformationen



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| Elementtyp | ComplexType für [**BackgroundType**](backgroundtype-complex-type.md) |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk                        |
| Schemaname  | Journal Leser                                                    |



 

 

 



