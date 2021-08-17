---
description: Definiert die Randlinien, die auf der Seite gezeichnet werden.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Margin-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ff764585919ff144ebc25ac568caf1af74410a2f337beb03d5ce484f7d1abe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350440"
---
# <a name="margin-element"></a>Margin-Element

Definiert die Randlinien, die auf der Seite gezeichnet werden.

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

nichts..

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
<th>attribute</th>
<th>type</th>
<th>Erforderlich</th>
<th>Beschreibung</th>
<th>Mögliche Werte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Stil</strong></td>
<td><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</td>
<td>Erforderlich</td>
<td>Gibt den Typ der zu zeichnenden Linie an.</td>
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
<td>Ein hexadezimaler RGB-Wert. Entspricht dem folgenden regulären Ausdruck: #[0-9a-zA-Z] {6} . Beispiel: #4a79B5.<br/></td>
</tr>
<tr class="odd">
<td><strong>Typ</strong></td>
<td><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</td>
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
<td>Abstand zwischen Seitenrand und Rand.</td>
<td>Eine beliebige nicht negative ganze Zahl.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|-----------------------------------------------------------|
| Elementtyp | [**complexType: MarginType**](margintype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                |
| Schemaname  | Journalreader                                            |



 

 

 




