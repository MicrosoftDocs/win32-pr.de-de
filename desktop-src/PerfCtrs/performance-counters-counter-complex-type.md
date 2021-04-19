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
# <a name="counter-complex-type"></a><span data-ttu-id="44cfe-103">komplexer Typ des Zählers</span><span class="sxs-lookup"><span data-stu-id="44cfe-103">counter Complex Type</span></span>

<span data-ttu-id="44cfe-104">Definiert einen-Counter.</span><span class="sxs-lookup"><span data-stu-id="44cfe-104">Defines a counter.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="44cfe-105">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44cfe-105">Child elements</span></span>



| <span data-ttu-id="44cfe-106">Element</span><span class="sxs-lookup"><span data-stu-id="44cfe-106">Element</span></span>               | <span data-ttu-id="44cfe-107">type</span><span class="sxs-lookup"><span data-stu-id="44cfe-107">Type</span></span>                                                                                 | <span data-ttu-id="44cfe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44cfe-108">Description</span></span>                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44cfe-109">**Counter-Attribute**</span><span class="sxs-lookup"><span data-stu-id="44cfe-109">**counterAttributes**</span></span> | [<span data-ttu-id="44cfe-110">**man: counterAttribute**</span><span class="sxs-lookup"><span data-stu-id="44cfe-110">**man:counterAttributes**</span></span>](performance-counters-counterattributes-complex-type.md) | <span data-ttu-id="44cfe-111">Listet die eindeutigen Attribute auf, die angeben, wie die gegen Daten in einer Consumeranwendung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="44cfe-111">Lists the unique attributes that specify how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="44cfe-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="44cfe-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="44cfe-113">Name</span><span class="sxs-lookup"><span data-stu-id="44cfe-113">Name</span></span></th>
<th><span data-ttu-id="44cfe-114">type</span><span class="sxs-lookup"><span data-stu-id="44cfe-114">Type</span></span></th>
<th><span data-ttu-id="44cfe-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44cfe-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="44cfe-116">aggregate</span><span class="sxs-lookup"><span data-stu-id="44cfe-116">aggregate</span></span></td>

