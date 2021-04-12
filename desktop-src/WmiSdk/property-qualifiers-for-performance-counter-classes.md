---
description: Eigenschafts Qualifizierer geben Informationen über den Leistungs Bezeichner an, dem die Eigenschaft zugeordnet wird.
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: Eigenschafts Qualifizierer für Leistungs Objektklassen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e060d072c34d248f9faf634aec7710f5638721b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218172"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="18c10-103">Eigenschafts Qualifizierer für Leistungs Objektklassen</span><span class="sxs-lookup"><span data-stu-id="18c10-103">Property Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="18c10-104">Eigenschafts Qualifizierer geben Informationen über den Leistungs Bezeichner an, dem die Eigenschaft zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="18c10-104">Property qualifiers specify information about the performance counter to which the property maps.</span></span>

-   [<span data-ttu-id="18c10-105">Eigenschaften Qualifizierer für formatierte und formatierte Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="18c10-105">Property Qualifiers for Raw and Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="18c10-106">Eigenschafts Qualifizierer für rohleistungs Klassen</span><span class="sxs-lookup"><span data-stu-id="18c10-106">Property Qualifiers for Raw Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="18c10-107">Eigenschafts Qualifizierer für formatierte Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="18c10-107">Property Qualifiers for Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="18c10-108">Interpretieren von Eigenschaften Qualifizierern</span><span class="sxs-lookup"><span data-stu-id="18c10-108">How to Interpret Property Qualifiers</span></span>](#how-to-interpret-property-qualifiers)
-   [<span data-ttu-id="18c10-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18c10-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="18c10-110">Der Leistungsdaten Träger ist Teil eines Leistungs [**Objekts, das \_**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) durch einen Leistungs Leistungs Leistungs- [Leistungs Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes) -Leistungs Leistungs Leistungs-Leistungs Leistungs-Leistungs Leistungs Leistungs-Leistungs Leistungs-Leistungs Leistungs-Leistungs Leistungs-Leistungs Leistungs-Leistungs Leistungs-Leistungs Leistungs-Objekt – \\</span><span class="sxs-lookup"><span data-stu-id="18c10-110">The performance counter is part of a performance object represented by a WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) Performance counter–specific qualifiers are automatically attached by the WbemPerfClass provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="18c10-111">Diese Informationen gelten für alle Instanzen der Performance-Klasse.</span><span class="sxs-lookup"><span data-stu-id="18c10-111">This information applies to all instances of the performance class.</span></span> <span data-ttu-id="18c10-112">Einige Qualifizierer mit **booleschen** Werten, die immer false sind, sind möglicherweise nicht für bestimmte Klassen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="18c10-112">Some qualifiers with **Boolean** values that are always false may not be present on specific classes.</span></span>

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a><span data-ttu-id="18c10-113">Eigenschaften Qualifizierer für formatierte und formatierte Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="18c10-113">Property Qualifiers for Raw and Formatted Performance Classes</span></span>

<span data-ttu-id="18c10-114">In der folgenden Liste sind die Qualifizierer aufgeführt, die für Eigenschaften in Klassen gelten, die entweder von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) oder [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="18c10-114">The following list lists qualifiers that apply to properties in classes that are derived either from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) or [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="18c10-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**Counter Type**](countertype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="18c10-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="18c10-116">**sint32**</span><span class="sxs-lookup"><span data-stu-id="18c10-116">**sint32**</span></span>

<span data-ttu-id="18c10-117">Ganzzahliger Wert in der Enumeration des Zählers, wie in Winperf. h oder Perflib. h definiert.</span><span class="sxs-lookup"><span data-stu-id="18c10-117">Integer value in the counter type enumeration, as defined in Winperf.h or Perflib.h.</span></span> <span data-ttu-id="18c10-118">Der [**Counter Type**](countertype-qualifier.md)-Qualifizierer gibt die Formel oder den Algorithmus zum Berechnen des Werts an, der im System Monitor für den Indikator angezeigt wird, den die Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="18c10-118">The [**CounterType**](countertype-qualifier.md)qualifier indicates the formula or algorithm used to calculate the value shown in System Monitor for the counter which the property represents.</span></span>

</dd> <dt>

<span data-ttu-id="18c10-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Display Name**</span><span class="sxs-lookup"><span data-stu-id="18c10-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="18c10-120">**string**</span><span class="sxs-lookup"><span data-stu-id="18c10-120">**string**</span></span>

<span data-ttu-id="18c10-121">Der Name des Leistungs Zählers, wie durch das Leistungsdaten-Hilfsprogramm (PDH) angegeben.</span><span class="sxs-lookup"><span data-stu-id="18c10-121">The performance Counter name, as specified by Performance Data Helper (PDH).</span></span>

</dd> <dt>

<span data-ttu-id="18c10-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**Helpindex**</span><span class="sxs-lookup"><span data-stu-id="18c10-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="18c10-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="18c10-123">**sint32**</span></span>

<span data-ttu-id="18c10-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="18c10-124">Not used.</span></span> <span data-ttu-id="18c10-125">Enthält immer 0.</span><span class="sxs-lookup"><span data-stu-id="18c10-125">Always contains 0.</span></span>

</dd> <dt>

<span data-ttu-id="18c10-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**Perfindex**</span><span class="sxs-lookup"><span data-stu-id="18c10-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="18c10-127">**sint32**</span><span class="sxs-lookup"><span data-stu-id="18c10-127">**sint32**</span></span>

<span data-ttu-id="18c10-128">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="18c10-128">Not used.</span></span> <span data-ttu-id="18c10-129">Enthält immer 0.</span><span class="sxs-lookup"><span data-stu-id="18c10-129">Always contains 0.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a><span data-ttu-id="18c10-130">Eigenschafts Qualifizierer für rohleistungs Klassen</span><span class="sxs-lookup"><span data-stu-id="18c10-130">Property Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="18c10-131">In der folgenden Liste sind die Qualifizierer aufgeführt, die für alle Eigenschaften von Klassen gelten, die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="18c10-131">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="18c10-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="18c10-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="18c10-133">**boolean**</span><span class="sxs-lookup"><span data-stu-id="18c10-133">**boolean**</span></span>

<span data-ttu-id="18c10-134">Gibt an, ob diese Eigenschaft der in Listenfeldern zu verwendende Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="18c10-134">Indicates whether this property is the default counter to use in list boxes.</span></span> <span data-ttu-id="18c10-135">Dieser Qualifizierer ist für die Leistungsindikatoren der Version 6,0 standardmäßig auf **false** eingestellt, da Sie keine Daten dafür bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="18c10-135">This qualifier defaults to **False** for Performance Counters Version 6.0 because they do not supply data for it.</span></span> <span data-ttu-id="18c10-136">Weitere Informationen finden Sie unter [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="18c10-136">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="18c10-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DEFAULTSCALE**</span><span class="sxs-lookup"><span data-stu-id="18c10-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**</span></span>
</dt> <dd>

<span data-ttu-id="18c10-138">**sint32**</span><span class="sxs-lookup"><span data-stu-id="18c10-138">**sint32**</span></span>

<span data-ttu-id="18c10-139">Die Potenz von 10, die für die Anzeige des Zählers verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="18c10-139">Power of 10 to use for display of the counter.</span></span> <span data-ttu-id="18c10-140">Bei 0 (null) beträgt der geschätzte Höchstwert 10 ^ 0 oder 1.</span><span class="sxs-lookup"><span data-stu-id="18c10-140">For zero, the estimated maximum is 10^0, or 1.</span></span>

</dd> <dt>

<span data-ttu-id="18c10-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="18c10-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="18c10-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="18c10-142">**sint32**</span></span>

<span data-ttu-id="18c10-143">Zielgruppe des Wissens.</span><span class="sxs-lookup"><span data-stu-id="18c10-143">Audience level of knowledge.</span></span> <span data-ttu-id="18c10-144">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="18c10-144">Not used.</span></span> <span data-ttu-id="18c10-145">Der Wert ist immer 100.</span><span class="sxs-lookup"><span data-stu-id="18c10-145">The value is always 100.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="18c10-146">Eigenschafts Qualifizierer für formatierte Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="18c10-146">Property Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="18c10-147">In der folgenden Liste sind die Qualifizierer aufgelistet, die für alle Eigenschaften von Klassen gelten, die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="18c10-147">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="18c10-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**Cookingtype**</span><span class="sxs-lookup"><span data-stu-id="18c10-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**</span></span>
</dt> <dd>

<span data-ttu-id="18c10-149">**string**</span><span class="sxs-lookup"><span data-stu-id="18c10-149">**string**</span></span>

<span data-ttu-id="18c10-150">Der Formel-Typ, mit dem das Ergebnis erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="18c10-150">Formula type used to produce the result.</span></span> <span data-ttu-id="18c10-151">Jeder zähtertyp verwendet die anderen Eigenschaften Qualifizierer, um das als Wert der aktuellen Eigenschaft angezeigte Ergebnis zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="18c10-151">Each counter type uses the other property qualifiers to calculate the result shown as the value of the current property.</span></span> <span data-ttu-id="18c10-152">Die Qualifizierer " **Counter**", " **perftimestamp**" und " **perftimefreq** " sind Eigenschaften in einer RAW-Klasse zugeordnet, die die Daten bereitstellen</span><span class="sxs-lookup"><span data-stu-id="18c10-152">The **Counter**, **PerfTimeStamp**, and **PerfTimeFreq** qualifiers map to properties in a raw class which supply the data.</span></span>

<span data-ttu-id="18c10-153">Weitere Informationen finden Sie unter [Counter Type-Qualifizierer](countertype-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="18c10-153">For more information, see [CounterType Qualifier](countertype-qualifier.md).</span></span>

</dd> <dt>

<span data-ttu-id="18c10-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Indikator**</span><span class="sxs-lookup"><span data-stu-id="18c10-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter**</span></span>
</dt> <dd>

<span data-ttu-id="18c10-155">**string**</span><span class="sxs-lookup"><span data-stu-id="18c10-155">**string**</span></span>

<span data-ttu-id="18c10-156">Der Name einer erforderlichen Eigenschaft in der entsprechenden RAW-Klasse, die als Leistungswert in der Koch Formel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="18c10-156">Name of a required property in the corresponding raw class to use as the counter value in the cooking formula.</span></span> <span data-ttu-id="18c10-157">Der Wert muss der Eigenschaftsname der Datenquellen Eigenschaft in der entsprechenden RAW-Klasse sein.</span><span class="sxs-lookup"><span data-stu-id="18c10-157">The value must be the property name of the data source property in the corresponding raw class.</span></span>

</dd> <dt>

<span data-ttu-id="18c10-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**Perftimestamp**</span><span class="sxs-lookup"><span data-stu-id="18c10-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="18c10-159">**string**</span><span class="sxs-lookup"><span data-stu-id="18c10-159">**string**</span></span>

<span data-ttu-id="18c10-160">Der Name einer Eigenschaft in einer RAW-Klasse, die als Häufigkeit in der Koch Formel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="18c10-160">Name of a property in a raw class to use as a frequency in the cooking formula.</span></span> <span data-ttu-id="18c10-161">Der entsprechende Standardwert auf Klassenebene wird verwendet, wenn dieser Qualifizierer für die Eigenschaft nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="18c10-161">The appropriate default value at the class level will be used if this qualifier is not present for the property.</span></span> <span data-ttu-id="18c10-162">Die Häufigkeit stellt die Ticks pro Sekunde des Zeitstempels dar.</span><span class="sxs-lookup"><span data-stu-id="18c10-162">The frequency represents the ticks per second of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="18c10-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**Perftimefreq**</span><span class="sxs-lookup"><span data-stu-id="18c10-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**</span></span>
</dt> <dd>

<span data-ttu-id="18c10-164">**string**</span><span class="sxs-lookup"><span data-stu-id="18c10-164">**string**</span></span>

<span data-ttu-id="18c10-165">Der Name einer Eigenschaft in einer RAW-Klasse, die in der Koch Formel als Zeitstempel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="18c10-165">Name of a property in a raw class to use as a timestamp in the cooking formula.</span></span> <span data-ttu-id="18c10-166">Der geeignete Standardwert auf Klassenebene wird verwendet, wenn dieser Qualifizierer für die Eigenschaft nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="18c10-166">The appropriate default value at the class level is used if this qualifier is not present for the property.</span></span> <span data-ttu-id="18c10-167">Ein automatisch generierter Zeitstempel kann einen Fehler in einer Berechnung verursachen, da der Zeitstempel ein Näherungswert ist und keinen mehr Aufwand verursacht, der durch das Marshalling und die tatsächliche Datenerfassung verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="18c10-167">An automatically generated time stamp may introduce error in a calculation because the timestamp is an approximation and does not account for overhead incurred by marshaling and actual data collection.</span></span>

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a><span data-ttu-id="18c10-168">Interpretieren von Eigenschaften Qualifizierern</span><span class="sxs-lookup"><span data-stu-id="18c10-168">How to Interpret Property Qualifiers</span></span>

<span data-ttu-id="18c10-169">Eigenschaften in den [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Klassen enthalten die berechneten Daten, die von der [formatierten Leistungs Datenanbieter](formatted-performance-data-provider.md)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="18c10-169">Properties in the [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data supplied by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span> <span data-ttu-id="18c10-170">Der Eigenschafts Wert ist das abschließende berechnete Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="18c10-170">The property value is the final calculated result.</span></span> <span data-ttu-id="18c10-171">Die Qualifizierer stellen eine Anleitung bereit.</span><span class="sxs-lookup"><span data-stu-id="18c10-171">The qualifiers supply a recipe.</span></span>

<span data-ttu-id="18c10-172">Der **Counter** -und der **Basis** Qualifizierer zeigen auf die Datenquellen, und **cookingtype** gibt die Formel an, mit der das Ergebnis erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="18c10-172">The **Counter** and **Base** qualifiers point to the sources of data and **CookingType** specifies the formula used to produce the result.</span></span> <span data-ttu-id="18c10-173">Der Zeitstempel und die Stichproben Häufigkeit stammen auch aus der entsprechenden RAW-Klasse und sind in **perftimestamp** und **perftimefreq** benannt.</span><span class="sxs-lookup"><span data-stu-id="18c10-173">The timestamp and sample frequency also come from the corresponding raw class and are named in **PerfTimeStamp** and **PerfTimeFreq**.</span></span>

<span data-ttu-id="18c10-174">Beispielsweise enthält eine der formatierten Klassen, die von WMI, [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), bereitgestellt wird, eine Eigenschaft mit dem Namen **avgdiskbytesperread**.</span><span class="sxs-lookup"><span data-stu-id="18c10-174">For example, one of the formatted classes supplied by WMI, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contains a property named **AvgDiskBytesPerRead**.</span></span> <span data-ttu-id="18c10-175">Der Name der Eigenschaft in der formatierten Klasse muss mit der Eigenschaft in der RAW-Klasse identisch sein.</span><span class="sxs-lookup"><span data-stu-id="18c10-175">The name of the property in the formatted class must be the same as the property in the raw class.</span></span> <span data-ttu-id="18c10-176">Die **avgdiskbytesperread** -Eigenschaft verfügt über die folgenden Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="18c10-176">The **AvgDiskBytesPerRead** property has the following qualifiers.</span></span>

<span data-ttu-id="18c10-177">In der folgenden Liste sind die verfügbaren Eigenschafts Qualifizierer für Eigenschaften aller von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleiteten Klassen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="18c10-177">The following list lists the available property qualifiers for properties of all classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>



| <span data-ttu-id="18c10-178">Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="18c10-178">Qualifier</span></span>         | <span data-ttu-id="18c10-179">Wert</span><span class="sxs-lookup"><span data-stu-id="18c10-179">Value</span></span>                     |
|-------------------|---------------------------|
| <span data-ttu-id="18c10-180">**Cookingtype**</span><span class="sxs-lookup"><span data-stu-id="18c10-180">**CookingType**</span></span>   | <span data-ttu-id="18c10-181">Durchschn. \_ Durchschnittswert \_</span><span class="sxs-lookup"><span data-stu-id="18c10-181">PERF\_AVERAGE\_BULK</span></span>       |
| <span data-ttu-id="18c10-182">**Leistungsindikator**</span><span class="sxs-lookup"><span data-stu-id="18c10-182">**Counter**</span></span>       | <span data-ttu-id="18c10-183">Avgdiskbytesperread</span><span class="sxs-lookup"><span data-stu-id="18c10-183">AvgDiskBytesPerRead</span></span>       |
| <span data-ttu-id="18c10-184">**Perftimestamp**</span><span class="sxs-lookup"><span data-stu-id="18c10-184">**PerfTimeStamp**</span></span> | <span data-ttu-id="18c10-185">Zeitstempel ( \_ PerfTime)</span><span class="sxs-lookup"><span data-stu-id="18c10-185">Timestamp\_PerfTime</span></span>       |
| <span data-ttu-id="18c10-186">**Perftimefreq**</span><span class="sxs-lookup"><span data-stu-id="18c10-186">**PerfTimeFreq**</span></span>  | <span data-ttu-id="18c10-187">\_PerfTime-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="18c10-187">Frequency\_PerfTime</span></span>       |
| <span data-ttu-id="18c10-188">**Perfindex**</span><span class="sxs-lookup"><span data-stu-id="18c10-188">**PerfIndex**</span></span>     | <span data-ttu-id="18c10-189">408</span><span class="sxs-lookup"><span data-stu-id="18c10-189">408</span></span>                       |
| <span data-ttu-id="18c10-190">**Helpindex**</span><span class="sxs-lookup"><span data-stu-id="18c10-190">**HelpIndex**</span></span>     | <span data-ttu-id="18c10-191">409</span><span class="sxs-lookup"><span data-stu-id="18c10-191">409</span></span>                       |
| <span data-ttu-id="18c10-192">**Sock**</span><span class="sxs-lookup"><span data-stu-id="18c10-192">**Base**</span></span>          | <span data-ttu-id="18c10-193">Avgdiskbytesperread- \_ Basis</span><span class="sxs-lookup"><span data-stu-id="18c10-193">AvgDiskBytesPerRead\_Base</span></span> |



 

<span data-ttu-id="18c10-194">Die **avgdiskbytesperread** -Eigenschaft meldet die durchschnittliche Anzahl von Bytes, die während Lesevorgängen vom Datenträger übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="18c10-194">The **AvgDiskBytesPerRead** property reports the average number of bytes transferred from the disk during read operations.</span></span> <span data-ttu-id="18c10-195">Die Formel für die durchschnittliche Leistungsdauer \_ \_ ist:</span><span class="sxs-lookup"><span data-stu-id="18c10-195">The formula for PERF\_AVERAGE\_BULK is:</span></span>

<span data-ttu-id="18c10-196">(Sample2-sample1)/(Base sample2-Base sample1)</span><span class="sxs-lookup"><span data-stu-id="18c10-196">(Sample2 - Sample1) / (Base Sample2 - Base Sample1)</span></span>

<span data-ttu-id="18c10-197">Der Lesevorgang wird mit der durch **perftimefreq** angegebenen Häufigkeit mit dem **perftimestamp** -Wert, der das aktuelle Beispiel anzeigt, abgefragt.</span><span class="sxs-lookup"><span data-stu-id="18c10-197">The read operation is sampled at the frequency specified by **PerfTimeFreq** with the **PerfTimeStamp** value indicating the most recent sample.</span></span> <span data-ttu-id="18c10-198">Die Rohdaten des Leistungsindikators in Bytes werden von der **avgdiskbytesperread** -Eigenschaft in der [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) -Klasse entnommen.</span><span class="sxs-lookup"><span data-stu-id="18c10-198">The raw counter data in bytes is taken from the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class.</span></span> <span data-ttu-id="18c10-199">Die Basis Anzahl der Vorgangs Daten wird von der **avgdiskbytesperread- \_ Basis** Eigenschaft in derselben Klasse entnommen.</span><span class="sxs-lookup"><span data-stu-id="18c10-199">The base number of operations data is taken from the **AvgDiskBytesPerRead\_Base** property in that same class.</span></span>

<span data-ttu-id="18c10-200">Weitere Informationen finden Sie unter Abrufen [statistischer Leistungsdaten](obtaining-statistical-performance-data.md) und über [Wachen von Leistungsdaten](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="18c10-200">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="18c10-201">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18c10-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18c10-202">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="18c10-202">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="18c10-203">Für WMI-Leistungsklassen spezifische Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="18c10-203">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="18c10-204">Leistungs Leistungsdaten-Klassen</span><span class="sxs-lookup"><span data-stu-id="18c10-204">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="18c10-205">Zugreifen auf vorinstallierte WMI-Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="18c10-205">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="18c10-206">WMI-Tasks: Leistungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="18c10-206">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
