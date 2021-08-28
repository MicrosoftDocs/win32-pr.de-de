---
description: Gibt die Typinformationen einer Eigenschaft an.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: Typeinfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a70c6eeaee63bcb99ee19217ccff5d3ff7086a2
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632168"
---
# <a name="typeinfo"></a>Typeinfo

Gibt die Typinformationen einer Eigenschaft an. Für jede [eigenschaftDescription](./propdesc-schema-propertydescription.md)sollte nur ein [typeInfo-Element]() vorhanden sein. Dieses Element wurde für Windows 7 geändert.

Wenn mehrere Elemente vorhanden sind, wird das letzte Element verwendet. Wenn kein [typeInfo-Element]() bereitgestellt wird, werden die Standardattributeinstellungen auf die Eigenschaftenbeschreibung angewendet.

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
| [propertyDescription](./propdesc-schema-propertydescription.md) | Keine           |



 

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col  />
<col  />
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
<td>Öffentlich. Optional. Der Standardwert ist &quot; &quot; Beliebig. Gibt den Typ der Eigenschaft an. Die folgenden Typen sind gültig, und ihre zugeordneten Variantentypen werden von <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a>abgerufen. 
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
<td>Standard. Das Eigenschaftensubsystem erzwingt oder erzwingt den Eigenschaftswert nicht. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> gibt VT_NULL zurück. Unabhängigen Softwareherstellern (INDEPENDENT Software Vendors, ISVs) wird dringend empfohlen, einen Typ bereitzustellen, anstatt auf diese Standardeinstellung zurückweichen zu müssen.</td>
</tr>
<tr class="even">
<td>Null</td>
<td>Für diese Eigenschaft ist kein Wert vorhanden. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> gibt VT_NULL zurück.</td>
</tr>
<tr class="odd">
<td>Zeichenfolge</td>
<td>Der Wert muss ein VT_LPWSTR sein, bei dem es sich um eine Unicode-Zeichenfolge handelt, die durch einen NULL-Verweis beendet wird.</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Der Wert muss ein VT_BOOL sein, bei dem es sich um einen booleschen Wert handelt.</td>
</tr>
<tr class="odd">
<td>Byte</td>
<td>Der Wert muss ein VT_UI1 sein, bei dem es sich um ein Byte handelt.</td>
</tr>
<tr class="even">
<td>Buffer</td>
<td>Der Wert muss ein VT_UI1 | VT_VECTOR Puffer von Bytes.</td>
</tr>
<tr class="odd">
<td>Int16</td>
<td>Der Wert muss ein VT_I2 sein, bei dem es sich um eine 16-Bit-Ganzzahl handelt.</td>
</tr>
<tr class="even">
<td>UInt16</td>
<td>Der Wert muss ein VT_UI2 sein, bei dem es sich um eine 16-Bit-Ganzzahl ohne Vorzeichen handelt.</td>
</tr>
<tr class="odd">
<td>Int32</td>
<td>Der Wert muss ein VT_I4 sein, bei dem es sich um eine 32-Bit-Ganzzahl handelt.</td>
</tr>
<tr class="even">
<td>UInt32</td>
<td>Der Wert muss ein VT_UI4 sein, bei dem es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen handelt.</td>
</tr>
<tr class="odd">
<td>Int64</td>
<td>Der Wert muss ein VT_I8 sein, bei dem es sich um eine 64-Bit-Ganzzahl handelt.</td>
</tr>
<tr class="even">
<td>UInt64</td>
<td>Der Wert muss ein VT_UI8 sein, bei dem es sich um eine 64-Bit-Ganzzahl ohne Vorzeichen handelt.</td>
</tr>
<tr class="odd">
<td>Double</td>
<td>Der Wert muss ein VT_R8 sein, was ein Double ist.</td>
</tr>
<tr class="even">
<td>Datetime</td>
<td>Der Wert muss ein VT_FILETIME sein, bei dem es sich um einen <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME-Wert</strong></a>handelt.</td>
</tr>
<tr class="odd">
<td>Guid</td>
<td>Der Wert muss ein VT_CLSID sein, bei dem es sich um einen Klassenbezeichner (CLSID) handelt.</td>
</tr>
<tr class="even">
<td>Blob</td>
<td>Der Wert muss ein VT_BLOB sein, bei dem es sich um Bytes mit Längenpräfix handelt.</td>
</tr>
<tr class="odd">
<td>STREAM</td>
<td>Der Wert muss ein VT_STREAM sein, bei dem es sich um ein Objekt handelt, das <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>implementiert.</td>
</tr>
<tr class="even">
<td>Zwischenablage</td>
<td>Der Wert muss ein VT_CF sein, bei dem es sich um ein Zwischenablageformat handelt.</td>
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
<td>groupingRange</td>
<td>Optional. Der Standardwert ist &quot; &quot; Discrete. Gibt an, wie die Eigenschaft angezeigt wird, wenn eine Sicht nach dieser Eigenschaft gruppiert wird. Sobald diese Werte hier festgelegt sind, werden sie von <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription::GetGroupingRange</strong></a>abgerufen. Die folgenden Typen sind gültig.

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
<td>Zeigt statische alphanumerische Bereiche für Werte an.</td>
</tr>
<tr class="odd">
<td>Size</td>
<td>Zeigt statische Größenbereiche für Werte an.</td>
</tr>
<tr class="even">
<td>Date</td>
<td>Zeigt Monats-/Jahresgruppen an. Standardwert für Eigenschaften vom Typ = &quot; DateTime &quot; .</td>
</tr>
<tr class="odd">
<td>TimeRelative</td>
<td>Wird in zeitbezogenen Gruppen angezeigt.</td>
</tr>
<tr class="even">
<td>Dynamisch</td>
<td>Zeigt dynamisch erstellte Bereiche für die Werte an.</td>
</tr>
<tr class="odd">
<td>Percent</td>
<td>Zeigt Prozent-Buckets an.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>isInnate</td>
<td>Öffentlich. Optional. Die Standardeinstellung lautet &quot;false&quot;. Gibt an, ob die Eigenschaft als innate betrachtet wird. Eine innate-Eigenschaft ist eine Eigenschaft, die entweder aus dem Inhalt einer Datei oder aus anderen Ressourcen oder Systemen berechnet wird. System.Size ist beispielsweise eine vom Dateisystem bereitgestellte innate-Eigenschaft. Das Ändern des Werts der -Eigenschaft in und selbst führt zu nichts. Weitere Beispiele sind System.Image.Dimensions und System.Document. PageCount, die von Programmen basierend auf dem Inhalt der Datei berechnet werden, nicht basierend auf einer vom Benutzer veränderbaren Einstellung. Das Festlegen von isInnate= &quot; true &quot; bedeutet, dass der Benutzer diese Eigenschaft nicht direkt über ein Eigenschaftensteuerelement bearbeiten kann. Dieser Wert wird dem in PDTF_ISINNATE-Flag PROPDESC_TYPE_FLAGS <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags verwendet.</strong></a> <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong></strong></a></td>
</tr>
<tr class="even">
<td>canBePurged</td>
<td><strong>Windows Vista mit Service Pack 1 (SP1) und höher.</strong> Öffentlich. Optional. Wenn diese Eigenschaft auf TRUE festgelegt ist, kann eine &quot; &quot; innierte Eigenschaft gelöscht werden. Innate-Eigenschaften, die aus anderen Eigenschaften berechnet werden, sind definitionsgemäß schreibgeschützt. Der Standardwert für dieses Attribut hängt vom <em>isInnate-Wert</em> ab.

