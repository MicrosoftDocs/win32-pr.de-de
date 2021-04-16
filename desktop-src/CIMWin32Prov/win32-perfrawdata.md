---
description: Die abstrakte Basisklasse für alle konkreten Klassen des-rohleistungs Zählers.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Win32_PerfRawData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfRawData
- Win32_PerfRawData.Caption
- Win32_PerfRawData.Description
- Win32_PerfRawData.Name
- Win32_PerfRawData.Frequency_Object
- Win32_PerfRawData.Frequency_PerfTime
- Win32_PerfRawData.Frequency_Sys100NS
- Win32_PerfRawData.Timestamp_Object
- Win32_PerfRawData.Timestamp_PerfTime
- Win32_PerfRawData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: db5b74ae7508d15a48d2f71c3a586ad7e40362f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524272"
---
# <a name="win32_perfrawdata-class"></a><span data-ttu-id="4c176-103">Win32 \_ perfrawdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="4c176-103">Win32\_PerfRawData class</span></span>

<span data-ttu-id="4c176-104">Die abstrakte Basisklasse für alle konkreten Klassen des-rohleistungs Zählers.</span><span class="sxs-lookup"><span data-stu-id="4c176-104">The abstract base class for all concrete raw performance counter classes.</span></span>

<span data-ttu-id="4c176-105">Um im System Monitor angezeigt zu werden, müssen Leistungsindikatoren Klassen zum Stamm \\ CIMV2-Namespace hinzugefügt und von **Win32 \_ perfrawdata** abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="4c176-105">To appear in System Monitor, performance counter classes must be added to the root\\cimv2 namespace and derived from **Win32\_PerfRawData**.</span></span> <span data-ttu-id="4c176-106">Die Daten in diesen Klassen werden vom Hochleistungs [Anbieter für Leistungs Anbieter](../wmisdk/performance-counter-provider.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4c176-106">Data in these classes are provided by the high-performance [Performance Counter Provider](../wmisdk/performance-counter-provider.md).</span></span>

<span data-ttu-id="4c176-107">Die folgenden Eigenschaften werden geerbt, wenn eine Klasse von **Win32 \_ perfrawdata** abgeleitet wird:</span><span class="sxs-lookup"><span data-stu-id="4c176-107">The following properties are inherited when a class is derived from **Win32\_PerfRawData**:</span></span>

-   <span data-ttu-id="4c176-108">**Zeitstempel ( \_ PerfTime)**</span><span class="sxs-lookup"><span data-stu-id="4c176-108">**Timestamp\_PerfTime**</span></span>
-   <span data-ttu-id="4c176-109">**Zeitstempel \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="4c176-109">**Timestamp\_Sys100NS**</span></span>
-   <span data-ttu-id="4c176-110">**Timestamp- \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="4c176-110">**Timestamp\_Object**</span></span>
-   <span data-ttu-id="4c176-111">**\_PerfTime-Häufigkeit**</span><span class="sxs-lookup"><span data-stu-id="4c176-111">**Frequency\_PerfTime**</span></span>
-   <span data-ttu-id="4c176-112">**Frequency \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="4c176-112">**Frequency\_Sys100NS**</span></span>
-   <span data-ttu-id="4c176-113">**Frequency- \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="4c176-113">**Frequency\_Object**</span></span>

<span data-ttu-id="4c176-114">In jedem Fall müssen die Eigenschaften vom Anbieter ausgefüllt werden, oder die Klasse kann nicht im System Monitor angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4c176-114">In each case, the properties must be filled out by the provider or the class cannot be displayed in System Monitor.</span></span> <span data-ttu-id="4c176-115">Diese Eigenschaften werden zum Berechnen von Counter-typformeln durch Consumer von Leistungsdaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c176-115">These properties are used to compute counter type formulas by consumers of performance data.</span></span>

<span data-ttu-id="4c176-116">Die folgende Syntax wird aus dem MOF-Code vereinfacht und zeigt alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4c176-116">The following syntax is simplified from MOF code and shows all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c176-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c176-117">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfRawData : Win32_Perf
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a><span data-ttu-id="4c176-118">Member</span><span class="sxs-lookup"><span data-stu-id="4c176-118">Members</span></span>

<span data-ttu-id="4c176-119">Die **Win32 \_ perfrawdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4c176-119">The **Win32\_PerfRawData** class has these types of members:</span></span>

-   [<span data-ttu-id="4c176-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4c176-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c176-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4c176-121">Properties</span></span>

<span data-ttu-id="4c176-122">Die **Win32 \_ perfrawdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4c176-122">The **Win32\_PerfRawData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c176-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4c176-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c176-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4c176-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c176-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4c176-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c176-126">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="4c176-126">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4c176-127">Kurze Textbeschreibung für die Statistik oder Metrik.</span><span class="sxs-lookup"><span data-stu-id="4c176-127">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="4c176-128">Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4c176-128">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c176-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4c176-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c176-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4c176-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c176-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4c176-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c176-132">Die Textbeschreibung der Statistik oder Metrik.</span><span class="sxs-lookup"><span data-stu-id="4c176-132">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="4c176-133">Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4c176-133">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c176-134">**Frequency- \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="4c176-134">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c176-135">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4c176-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4c176-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4c176-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c176-137">Häufigkeit in Ticks pro Sekunde der **timestamp- \_ Objekt** Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4c176-137">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="4c176-138">Bei einer untergeordneten Definition definiert der Anbieter diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4c176-138">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="4c176-139">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4c176-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="4c176-140">Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4c176-140">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c176-141">**\_PerfTime-Häufigkeit**</span><span class="sxs-lookup"><span data-stu-id="4c176-141">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c176-142">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4c176-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4c176-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4c176-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c176-144">Häufigkeit in Ticks pro Sekunde der Eigenschaft " **Frequency \_ PerfTime** ".</span><span class="sxs-lookup"><span data-stu-id="4c176-144">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="4c176-145">Ein Wert kann durch Aufrufen der Windows-Funktion " [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4c176-145">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="4c176-146">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4c176-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="4c176-147">Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4c176-147">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c176-148">**Frequency \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="4c176-148">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c176-149">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4c176-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4c176-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4c176-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c176-151">Häufigkeit in Ticks pro Sekunde der **timestamp \_ Sys100NS** -Eigenschaft (10 Millionen).</span><span class="sxs-lookup"><span data-stu-id="4c176-151">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="4c176-152">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4c176-152">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="4c176-153">Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4c176-153">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c176-154">**Name**</span><span class="sxs-lookup"><span data-stu-id="4c176-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c176-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4c176-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c176-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4c176-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c176-157">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="4c176-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4c176-158">Bezeichnung, nach der die Statistik oder Metrik bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="4c176-158">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="4c176-159">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4c176-159">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4c176-160">Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4c176-160">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c176-161">**Timestamp- \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="4c176-161">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c176-162">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4c176-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4c176-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4c176-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c176-164">Objekt definierter Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="4c176-164">Object-defined timestamp.</span></span> <span data-ttu-id="4c176-165">Der Anbieter definiert seine-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4c176-165">The provider defines his property.</span></span>

<span data-ttu-id="4c176-166">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4c176-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="4c176-167">Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4c176-167">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c176-168">**Zeitstempel ( \_ PerfTime)**</span><span class="sxs-lookup"><span data-stu-id="4c176-168">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c176-169">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4c176-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4c176-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4c176-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c176-171">Hoher Leistungszeit Stempel-Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="4c176-171">High Performance counter timestamp.</span></span> <span data-ttu-id="4c176-172">Ein Wert kann durch Aufrufen der Windows-Funktion " [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4c176-172">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="4c176-173">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4c176-173">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="4c176-174">Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4c176-174">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c176-175">**Zeitstempel \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="4c176-175">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c176-176">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4c176-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4c176-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4c176-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c176-178">Timestamp-Wert in 100 Nanosekunden-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="4c176-178">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="4c176-179">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4c176-179">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="4c176-180">Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4c176-180">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c176-181">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c176-181">Remarks</span></span>

<span data-ttu-id="4c176-182">Die **Win32 \_ perfrawdata** -Klasse wird von [**Win32- \_ perf**](win32-perf.md)abgeleitet, die von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="4c176-182">The **Win32\_PerfRawData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

<span data-ttu-id="4c176-183">Alle Klassen, die von [**Win32 \_ perf**](win32-perf.md) abgeleitet werden, sind für die Verwendung [*mit einem*](../wmisdk/gloss-r.md) Aktualisierungs Objekt konzipiert.</span><span class="sxs-lookup"><span data-stu-id="4c176-183">All classes derived from [**Win32\_Perf**](win32-perf.md) are designed to be used with a [*refresher*](../wmisdk/gloss-r.md) object.</span></span> <span data-ttu-id="4c176-184">Weitere Informationen zum Erstellen und Verwenden eines Aktualisierungs Objekts in der Programmiersprache C++ finden Sie unter [zugreifen auf Leistungsdaten in C++](../wmisdk/accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="4c176-184">For more information about how to create and use a refresher object in the C++ programming language, see [Accessing Performance Data in C++](../wmisdk/accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="4c176-185">Weitere Informationen zum Erstellen und Verwenden eines Aktualisierungs Objekts in einer Skript Programmiersprache finden Sie unter Aktualisieren von [WMI-Daten in](../wmisdk/refreshing-wmi-data-in-scripts.md)Skripts.</span><span class="sxs-lookup"><span data-stu-id="4c176-185">For more information about how to create and use a refresher object in a script programming language, see [Refreshing WMI Data in Scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c176-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c176-186">Requirements</span></span>



| <span data-ttu-id="4c176-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c176-187">Requirement</span></span> | <span data-ttu-id="4c176-188">Wert</span><span class="sxs-lookup"><span data-stu-id="4c176-188">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c176-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c176-189">Minimum supported client</span></span><br/> | <span data-ttu-id="4c176-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c176-190">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="4c176-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c176-191">Minimum supported server</span></span><br/> | <span data-ttu-id="4c176-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c176-192">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="4c176-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c176-193">Namespace</span></span><br/>                | <span data-ttu-id="4c176-194">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4c176-194">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="4c176-195">MOF</span><span class="sxs-lookup"><span data-stu-id="4c176-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c176-196"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4c176-196"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="4c176-197">DLL</span><span class="sxs-lookup"><span data-stu-id="4c176-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c176-198"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c176-198"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c176-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c176-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c176-200">**Win32 \_ -Leistung**</span><span class="sxs-lookup"><span data-stu-id="4c176-200">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="4c176-201">Leistungs Leistungsdaten-Klassen</span><span class="sxs-lookup"><span data-stu-id="4c176-201">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="4c176-202">Zugreifen auf vorinstallierte WMI-Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="4c176-202">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="4c176-203">WMI-Tasks: Leistungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="4c176-203">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="4c176-204">Zugreifen auf Leistungsdaten im Skript</span><span class="sxs-lookup"><span data-stu-id="4c176-204">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
