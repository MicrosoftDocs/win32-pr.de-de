---
description: Gibt an, welches Steuerelement beim einfachen Anzeigen der -Eigenschaft verwendet werden soll.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: drawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a330854f19005f7f2863c337451b1dcc56cea3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632048"
---
# <a name="drawcontrol"></a>drawControl

Gibt an, welches Steuerelement beim einfachen Anzeigen der -Eigenschaft verwendet werden soll. Es sollte nur ein [drawControl-Element]() für jedes [displayInfo-Element](./propdesc-schema-displayinfo.md) vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird das letzte Element verwendet. Wenn kein [drawControl-Element]() bereitgestellt wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

Diese Form des Steuerelements lässt keine Eigenschaftenbearbeitung zu.

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
<td>Standard. Verwendet das Standardsteuerelement basierend auf dem <typeInfo type=&quot;&quot;> -Attribut. Der Standardtyp ist &quot; String &quot; (mehrwertiges Steuerelement), und das Standardsteuerelement ist &quot; MultiValueText. &quot; Jeder andere Typ führt zur Verwendung des &quot; &quot; StaticText-Steuerelements.</td>
</tr>
<tr class="even">
<td>MultiLineText</td>
<td>Verwendet das mehrzeilige Textsteuerelement.</td>
</tr>
<tr class="odd">
<td>MultiValueText</td>
<td>Verwendet das Mehrwert-Textsteuerelement.</td>
</tr>
<tr class="even">
<td>PercentBar</td>
<td>Verwendet das Prozentleisten-Steuerelement.</td>
</tr>
<tr class="odd">
<td>ProgressBar</td>
<td>Verwendet das Statusanzeige-Steuerelement.</td>
</tr>
<tr class="even">
<td>Rating</td>
<td>Verwendet das 5-Stern-Bewertungssteuerelement.</td>
</tr>
<tr class="odd">
<td>StaticText</td>
<td>Verwendet <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription::FormatForDisplay,</strong></a> um den Eigenschaftswert anzuzeigen.</td>
</tr>
<tr class="even">
<td>IconList</td>
<td><strong>Windows 7 und höher.</strong> Eine Enumeration von Symbolen.</td>
</tr>
<tr class="odd">
<td>BooleanCheckMark</td>
<td><strong>Windows 7 und höher.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