<td><span data-ttu-id="44cfe-117">Die Aggregations Funktion, die angewendet werden soll, wenn das <strong>instance</strong> -Attribut von <a href="performance-counters-counterset-complex-type.md"><strong>CounterSet</strong></a> Global Aggregate, MultipleAggregate oder globalaggregatehistory ist.</span><span class="sxs-lookup"><span data-stu-id="44cfe-117">The aggregation function to apply if the <strong>instances</strong> attribute of <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> is globalAggregate, multipleAggregate, or globalAggregateHistory.</span></span> <span data-ttu-id="44cfe-118">Es folgen die möglichen Aggregations Funktionen, die Sie anwenden können:</span><span class="sxs-lookup"><span data-stu-id="44cfe-118">The following are the possible aggregation functions that you can apply:</span></span><br/> <dl> <span data-ttu-id="44cfe-119"><dt><span id="max"></span><span id="MAX"></span>Max</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-119"><dt><span id="max"></span><span id="MAX"></span>max</dt> </span></span><dd> <span data-ttu-id="44cfe-120">Der maximale Zählers Wert wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44cfe-120">The maximum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="44cfe-121"><dt><span id="min"></span><span id="MIN"></span>man</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-121"><dt><span id="min"></span><span id="MIN"></span>min</dt> </span></span><dd> <span data-ttu-id="44cfe-122">Der minimale Zählers Wert wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44cfe-122">The minimum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="44cfe-123"><dt><span id="avg"></span><span id="AVG"></span>AVG</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-123"><dt><span id="avg"></span><span id="AVG"></span>avg</dt> </span></span><dd> <span data-ttu-id="44cfe-124">Der durchschnittliche Leistungswert wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44cfe-124">The average counter value is returned.</span></span><br/> </dd> <span data-ttu-id="44cfe-125"><dt><span id="sum"></span><span id="SUM"></span>Pauschalen</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-125"><dt><span id="sum"></span><span id="SUM"></span>sum</dt> </span></span><dd> <span data-ttu-id="44cfe-126">Die Summe der Wert Werte wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44cfe-126">The sum of the counter values is returned.</span></span><br/> </dd> <span data-ttu-id="44cfe-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>definiert</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>undefined</dt> </span></span><dd> <span data-ttu-id="44cfe-128">Diesen Zählers nicht aggregieren.</span><span class="sxs-lookup"><span data-stu-id="44cfe-128">Do not aggregate this counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44cfe-129">BaseID</span><span class="sxs-lookup"><span data-stu-id="44cfe-129">baseID</span></span></td>
<td><span data-ttu-id="44cfe-130"><a href="performance-counters-uint32type-simple-type.md"><strong>man: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="44cfe-130"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="44cfe-131">Der Bezeichner eines anderen Zählers innerhalb desselben Satz Satzes, dessen Wert verwendet wird, um den Wert dieses Leistungs Zählers zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="44cfe-131">The identifier of another counter within the same counter set, whose value is used to calculate this counter's value.</span></span> <span data-ttu-id="44cfe-132">Die folgenden Counter-Typen erfordern einen Basis-Counter:</span><span class="sxs-lookup"><span data-stu-id="44cfe-132">The following counter types require a base counter:</span></span><br/> <dl> <span data-ttu-id="44cfe-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span></span><dd> <span data-ttu-id="44cfe-134">Erfordert den PERF_AVERAGE_BASE Basis Zählers.</span><span class="sxs-lookup"><span data-stu-id="44cfe-134">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="44cfe-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span></span><dd> <span data-ttu-id="44cfe-136">Erfordert den PERF_AVERAGE_BASE Basis Zählers.</span><span class="sxs-lookup"><span data-stu-id="44cfe-136">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="44cfe-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span></span><dd> <span data-ttu-id="44cfe-138">Erfordert den PERF_COUNTER_MULTI_BASE Basis Zählers.</span><span class="sxs-lookup"><span data-stu-id="44cfe-138">Requires the PERF_COUNTER_MULTI_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="44cfe-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="44cfe-140">Erfordert den PERF_LARGE_RAW_BASE Basis Zählers.</span><span class="sxs-lookup"><span data-stu-id="44cfe-140">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="44cfe-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span></span><dd> <span data-ttu-id="44cfe-142">Erfordert den PERF_LARGE_RAW_BASE Basis Zählers.</span><span class="sxs-lookup"><span data-stu-id="44cfe-142">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="44cfe-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="44cfe-144">Erfordert den PERF_RAW_BASE Basis Zählers.</span><span class="sxs-lookup"><span data-stu-id="44cfe-144">Requires the PERF_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="44cfe-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span></span><dd> <span data-ttu-id="44cfe-146">Erfordert den PERF_SAMPLE_BASE Basis Zählers.</span><span class="sxs-lookup"><span data-stu-id="44cfe-146">Requires the PERF_SAMPLE_BASE base counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="44cfe-147">DEFAULTSCALE</span><span class="sxs-lookup"><span data-stu-id="44cfe-147">defaultScale</span></span></td>

<td><span data-ttu-id="44cfe-148">Der Skalierungsfaktor, der auf den Leistungs Zählers (Faktor \*-Leistungswert) angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="44cfe-148">The scale factor to apply to the counter value (factor \* counter value).</span></span> <span data-ttu-id="44cfe-149">Der Standardwert ist 0 (null), wenn keine Skala angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="44cfe-149">The default is zero if no scale is applied.</span></span> <span data-ttu-id="44cfe-150">Gültige Werte liegen im Bereich von 10 bis 10 (0,0000000001 bis 1 Milliarde).</span><span class="sxs-lookup"><span data-stu-id="44cfe-150">Valid values range from  10 to 10 (0.0000000001 to 1000000000).</span></span> <span data-ttu-id="44cfe-151">Wenn dieser Wert 0 (null) ist, ist der Skalierungs Wert 1. Wenn dieser Wert 1 ist, ist der Skalierungs Wert 10. Wenn dieser Wert 1 ist, ist der Skalierungs Wert. 10; Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="44cfe-151">If this value is zero, the scale value is 1; if this value is 1, the scale value is 10; if this value is  1, the scale value is .10; and so on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44cfe-152">description</span><span class="sxs-lookup"><span data-stu-id="44cfe-152">description</span></span></td>
<td><span data-ttu-id="44cfe-153"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="44cfe-153"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="44cfe-154">Eine kurze Beschreibung des Zählers.</span><span class="sxs-lookup"><span data-stu-id="44cfe-154">A short description of the counter.</span></span> <span data-ttu-id="44cfe-155">Sie müssen dieses Attribut nicht angeben, wenn der Counter das <a href="performance-counters-counterattribute-complex-type.md"><strong>nodisplay</strong></a> -Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="44cfe-155">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="44cfe-156">detailLevel</span><span class="sxs-lookup"><span data-stu-id="44cfe-156">detailLevel</span></span></td>

