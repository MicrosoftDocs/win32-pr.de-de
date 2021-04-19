---
description: Definiert einen-Counter.
ms.assetid: 8f1338c0-7ea6-4d0c-af71-51012973e4a0
title: komplexer Typ des Zählers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d591d4c23b626eaf2e2bfb10b528ff7c054507df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356167"
---
# <a name="counter-complex-type"></a>komplexer Typ des Zählers

Definiert einen-Counter.

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



| Element               | type                                                                                 | BESCHREIBUNG                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| **Counter-Attribute** | [**man: counterAttribute**](performance-counters-counterattributes-complex-type.md) | Listet die eindeutigen Attribute auf, die angeben, wie die gegen Daten in einer Consumeranwendung angezeigt werden.<br/> |



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
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>aggregate</td>

<td>Die Aggregations Funktion, die angewendet werden soll, wenn das <strong>instance</strong> -Attribut von <a href="performance-counters-counterset-complex-type.md"><strong>CounterSet</strong></a> Global Aggregate, MultipleAggregate oder globalaggregatehistory ist. Es folgen die möglichen Aggregations Funktionen, die Sie anwenden können:<br/> <dl> <dt><span id="max"></span><span id="MAX"></span>Max</dt> <dd> Der maximale Zählers Wert wird zurückgegeben.<br/> </dd> <dt><span id="min"></span><span id="MIN"></span>man</dt> <dd> Der minimale Zählers Wert wird zurückgegeben.<br/> </dd> <dt><span id="avg"></span><span id="AVG"></span>AVG</dt> <dd> Der durchschnittliche Leistungswert wird zurückgegeben.<br/> </dd> <dt><span id="sum"></span><span id="SUM"></span>Pauschalen</dt> <dd> Die Summe der Wert Werte wird zurückgegeben.<br/> </dd> <dt><span id="undefined"></span><span id="UNDEFINED"></span>definiert</dt> <dd> Diesen Zählers nicht aggregieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>BaseID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man: UInt32Type</strong></a></td>
<td>Der Bezeichner eines anderen Zählers innerhalb desselben Satz Satzes, dessen Wert verwendet wird, um den Wert dieses Leistungs Zählers zu berechnen. Die folgenden Counter-Typen erfordern einen Basis-Counter:<br/> <dl> <dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> <dd> Erfordert den PERF_AVERAGE_BASE Basis Zählers.<br/> </dd> <dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> <dd> Erfordert den PERF_AVERAGE_BASE Basis Zählers.<br/> </dd> <dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> <dd> Erfordert den PERF_COUNTER_MULTI_BASE Basis Zählers.<br/> </dd> <dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> <dd> Erfordert den PERF_LARGE_RAW_BASE Basis Zählers.<br/> </dd> <dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> <dd> Erfordert den PERF_LARGE_RAW_BASE Basis Zählers.<br/> </dd> <dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> <dd> Erfordert den PERF_RAW_BASE Basis Zählers.<br/> </dd> <dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> <dd> Erfordert den PERF_SAMPLE_BASE Basis Zählers.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td>DEFAULTSCALE</td>

<td>Der Skalierungsfaktor, der auf den Leistungs Zählers (Faktor *-Leistungswert) angewendet werden soll. Der Standardwert ist 0 (null), wenn keine Skala angewendet wird. Gültige Werte liegen im Bereich von 10 bis 10 (0,0000000001 bis 1 Milliarde). Wenn dieser Wert 0 (null) ist, ist der Skalierungs Wert 1. Wenn dieser Wert 1 ist, ist der Skalierungs Wert 10. Wenn dieser Wert 1 ist, ist der Skalierungs Wert. 10; Und so weiter.<br/></td>
</tr>
<tr class="even">
<td>description</td>
<td><strong>xs:string</strong></td>
<td>Eine kurze Beschreibung des Zählers. Sie müssen dieses Attribut nicht angeben, wenn der Counter das <a href="performance-counters-counterattribute-complex-type.md"><strong>nodisplay</strong></a> -Attribut enthält.<br/></td>
</tr>
<tr class="odd">
<td>detailLevel</td>

