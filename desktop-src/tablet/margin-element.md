---
description: Definiert die Rand Linien, die auf der Seite gezeichnet werden.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Margin-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0500d4db165012393cb600c1e118089b68c76695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218361"
---
# <a name="margin-element"></a>Margin-Element

Definiert die Rand Linien, die auf der Seite gezeichnet werden.

## <a name="definition"></a>Definition

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>Übergeordnete Elemente

Keine

## <a name="child-elements"></a>Untergeordnete Elemente

Keine...

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
<td><strong>Type</strong></td>
<td><a href="margintypetype-simple-type.md"><strong>Margintypetype</strong></a> simpleType</td>
<td>Optional</td>
<td>Gibt den linken oder rechten Rand an.</td>
<td><ul>
<li>Left</li>
<li>Right</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Abstand</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Optional</td>
<td>Abstand zwischen dem Rand der Seite und dem Rand.</td>
<td>Eine beliebige nicht negative ganze Zahl.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Elementinformationen



|              |                                                           |
|--------------|-----------------------------------------------------------|
| Elementtyp | ComplexType ' [**margintype**](margintype-complex-type.md) ' |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk                |
| Schemaname  | Journal Leser                                            |



 

 

 




