---
description: Wird in Windows 7 und höher nicht unterstützt. Gibt an, welches Steuerelement im Abfrage-Generator verwendet werden soll.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: querycontrol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448b47038f82afb9f860209bfe89eb9e6eecb890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356632"
---
# <a name="querycontrol"></a>querycontrol

Wird in Windows 7 und höher nicht unterstützt. Gibt an, welches Steuerelement im Abfrage-Generator verwendet werden soll. Es darf nur ein [querycontrol]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet. Wenn kein [querycontrol]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.

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
| [Display Info](./propdesc-schema-displayinfo.md) | Keine           |



 

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Steuerung</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist Default &quot; &quot; . Die folgenden Werte sind gültig. 
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
<td>Standard. Verwendet das Standard Steuerelement auf Grundlage des- <typeInfo type=&quot;&quot;> Attributs. Die Standardtypen sind unten aufgeführt. Jeder andere Typ führt zur Verwendung des &quot; Text- &quot; Steuer Elements. 
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
<td>Zeichenfolge (mehrere Werte)</td>
<td>Multivaluetext</td>
</tr>
<tr class="odd">
<td>Anzahl oder Größe</td>
<td>Numerictext</td>
</tr>
<tr class="even">
<td>Number oder size (Enum)</td>
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
<td>Verwendet das Dropdown-Kalender Steuerelement.</td>
</tr>
<tr class="even">
<td>Checkboxdroplist</td>
<td>Verwendet das Listen Steuerelement mit Kontrollkästchen.</td>
</tr>
<tr class="odd">
<td>Droplist</td>
<td>Verwendet das Dropdown Listen-Steuerelement.</td>
</tr>
<tr class="even">
<td>Multivaluetext</td>
<td>Verwendet das mehrwertige Text Bearbeitungs Steuerelement.</td>
</tr>
<tr class="odd">
<td>Numerictext</td>
<td>Verwendet das numerische Textbearbeitungs-Steuerelement.</td>
</tr>
<tr class="even">
<td>Rating</td>
<td>Verwendet das 5-Sterne-Bewertungs Steuerelement.</td>
</tr>
<tr class="odd">
<td>Text</td>
<td>Verwendet das Steuerelement für die Textbearbeitung.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
