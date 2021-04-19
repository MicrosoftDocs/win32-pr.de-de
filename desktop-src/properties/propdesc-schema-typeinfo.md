---
description: Gibt die Typinformationen einer Eigenschaft an.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: TypeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356631"
---
# <a name="typeinfo"></a>TypeInfo

Gibt die Typinformationen einer Eigenschaft an. Es darf nur ein [TypeInfo]() -Element für jede [propertydescription](./propdesc-schema-propertydescription.md)vorhanden sein. Dieses Element wurde für Windows 7 geändert.

Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet. Wenn kein [TypeInfo]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.

## <a name="syntax-for-windows-7"></a>Syntax für Windows 7


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                   | Untergeordnete Elemente |
|------------------------------------------------------------------|----------------|
| [propertydescription](./propdesc-schema-propertydescription.md) | Keine           |



 

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
<td>type</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot; Any &quot; . Gibt den Typ der Eigenschaft an. Die folgenden Typen sind gültig, und die zugehörigen Variant-Typen werden von <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>ipropertydescription:: GetPropertyType</strong></a>abgerufen. 
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Any</td>
<td>Standard. Das Eigenschafts Subsystem erzwingt oder wandelt den Eigenschafts Wert nicht um. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>Ipropertydescription:: GetPropertyType</strong></a> gibt VT_NULL zurück. Unabhängigen Softwareanbietern (ISVs) wird dringend empfohlen, einen Typ bereitzustellen, anstatt diesen Standardwert zu überschreiten.</td>
</tr>
<tr class="even">
<td>Null</td>
<td>Für diese Eigenschaft ist kein Wert vorhanden. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>Ipropertydescription:: GetPropertyType</strong></a> gibt VT_NULL zurück.</td>
</tr>
<tr class="odd">
<td>String</td>
<td>Der Wert muss eine VT_LPWSTR sein, die eine Unicode-Zeichenfolge ist, die durch einen NULL-Verweis beendet wird.</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Der Wert muss ein VT_BOOL sein, bei dem es sich um einen booleschen Wert handelt.</td>
</tr>
<tr class="odd">
<td>Byte</td>
<td>Der Wert muss ein VT_UI1 sein, d. h. ein Byte.</td>
</tr>
<tr class="even">
<td>Buffer</td>
<td>Der Wert muss ein VT_UI1 sein | VT_VECTOR Puffer bytes.</td>
</tr>
<tr class="odd">
<td>Int16</td>
<td>Der Wert muss eine VT_I2 sein, bei der es sich um eine 16-Bit-Ganzzahl handelt.</td>
</tr>
<tr class="even">
<td>UInt16</td>
<td>Der Wert muss eine VT_UI2 sein, bei der es sich um eine 16-Bit-Ganzzahl ohne Vorzeichen handelt.</td>
</tr>
<tr class="odd">
<td>Int32</td>
<td>Der Wert muss eine VT_I4 sein, eine ganze Zahl mit 32 Bit.</td>
</tr>
<tr class="even">
<td>UInt32</td>
<td>Der Wert muss eine VT_UI4 sein, bei der es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen handelt.</td>
</tr>
<tr class="odd">
<td>Int64</td>
<td>Der Wert muss eine VT_I8 sein, eine ganze Zahl mit 64 Bit.</td>
</tr>
<tr class="even">
<td>UInt64</td>
<td>Der Wert muss eine VT_UI8 sein, bei der es sich um eine 64-Bit-Ganzzahl ohne Vorzeichen handelt.</td>
</tr>
<tr class="odd">
<td>Double</td>
<td>Der Wert muss eine VT_R8 sein, bei der es sich um einen Double-Wert handelt.</td>
</tr>
<tr class="even">
<td>Datetime</td>
<td>Der Wert muss eine VT_FILETIME sein, die eine <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>ist.</td>
</tr>
<tr class="odd">
<td>GUID</td>
<td>Der Wert muss eine VT_CLSID sein, bei der es sich um einen Klassen Bezeichner (CLSID) handelt.</td>
</tr>
<tr class="even">
<td>Blob</td>
<td>Der Wert muss ein VT_BLOB sein, bei dem es sich um ein Byte mit Längen Präfix handelt.</td>
</tr>
<tr class="odd">
<td>Datenstrom</td>
<td>Der Wert muss ein VT_STREAM sein, bei dem es sich um ein Objekt handelt, das <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>implementiert.</td>
</tr>
<tr class="even">
<td>Zwischenablage</td>
<td>Der Wert muss eine VT_CF sein, bei der es sich um ein Zwischenablage Format handelt.</td>
</tr>
<tr class="odd">
<td>Object</td>
<td>Der Wert muss ein VT_UNKNOWN sein, bei dem es sich um ein Objekt handelt, das <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>implementiert.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>groupingrange</td>
<td>Dies ist optional. Der Standardwert ist &quot; diskret &quot; . Gibt an, wie die-Eigenschaft angezeigt wird, wenn eine Ansicht nach dieser Eigenschaft gruppiert wird. Nachdem diese Werte hier festgelegt wurden, werden Sie von <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>ipropertydescription:: getgroupingrange</strong></a>abgerufen. Die folgenden Typen sind gültig.

