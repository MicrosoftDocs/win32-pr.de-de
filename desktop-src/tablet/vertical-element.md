---
description: Enthält die Informationen, die die vertikale Komponente der Zeilen in der von der Journal Notiz verwendeten Schreibweise beschreiben. Wird beispielsweise verwendet, wenn der Hinweis Rasterlinien enthält.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Vertikales Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191a9c5cb3190cff9b1e379a68dbfab49ddc25a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343269"
---
# <a name="vertical-element"></a>Vertikales Element

Enthält die Informationen, die die vertikale Komponente der Zeilen in der von der Journal Notiz verwendeten Schreibweise beschreiben. Wird beispielsweise verwendet, wenn der Hinweis Rasterlinien enthält.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Linelayout**](linelayout-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

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
<td><a href="linelayoutstyletype-simple-type.md"><strong>Linelayoutstyletype</strong></a> simpleType</td>
<td>Erforderlich</td>
<td>Gibt den Typ der zu Zeichenden Zeile an.</td>
<td><ul>
<li>Keine</li>
<li>Basis</li>
<li>Strich</li>
<li>Punkt</li>
<li>DashDot</li>
<li>DashDotDot</li>
<li>Double</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Farbe</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</td>
<td>Optional</td>
<td>Farbe des Elements.</td>
<td>Ein Hexadezimal-RGB-Wert. Entspricht dem folgenden regulären Ausdruck: # [0-9a-zA-Z] {6} . Beispielsweise #4a79B5.<br/></td>
</tr>
<tr class="odd">
<td><strong>SpacingBefore</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Optional</td>
<td>Abstand vor dem Element.</td>
<td>Eine beliebige nicht negative ganze Zahl.</td>
</tr>
<tr class="even">
<td><strong>Abstand zwischen</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Optional</td>
<td>Abstand zwischen diesem Element und umgebenden Elementen.</td>
<td>Eine beliebige nicht negative ganze Zahl.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Elementinformationen



|              |                                                               |
|--------------|---------------------------------------------------------------|
| Elementtyp | ComplexType ' [**verticaltype**](verticaltype-complex-type.md) ' |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk                    |
| Schemaname  | Journal Leser                                                |



 

 

 




