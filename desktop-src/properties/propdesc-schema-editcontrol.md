---
description: Gibt an, welches Steuerelement beim Bearbeiten der Eigenschaft verwendet werden soll.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdb47a3866c156ff10dba8eed4584f814793b863e8f615ae5e1a10b8d687ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118055990"
---
# <a name="editcontrol"></a>editControl

Gibt an, welches Steuerelement beim Bearbeiten der Eigenschaft verwendet werden soll. Es sollte nur ein [editControl-Element]() für jedes [displayInfo-Element geben.](./propdesc-schema-displayinfo.md)

Wenn mehrere Elemente enthalten sind, wird das letzte verwendet. Wenn kein [editControl-Element]() angegeben wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

Gibt <typeInfo isInnate="true"> an, dass dieses Element ignoriert wird, da eine innierte Eigenschaft nicht bearbeitet werden kann.

## <a name="syntax"></a>Syntax


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Steuerung</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot; Default &quot; . Die folgenden Werte sind gültig. 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Standard</td>
<td>Standard. Verwendet das standard-Steuerelement, das auf dem -Attribut <typeInfo type=&quot;&quot;> basiert. Die Standardtypen sind unten aufgeführt. Jeder andere Typ führt zur Verwendung des &quot; &quot; Text-Steuerelements. 
<table>
<thead>
<tr class="header">
<th>Typ</th>
<th>Control</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Text</td>
</tr>
<tr class="even">
<td>Zeichenfolge (Mehrwert)</td>
<td>MultiValueText</td>
</tr>
<tr class="odd">
<td>Datetime</td>
<td>Kalender</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Kalender</td>
<td>Verwendet das Calendar-Steuerelement.</td>
</tr>
<tr class="odd">
<td>CheckboxDropList</td>
<td>Verwendet das Listensteuerfeld mit Kontrollkästchen.</td>
</tr>
<tr class="even">
<td>DropList</td>
<td>Verwendet das Dropdownlisten-Steuerelement.</td>
</tr>
<tr class="odd">
<td>MultiLineText</td>
<td>Verwendet das mehrzeilenbasierte Textbearbeitungssteuerfeld.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Verwendet das mehrwertige Textbearbeitungssteuerfeld.</td>
</tr>
<tr class="odd">
<td>Rating</td>
<td>Verwendet das 5-Stern-Bewertungssteuer steuerelement.</td>
</tr>
<tr class="even">
<td>Text</td>
<td>Verwendet das Textbearbeitungssteuerfeld.</td>
</tr>
<tr class="odd">
<td>IconList</td>
<td><strong>Windows 7 und höher.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
