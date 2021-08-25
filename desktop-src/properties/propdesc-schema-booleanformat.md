---
description: Gibt an, wie IPropertyDescription::FormatForDisplay den Wert der booleanFormat-Eigenschaft als Zeichenfolge formatieren soll.
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6ed13194fa18ba558c9c7fbac8fb7cd4317b67
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623716"
---
# <a name="booleanformat"></a>booleanFormat

Gibt an, wie [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType="String"> . Es sollte nur ein [booleanFormat-Element]() für jedes [displayInfo-Element](./propdesc-schema-displayinfo.md) vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird das letzte Element verwendet. Wenn kein [booleanFormat-Element]() angegeben wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

## <a name="syntax"></a>Syntax


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="YesNo"/>
                <xs:enumeration value="OnOff"/>
                <xs:enumeration value="TrueFalse"/>
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
<td>formatAs</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot; &quot; YesNo. Die folgenden Werte sind gültig. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>YesNo</td>
<td>Standard. Formatiert den Wert entweder als &quot; Ja &quot; oder &quot; &quot; Nein. Erfordert, dass der Eigenschaftstyp boolesch ist.</td>
</tr>
<tr class="even">
<td>OnOff</td>
<td>Formatiert den Wert entweder als &quot; Ein &quot; oder &quot; &quot; Aus. Erfordert, dass der Eigenschaftstyp boolesch ist.</td>
</tr>
<tr class="odd">
<td>TrueFalse</td>
<td>Formatiert den Wert entweder als &quot; True &quot; oder &quot; &quot; False. Erfordert, dass der Eigenschaftstyp boolesch ist.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