<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Discrete</td>
<td>Standard. Zeigt einzelne Werte an.</td>
</tr>
<tr class="even">
<td>Alphanumerisch</td>
<td>Zeigt statische alphanumerische Bereiche für-Werte an.</td>
</tr>
<tr class="odd">
<td>Size</td>
<td>Zeigt statische Größenbereiche für Werte an.</td>
</tr>
<tr class="even">
<td>Date</td>
<td>Zeigt Monat/Jahr-Gruppen an. Der Standardwert für Eigenschaften vom Typ = &quot; DateTime &quot; .</td>
</tr>
<tr class="odd">
<td>Timerelative</td>
<td>Wird in Zeit relativen Gruppen angezeigt.</td>
</tr>
<tr class="even">
<td>Dynamisch</td>
<td>Zeigt dynamisch erstellte Bereiche für die Werte an.</td>
</tr>
<tr class="odd">
<td>Percent</td>
<td>Zeigt Prozent Behälter an.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>isinnate</td>
<td>Öffentlich. Dies ist optional. Die Standardeinstellung lautet &quot;false&quot;. Gibt an, ob die Eigenschaft als "als" festgelegt Eine angeborene Eigenschaft ist eine Eigenschaft, die entweder aus dem Inhalt einer Datei oder aus anderen Ressourcen oder Systemen berechnet wird. System. Size ist beispielsweise eine angeborene Eigenschaft, die vom Datei System bereitgestellt wird. Das Ändern des Werts der-Eigenschaft in und von sich selbst bewirkt nichts. Weitere Beispiele sind System. Image. Dimensions und System.Doc-Umschlag. PageCount, die von Programmen basierend auf dem Inhalt der Datei berechnet werden, nicht basierend auf einer Benutzer veränderlichen Einstellung. Das Festlegen von isinnate = &quot; true bedeutet, dass &quot; der Benutzer diese Eigenschaft nicht direkt über ein Eigenschaften Steuerelement bearbeiten kann. Dieser Wert wird dem PDTF_ISINNATE Flag zugeordnet, das in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> definiert und in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>ipropertydescription:: gettypeer Flags</strong></a>verwendet wird.</td>
</tr>
<tr class="even">
<td>canbebereinigt</td>
<td><strong>Nur Windows Vista mit Service Pack 1 (SP1) und</strong>höher. Öffentlich. Dies ist optional. Wenn diese Eigenschaft auf true festgelegt &quot; &quot; ist, kann eine angeborene Eigenschaft gelöscht werden. Angeborene Eigenschaften, die aus anderen Eigenschaften berechnet werden, sind definitionsgemäß schreibgeschützt. Der Standardwert für dieses Attribut hängt vom <em>isinnate</em> -Wert ab.

<table>
<thead>
<tr class="header">
<th>isinnate</th>
<th>der Standardwert für canbebereinigt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>true</td>
<td>false</td>
</tr>
<tr class="even">
<td>false</td>
<td>true</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Eine Eigenschaft, deren <em>isinnate</em> -Wert &quot; false ist &quot; (was bedeutet, dass die Eigenschaft Lese-/Schreibzugriff ist), kann den <em>canbepuredwert</em> nicht auch auf &quot; false festlegen &quot; . Diese Einschränkung wird vom Betriebssystem erzwungen.
</blockquote>
</div>
<div>
 
