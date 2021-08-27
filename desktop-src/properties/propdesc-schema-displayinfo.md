---
description: Gibt die Anzeigeinformationen einer Eigenschaft an.
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: displayInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0bbc3cf0f17d24672e30a110d95341c1cb902d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622086"
---
# <a name="displayinfo"></a>displayInfo

Gibt die Anzeigeinformationen einer Eigenschaft an. Es sollte nur ein [displayInfo-Element]() für jede [eigenschaftDescription vorhanden](./propdesc-schema-propertydescription.md)sein.

Wenn mehrere Elemente vorhanden sind, wird das letzte Element verwendet. Wenn kein [displayInfo-Element]() bereitgestellt wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

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
| [propertyDescription](./propdesc-schema-propertydescription.md) | [Stringformat](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [booleanFormat](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [Numberformat](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [dateTimeFormat](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [enumeratedList](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [drawControl](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [editControl](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [Filtercontrol](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | [queryControl](./propdesc-schema-querycontrol.md) (nur Windows Vista. Wird in Windows 7 und höher nicht unterstützt.) |



 

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
<td>defaultColumnWidth</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot; &quot; 20.</td>
</tr>
<tr class="even">
<td>displayType</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot; &quot; String. Gibt den Typ der Anzeigezeichenfolge an. Sobald sie hier festgelegt sind, werden die zugeordneten <strong>PROPDESC_DISPLAYTYPE</strong> Werte von <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription::GetDisplayType</strong></a>abgerufen. Die folgenden Typen sind gültig. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Zeichenfolge</td>
<td>Standard. Der Wert wird als Zeichenfolge angezeigt. Verwenden Sie &quot; stringFormat &quot; zum Formatieren. Die Methode gibt PDDT_STRING zurück.</td>
</tr>
<tr class="even">
<td>Number</td>
<td>Standardwert für numerische Eigenschaften. Der Wert wird als Zahl angezeigt. Verwenden Sie &quot; numberFormat &quot; zum Formatieren. Die Methode gibt PDDT_NUMBER zurück.</td>
</tr>
<tr class="odd">
<td>Boolean</td>
<td>Der Standardwert ist , wenn <typeInfo type=&quot;Boolean&quot;> . Der Wert wird als boolescher Wert angezeigt. Formatieren Sie &quot; &quot; booleanFormat. Die Methode gibt PDDT_BOOLEAN zurück.</td>
</tr>
<tr class="even">
<td>Datetime</td>
<td>Der Standardwert ist , wenn <typeInfo type=&quot;DateTime&quot;> . Der Wert wird als Datum oder Uhrzeit angezeigt. Verwenden Sie &quot; dateTimeFormat &quot; zum Formatieren. Die Methode gibt PDDT_DATETIME zurück.</td>
</tr>
<tr class="odd">
<td>Enumeration</td>
<td>Der Wert wird als Anzeigezeichenfolgenzuordnung angezeigt, die vom &quot; enumeratedList-Element bereitgestellt &quot; wird. Die Methode gibt PDDT_ENUMERATED zurück.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>Ausrichtung</td>
<td>Optional. Der Standardwert ist &quot; Left &quot; . 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Left</td>
<td>Standard. Links ausrichten.</td>
</tr>
<tr class="even">
<td>Zentrum</td>
<td>Richten Sie den Mittelpunkt aus.</td>
</tr>
<tr class="odd">
<td>Right</td>
<td>Rechts ausrichten.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>relativeDescriptionType</td>
<td>Optional. Der Standardwert ist &quot; &quot; Allgemein. Gibt an, wie zwei Werte dieser Eigenschaft beschrieben werden sollen, wenn sie miteinander verglichen werden. Im Fall von Gleichheit &quot; wird immer Same &quot; verwendet. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription::GetRelativeDescription</strong></a> und <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription::GetRelativeDescriptionType</strong></a> verwenden diesen Wert, um zu bestimmen, welche relativen Beschreibungsanzeigenamen verwendet werden sollen. 
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
<td>Standard. Verwendet &quot; unterschiedliche &quot;  /  &quot; &quot;  /  &quot; unterschiedliche &quot; .</td>
</tr>
<tr class="even">
<td>Date</td>
<td>Der Standardwert ist , wenn <typeInfo type=&quot;DateTime&quot;> . Verwendet &quot; früher Same Later oder &quot;  /  &quot; older &quot;  /  &quot; &quot; Same &quot; &quot;  /  &quot; &quot;  /  &quot; Newer &quot; oder &quot; sooner Same &quot;  /  &quot; &quot;  /  &quot; Later &quot; .</td>
</tr>
<tr class="odd">
<td>Size</td>
<td>Verwendet &quot; &quot;  /  &quot; kleinere, gleich &quot;  /  &quot; größere&quot;</td>
</tr>
<tr class="even">
<td>Anzahl</td>
<td>Verwendet &quot; &quot;  /  &quot; kleinere, gleich &quot;  /  &quot; größere&quot;</td>
</tr>
<tr class="odd">
<td>Revision</td>
<td>Verwendet &quot; früher &quot;  /  &quot; und &quot;  /  &quot; später&quot;</td>
</tr>
<tr class="even">
<td>Länge</td>
<td>Verwendet &quot; &quot;  /  &quot; kürzere, &quot;  /  &quot; längere Zeit&quot;</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Verwendet &quot; &quot;  /  &quot; kürzere, &quot;  /  &quot; längere Zeit&quot;</td>
</tr>
<tr class="even">
<td>Geschwindigkeit</td>
<td>Verwendet &quot; &quot;  /  &quot; langsameres &quot;  /  &quot; gleiches schnelleres&quot;</td>
</tr>
<tr class="odd">
<td>Rate</td>
<td>Verwendet &quot; langsamer &quot;  /  &quot; und &quot;  /  &quot; schneller.&quot;</td>
</tr>
<tr class="even">
<td>Rating</td>
<td>Verwendet &quot; einen &quot;  /  &quot; niedrigeren gleichen &quot;  /  &quot; höheren&quot;</td>
</tr>
<tr class="odd">
<td>Priorität</td>
<td>Verwendet &quot; einen &quot;  /  &quot; niedrigeren gleichen &quot;  /  &quot; höheren&quot;</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>defaultSortDirection</td>
<td>Gibt die Sortierrichtung an. Der Standardwert ist &quot; &quot; Aufsteigend. 
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
<td>Sortiert aufsteigend.</td>
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



 

 

 
