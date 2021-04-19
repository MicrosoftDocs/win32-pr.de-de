---
description: Die Basisklasse für die Leistungs Zählers-Klassen Win32 \_ perfrawdata und Win32 \_ perfformatteddata.
ms.assetid: c754b619-a70f-4a56-8a43-2b36c8f8370b
ms.tgt_platform: multiple
title: Win32_Perf-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Perf
- Root\CIMV2.Win32_Perf.Caption
- Root\CIMV2.Win32_Perf.Description
- Root\CIMV2.Win32_Perf.Name
- Root\CIMV2.Win32_Perf.Frequency_Object
- Root\CIMV2.Win32_Perf.Frequency_PerfTime
- Root\CIMV2.Win32_Perf.Frequency_Sys100NS
- Root\CIMV2.Win32_Perf.Timestamp_Object
- Root\CIMV2.Win32_Perf.Timestamp_PerfTime
- Root\CIMV2.Win32_Perf.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 13b339e95e175e4d2dff50c0a9674f8002933c1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344221"
---
# <a name="win32_perf-class"></a><span data-ttu-id="1c361-103">Win32- \_ perf-Klasse</span><span class="sxs-lookup"><span data-stu-id="1c361-103">Win32\_Perf class</span></span>

<span data-ttu-id="1c361-104">Die Basisklasse für die Leistungs Zählers-Klassen [**Win32 \_ perfrawdata**](win32-perfrawdata.md) und [**Win32 \_ perfformatteddata**](win32-perfformatteddata.md).</span><span class="sxs-lookup"><span data-stu-id="1c361-104">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

<span data-ttu-id="1c361-105">**Win32 \_ Perf** definiert die erforderlichen Zeitstempel-und Häufigkeits Eigenschaften, die in den [**CounterType**](../wmisdk/countertype-qualifier.md) -Algorithmen für die Leistungsindikator Klassen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c361-105">**Win32\_Perf** defines the required timestamp and frequency properties used in the [**CounterType**](../wmisdk/countertype-qualifier.md) algorithms for the performance counter classes.</span></span>

<span data-ttu-id="1c361-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1c361-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1c361-107">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="1c361-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c361-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c361-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_Perf : CIM_StatisticalInformation
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

## <a name="members"></a><span data-ttu-id="1c361-109">Member</span><span class="sxs-lookup"><span data-stu-id="1c361-109">Members</span></span>

<span data-ttu-id="1c361-110">Die **Win32- \_ perf** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1c361-110">The **Win32\_Perf** class has these types of members:</span></span>

-   [<span data-ttu-id="1c361-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1c361-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c361-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1c361-112">Properties</span></span>

<span data-ttu-id="1c361-113">Die **Win32- \_ perf** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1c361-113">The **Win32\_Perf** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c361-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1c361-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c361-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c361-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c361-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c361-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c361-117">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1c361-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1c361-118">Kurze Textbeschreibung für die Statistik oder Metrik.</span><span class="sxs-lookup"><span data-stu-id="1c361-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="1c361-119">Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c361-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c361-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c361-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c361-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c361-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c361-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c361-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c361-123">Die Textbeschreibung der Statistik oder Metrik.</span><span class="sxs-lookup"><span data-stu-id="1c361-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="1c361-124">Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c361-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c361-125">**Frequency- \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="1c361-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c361-126">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c361-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c361-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c361-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c361-128">Häufigkeit in Ticks pro Sekunde der **timestamp- \_ Objekt** Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1c361-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="1c361-129">Bei einer untergeordneten Definition definiert der Anbieter diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1c361-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="1c361-130">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1c361-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1c361-131">**\_PerfTime-Häufigkeit**</span><span class="sxs-lookup"><span data-stu-id="1c361-131">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c361-132">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c361-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c361-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c361-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c361-134">Häufigkeit in Ticks pro Sekunde der Eigenschaft " **Frequency \_ PerfTime** ".</span><span class="sxs-lookup"><span data-stu-id="1c361-134">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="1c361-135">Ein Wert kann durch Aufrufen der Windows-Funktion " [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1c361-135">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="1c361-136">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1c361-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1c361-137">**Frequency \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="1c361-137">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c361-138">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c361-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c361-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c361-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c361-140">Häufigkeit in Ticks pro Sekunde der **timestamp \_ Sys100NS** -Eigenschaft (10 Millionen).</span><span class="sxs-lookup"><span data-stu-id="1c361-140">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="1c361-141">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1c361-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1c361-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="1c361-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c361-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c361-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c361-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c361-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c361-145">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1c361-145">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1c361-146">Bezeichnung, nach der die Statistik oder Metrik bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="1c361-146">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="1c361-147">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1c361-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="1c361-148">Diese Eigenschaft wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c361-148">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c361-149">**Timestamp- \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="1c361-149">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c361-150">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c361-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c361-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c361-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c361-152">Objekt definierter Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="1c361-152">Object-defined timestamp.</span></span> <span data-ttu-id="1c361-153">Der Anbieter definiert seine-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1c361-153">The provider defines his property.</span></span>

<span data-ttu-id="1c361-154">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1c361-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1c361-155">**Zeitstempel ( \_ PerfTime)**</span><span class="sxs-lookup"><span data-stu-id="1c361-155">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c361-156">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c361-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c361-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c361-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c361-158">Hoher Leistungszeit Stempel-Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="1c361-158">High Performance counter timestamp.</span></span> <span data-ttu-id="1c361-159">Ein Wert kann durch Aufrufen der Windows-Funktion " [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1c361-159">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="1c361-160">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1c361-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1c361-161">**Zeitstempel \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="1c361-161">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c361-162">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c361-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c361-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c361-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c361-164">Timestamp-Wert in 100 Nanosekunden-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="1c361-164">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="1c361-165">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1c361-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c361-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c361-166">Remarks</span></span>

<span data-ttu-id="1c361-167">Die **Win32- \_ perf** -Klasse wird von [**CIM \_ statisticalinformation**](cim-statisticalinformation.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1c361-167">The **Win32\_Perf** class derives from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c361-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c361-168">Requirements</span></span>



| <span data-ttu-id="1c361-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c361-169">Requirement</span></span> | <span data-ttu-id="1c361-170">Wert</span><span class="sxs-lookup"><span data-stu-id="1c361-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c361-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c361-171">Minimum supported client</span></span><br/> | <span data-ttu-id="1c361-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c361-172">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="1c361-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c361-173">Minimum supported server</span></span><br/> | <span data-ttu-id="1c361-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c361-174">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="1c361-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c361-175">Namespace</span></span><br/>                | <span data-ttu-id="1c361-176">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1c361-176">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="1c361-177">DLL</span><span class="sxs-lookup"><span data-stu-id="1c361-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c361-178"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c361-178"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c361-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c361-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c361-180">**CIM- \_ statisticalinformation**</span><span class="sxs-lookup"><span data-stu-id="1c361-180">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dt>

[<span data-ttu-id="1c361-181">Leistungs Leistungsdaten-Klassen</span><span class="sxs-lookup"><span data-stu-id="1c361-181">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="1c361-182">Zugreifen auf vorinstallierte WMI-Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="1c361-182">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="1c361-183">WMI-Tasks: Leistungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="1c361-183">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="1c361-184">Zugreifen auf Leistungsdaten im Skript</span><span class="sxs-lookup"><span data-stu-id="1c361-184">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