<td>Gibt die Zielgruppe für die Details des Zählers an. Folgende Werte sind möglich:<br/> <dl> <dt><span id="standard"></span><span id="STANDARD"></span>Norm</dt> <dd> Anzeigen von Details zum Gegenstand, die ein typischer Benutzer versteht.<br/> </dd> <dt><span id="advanced"></span><span id="ADVANCED"></span>führende</dt> <dd> Anzeigen von Details zum-Counter, die nur von einem erweiterten Benutzer verstanden werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>Feld</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man: csymboltype</strong></a></td>
<td>Der Name eines Felds in der Struktur, das den Wert des Zählers enthält. Dieses Attribut ist für benutzermodusanbieter nicht zulässig.<br/></td>
</tr>
<tr class="odd">
<td>id</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man: UInt32Type</strong></a></td>
<td>Eine eindeutige Zahl, die den Wert des Zählers innerhalb des Satz Satzes identifiziert.<br/></td>
</tr>
<tr class="even">
<td>multicounterid</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man: UInt32Type</strong></a></td>
<td>Der Bezeichner eines anderen Zählers innerhalb desselben Satz Satzes, dessen Multiplikatorwert verwendet wird, um den Wert dieses Leistungs Zählers zu berechnen. Die folgenden Counter-Typen erfordern einen Multiplikator-Wert. Der referenzierte Wert muss vom Typ "PERF_COUNTER_RAWCOUNT" sein.<br/>
<ul>
<li>PERF_COUNTER_MULTI_TIMER</li>
<li>PERF_COUNTER_MULTI_TIMER_INV</li>
<li>PERF_100NSEC_MULTI_TIMER</li>
<li>PERF_100NSEC_MULTI_TIMER_INV</li>
</ul></td>
</tr>
<tr class="odd">
<td>name</td>

<td>Der Name des Leistungsindikators. Der Name muss eindeutig und kleiner als 1.024 Zeichen sein. Beim Namen wird die Groß- und Kleinschreibung berücksichtigt. Sie müssen dieses Attribut nicht angeben, wenn der Counter das <a href="performance-counters-counterattribute-complex-type.md"><strong>nodisplay</strong></a> -Attribut enthält.<br/></td>
</tr>
<tr class="even">
<td>perffreqid</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man: UInt32Type</strong></a></td>
<td>Der Bezeichner eines anderen Zählers innerhalb desselben Satz Satzes, dessen Frequency-Wert verwendet wird, um den Wert dieses Leistungs Zählers zu berechnen. Die folgenden Counter-Typen erfordern eine Häufigkeit. Der PERF_COUNTER_LARGE_RAWCOUNT zähtertyp enthält den Zeitstempelwert.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="odd">
<td>perftimeid</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man: UInt32Type</strong></a></td>
<td>Der Bezeichner eines anderen Zählers innerhalb desselben Satz Satzes, dessen Zeitstempelwert verwendet wird, um den Wert dieses Zählers zu berechnen. Die folgenden Counter-Typen erfordern einen Zeitstempel. Der PERF_COUNTER_LARGE_RAWCOUNT zähtertyp enthält den Zeitstempelwert.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="even">
<td>struct</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man: csymboltype</strong></a></td>
<td>Der Name eines struct-Elements, das diesen Leistungswert enthält. Dieses Attribut ist für benutzermodusanbieter nicht zulässig.<br/></td>
</tr>
<tr class="odd">
<td>Symbol</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man: csymboltype</strong></a></td>
<td>Ein symbolischer Name, der den-Wert identifiziert. Das <a href="ctrpp.md">ctrpp</a> -Tool erstellt eine Konstante, die Sie verwenden können, wenn Sie Funktionen aufrufen, die einen Indikator Bezeichner erfordern (z. b. <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>perfincrementulongcountervalue</strong></a>). Der Name der Konstante ist der symbolische Name.<br/></td>
</tr>
<tr class="even">
<td>type</td>

<td>Der Name des Zählers. Mögliche Werte finden Sie im obigen Syntax Block. Ausführliche Informationen zu den einzelnen Typen finden Sie unter <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">counter Types</a> im Bereitstellungs Handbuch für Windows 2003. Beim Namen wird Groß-/Kleinschreibung beachtet. <br/></td>
</tr>
<tr class="odd">
<td>uri</td>
<td><strong>xs:anyURI</strong></td>
<td>Ein eindeutiger einheitlicher Ressourcen Bezeichner, mit dem Benutzer von einem beliebigen Speicherort Werte abrufen können.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Um Abwärtskompatibilität zu gewährleisten, sollte jeder Leistungs Monitor im Counter-Satz dieselben Werte für **perffreqid** und **perftimeid** angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

