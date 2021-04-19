---
description: Enthält den Inhalt für eine Journal Seite.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content-Element [Journal Reader]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b5a7c9631cd69d38b8db54e2a2f8e69636f7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349975"
---
# <a name="content-element-journal-reader"></a>Inhalts Element- \[ Journal Leser\]

Enthält den Inhalt für eine Journal Seite.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Journalpage**](journalpage-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**-Gruppenknoten**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**Zeichnung**](drawing-element.md)

[**Text**](text-element.md)

[**Image**](image-element.md)

[**Flag**](flag-element.md)

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
<th>PossibleValues</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Type</strong></td>
<td><a href="contenttype-complex-type.md"><strong>ComplexType für ContentType</strong></a></td>
<td>Erforderlich</td>
<td>Wenn der Typ " &quot; inert" ist &quot; , kann der Inhalt nicht geändert werden.<br/></td>
<td><ul>
<li>Normal</li>
<li>Schwei</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Elementinformationen



|              |                                                             |
|--------------|-------------------------------------------------------------|
| Elementtyp | ComplexType für [**ContentType**](contenttype-complex-type.md) |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk                  |
| Schemaname  | Journal Leser                                              |



 

 

 




