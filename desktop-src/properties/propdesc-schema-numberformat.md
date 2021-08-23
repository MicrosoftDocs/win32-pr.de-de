---
description: Gibt an, wie IPropertyDescription::FormatForDisplay den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType=&\#0034;Number&\#0034;> .
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: Numberformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1ad529b6f23191f4cfb703862a70164c4ce32d1bbb9c039fdc881e2f19cdc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718230"
---
# <a name="numberformat"></a>Numberformat

Gibt an, wie [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType="Number"> . Es sollte nur ein [numberFormat-Element]() für jedes [displayInfo-Element](./propdesc-schema-displayinfo.md) vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird das letzte Element verwendet. Wenn kein [numberFormat-Element]() angegeben wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

## <a name="syntax"></a>Syntax


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Percentage"/>
                <xs:enumeration value="ByteSize"/>
                <xs:enumeration value="KBSize"/>
                <xs:enumeration value="SampleSize"/>
                <xs:enumeration value="Bitrate"/>
                <xs:enumeration value="SampleRate"/>
                <xs:enumeration value="FrameRate"/>
                <xs:enumeration value="Pixels"/>
                <xs:enumeration value="DPI"/>
                <xs:enumeration value="Duration"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDurationAs">
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
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
<td>Öffentlich. Optional. Der Standardwert ist &quot; &quot; Allgemein. Gibt das Anzeigeformat an. Die folgenden Werte sind gültig. 
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
<td>Standard. Zeigt den Wert als unformatierte Zahl an.</td>
</tr>
<tr class="even">
<td>Prozentsatz</td>
<td>Formatiert den Wert als Prozentsatz. Erfordert, dass die -Eigenschaft UInt32 ist.</td>
</tr>
<tr class="odd">
<td>ByteSize</td>
<td>Formatiert den Wert je nach Bedarf als Byte, &quot; &quot; &quot; KB, MB &quot; oder &quot; &quot; GB. Erfordert, dass die -Eigenschaft UInt64 ist.</td>
</tr>
<tr class="even">
<td>KBSize</td>
<td>Formatiert den Wert als &quot; &quot; KB, unabhängig davon, welcher Wert ist. Erfordert, dass die -Eigenschaft UInt64 ist.</td>
</tr>
<tr class="odd">
<td>SampleSize</td>
<td>Formatiert den Wert als Anzahl von Bits. Erfordert, dass die -Eigenschaft UInt32 ist.</td>
</tr>
<tr class="even">
<td>BitRate</td>
<td>Formatiert den Wert in &quot; KBit/s. &quot; Erfordert, dass die -Eigenschaft UInt32 ist. Der Wert muss in Bits pro Sekunde gespeichert &quot; &quot; werden.</td>
</tr>
<tr class="odd">
<td>Samplerate</td>
<td>Formatiert den Wert in &quot; &quot; KHz. Erfordert, dass die -Eigenschaft UInt32 ist. Der Wert muss in &quot; Hertz-Einheiten gespeichert &quot; werden.</td>
</tr>
<tr class="even">
<td>FrameRate</td>
<td>Formatiert den Wert in Frames/Sekunde. Erfordert, dass die -Eigenschaft UInt32 ist. Der Wert muss in &quot; Kiloframes pro Sekunde gespeichert &quot; werden.</td>
</tr>
<tr class="odd">
<td>Okkludierte</td>
<td>Formatiert den Wert in Pixeleinheiten. Erfordert, dass die -Eigenschaft UInt32 ist.</td>
</tr>
<tr class="even">
<td>DPI</td>
<td>Formatiert den Wert in Punkt pro Zoll. Erfordert, dass die -Eigenschaft UInt32 ist.</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Formatiert den Wert als Dauer. Verwenden Sie <formatDurationAs> , um das Format der Dauer anzugeben. Erfordert, dass die -Eigenschaft UInt64 ist.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatDurationAs</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot; hh:mm:ss. &quot; Gilt nur, wenn <em>formatAs= &quot; Duration &quot; </em>. Erfordert, dass die -Eigenschaft UInt64 ist. Die folgenden Werte sind gültig. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>hh:mm</td>
<td>Formatiert den Wert in Stunden und Minuten.</td>
</tr>
<tr class="even">
<td>hh:mm:ss</td>
<td>Standard. Formatiert den Wert in Stunden, Minuten und Sekunden.</td>
</tr>
<tr class="odd">
<td>hh:mm:ss.fff</td>
<td>Formatiert den Wert in Stunden, Minuten, Sekunden und Millisekunden.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
