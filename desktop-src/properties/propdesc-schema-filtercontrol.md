---
description: Gibt an, welches Steuerelement im Headerfiltermenü verwendet werden soll.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: Filtercontrol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f002543b220347ba9aaba3659aa9a66f8aea7760b9d8a9177ef2980a823434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885960"
---
# <a name="filtercontrol"></a>Filtercontrol

Gibt an, welches Steuerelement im Headerfiltermenü verwendet werden soll. Es sollte nur ein [filterControl-Element]() für jedes [displayInfo-Element geben.](./propdesc-schema-displayinfo.md)

Wenn mehrere Elemente enthalten sind, wird das letzte verwendet. Wenn kein [filterControl-Element]() bereitgestellt wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

## <a name="syntax"></a>Syntax


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="control">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="Default"/>
                <xs:enumeration value="Calendar"/>
                <xs:enumeration value="Rating"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                   | Untergeordnete Elemente |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | Keine           |



 

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Steuerung</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot; Default &quot; . Die folgenden Werte sind gültig. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Standard</td>
<td>Standard. Verwendet das standard-Steuerelement, das auf dem -Attribut <typeInfo type=&quot;&quot;> basiert. Der Standardtyp ist &quot; &quot; DateTime, und das Standardsteuer steuerelement ist &quot; &quot; Calendar. Jeder andere Typ führt zu keinem speziellen Filtersteuerzeichen.</td>
</tr>
<tr class="even">
<td>Kalender</td>
<td>Verwendet das Calendar-Steuerelement.</td>
</tr>
<tr class="odd">
<td>Rating</td>
<td>Verwendet das 5-Stern-Bewertungssteuer steuerelement.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
