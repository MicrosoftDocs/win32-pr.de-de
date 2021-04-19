---
description: Gibt die Anzeigeinformationen einer Eigenschaft an.
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: Display Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fff0bb441b4535c0b6c6f3183671fbe8ade09183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360558"
---
# <a name="displayinfo"></a>Display Info

Gibt die Anzeigeinformationen einer Eigenschaft an. Es darf nur ein [DisplayInfo]() -Element für jede [propertydescription](./propdesc-schema-propertydescription.md)vorhanden sein.

Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet. Wenn kein [DisplayInfo]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.

## <a name="syntax"></a>Syntax


```
<!-- displayInfo -->
<xs:element name="displayInfo">
    <xs:complexType>
        <xs:all>
            <xs:element name="stringFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="booleanFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="numberFormat" minOccurs="0" maxOccurs="1">
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
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="hh:mm"/>
                                <xs:enumeration value="hh:mm:ss"/>
                                <xs:enumeration value="hh:mm:ss.fff"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="dateTimeFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="enumeratedList" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="value" type="xs:string" use="required"/>
                                <xs:attribute name="text" type="xs:string" use="required"/>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="minValue" type="xs:string" use="required"/>
                                <xs:attribute name="setValue" type="xs:string"/>
                                <xs:attribute name="text" type="xs:string"/>
                            </xs:complexType>
                        </xs:element>
                    </xs:sequence>

                    <xs:attribute name="defaultText" type="xs:string"/>
                    <xs:attribute name="useValueForDefault" type="xs:boolean"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="drawControl" minOccurs="0" maxOccurs="1">
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
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="editControl" minOccurs="0" maxOccurs="1">
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
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="filterControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="Rating"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="queryControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Boolean"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="CheckboxDropList"/>
                                <xs:enumeration value="DropList"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="NumericText"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="Text"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
        </xs:all>

        <xs:attribute name="defaultColumnWidth" type="xs:nonNegativeInteger" default="20"/>
        <xs:attribute name="displayType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        
        <xs:attribute name="alignment" default="Left">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Left"/>
                    <xs:enumeration value="Center"/>
                    <xs:enumeration value="Right"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="relativeDescriptionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Count"/>
                    <xs:enumeration value="Revision"/>
                    <xs:enumeration value="Length"/>
                    <xs:enumeration value="Duration"/>
                    <xs:enumeration value="Speed"/>
                    <xs:enumeration value="Rate"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Priority"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultSortDirection" default="Ascending">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                  <xs:enumeration value="Ascending"/>
                  <xs:enumeration value="Descending"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                   | Untergeordnete Elemente                                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [propertydescription](./propdesc-schema-propertydescription.md) | [StringFormat](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [BooleanFormat](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [NumberFormat](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [dateTimeFormat](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [enumeratedlist](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [DrawControl](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [editcontrol](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [FilterControl](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | [querycontrol](./propdesc-schema-querycontrol.md) (nur Windows Vista). Wird in Windows 7 und höher nicht unterstützt.) |



 

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
<td>defaultcolumnwidth</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot; 20 &quot; .</td>
</tr>
<tr class="even">
<td>Display Type</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot; String &quot; . Gibt den Typ der Anzeige Zeichenfolge an. Nachdem Sie hier festgelegt haben, werden die zugeordneten <strong>PROPDESC_DISPLAYTYPE</strong> Werte von <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>ipropertydescription:: getdisplaytype</strong></a>abgerufen. Die folgenden Typen sind gültig. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Standard. Der Wert wird als Zeichenfolge angezeigt. Verwenden &quot; Sie StringFormat &quot; , um zu formatieren. Die Methode gibt PDDT_STRING zurück.</td>
</tr>
<tr class="even">
<td>Number</td>
<td>Standardwert für numerische Eigenschaften. Der Wert wird als Zahl angezeigt. Verwenden &quot; Sie "NumFormat" &quot; zum Formatieren. Die Methode gibt PDDT_NUMBER zurück.</td>
</tr>
<tr class="odd">
<td>Boolean</td>
<td>Standardwert, wenn <typeInfo type=&quot;Boolean&quot;> . Der Wert wird als boolescher Wert angezeigt. Verwenden &quot; Sie BooleanFormat &quot; , um zu formatieren. Die Methode gibt PDDT_BOOLEAN zurück.</td>
</tr>
<tr class="even">
<td>Datetime</td>
<td>Standardwert, wenn <typeInfo type=&quot;DateTime&quot;> . Der Wert wird als Datum oder Uhrzeit angezeigt. Verwenden &quot; Sie DateTimeFormat &quot; , um zu formatieren. Die Methode gibt PDDT_DATETIME zurück.</td>
</tr>
<tr class="odd">
<td>Enumeration</td>
<td>Der Wert wird als Darstellung der Anzeige Zeichenfolge angezeigt, die vom &quot; enumeratedlist-Element bereitgestellt wird &quot; . Die Methode gibt PDDT_ENUMERATED zurück.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>Ausrichtung</td>
<td>Dies ist optional. Der Standardwert ist &quot; left &quot; . 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Links</td>
<td>Standard. Links ausrichten.</td>
</tr>
<tr class="even">
<td>Zentrum</td>
<td>Zentriert ausrichten.</td>
</tr>
<tr class="odd">
<td>Rechts</td>
<td>Rechts ausrichten.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>relativedescriptiontype</td>
<td>Dies ist optional. Der Standardwert ist &quot; Allgemein &quot; . Gibt an, wie zwei Werte dieser Eigenschaft beschrieben werden sollen, wenn Sie miteinander verglichen werden. Im Fall von Äquivalenz &quot; &quot; wird immer derselbe verwendet. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>Ipropertydescription:: getrelativedescription</strong></a> und <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>ipropertydescription:: getrelativedescriptiontype</strong></a> verwenden Sie diesen Wert, um zu bestimmen, welche Namen für die relative Beschreibungs Anzeige verwendet werden sollen. 
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
<td>Standard. Verwendet &quot; unterschiedliche &quot;  /  &quot; &quot;  /  &quot; andere &quot; .</td>
</tr>
<tr class="even">
<td>Date</td>
<td>Standardwert, wenn <typeInfo type=&quot;DateTime&quot;> . &quot;Wird früher &quot;  /  &quot; gleich &quot;  /  &quot; später verwendet, oder es wird &quot; älter oder &quot; &quot;  /  &quot; &quot;  /  &quot; &quot; früher oder &quot; früher verwendet &quot;  /  &quot; &quot;  /  &quot; &quot; .</td>
</tr>
<tr class="odd">
<td>Size</td>
<td>Von wird eine geringere Größe verwendet. &quot; &quot;  /  &quot; &quot;  /  &quot;&quot;</td>
</tr>
<tr class="even">
<td>Anzahl</td>
<td>Von wird eine geringere Größe verwendet. &quot; &quot;  /  &quot; &quot;  /  &quot;&quot;</td>
</tr>
<tr class="odd">
<td>Revision</td>
<td>Wird &quot; früher &quot;  /  &quot; gleich &quot;  /  &quot; später verwendet&quot;</td>
</tr>
<tr class="even">
<td>Länge</td>
<td>Verwendet &quot; kürzer und &quot;  /  &quot; &quot;  /  &quot; länger&quot;</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Verwendet &quot; kürzer und &quot;  /  &quot; &quot;  /  &quot; länger&quot;</td>
</tr>
<tr class="even">
<td>Geschwindigkeit</td>
<td>Verwendet &quot; langsamer und &quot;  /  &quot; &quot;  /  &quot; schneller&quot;</td>
</tr>
<tr class="odd">
<td>Rate</td>
<td>Verwendet &quot; langsamer und &quot;  /  &quot; &quot;  /  &quot; schneller&quot;</td>
</tr>
<tr class="even">
<td>Rating</td>
<td>Verwendet &quot; niedriger &quot;  /  &quot; gleich &quot;  /  &quot; höher&quot;</td>
</tr>
<tr class="odd">
<td>Priorität</td>
<td>Verwendet &quot; niedriger &quot;  /  &quot; gleich &quot;  /  &quot; höher&quot;</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>defaultsortdirection</td>
<td>Gibt die Sortierrichtung an. Der Standardwert ist &quot; Aufsteigend &quot; . 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aufsteigend</td>
<td>Sortiert Aufsteigend.</td>
</tr>
<tr class="even">
<td>Absteigend</td>
<td>Sortiert absteigend.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