<td><span data-ttu-id="44cfe-157">Gibt die Zielgruppe für die Details des Zählers an.</span><span class="sxs-lookup"><span data-stu-id="44cfe-157">Specifies the target audience for the counter details.</span></span> <span data-ttu-id="44cfe-158">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="44cfe-158">The following are the possible values:</span></span><br/> <dl> <span data-ttu-id="44cfe-159"><dt><span id="standard"></span><span id="STANDARD"></span>Norm</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-159"><dt><span id="standard"></span><span id="STANDARD"></span>standard</dt> </span></span><dd> <span data-ttu-id="44cfe-160">Anzeigen von Details zum Gegenstand, die ein typischer Benutzer versteht.</span><span class="sxs-lookup"><span data-stu-id="44cfe-160">Display details about the counter that a typical user would understand.</span></span><br/> </dd> <span data-ttu-id="44cfe-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>führende</dt> </span><span class="sxs-lookup"><span data-stu-id="44cfe-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>advanced</dt> </span></span><dd> <span data-ttu-id="44cfe-162">Anzeigen von Details zum-Counter, die nur von einem erweiterten Benutzer verstanden werden.</span><span class="sxs-lookup"><span data-stu-id="44cfe-162">Display details about the counter that only an advanced user would understand.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44cfe-163">Feld</span><span class="sxs-lookup"><span data-stu-id="44cfe-163">field</span></span></td>
<td><span data-ttu-id="44cfe-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>man: csymboltype</strong></a></span><span class="sxs-lookup"><span data-stu-id="44cfe-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="44cfe-165">Der Name eines Felds in der Struktur, das den Wert des Zählers enthält.</span><span class="sxs-lookup"><span data-stu-id="44cfe-165">The name of a field within the struct that contains the counter value.</span></span> <span data-ttu-id="44cfe-166">Dieses Attribut ist für benutzermodusanbieter nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="44cfe-166">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="44cfe-167">id</span><span class="sxs-lookup"><span data-stu-id="44cfe-167">id</span></span></td>
<td><span data-ttu-id="44cfe-168"><a href="performance-counters-uint32type-simple-type.md"><strong>man: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="44cfe-168"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="44cfe-169">Eine eindeutige Zahl, die den Wert des Zählers innerhalb des Satz Satzes identifiziert.</span><span class="sxs-lookup"><span data-stu-id="44cfe-169">A unique number that identifies the counter within the counter set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44cfe-170">multicounterid</span><span class="sxs-lookup"><span data-stu-id="44cfe-170">multiCounterID</span></span></td>
<td><span data-ttu-id="44cfe-171"><a href="performance-counters-uint32type-simple-type.md"><strong>man: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="44cfe-171"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="44cfe-172">Der Bezeichner eines anderen Zählers innerhalb desselben Satz Satzes, dessen Multiplikatorwert verwendet wird, um den Wert dieses Leistungs Zählers zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="44cfe-172">The identifier of another counter within the same counter set, whose multiplier value is used to calculate this counter's value.</span></span> <span data-ttu-id="44cfe-173">Die folgenden Counter-Typen erfordern einen Multiplikator-Wert.</span><span class="sxs-lookup"><span data-stu-id="44cfe-173">The following counter types require a multiplier value.</span></span> <span data-ttu-id="44cfe-174">Der referenzierte Wert muss vom Typ "PERF_COUNTER_RAWCOUNT" sein.</span><span class="sxs-lookup"><span data-stu-id="44cfe-174">The referenced counter must be of type PERF_COUNTER_RAWCOUNT.</span></span><br/>
<ul>
<li><span data-ttu-id="44cfe-175">PERF_COUNTER_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="44cfe-175">PERF_COUNTER_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="44cfe-176">PERF_COUNTER_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="44cfe-176">PERF_COUNTER_MULTI_TIMER_INV</span></span></li>
<li><span data-ttu-id="44cfe-177">PERF_100NSEC_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="44cfe-177">PERF_100NSEC_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="44cfe-178">PERF_100NSEC_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="44cfe-178">PERF_100NSEC_MULTI_TIMER_INV</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="44cfe-179">name</span><span class="sxs-lookup"><span data-stu-id="44cfe-179">name</span></span></td>

