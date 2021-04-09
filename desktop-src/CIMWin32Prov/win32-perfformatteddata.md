---
description: Eine abstrakte Basisklasse für die vorinstallierten, berechneten Daten Klassen.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Win32_PerfFormattedData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: c28d0366c80e8838b36e17cd0fa1074b6ad33629
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958538"
---
# <a name="win32_perfformatteddata-class"></a><span data-ttu-id="1d4f8-103">Win32 \_ perfformatteddata-Klasse</span><span class="sxs-lookup"><span data-stu-id="1d4f8-103">Win32\_PerfFormattedData class</span></span>

<span data-ttu-id="1d4f8-104">Eine abstrakte Basisklasse für die vorinstallierten, berechneten Daten Klassen.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-104">An abstract base class for the preinstalled, calculated data classes.</span></span> <span data-ttu-id="1d4f8-105">Ein Beispiel für eine solche Klasse ist [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="1d4f8-105">An example of such a class is [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="1d4f8-106">Diese Klassen enthalten berechnete Werte, die durch die [Leistungs Datenanbieter leistungsstarke formatierte Leistungs](../wmisdk/formatted-performance-data-provider.md)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-106">These classes contain calculated values provided by the high-performance [Formatted Performance Data Provider](../wmisdk/formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="1d4f8-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und zeigt alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-107">The following syntax is simplified from MOF code and shows all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4f8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d4f8-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
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

## <a name="members"></a><span data-ttu-id="1d4f8-109">Member</span><span class="sxs-lookup"><span data-stu-id="1d4f8-109">Members</span></span>

<span data-ttu-id="1d4f8-110">Die **Win32 \_ perfformatteddata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1d4f8-110">The **Win32\_PerfFormattedData** class has these types of members:</span></span>

-   [<span data-ttu-id="1d4f8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d4f8-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d4f8-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d4f8-112">Properties</span></span>

<span data-ttu-id="1d4f8-113">Die **Win32 \_ perfformatteddata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-113">The **Win32\_PerfFormattedData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d4f8-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d4f8-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d4f8-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d4f8-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d4f8-117">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1d4f8-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1d4f8-118">Kurze Textbeschreibung für die Statistik oder Metrik.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="1d4f8-119">Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d4f8-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d4f8-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d4f8-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d4f8-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d4f8-123">Die Textbeschreibung der Statistik oder Metrik.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="1d4f8-124">Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d4f8-125">**Frequency- \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d4f8-126">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d4f8-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d4f8-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d4f8-128">Häufigkeit in Ticks pro Sekunde der **timestamp- \_ Objekt** Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="1d4f8-129">Bei einer untergeordneten Definition definiert der Anbieter diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="1d4f8-130">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d4f8-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="1d4f8-131">Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-131">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d4f8-132">**\_PerfTime-Häufigkeit**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-132">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d4f8-133">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d4f8-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d4f8-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d4f8-135">Häufigkeit in Ticks pro Sekunde der Eigenschaft " **Frequency \_ PerfTime** ".</span><span class="sxs-lookup"><span data-stu-id="1d4f8-135">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="1d4f8-136">Ein Wert kann durch Aufrufen der Windows-Funktion " [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-136">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="1d4f8-137">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d4f8-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="1d4f8-138">Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-138">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d4f8-139">**Frequency \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-139">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d4f8-140">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d4f8-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d4f8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d4f8-142">Häufigkeit in Ticks pro Sekunde der **timestamp \_ Sys100NS** -Eigenschaft (10 Millionen).</span><span class="sxs-lookup"><span data-stu-id="1d4f8-142">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="1d4f8-143">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d4f8-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="1d4f8-144">Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-144">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d4f8-145">**Name**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d4f8-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d4f8-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d4f8-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d4f8-148">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1d4f8-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1d4f8-149">Bezeichnung, nach der die Statistik oder Metrik bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-149">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="1d4f8-150">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-150">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="1d4f8-151">Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-151">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d4f8-152">**Timestamp- \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-152">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d4f8-153">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d4f8-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d4f8-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d4f8-155">Objekt definierter Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-155">Object-defined timestamp.</span></span> <span data-ttu-id="1d4f8-156">Der Anbieter definiert seine-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-156">The provider defines his property.</span></span>

<span data-ttu-id="1d4f8-157">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d4f8-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="1d4f8-158">Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-158">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d4f8-159">**Zeitstempel ( \_ PerfTime)**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-159">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d4f8-160">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d4f8-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d4f8-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d4f8-162">Hoher Leistungszeit Stempel-Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-162">High Performance counter timestamp.</span></span> <span data-ttu-id="1d4f8-163">Ein Wert kann durch Aufrufen der Windows-Funktion " [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-163">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="1d4f8-164">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d4f8-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="1d4f8-165">Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-165">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d4f8-166">**Zeitstempel \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-166">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d4f8-167">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d4f8-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d4f8-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d4f8-169">Timestamp-Wert in 100 Nanosekunden-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-169">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="1d4f8-170">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d4f8-170">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="1d4f8-171">Diese Eigenschaft wird von [**Win32 \_ perf**](win32-perf.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-171">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d4f8-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d4f8-172">Remarks</span></span>

<span data-ttu-id="1d4f8-173">Die **Win32-Klasse \_ perfformatteddata** ist von [**Win32 \_ perf**](win32-perf.md)abgeleitet, das von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-173">The **Win32\_PerfFormattedData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span> <span data-ttu-id="1d4f8-174">Die-Klasse befindet sich im **root \\ CIMV2** -Namespace.</span><span class="sxs-lookup"><span data-stu-id="1d4f8-174">The class is found in the **root\\cimv2** namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d4f8-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d4f8-175">Requirements</span></span>



| <span data-ttu-id="1d4f8-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d4f8-176">Requirement</span></span> | <span data-ttu-id="1d4f8-177">Wert</span><span class="sxs-lookup"><span data-stu-id="1d4f8-177">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4f8-178">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d4f8-178">Minimum supported client</span></span><br/> | <span data-ttu-id="1d4f8-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d4f8-179">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="1d4f8-180">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d4f8-180">Minimum supported server</span></span><br/> | <span data-ttu-id="1d4f8-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d4f8-181">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="1d4f8-182">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d4f8-182">Namespace</span></span><br/>                | <span data-ttu-id="1d4f8-183">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1d4f8-183">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="1d4f8-184">MOF</span><span class="sxs-lookup"><span data-stu-id="1d4f8-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d4f8-185"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1d4f8-185"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="1d4f8-186">DLL</span><span class="sxs-lookup"><span data-stu-id="1d4f8-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d4f8-187"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d4f8-187"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d4f8-188">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d4f8-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4f8-189">**Win32 \_ -Leistung**</span><span class="sxs-lookup"><span data-stu-id="1d4f8-189">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="1d4f8-190">Leistungs Leistungsdaten-Klassen</span><span class="sxs-lookup"><span data-stu-id="1d4f8-190">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="1d4f8-191">Zugreifen auf vorinstallierte WMI-Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="1d4f8-191">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="1d4f8-192">WMI-Tasks: Leistungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="1d4f8-192">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="1d4f8-193">Zugreifen auf Leistungsdaten im Skript</span><span class="sxs-lookup"><span data-stu-id="1d4f8-193">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
