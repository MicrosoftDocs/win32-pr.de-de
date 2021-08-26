---
description: Wird in Windows 7 und höher nicht unterstützt. Gibt an, welches Steuerelement im Abfrage-Generator verwendet werden soll.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3652a46d403bc258226de5a48f34ae16960ff517
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626316"
---
# <a name="querycontrol"></a>queryControl

Wird in Windows 7 und höher nicht unterstützt. Gibt an, welches Steuerelement im Abfrage-Generator verwendet werden soll. Es sollte nur ein [queryControl-Element]() für jedes [displayInfo-Element](./propdesc-schema-displayinfo.md) vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird das letzte Element verwendet. Wenn kein [queryControl-Element]() bereitgestellt wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

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
<colgroup>
<col  />
<col  />
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
<td>Standard. Verwendet das Standardsteuerelement basierend auf dem <typeInfo type=&quot;&quot;> -Attribut. Die Standardtypen sind unten aufgeführt. Jeder andere Typ führt dazu, dass das &quot; Text-Steuerelement verwendet &quot; wird. 
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
<td>Zeichenfolge (mehrwertige Zeichenfolge)</td>
<td>MultiValueText</td>
</tr>
<tr class="odd">
<td>Zahl oder Größe</td>
<td>NumericText</td>
</tr>
<tr class="even">
<td>Zahl oder Größe (Enumeration)</td>
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
<td>KontrollkästchenDropList</td>
<td>Verwendet das Listensteuerelement mit Kontrollkästchen.</td>
</tr>
<tr class="odd">
<td>DropList</td>
<td>Verwendet das Dropdownlisten-Steuerelement.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Verwendet das Textbearbeitungssteuerelement mit mehreren Werten.</td>
</tr>
<tr class="odd">
<td>NumericText</td>
<td>Verwendet das Numerische Textbearbeitungssteuerelement.</td>
</tr>
<tr class="even">
<td>Rating</td>
<td>Verwendet das 5-Stern-Bewertungssteuerelement.</td>
</tr>
<tr class="odd">
<td>Text</td>
<td>Verwendet das Textbearbeitungssteuerelement.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
