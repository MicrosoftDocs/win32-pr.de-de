---
description: Enthält Titelinformationen zur Journalnotiz.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Title-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef687f809aae5c3722cdad84ee63d79c7bfcfb21
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432222"
---
# <a name="title-element"></a>Title-Element

Enthält Titelinformationen zur Journalnotiz.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Briefpapier**](stationery-element.md)

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
<td><strong>xs:string</strong></td>
<td>Erforderlich</td>
<td>Gibt den Typ des Rahmens um den Titel der Notiz an.</td>
<td><ul>
<li>Keine</li>
<li>SolidSquare</li>
<li>OutlineSquare</li>
<li>SolidRoundRect</li>
<li>OutlineRoundRect</li>
<li>SolidRoundRectDottedBaseline</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>DateStyle</strong></td>
<td><strong>xs:string</strong></td>
<td>Erforderlich</td>
<td>Definiert, ob der Titel ein Datum enthält oder nicht.</td>
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



| Element      | Wert                                                   |
|--------------|---------------------------------------------------------|
| Elementtyp | [**complexType: TitleType**](titletype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink              |
| Schemaname  | Journalreader                                          |



 

 

 