</div>
<p>Obwohl dieses Attribut in Windows Vista mit Service Pack 1 (SP1) eingeführt wurde, ist eine. PropDesc-Datei mit diesem Attribut vor Windows Vista mit SP1 mit Windows Vista kompatibel. Das <em>canbepuring</em> -Attribut wird in dieser Situation einfach ignoriert.</p></td>
</tr>
<tr class="odd">
<td>multiplevalues</td>
<td>Öffentlich. Dies ist optional. Die Standardeinstellung lautet &quot;false&quot;. Gibt an, ob diese Eigenschaft mehrere Werte aufweisen kann. Dieser Wert wird dem PDTF_MULTIPLEVALUES Flag zugeordnet, das in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> definiert und in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>ipropertydescription:: gettypeer Flags</strong></a>verwendet wird. Dies wirkt sich auch darauf aus, ob VT_VECTOR oder auf den VarType-Wert des Eigenschafts Werts folgt.</td>
</tr>
<tr class="even">
<td>isGroup</td>
<td>Öffentlich. Dies ist optional. Die Standardeinstellung lautet &quot;false&quot;. Gibt an, ob die Eigenschaft eine Gruppen Überschrift ist. Eine Gruppen Überschrift wird in proplists strikt verwendet, hat keinen Wert, wird nie in einer Datei gespeichert und sollte auch über verfügen <typeInfo type=&quot;Null&quot;> . Eine Benutzeroberfläche im System verwendet proplists, um die Reihenfolge der anzuzeigenden Eigenschaften anzugeben. Diese proplists können Verweise auf Gruppen Überschriften (z. b. System. propgroup. Camera) enthalten, die der Benutzeroberfläche mitteilen, dass ein neuer Gruppenabschnitt (z. b. &quot; Kameraeinstellungen) gestartet werden soll &quot; . Eine Eigenschafts Beschreibung mit isGroup = &quot; true &quot; sollte einen angeben <labelInfo label=&quot;Some localized label&quot;> , andernfalls ist Sie keine nützliche Eigenschaft. Dieser Wert wird dem PDTF_ISGROUP Flag zugeordnet, das in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> definiert und in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>ipropertydescription:: gettypeer Flags</strong></a>verwendet wird.</td>
</tr>
<tr class="odd">
<td>aggregationType</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist Default &quot; &quot; . Gibt an, wie Aggregat Eigenschaften angezeigt werden, wenn mehrere Elemente ausgewählt werden. Nachdem diese Werte hier festgelegt wurden, werden Sie von <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>ipropertydescription:: getaggregationtype</strong></a> als <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>abgerufen. Die folgenden Typen sind gültig.

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
<td>Standard. Zeigt einen Platzhalter für <strong>mehrere Werte</strong> in der Benutzeroberfläche an. Dies ist die Standardeinstellung, wenn der <em>Typ</em> mit dem angegebenen <em>AggregationType</em>nicht kompatibel ist.</td>
</tr>
<tr class="even">
<td>First</td>
<td>Zeigt den Eigenschafts Wert des ersten Elements in der Auswahl oder Auflistung an.</td>
</tr>
<tr class="odd">
<td>SUM</td>
<td>Zeigt die Summe der numerischen Werte an. Nützlich für Eigenschaften wie z. b. System. Media. Duration oder System. Size. Dieser Wert ist nicht mit nicht numerischen Typen kompatibel.</td>
</tr>
<tr class="even">
<td>Average</td>
<td>Zeigt den Durchschnitt der numerischen Werte an. Nützlich für Eigenschaften wie z. b. System. Rating. Dieser Wert ist nicht mit nicht numerischen Typen kompatibel.</td>
</tr>
<tr class="odd">
<td>DateRange</td>
<td>Zeigt einen Datumsbereich an. Nützlich für Eigenschaften wie z. b. System. Photo. DateTaken. Dieser Wert ist mit Ausnahme von Type = &quot; DateTime nicht kompatibel &quot; und ist der Standardwert für Eigenschaften dieses Typs.</td>
</tr>
<tr class="even">
<td>Union</td>
<td>Zeigt eine Vereinigung aller Werte in der Auswahl oder Auflistung an. Die Reihenfolge, in der die Werte angezeigt werden, ist nicht definiert. Dieser Wert ist der Standardwert für Eigenschaften vom Typ = &quot; String &quot; und multiplevalues = &quot; true &quot; .</td>
</tr>
<tr class="odd">
<td>Maximum</td>
<td>Zeigt den maximalen Wert in der Auflistung an. Nützlich für Eigenschaften wie z. b. System. DateModified. Nicht mit nicht numerischen oder nicht Datums Typen kompatibel.</td>
</tr>
<tr class="even">
<td>Minimum</td>
<td>Zeigt den minimalen Wert in der Auflistung an. Nicht mit nicht numerischen oder nicht Datums Typen kompatibel.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>istreeproperty</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>isviewable</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot;false&quot;. Gibt an, ob diese Eigenschaft für den Benutzer sichtbar sein soll. Beispielsweise werden in der Benutzeroberfläche für die Spaltenauswahl nur die Eigenschaften angezeigt, die isviewable = &quot; true aufweisen &quot; . Bei der Ausnahme handelt es sich um eine Benutzeroberfläche, die durch eine proplist gesteuert wird, die immer die-Eigenschaft anzeigt. Wenn Sie über eine Eigenschaft verfügen, die nur für das überführen von Daten zwischen zwei Objekten vorgesehen ist und nie vom Benutzer angezeigt werden soll, sollte dieses Attribut "false" lauten. Dieser Wert wird dem PDTF_ISVIEWABLE Flag zugeordnet, das in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> definiert und in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>ipropertydescription:: gettypeer Flags</strong></a>verwendet wird.</td>
</tr>
<tr class="even">
<td>isquerable</td>
<td>Nur Windows Vista. Wird in Windows 7 und höher nicht unterstützt. Öffentlich. Dies ist optional. Der Standardwert ist &quot;false&quot;. Gibt an, ob diese Eigenschaft in der Such Abfrage-Generator-Benutzeroberfläche verfügbar sein soll. Für eine Eigenschaft muss isviewable = true festgelegt sein, &quot; &quot; bevor isquervable = &quot; true &quot; respektiert wird. Dieser Wert wird dem PDTF_ISQUERYABLE Flag zugeordnet, das in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> definiert und in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>ipropertydescription:: gettypeer Flags</strong></a>verwendet wird.</td>
</tr>
<tr class="odd">
<td>searchrawvalue</td>
<td><strong>Windows 7 und höher.</strong> Öffentlich. Dies ist optional. Der Standardwert ist &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>includeinfulltextquery</td>
<td>Nur Windows Vista. Wird in Windows 7 und höher nicht unterstützt. Öffentlich. Dies ist optional. Der Standardwert ist &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>conditionType</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot; String &quot; . Gibt einen Hinweis für die Such Abfrage-Generator Benutzeroberfläche an, damit die Liste möglicher Bedingungs Operatoren innerhalb eines Prädikats bestimmt werden kann. Die folgenden Werte werden erkannt. 
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
<td>Standard. Die folgenden Operatoren werden verwendet: &quot; ist &quot; , &quot; ist nicht &quot; , &quot; &lt; &quot; , &quot; &gt; &quot; , &quot; <= &quot; , &quot; >= &quot; , &quot; beginnt mit &quot; , &quot; endet mit &quot; , &quot; enthält, enthält nicht, &quot; &quot; &quot; &quot; entspricht &quot; .</td>
</tr>
<tr class="even">
<td>Number</td>
<td>Standardwert für numerische Eigenschaften. Die folgenden Operatoren werden verwendet: ist &quot; gleich &quot; , ist &quot; nicht gleich &quot; , &quot; ist kleiner als &quot; , &quot; ist größer als &quot; , &quot; ist kleiner als oder gleich &quot; , &quot; ist größer als oder gleich &quot; .</td>
</tr>
<tr class="odd">
<td>Datetime</td>
<td>Der Standardwert für Eigenschaften vom Typ = &quot; DateTime &quot; . Die folgenden Operatoren werden verwendet: &quot; ist &quot; , &quot; ist nicht &quot; , &quot; ist vor &quot; , &quot; ist after &quot; , &quot; ist vor, ist &quot; jedoch, &quot; ist after, aber enthält &quot; .</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Der Standardwert für Eigenschaften vom Typ = &quot; boolescher Wert &quot; . Identisch mit der Zahl.</td>
</tr>
<tr class="odd">
<td>Size</td>
<td>Identisch mit der Zahl.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>DefaultOperation</td>
<td>Öffentlich. Dies ist optional. Der Standardwert ist &quot; gleich &quot; . Gibt einen Hinweis für das Such Abfrage-Generator Tool an, damit der Standard Operator bestimmt werden kann. Die folgenden Werte sind möglich:

<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Equal</td>
<td>Standard. Gibt ein entsprechendes an.</td>
</tr>
<tr class="even">
<td>NotEqual</td>
<td>Gibt nicht äquivalent an.</td>
</tr>
<tr class="odd">
<td>LessThan</td>
<td>Gibt weniger als an.</td>
</tr>
<tr class="even">
<td>GreaterThan</td>
<td>Der Standardwert für die Eigenschaften von ConditionType = &quot; size &quot; . Gibt einen größer als an.</td>
</tr>
<tr class="odd">
<td>Enthält</td>
<td>Der Standardwert für die Eigenschaften von ConditionType = &quot; String &quot; . Gibt die Aufnahme an.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
