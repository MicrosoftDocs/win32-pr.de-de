---
description: Definiert einen Zähler.
ms.assetid: 8f1338c0-7ea6-4d0c-af71-51012973e4a0
title: Komplexer Indikatortyp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 754b72d47e4fecbc5de3697cbec255251714885835a2ec429210c9ce5f489c77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793754"
---
# <a name="counter-complex-type"></a>Komplexer Indikatortyp

Definiert einen Zähler.

``` syntax
<xs:complexType name="counter">
    <xs:choice
        minOccurs="0"
        maxOccurs="1"
    >
        <xs:element name="counterAttributes"
            type="man:counterAttributes"
        >
            <xs:key name="uniqueCounterAttributeName">
                <xs:selector
                    xpath="./man:counterAttribute"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="id"
        type="man:UInt32Type"
        use="required"
     />
    <xs:attribute name="uri"
        type="xs:anyURI"
        use="required"
     />
    <xs:attribute name="name"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:maxLength
                    value="1023"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="description"
        type="xs:string"
        use="optional"
     />
    <xs:attribute name="type"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="perf_counter_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer"
                 />
                <xs:enumeration
                    value="perf_counter_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_large_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_100ns_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_obj_time_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_bulk_count"
                 />
                <xs:enumeration
                    value="perf_counter_text"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_sample_fraction"
                 />
                <xs:enumeration
                    value="perf_sample_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer_inv"
                 />
                <xs:enumeration
                    value="perf_sample_base"
                 />
                <xs:enumeration
                    value="perf_average_timer"
                 />
                <xs:enumeration
                    value="perf_average_base"
                 />
                <xs:enumeration
                    value="perf_average_bulk"
                 />
                <xs:enumeration
                    value="perf_obj_time_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_base"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_large_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_raw_base"
                 />
                <xs:enumeration
                    value="perf_large_raw_base"
                 />
                <xs:enumeration
                    value="perf_elapsed_time"
                 />
                <xs:enumeration
                    value="perf_counter_delta"
                 />
                <xs:enumeration
                    value="perf_counter_large_delta"
                 />
                <xs:enumeration
                    value="perf_precision_system_timer"
                 />
                <xs:enumeration
                    value="perf_precision_100ns_timer"
                 />
                <xs:enumeration
                    value="perf_precision_object_timer"
                 />
                <xs:enumeration
                    value="perf_counter_composite"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="baseID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="detailLevel"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="standard"
                 />
                <xs:enumeration
                    value="advanced"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="defaultScale"
        use="optional"
        default="0"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:integer"
            >
                <xs:minInclusive
                    value="-10"
                 />
                <xs:maxInclusive
                    value="10"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="aggregate"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="sum"
                 />
                <xs:enumeration
                    value="avg"
                 />
                <xs:enumeration
                    value="max"
                 />
                <xs:enumeration
                    value="min"
                 />
                <xs:enumeration
                    value="undefined"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="perfTimeID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="perfFreqID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="multiCounterID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="struct"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="field"
        type="man:CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element               | type                                                                                 | Beschreibung                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| **counterAttributes** | [**man:counterAttributes**](performance-counters-counterattributes-complex-type.md) | Listet die eindeutigen Attribute auf, die angeben, wie die Indikatordaten in einer Consumeranwendung angezeigt werden.<br/> |



## <a name="attributes"></a>Attributes



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>type</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>aggregate</td>

<td>Die aggregation-Funktion, die angewendet werden soll, wenn das <strong>Instances-Attribut</strong> von <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> globalAggregate, multipleAggregate oder globalAggregateHistory ist. Es folgen die möglichen Aggregationsfunktionen, die Sie anwenden können:<br/> <dl> <dt><span id="max"></span><span id="MAX"></span>Max</dt> <dd> Der maximale Indikatorwert wird zurückgegeben.<br/> </dd> <dt><span id="min"></span><span id="MIN"></span>Min</dt> <dd> Der minimale Indikatorwert wird zurückgegeben.<br/> </dd> <dt><span id="avg"></span><span id="AVG"></span>Avg</dt> <dd> Der durchschnittliche Indikatorwert wird zurückgegeben.<br/> </dd> <dt><span id="sum"></span><span id="SUM"></span>Summe</dt> <dd> Die Summe der Indikatorwerte wird zurückgegeben.<br/> </dd> <dt><span id="undefined"></span><span id="UNDEFINED"></span>Undefined</dt> <dd> Aggregieren Sie diesen Leistungsindikator nicht.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>baseID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td>Der Bezeichner eines anderen Zählers innerhalb desselben Indikatorsatzes, dessen Wert zum Berechnen des Werts dieses Zählers verwendet wird. Die folgenden Indikatortypen erfordern einen Basiszähler:<br/> <dl> <dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> <dd> Erfordert den PERF_AVERAGE_BASE Basisindikator.<br/> </dd> <dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> <dd> Erfordert den PERF_AVERAGE_BASE Basisindikator.<br/> </dd> <dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> <dd> Erfordert den PERF_COUNTER_MULTI_BASE Basiszähler.<br/> </dd> <dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> <dd> Erfordert den PERF_LARGE_RAW_BASE Basisindikator.<br/> </dd> <dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> <dd> Erfordert den PERF_LARGE_RAW_BASE Basisindikator.<br/> </dd> <dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> <dd> Erfordert den PERF_RAW_BASE Basiszähler.<br/> </dd> <dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> <dd> Erfordert den PERF_SAMPLE_BASE Basisindikator.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td>defaultScale</td>

<td>Der Skalierungsfaktor, der auf den Indikatorwert angewendet werden soll (Faktor * Indikatorwert). Der Standardwert ist 0 (null), wenn keine Skalierung angewendet wird. Gültige Werte liegen zwischen 10 und 10 (0,0000000001 bis 1000000000). Wenn dieser Wert 0 (null) ist, ist der Skalierungswert 1. wenn dieser Wert 1 ist, ist der Skalierungswert 10; wenn dieser Wert 1 ist, ist der Skalierungswert .10; Und so weiter.<br/></td>
</tr>
<tr class="even">
<td>description</td>
<td><strong>xs:string</strong></td>
<td>Eine kurze Beschreibung des Leistungsindikators. Sie müssen dieses Attribut nicht angeben, wenn der Leistungsindikator das <a href="performance-counters-counterattribute-complex-type.md"><strong>NoDisplay-Attribut</strong></a> enthält.<br/></td>
</tr>
<tr class="odd">
<td>detailLevel</td>

<td>Gibt die Zielgruppe für die Indikatordetails an. Folgende Werte sind möglich:<br/> <dl> <dt><span id="standard"></span><span id="STANDARD"></span>Standard</dt> <dd> Zeigt Details zum Leistungsindikator an, den ein typischer Benutzer versteht.<br/> </dd> <dt><span id="advanced"></span><span id="ADVANCED"></span>Erweiterte</dt> <dd> Zeigt Details zum Leistungsindikator an, die nur ein erweiterter Benutzer versteht.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>Feld</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></td>
<td>Der Name eines Felds innerhalb der Struktur, die den Zählerwert enthält. Dieses Attribut ist für Benutzermodusanbieter nicht zulässig.<br/></td>
</tr>
<tr class="odd">
<td>id</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td>Eine eindeutige Zahl, die den Indikator innerhalb des Indikatorensatzes identifiziert.<br/></td>
</tr>
<tr class="even">
<td>multiCounterID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td>Der Bezeichner eines anderen Indikators innerhalb desselben Indikatorsatzes, dessen Multiplikatorwert zum Berechnen des Werts dieses Zählers verwendet wird. Die folgenden Indikatortypen erfordern einen Multiplikatorwert. Der Indikator, auf den verwiesen wird, muss vom Typ PERF_COUNTER_RAWCOUNT sein.<br/>
<ul>
<li>PERF_COUNTER_MULTI_TIMER</li>
<li>PERF_COUNTER_MULTI_TIMER_INV</li>
<li>PERF_100NSEC_MULTI_TIMER</li>
<li>PERF_100NSEC_MULTI_TIMER_INV</li>
</ul></td>
</tr>
<tr class="odd">
<td>name</td>

<td>Der Name des Leistungsindikators. Der Name muss eindeutig und kleiner als 1.024 Zeichen sein. Beim Namen wird die Groß- und Kleinschreibung berücksichtigt. Sie müssen dieses Attribut nicht angeben, wenn der Leistungsindikator das <a href="performance-counters-counterattribute-complex-type.md"><strong>NoDisplay-Attribut</strong></a> enthält.<br/></td>
</tr>
<tr class="even">
<td>perfFreqID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td>Der Bezeichner eines anderen Zählers innerhalb desselben Indikatorensatzes, dessen Frequency-Wert zum Berechnen des Werts dieses Zählers verwendet wird. Die folgenden Indikatortypen erfordern eine Häufigkeit. Der PERF_COUNTER_LARGE_RAWCOUNT Indikatortyp enthält den Zeitstempelwert.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="odd">
<td>perfTimeID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td>Der Bezeichner eines anderen Zählers innerhalb desselben Indikatorsatzes, dessen Zeitstempelwert zum Berechnen des Werts dieses Zählers verwendet wird. Die folgenden Indikatortypen erfordern einen Zeitstempel. Der PERF_COUNTER_LARGE_RAWCOUNT Indikatortyp enthält den Zeitstempelwert.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="even">
<td>struct</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></td>
<td>Der Name eines Strukturelements, das diesen Indikatorwert enthält. Dieses Attribut ist für Benutzermodusanbieter nicht zulässig.<br/></td>
</tr>
<tr class="odd">
<td>Symbol</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></td>
<td>Ein symbolischer Name, der den Zähler identifiziert. Das <a href="ctrpp.md">CTRPP-Tool</a> erstellt eine Konstante, die Sie verwenden können, wenn Sie Funktionen aufrufen, die einen Indikatorbezeichner erfordern (z. B. <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>). Der Name der Konstante ist der symbolische Name.<br/></td>
</tr>
<tr class="even">
<td>Type</td>

<td>Der Name des Indikatortyps. Mögliche Werte finden Sie im obigen Syntaxblock. Ausführliche Informationen zu den einzelnen Typen finden Sie im Windows 2003-Bereitstellungshandbuch unter <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Indikatortypen.</a> Bei dem Namen muss die Groß-/Kleinschreibung beachtet werden. <br/></td>
</tr>
<tr class="odd">
<td>uri</td>
<td><strong>xs:anyURI</strong></td>
<td>Ein eindeutiger uniformer Ressourcenbezeichner, mit dem Benutzer Indikatorwerte von einem beliebigen Speicherort abrufen können.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Hinweise

Um Abwärtskompatibilität zu gewährleisten, sollte jeder Indikator im Indikatorensatz die gleichen **perfFreqID-** und **perfTimeID-Werte** angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