<td><span data-ttu-id="44cfe-180">Der Name des Leistungsindikators.</span><span class="sxs-lookup"><span data-stu-id="44cfe-180">The name of the counter.</span></span> <span data-ttu-id="44cfe-181">Der Name muss eindeutig und kleiner als 1.024 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="44cfe-181">The name must be unique and less than 1,024 characters.</span></span> <span data-ttu-id="44cfe-182">Beim Namen wird die Groß- und Kleinschreibung berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="44cfe-182">The name is case-sensitive.</span></span> <span data-ttu-id="44cfe-183">Sie müssen dieses Attribut nicht angeben, wenn der Counter das <a href="performance-counters-counterattribute-complex-type.md"><strong>nodisplay</strong></a> -Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="44cfe-183">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44cfe-184">perffreqid</span><span class="sxs-lookup"><span data-stu-id="44cfe-184">perfFreqID</span></span></td>
<td><span data-ttu-id="44cfe-185"><a href="performance-counters-uint32type-simple-type.md"><strong>man: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="44cfe-185"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="44cfe-186">Der Bezeichner eines anderen Zählers innerhalb desselben Satz Satzes, dessen Frequency-Wert verwendet wird, um den Wert dieses Leistungs Zählers zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="44cfe-186">The identifier of another counter within the same counter set, whose frequency value is used to calculate this counter's value.</span></span> <span data-ttu-id="44cfe-187">Die folgenden Counter-Typen erfordern eine Häufigkeit.</span><span class="sxs-lookup"><span data-stu-id="44cfe-187">The following counter types require a frequency.</span></span> <span data-ttu-id="44cfe-188">Der PERF_COUNTER_LARGE_RAWCOUNT zähtertyp enthält den Zeitstempelwert.</span><span class="sxs-lookup"><span data-stu-id="44cfe-188">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="44cfe-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="44cfe-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="44cfe-190">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="44cfe-190">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="44cfe-191">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="44cfe-191">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="44cfe-192">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="44cfe-192">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="44cfe-193">perftimeid</span><span class="sxs-lookup"><span data-stu-id="44cfe-193">perfTimeID</span></span></td>
<td><span data-ttu-id="44cfe-194"><a href="performance-counters-uint32type-simple-type.md"><strong>man: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="44cfe-194"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="44cfe-195">Der Bezeichner eines anderen Zählers innerhalb desselben Satz Satzes, dessen Zeitstempelwert verwendet wird, um den Wert dieses Zählers zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="44cfe-195">The identifier of another counter within the same counter set, whose time stamp value is used to calculate this counter's value.</span></span> <span data-ttu-id="44cfe-196">Die folgenden Counter-Typen erfordern einen Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="44cfe-196">The following counter types require a time stamp.</span></span> <span data-ttu-id="44cfe-197">Der PERF_COUNTER_LARGE_RAWCOUNT zähtertyp enthält den Zeitstempelwert.</span><span class="sxs-lookup"><span data-stu-id="44cfe-197">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="44cfe-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="44cfe-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="44cfe-199">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="44cfe-199">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="44cfe-200">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="44cfe-200">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="44cfe-201">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="44cfe-201">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44cfe-202">struct</span><span class="sxs-lookup"><span data-stu-id="44cfe-202">struct</span></span></td>
<td><span data-ttu-id="44cfe-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>man: csymboltype</strong></a></span><span class="sxs-lookup"><span data-stu-id="44cfe-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="44cfe-204">Der Name eines struct-Elements, das diesen Leistungswert enthält.</span><span class="sxs-lookup"><span data-stu-id="44cfe-204">The name of a struct element that contains this counter value.</span></span> <span data-ttu-id="44cfe-205">Dieses Attribut ist für benutzermodusanbieter nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="44cfe-205">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="44cfe-206">Symbol</span><span class="sxs-lookup"><span data-stu-id="44cfe-206">symbol</span></span></td>
<td><span data-ttu-id="44cfe-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>man: csymboltype</strong></a></span><span class="sxs-lookup"><span data-stu-id="44cfe-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="44cfe-208">Ein symbolischer Name, der den-Wert identifiziert.</span><span class="sxs-lookup"><span data-stu-id="44cfe-208">A symbolic name that identifies the counter.</span></span> <span data-ttu-id="44cfe-209">Das <a href="ctrpp.md">ctrpp</a> -Tool erstellt eine Konstante, die Sie verwenden können, wenn Sie Funktionen aufrufen, die einen Indikator Bezeichner erfordern (z. b. <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>perfincrementulongcountervalue</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="44cfe-209">The <a href="ctrpp.md">CTRPP</a> tool creates a constant that you can use when calling functions that require a counter identifier (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>).</span></span> <span data-ttu-id="44cfe-210">Der Name der Konstante ist der symbolische Name.</span><span class="sxs-lookup"><span data-stu-id="44cfe-210">The name of the constant is the symbolic name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44cfe-211">type</span><span class="sxs-lookup"><span data-stu-id="44cfe-211">type</span></span></td>

<td><span data-ttu-id="44cfe-212">Der Name des Zählers.</span><span class="sxs-lookup"><span data-stu-id="44cfe-212">The name of the counter type.</span></span> <span data-ttu-id="44cfe-213">Mögliche Werte finden Sie im obigen Syntax Block.</span><span class="sxs-lookup"><span data-stu-id="44cfe-213">For possible values, see the above syntax block.</span></span> <span data-ttu-id="44cfe-214">Ausführliche Informationen zu den einzelnen Typen finden Sie unter <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">counter Types</a> im Bereitstellungs Handbuch für Windows 2003.</span><span class="sxs-lookup"><span data-stu-id="44cfe-214">For details of each type, see <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Counter Types</a> in the Windows 2003 Deployment Guide.</span></span> <span data-ttu-id="44cfe-215">Beim Namen wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="44cfe-215">The name is case-sensitive use lowercase.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="44cfe-216">uri</span><span class="sxs-lookup"><span data-stu-id="44cfe-216">uri</span></span></td>
<td><span data-ttu-id="44cfe-217"><strong>xs:anyURI</strong></span><span class="sxs-lookup"><span data-stu-id="44cfe-217"><strong>xs:anyURI</strong></span></span></td>
<td><span data-ttu-id="44cfe-218">Ein eindeutiger einheitlicher Ressourcen Bezeichner, mit dem Benutzer von einem beliebigen Speicherort Werte abrufen können.</span><span class="sxs-lookup"><span data-stu-id="44cfe-218">A unique uniform resource identifier that lets users retrieve counter values from any location.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="44cfe-219">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44cfe-219">Remarks</span></span>

<span data-ttu-id="44cfe-220">Um Abwärtskompatibilität zu gewährleisten, sollte jeder Leistungs Monitor im Counter-Satz dieselben Werte für **perffreqid** und **perftimeid** angeben.</span><span class="sxs-lookup"><span data-stu-id="44cfe-220">To provide backwards-compatibility, each counter in the counter set should specify the same **perfFreqID** and **perfTimeID** values.</span></span>

## <a name="requirements"></a><span data-ttu-id="44cfe-221">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44cfe-221">Requirements</span></span>



| <span data-ttu-id="44cfe-222">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44cfe-222">Requirement</span></span> | <span data-ttu-id="44cfe-223">Wert</span><span class="sxs-lookup"><span data-stu-id="44cfe-223">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44cfe-224">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44cfe-224">Minimum supported client</span></span><br/> | <span data-ttu-id="44cfe-225">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44cfe-225">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44cfe-226">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44cfe-226">Minimum supported server</span></span><br/> | <span data-ttu-id="44cfe-227">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44cfe-227">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