<table>
<thead>
<tr class="header">
<th>isInnate</th>
<th>canBePurged-Standardwert</th>
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
Eine Eigenschaft, deren <em>isInnate-Wert</em> FALSE ist (d. h., die Eigenschaft ist &quot; &quot; lese-/schreibbar), kann den <em>canBePurged-Wert</em> nicht auch auf &quot; FALSE &quot; festlegen. Diese Einschränkung wird vom Betriebssystem erzwungen.
</blockquote>
</div>
<div>
 
</div>
<p>Obwohl dieses Attribut in Windows Vista mit Service Pack 1 (SP1) eingeführt wurde, ist eine PROPDESC-Datei, die dieses Attribut enthält, mit Windows Vista vor Windows Vista mit SP1 kompatibel. Das <em>canBePurged-Attribut</em> wird in dieser Situation einfach ignoriert.</p></td>
</tr>
<tr class="odd">
<td>multipleValues</td>
<td>Öffentlich. Optional. Die Standardeinstellung lautet &quot;false&quot;. Gibt an, ob diese Eigenschaft mehrere Werte enthalten kann. Dieser Wert wird dem in PROPDESC_TYPE_FLAGS <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong></strong></a> definierten und in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>verwendeten Flag "PDTF_MULTIPLEVALUES". Dies wirkt sich auch darauf VT_VECTOR, ob der WERT OR'd für vartype des Eigenschaftswerts ist.</td>
</tr>
<tr class="even">
<td>isGroup</td>
<td>Öffentlich. Optional. Die Standardeinstellung lautet &quot;false&quot;. Gibt an, ob die Eigenschaft eine Gruppenüberschrift ist. Eine Gruppenüberschrift wird streng in Proplists verwendet, hat keinen Wert, wird nie in einer Datei gespeichert und sollte auch über <typeInfo type=&quot;Null&quot;> verfügen. Einige Benutzeroberflächen im System verwenden Proplists, um die Reihenfolge der anzuzeigenden Eigenschaften anzugeben. Diese Proplists können Verweise auf Gruppenüberschriften (z.B. System.PropGroup.Camera) enthalten, die die Benutzeroberfläche anraten, einen neuen Gruppenabschnitt zu starten (z.B. &quot; Camera Einstellungen &quot; ). Eine Eigenschaftenbeschreibung mit isGroup= &quot; true &quot; sollte eine angeben, andernfalls ist sie <labelInfo label=&quot;Some localized label&quot;> keine nützliche Eigenschaft. Dieser Wert wird dem <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PDTF_ISGROUP-Flag</strong></a> PROPDESC_TYPE_FLAGS <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags verwendet.</strong></a></td>
</tr>
<tr class="odd">
<td>aggregationType</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot; Default &quot; . Gibt an, wie Aggregateigenschaften angezeigt werden, wenn mehrere Elemente ausgewählt werden. Nachdem diese Werte hier festgelegt wurden, werden sie von <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription::GetAggregationType</strong></a> als <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE.</strong></a> Im Folgenden finden Sie gültige Typen.

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
<td>Standard. Zeigt einen <strong>Platzhalter für mehrere</strong> Werte auf der Benutzeroberfläche an. Dies ist die Standardeinstellung, <em>wenn der Typ</em> nicht mit dem angegebenen <em>aggregationType kompatibel ist.</em></td>
</tr>
<tr class="even">
<td>First</td>
<td>Zeigt den Eigenschaftswert des ersten Elements in der Auswahl oder Auflistung an.</td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>Zeigt die Summe der numerischen Werte an. Nützlich für Eigenschaften wie System.Media.Duration oder System.Size. Dieser Wert ist nicht kompatibel mit nicht numerischen Typen.</td>
</tr>
<tr class="even">
<td>Average</td>
<td>Zeigt den Durchschnitt der numerischen Werte an. Nützlich für Eigenschaften wie System.Rating. Dieser Wert ist nicht kompatibel mit nicht numerischen Typen.</td>
</tr>
<tr class="odd">
<td>DateRange</td>
<td>Zeigt einen Datumsbereich an. Nützlich für Eigenschaften wie System.Photo.DateTaken. Dieser Wert ist mit nichts außer type= DateTime kompatibel und ist der Standardwert &quot; &quot; für Eigenschaften dieses Typs.</td>
</tr>
<tr class="even">
<td>Union</td>
<td>Zeigt eine Vereinigung aller Werte in der Auswahl oder Auflistung an. Die Reihenfolge, in der die Werte angezeigt werden, ist nicht definiert. Dieser Wert ist der Standardwert für Eigenschaften von type= &quot; String &quot; und multipleValues= &quot; true &quot; .</td>
</tr>
<tr class="odd">
<td>Maximum</td>
<td>Zeigt den Maximalwert in der Auflistung an. Nützlich für Eigenschaften wie System.DateModified. Nicht kompatibel mit nicht numerischen oder nicht datumsbasierten Typen.</td>
</tr>
<tr class="even">
<td>Minimum</td>
<td>Zeigt den Mindestwert in der Auflistung an. Nicht kompatibel mit nicht numerischen oder nicht datumsbasierten Typen.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>isTreeProperty</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>isViewable</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot;false&quot;. Gibt an, ob diese Eigenschaft für den Benutzer angezeigt werden soll. Die Benutzeroberfläche für die Spaltenwähler zeigt z. B. nur die Eigenschaften an, die isViewable= &quot; true &quot; aufweisen. Die Ausnahme ist die Benutzeroberfläche, die von einer Proplist gesteuert wird, die immer die -Eigenschaft zeigt. Wenn Sie über eine Eigenschaft verfügen, die nur dazu dient, Daten zwischen zwei Objekten zu verwahren und nie vom Benutzer angezeigt zu werden, sollte dieses Attribut false sein. Dieser Wert wird dem in PDTF_ISVIEWABLE-Flag PROPDESC_TYPE_FLAGS <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags verwendet.</strong></a> <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong></strong></a></td>
</tr>
<tr class="even">
<td>isQueryable</td>
<td>Windows Nur Vista. Wird in Windows 7 und höher nicht unterstützt. Öffentlich. Optional. Der Standardwert ist &quot;false&quot;. Gibt an, ob diese Eigenschaft auf der Suchoberfläche verfügbar sein Abfrage-Generator soll. Eine Eigenschaft muss isViewable= &quot; true &quot; haben, bevor isQueryable= &quot; true beachtet &quot; wird. Dieser Wert wird dem <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PDTF_ISQUERYABLE-Flag</strong></a> PROPDESC_TYPE_FLAGS <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags verwendet.</strong></a></td>
</tr>
<tr class="odd">
<td>searchRawValue</td>
<td><strong>Windows 7 und höher.</strong> Öffentlich. Optional. Der Standardwert ist &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>includeInFullTextQuery</td>
<td>Windows Nur Vista. Wird in Windows 7 und höher nicht unterstützt. Öffentlich. Optional. Der Standardwert ist &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>conditionType</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot; &quot; String. Gibt einen Hinweis auf die Benutzeroberfläche von Search Abfrage-Generator an, damit die Liste der möglichen Bedingungsoperatoren innerhalb eines Prädikats bestimmt werden kann. Die folgenden Werte werden erkannt. 
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
<td>Standard. Die folgenden Operatoren werden verwendet: &quot; ist , ist nicht , &quot; , &quot; , &quot; , &quot; &lt; &quot; &quot; &gt; &quot; &quot; <= &quot; &quot; >= &quot; beginnt mit , &quot; endet mit , enthält , enthält nicht , ist &quot; wie &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Number</td>
<td>Standardwert für numerische Eigenschaften. Die folgenden Operatoren werden verwendet: &quot; ist gleich &quot; , &quot; entspricht nicht , ist kleiner als &quot; , ist größer als , ist kleiner als oder gleich , &quot; ist größer oder gleich &quot; &quot; &quot; &quot; &quot; &quot; &quot; .</td>
</tr>
<tr class="odd">
<td>Datetime</td>
<td>Standardwert für Eigenschaften vom Typ = &quot; DateTime &quot; . Die folgenden Operatoren werden verwendet: &quot; ist , ist nicht , ist vor , ist nach &quot; , &quot; ist &quot; &quot; &quot; &quot; &quot; &quot; vor, enthält jedoch , ist &quot; nach , enthält jedoch &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Standardwert für Eigenschaften vom Typ = &quot; Boolescher &quot; Wert. Identisch mit Number.</td>
</tr>
<tr class="odd">
<td>Size</td>
<td>Identisch mit Number.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>defaultOperation</td>
<td>Öffentlich. Optional. Der Standardwert ist &quot; &quot; Gleich. Gibt einen Hinweis für das Search Abfrage-Generator Tool an, damit der Standardoperator bestimmt werden kann. Die folgenden Werte sind möglich:

<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gleich</td>
<td>Standard. Gibt eine Entsprechung an.</td>
</tr>
<tr class="even">
<td>NotEqual</td>
<td>Gibt an, dass nicht gleichwertig ist.</td>
</tr>
<tr class="odd">
<td>LessThan</td>
<td>Gibt kleiner als an.</td>
</tr>
<tr class="even">
<td>GreaterThan</td>
<td>Standardwert für Eigenschaften von conditionType= &quot; Size &quot; . Gibt größer als an.</td>
</tr>
<tr class="odd">
<td>Enthält</td>
<td>Standardwert für Eigenschaften von conditionType= &quot; String &quot; . Gibt Einschluss an.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
