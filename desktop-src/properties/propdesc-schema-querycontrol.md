---
description: Wird in Windows 7 und höher nicht unterstützt. Gibt an, welches Steuerelement im Abfrage-Generator verwendet werden soll.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f05800fc026c61a4ea50098fb1d8f4deb98d971c9eecfed478d71bd3c01033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823560"
---
# <a name="querycontrol"></a>queryControl

Wird in Windows 7 und höher nicht unterstützt. Gibt an, welches Steuerelement im Abfrage-Generator verwendet werden soll. Es sollte nur ein [queryControl-Element]() für jedes [displayInfo-Element geben.](./propdesc-schema-displayinfo.md)

Wenn mehrere Elemente enthalten sind, wird das letzte verwendet. Wenn kein [queryControl-Element]() angegeben wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

## <a name="syntax"></a>Syntax


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
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
<th>ConditionType</th>
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
<td>Zahl oder Größe</td>
<td>NumericText</td>
</tr>
<tr class="even">
<td>Zahl oder Größe (enum)</td>
<td>List</td>
</tr>
<tr class="odd">
<td>Datetime</td>
<td>Kalender</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Boolean</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Verwendet das boolesche Steuerelement.</td>
</tr>
<tr class="odd">
<td>Kalender</td>
<td>Verwendet das Dropdownkalender-Steuerelement.</td>
</tr>
<tr class="even">
<td>CheckboxDropList</td>
<td>Verwendet das Listensteuerfeld mit Kontrollkästchen.</td>
</tr>
<tr class="odd">
<td>DropList</td>
<td>Verwendet das Dropdownlisten-Steuerelement.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Verwendet das mehrwertige Textbearbeitungssteuerfeld.</td>
</tr>
<tr class="odd">
<td>NumericText</td>
<td>Verwendet das Numerische Textbearbeitungssteuerfeld.</td>
</tr>
<tr class="even">
<td>Rating</td>
<td>Verwendet das 5-Stern-Bewertungssteuer steuerelement.</td>
</tr>
<tr class="odd">
<td>Text</td>
<td>Verwendet das Textbearbeitungssteuerfeld.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
