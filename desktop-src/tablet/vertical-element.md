---
description: Enthält die Informationen, die die vertikale Komponente der Linien im Von der Journalnotiz verwendeten Stationery beschreiben. Wird z. B. verwendet, wenn die Notiz Gitternetzlinien hat.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Vertical-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42565e6f2828c4ef27d1b28830502303a03e6f13
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432122"
---
# <a name="vertical-element"></a>Vertical-Element

Enthält die Informationen, die die vertikale Komponente der Linien im Von der Journalnotiz verwendeten Stationery beschreiben. Wird z. B. verwendet, wenn die Notiz Gitternetzlinien hat.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**LineLayout**](linelayout-element.md)

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
<th>attribute</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
<th>Mögliche Werte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Stil</strong></td>
<td><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</td>
<td>Erforderlich</td>
<td>Gibt den Typ der zu zeichneten Linie an.</td>
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
<td><strong>SpacingBefore</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Optional</td>
<td>Abstand vor dem Element.</td>
<td>Eine nicht negative ganze Zahl.</td>
</tr>
<tr class="even">
<td><strong>SpacingBetween</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Optional</td>
<td>Abstand zwischen diesem Element und den umgebenden Elementen.</td>
<td>Eine nicht negative ganze Zahl.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                         |
|--------------|---------------------------------------------------------------|
| Elementtyp | [**complexType: VerticalType**](verticaltype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                    |
| Schemaname  | Journalreader                                                |



 

 

 




