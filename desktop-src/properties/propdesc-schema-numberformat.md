---
description: 'Gibt an, wie ipropertydescription:: formatfordisplay den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType=&\#0034;Number&\#0034;> .'
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: NumberFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750a9fb4dcf6a7a56c350fccf80241644b956da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355624"
---
# <a name="numberformat"></a>NumberFormat

Gibt an, wie [**ipropertydescription:: formatfordisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType="Number"> . Es darf nur ein " [infoformat]() "-Element für jedes " [DisplayInfo](./propdesc-schema-displayinfo.md) "-Element vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet. Wenn kein [NumFormat-]() Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.

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
<td>formatas</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot; Allgemein &quot; . Gibt das Anzeige Format an. Die folgenden Werte sind gültig. 
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
<td>Prozentwert</td>
<td>Formatiert den Wert als Prozentsatz. Erfordert, dass die-Eigenschaft UInt32 ist.</td>
</tr>
<tr class="odd">
<td>ByteSize</td>
<td>Formatiert den Wert nach Bedarf als Byte, &quot; KB &quot; , &quot; MB &quot; oder &quot; GB &quot; . Erfordert, dass die-Eigenschaft UInt64 ist.</td>
</tr>
<tr class="even">
<td>Kbsize</td>
<td>Formatiert den Wert in &quot; KB &quot; , unabhängig davon, was der Wert ist. Erfordert, dass die-Eigenschaft UInt64 ist.</td>
</tr>
<tr class="odd">
<td>Sample Size (</td>
<td>Formatiert den Wert als Anzahl von Bits. Erfordert, dass die-Eigenschaft UInt32 ist.</td>
</tr>
<tr class="even">
<td>BitRate</td>
<td>Formatiert den Wert in Kbit/s &quot; &quot; . Erfordert, dass die-Eigenschaft UInt32 ist. Der Wert muss in &quot; Bits-pro-Sekunde-Einheiten gespeichert werden &quot; .</td>
</tr>
<tr class="odd">
<td>Sample Rate</td>
<td>Formatiert den Wert in &quot; kHz &quot; . Erfordert, dass die-Eigenschaft UInt32 ist. Der Wert muss in Hertz- &quot; Einheiten gespeichert werden &quot; .</td>
</tr>
<tr class="even">
<td>FrameRate</td>
<td>Formatiert den Wert in Frames/Sekunde. Erfordert, dass die-Eigenschaft UInt32 ist. Der Wert muss in &quot; Kilo-Frames-pro Sekunde-Einheiten gespeichert werden &quot; .</td>
</tr>
<tr class="odd">
<td>Okkludierte</td>
<td>Formatiert den Wert in Pixel Einheiten. Erfordert, dass die-Eigenschaft UInt32 ist.</td>
</tr>
<tr class="even">
<td>DPI</td>
<td>Formatiert den Wert in Punkten pro Zoll. Erfordert, dass die-Eigenschaft UInt32 ist.</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Formatiert den Wert als Dauer. Verwenden <formatDurationAs> Sie, um das Format für die Dauer anzugeben. Erfordert, dass die-Eigenschaft UInt64 ist.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatdurationas</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot; hh: mm: SS &quot; . Gilt nur, wenn <em>formatas &quot; = &quot; Duration</em>ist. Erfordert, dass die-Eigenschaft UInt64 ist. Die folgenden Werte sind gültig. 
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
<td>hh: mm: SS. fff</td>
<td>Formatiert den Wert in Stunden, Minuten, Sekunden und Millisekunden.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
