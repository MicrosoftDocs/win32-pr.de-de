---
description: Gibt das Steuerelement an, das beim Bearbeiten der Eigenschaft verwendet werden soll.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editcontrol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966f9742082fd6b5f939941a956eaae1ac4e427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959832"
---
# <a name="editcontrol"></a>editcontrol

Gibt das Steuerelement an, das beim Bearbeiten der Eigenschaft verwendet werden soll. Es darf nur ein [editcontrol]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet. Wenn kein [editcontrol]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.

Wenn <typeInfo isInnate="true"> , wird dieses Element ignoriert, da eine angeborene Eigenschaft nicht bearbeitet werden kann.

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
<th>type</th>
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
<td>Datetime</td>
<td>Kalender</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Kalender</td>
<td>Verwendet das Kalender Steuerelement.</td>
</tr>
<tr class="odd">
<td>Checkboxdroplist</td>
<td>Verwendet das Listen Steuerelement mit Kontrollkästchen.</td>
</tr>
<tr class="even">
<td>Droplist</td>
<td>Verwendet das Dropdown Listen-Steuerelement.</td>
</tr>
<tr class="odd">
<td>Multilinetext</td>
<td>Verwendet das mehrzeilige Textbearbeitungs-Steuerelement.</td>
</tr>
<tr class="even">
<td>Multivaluetext</td>
<td>Verwendet das mehrwertige Text Bearbeitungs Steuerelement.</td>
</tr>
<tr class="odd">
<td>Rating</td>
<td>Verwendet das 5-Sterne-Bewertungs Steuerelement.</td>
</tr>
<tr class="even">
<td>Text</td>
<td>Verwendet das Steuerelement für die Textbearbeitung.</td>
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



 

 

 
