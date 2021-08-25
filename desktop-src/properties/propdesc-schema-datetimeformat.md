---
description: Gibt an, wie IPropertyDescription::FormatForDisplay den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType=&\#0034;DateTime&\#0034;> .
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950f10106d7850f4a5b58aeb165e8cb4cc9ffcd4
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629172"
---
# <a name="datetimeformat"></a>dateTimeFormat

Gibt an, [**wie IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType="DateTime"> . Es sollte nur ein [dateTimeFormat-Element]() für jedes [displayInfo-Element geben.](./propdesc-schema-displayinfo.md)

Wenn mehrere Elemente enthalten sind, wird das letzte verwendet. Wenn kein [dateTimeFormat-Element]() angegeben wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

## <a name="syntax"></a>Syntax


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Month"/>
                <xs:enumeration value="YearMonth"/>
                <xs:enumeration value="Year"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatTimeAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortTime"/>
                <xs:enumeration value="LongTime"/>
                <xs:enumeration value="HideTime"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDateAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortDate"/>
                <xs:enumeration value="LongDate"/>
                <xs:enumeration value="HideDate"/>
                <xs:enumeration value="RelativeShortDate"/>
                <xs:enumeration value="RelativeLongDate"/>
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
<td>Standard. Formatiert den Datum/Uhrzeit-Wert <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>mit SHFormatDateTime</strong></a>. Verwenden Sie <em>die Attribute formatTimeAs</em> <em>und formatDateAs,</em> um anzugeben, wie Uhrzeit und Datum formatiert werden. Erfordert, dass der Eigenschaftstyp DateTime ist.</td>
</tr>
<tr class="even">
<td>Month (Monat)</td>
<td>Formatiert den Wert als einen der Monate des Jahres. Erfordert, dass der Eigenschaftentyp Int32 ist. Der Wert muss als numerischer Wert mit 1 gespeichert werden, der den ersten Monat des Jahres darstellt.</td>
</tr>
<tr class="odd">
<td>YearMonth</td>
<td>Formatiert den Wert als &quot; Year - Month &quot; . Erfordert, dass der Eigenschaftentyp Int32 ist. Der Wert muss so gespeichert werden, dass die beiden höchsten Bytes das Jahr und die unteren zwei Bytes den Monat angeben.</td>
</tr>
<tr class="even">
<td>Jahr</td>
<td>Formatiert den Wert als einfache Zeichenfolge.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatTimeAs</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot; &quot; ShortTime. Gibt das Format an, in dem die Uhrzeit angezeigt werden soll. Gilt, wenn <strong>formatAs= &quot; Allgemein ist. &quot; </strong> Die folgenden Werte sind gültig. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShortTime</td>
<td>Standard. Zeigt die Uhrzeit wie &quot; 19:48 Uhr &quot; an.</td>
</tr>
<tr class="even">
<td>Langjährige</td>
<td>Zeigt die Uhrzeit wie &quot; 19:48:33 Uhr &quot; an.</td>
</tr>
<tr class="odd">
<td>HideTime</td>
<td>Der Zeitteil des Datums wird nicht angezeigt.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>formatDateAs</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot; &quot; ShortDate. Gibt das Format an, in dem das Datum angezeigt werden soll. Gilt, wenn <strong>formatAs= &quot; Allgemein ist. &quot; </strong> Die folgenden Werte sind gültig. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShortDate</td>
<td>Standard. Zeigt das Datum wie &quot; 13.05.59 &quot; an.</td>
</tr>
<tr class="even">
<td>LongDate</td>
<td>Zeigt das Datum wie &quot; Mittwoch, 13. Mai 1959 &quot; an.</td>
</tr>
<tr class="odd">
<td>HideDate</td>
<td>Zeigen Sie den Datumsteil nicht an.</td>
</tr>
<tr class="even">
<td>RelativeShortDate</td>
<td>Zeigen Sie das Datum wie ShortDate an, verwenden Sie aber nach Möglichkeit relative Beschreibungen, z. B. &quot; &quot; &quot; &quot; gestrige.</td>
</tr>
<tr class="odd">
<td>RelativeLongDate</td>
<td>Zeigen Sie das Datum wie LongDate an, verwenden Sie aber nach Möglichkeit relative Beschreibungen, z. &quot; &quot; B. &quot; &quot; gestrige.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
