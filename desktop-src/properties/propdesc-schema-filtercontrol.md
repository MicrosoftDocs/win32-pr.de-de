---
description: Gibt an, welches Steuerelement im Headerfiltermenü verwendet werden soll.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: Filtercontrol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac7424cf281c08f1d8de87686e95a38be3f4f3a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627546"
---
# <a name="filtercontrol"></a>Filtercontrol

Gibt an, welches Steuerelement im Headerfiltermenü verwendet werden soll. Es sollte nur ein [filterControl-Element]() für jedes [displayInfo-Element](./propdesc-schema-displayinfo.md) vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird das letzte Element verwendet. Wenn kein [filterControl-Element]() bereitgestellt wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

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
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Steuerung</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot; &quot; Standard. Die folgenden Werte sind gültig. 
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
<td>Standard. Verwendet das Standardsteuerelement basierend auf dem <typeInfo type=&quot;&quot;> -Attribut. Der Standardtyp ist &quot; &quot; DateTime, und das Standardsteuerelement ist &quot; &quot; Calendar. Jeder andere Typ führt zu keinem speziellen Filtersteuerelement.</td>
</tr>
<tr class="even">
<td>Kalender</td>
<td>Verwendet das Kalendersteuerelement.</td>
</tr>
<tr class="odd">
<td>Rating</td>
<td>Verwendet das 5-Stern-Bewertungssteuerelement.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
