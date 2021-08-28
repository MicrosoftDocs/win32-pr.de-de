---
description: Enthält den Hintergrund für ein JournalDocument-Element oder ein JournalPage-Element.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Background-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4896266887a075fed41a01d2e4493c417d2e01560f4537e272db28aacef820e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111280"
---
# <a name="background-element"></a>Background-Element

Enthält den Hintergrund für ein [**JournalDocument-Element**](journaldocument-element.md) oder [**ein JournalPage-Element.**](journalpage-element.md)

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Briefpapier**](stationery-element.md)

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
<td><strong>xs:string</strong></td>
<td>Erforderlich</td>
<td>Gibt den Stil des Hintergrunds an.</td>
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



|                  | Wert                                                             |
|------------------|-------------------------------------------------------------------|
| **Elementtyp** | [**complexType: BackgroundType**](backgroundtype-complex-type.md) |
| **Namespace**    | urn:schemas-microsoft-com:tabletpc:richink                        |
| **Schemaname**  | Journalreader                                                    |



 

 

 



