---
description: 'Gibt an, wie ipropertydescription:: formatfordisplay den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType=&\#0034;DateTime&\#0034;> .'
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215399"
---
# <a name="datetimeformat"></a>dateTimeFormat

Gibt an, wie [**ipropertydescription:: formatfordisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) den Wert der Eigenschaft als Zeichenfolge formatieren soll. Dies gilt nur, wenn <displayInfo displayType="DateTime"> . Es darf nur ein [DateTimeFormat]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet. Wenn kein [DateTimeFormat]() -Element angegeben wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.

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
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot; Allgemein &quot; . Die folgenden Werte sind gültig. 
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
<td>Standard. Formatiert den Datums-/Uhrzeitwert mit " <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>shformatdatetime</strong></a>". Verwenden Sie die Attribute <em>formattimeas</em> und <em>formatdateas</em> , um anzugeben, wie Uhrzeit und Datum formatiert werden. Erfordert, dass der Eigenschaftentyp DateTime ist.</td>
</tr>
<tr class="even">
<td>Monat</td>
<td>Formatiert den Wert in einem der Monate des Jahres. Erfordert, dass der Eigenschaftentyp Int32 ist. Der Wert muss als numerischer Wert mit 1 gespeichert werden, der den ersten Monat des Jahres darstellt.</td>
</tr>
<tr class="odd">
<td>Jährlicher Monat</td>
<td>Formatiert den Wert als &quot; Jahr-Monat &quot; . Erfordert, dass der Eigenschaftentyp Int32 ist. Der Wert muss so gespeichert werden, dass die beiden höchsten Bytes das Jahr und die unteren zwei Bytes den Monat angeben.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>Formatiert den Wert als einfache Zeichenfolge.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formattimeas</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot; Kurzzeit &quot; . Gibt das Format an, in dem die Uhrzeit angezeigt werden soll. Gilt, wenn <strong>formatas &quot; = &quot; Allgemein</strong>. Die folgenden Werte sind gültig. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kurzzeit</td>
<td>Standard. Zeigen Sie die Zeit wie &quot; 7:48 pm an &quot; .</td>
</tr>
<tr class="even">
<td>Jährige</td>
<td>Zeigen Sie die Zeit wie &quot; 7:48:33 pm an &quot; .</td>
</tr>
<tr class="odd">
<td>Hidetime</td>
<td>Zeigen Sie den Uhrzeit Teil des Datums nicht an.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>formatdateas</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot; SHORTDATE &quot; . Gibt das Format an, in dem das Datum angezeigt werden soll. Gilt, wenn <strong>formatas &quot; = &quot; Allgemein</strong>. Die folgenden Werte sind gültig. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SHORTDATE</td>
<td>Standard. Zeigt das Datum wie &quot; 5/13/59 an &quot; .</td>
</tr>
<tr class="even">
<td>LongDate</td>
<td>Zeigt das Datum wie &quot; Mittwoch, 13. Mai 1959 an &quot; .</td>
</tr>
<tr class="odd">
<td>Hidedate</td>
<td>Der Datums Teil wird nicht angezeigt.</td>
</tr>
<tr class="even">
<td>Relativeshortdate</td>
<td>Zeigen Sie das Datum wie &quot; SHORTDATE an &quot; , aber verwenden Sie relative Beschreibungen wie &quot; gestern, &quot; wann immer dies möglich ist.</td>
</tr>
<tr class="odd">
<td>Relativelongdate</td>
<td>Zeigen Sie das Datum wie &quot; longDate an &quot; , aber verwenden Sie relative Beschreibungen, z &quot; . b &quot; . gestern, wann immer möglich.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
