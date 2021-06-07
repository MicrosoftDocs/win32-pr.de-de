---
description: Enthält den Inhalt für eine Journalseite.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content-Element [JournalReader]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432152"
---
# <a name="content-element-journal-reader"></a>Content Element \[ Journal Reader\]

Enthält den Inhalt für eine Journalseite.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**JournalPage**](journalpage-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**GroupNode**](groupnode-element.md)

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
<th>attribute</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
<th>PossibleValues</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Typ</strong></td>
<td><a href="contenttype-complex-type.md"><strong>complexType: ContentType</strong></a></td>
<td>Erforderlich</td>
<td>Wenn der Typ &quot; Inert &quot; ist, kann der Inhalt nicht geändert werden.<br/></td>
<td><ul>
<li>Normal</li>
<li>Inert</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|-------------------------------------------------------------|
| Elementtyp | [**complexType: ContentType**](contenttype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                  |
| Schemaname  | Journalreader                                              |



 

 

 




