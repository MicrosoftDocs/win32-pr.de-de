---
description: Gibt das Steuerelement an, das beim einfachen Anzeigen der Eigenschaft verwendet werden soll.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: DrawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318fdebc995ff45932f75b4000ceda6e74068e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042032"
---
# <a name="drawcontrol"></a>DrawControl

Gibt das Steuerelement an, das beim einfachen Anzeigen der Eigenschaft verwendet werden soll. Es darf nur ein [DrawControl]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet. Wenn kein [DrawControl]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.

Diese Form des Steuer Elements ermöglicht keine Eigenschaften Bearbeitung.

## <a name="syntax"></a>Syntax


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="PercentBar"/>
                    <xs:enumeration value="ProgressBar"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="StaticText"/>
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
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
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Standard</td>
<td>Standard. Verwendet das Standard Steuerelement auf Grundlage des- <typeInfo type=&quot;&quot;> Attributs. Der Standardtyp ist &quot; String &quot; (MultiValue), und das Standard Steuerelement ist &quot; multivaluetext &quot; . Jeder andere Typ führt zur Verwendung des &quot; StaticText- &quot; Steuer Elements.</td>
</tr>
<tr class="even">
<td>Multilinetext</td>
<td>Verwendet das mehrzeilige Text Steuerelement.</td>
</tr>
<tr class="odd">
<td>Multivaluetext</td>
<td>Verwendet das mehrwertige Text Steuerelement.</td>
</tr>
<tr class="even">
<td>Prozentualbar</td>
<td>Verwendet das Prozent leisten-Steuerelement.</td>
</tr>
<tr class="odd">
<td>ProgressBar</td>
<td>Verwendet das Statusanzeige-Steuerelement.</td>
</tr>
<tr class="even">
<td>Rating</td>
<td>Verwendet das 5-Sterne-Bewertungs Steuerelement.</td>
</tr>
<tr class="odd">
<td>StaticText</td>
<td>Verwendet <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>ipropertydescription:: formatfordisplay</strong></a> , um den Eigenschafts Wert anzuzeigen.</td>
</tr>
<tr class="even">
<td>IconList</td>
<td><strong>Windows 7 und höher.</strong> Eine Enumeration von Symbolen.</td>
</tr>
<tr class="odd">
<td>Booleancheckmark</td>
<td><strong>Windows 7 und höher.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
