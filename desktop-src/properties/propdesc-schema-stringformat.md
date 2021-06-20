---
description: Gibt an, wie IPropertyDescription::FormatForDisplay den Wert der stringFormat-Eigenschaft als Zeichenfolge formatieren soll.
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730355507b78d99eba02e82666427dd29425c942
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408353"
---
# <a name="stringformat"></a>stringFormat

Gibt an, wie [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType="String"> . Es sollte nur ein [stringFormat-Element]() für jedes [displayInfo-Element](./propdesc-schema-displayinfo.md) vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird das letzte Element verwendet. Wenn kein [stringFormat-Element]() bereitgestellt wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

## <a name="syntax"></a>Syntax


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="formatAs">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="FileName"/>
                    <xs:enumeration value="FilePath"/>
                    <xs:enumeration value="Hyperlink"/>
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
<td>formatAs</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot; &quot; Allgemein. Die folgenden Werte sind gültig. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Allgemein</td>
<td>Standard. Gibt den Wert als unformatierte Zeichenfolge zurück.</td>
</tr>
<tr class="even">
<td>FileName</td>
<td>Formatiert den Wert als Dateinamen. Blendet die Erweiterung entsprechend den Benutzereinstellungen aus. Erfordert, dass der Eigenschaftstyp String ist.</td>
</tr>
<tr class="odd">
<td>FilePath</td>
<td>Formatiert den Wert als Dateipfad. Blendet die Erweiterung entsprechend den Benutzereinstellungen aus. Erfordert, dass der Eigenschaftstyp String ist.</td>
</tr>
<tr class="even">
<td>Hyperlink</td>
<td>Formatiert den Wert als Link.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
