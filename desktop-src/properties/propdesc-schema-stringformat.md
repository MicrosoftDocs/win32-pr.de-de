---
description: Gibt an, wie IPropertyDescription::FormatForDisplay den Wert der stringFormat-Eigenschaft als Zeichenfolge formatieren soll.
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb40ec92ed7b31486062b5cca027eb5257e07af
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631899"
---
# <a name="stringformat"></a>stringFormat

Gibt an, [**wie IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType="String"> . Es sollte nur ein [stringFormat-Element]() für jedes [displayInfo-Element geben.](./propdesc-schema-displayinfo.md)

Wenn mehrere Elemente enthalten sind, wird das letzte verwendet. Wenn kein [stringFormat-Element]() angegeben wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

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
<td>Öffentlich. Optional. Der Standardwert ist &quot; &quot; Allgemein. Die folgenden Werte sind gültig. 
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
<td>Formatiert den Wert als Dateinamen. Blendet die Erweiterung gemäß den Benutzereinstellungen aus. Erfordert, dass der Eigenschaftentyp String ist.</td>
</tr>
<tr class="odd">
<td>FilePath</td>
<td>Formatiert den Wert als Dateipfad. Blendet die Erweiterung gemäß den Benutzereinstellungen aus. Erfordert, dass der Eigenschaftentyp String ist.</td>
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



 

 

 
