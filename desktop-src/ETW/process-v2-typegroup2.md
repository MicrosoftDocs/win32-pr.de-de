---
description: Diese Klasse ist die Ereignistyp Klasse für Prozess-Counter-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Process_V2_TypeGroup2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup2
- Process_V2_TypeGroup2.ProcessId
- Process_V2_TypeGroup2.PageFaultCount
- Process_V2_TypeGroup2.HandleCount
- Process_V2_TypeGroup2.Reserved
- Process_V2_TypeGroup2.PeakVirtualSize
- Process_V2_TypeGroup2.PeakWorkingSetSize
- Process_V2_TypeGroup2.PeakPagefileUsage
- Process_V2_TypeGroup2.QuotaPeakPagedPoolUsage
- Process_V2_TypeGroup2.QuotaPeakNonPagedPoolUsage
- Process_V2_TypeGroup2.VirtualSize
- Process_V2_TypeGroup2.WorkingSetSize
- Process_V2_TypeGroup2.PagefileUsage
- Process_V2_TypeGroup2.QuotaPagedPoolUsage
- Process_V2_TypeGroup2.QuotaNonPagedPoolUsage
- Process_V2_TypeGroup2.PrivatePageCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 284b77da03b53f9c2662c8729a7bf6606c45630a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867707"
---
# <a name="process_v2_typegroup2-class"></a><span data-ttu-id="c6c59-104">Process \_ v2 \_ TypeGroup2-Klasse</span><span class="sxs-lookup"><span data-stu-id="c6c59-104">Process\_V2\_TypeGroup2 class</span></span>

<span data-ttu-id="c6c59-105">Diese Klasse ist die Ereignistyp Klasse für Prozess-Counter-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="c6c59-105">This class is the event type class for process counter events.</span></span>

<span data-ttu-id="c6c59-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c6c59-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c59-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6c59-107">Syntax</span></span>

``` syntax
[EventType{32, 33}, EventTypeName{"PerfCtr", PerfCtrRundown"}]
class Process_V2_TypeGroup2 : Process_V2
{
  uint32 ProcessId;
  uint32 PageFaultCount;
  uint32 HandleCount;
  uint32 Reserved;
  object PeakVirtualSize;
  object PeakWorkingSetSize;
  object PeakPagefileUsage;
  object QuotaPeakPagedPoolUsage;
  object QuotaPeakNonPagedPoolUsage;
  object VirtualSize;
  object WorkingSetSize;
  object PagefileUsage;
  object QuotaPagedPoolUsage;
  object QuotaNonPagedPoolUsage;
  object PrivatePageCount;
};
```

## <a name="members"></a><span data-ttu-id="c6c59-108">Member</span><span class="sxs-lookup"><span data-stu-id="c6c59-108">Members</span></span>

<span data-ttu-id="c6c59-109">Die **Process \_ v2 \_ TypeGroup2** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c6c59-109">The **Process\_V2\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="c6c59-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6c59-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6c59-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6c59-111">Properties</span></span>

<span data-ttu-id="c6c59-112">Die **Process \_ v2 \_ TypeGroup2** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c6c59-112">The **Process\_V2\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6c59-113">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="c6c59-113">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6c59-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-116">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="c6c59-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-117">Anzahl der verwendeten Handles.</span><span class="sxs-lookup"><span data-stu-id="c6c59-117">Count of used handles.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-118">**Pagefehlercount**</span><span class="sxs-lookup"><span data-stu-id="c6c59-118">**PageFaultCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6c59-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-121">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="c6c59-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-122">Anzahl der Seiten Fehler.</span><span class="sxs-lookup"><span data-stu-id="c6c59-122">Count of page faults.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-123">**PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="c6c59-123">**PagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-124">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c6c59-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-126">Qualifizierer: wmidataid (12), Erweiterung ("sizet")</span><span class="sxs-lookup"><span data-stu-id="c6c59-126">Qualifiers: WmiDataId(12), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-127">Aktuelle Verwendung der Auslagerungs Datei.</span><span class="sxs-lookup"><span data-stu-id="c6c59-127">Current page file usage.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-128">**"Peer Page File Usage"**</span><span class="sxs-lookup"><span data-stu-id="c6c59-128">**PeakPagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-129">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c6c59-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-131">Qualifizierer: wmidataid (7), Erweiterung ("sizet")</span><span class="sxs-lookup"><span data-stu-id="c6c59-131">Qualifiers: WmiDataId(7), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-132">Die größte verwendete Seiten Dateigröße.</span><span class="sxs-lookup"><span data-stu-id="c6c59-132">Largest page file size used.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-133">**Peakvirtualsize**</span><span class="sxs-lookup"><span data-stu-id="c6c59-133">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-134">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c6c59-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-136">Qualifizierer: wmidataid (5), Erweiterung ("sizet")</span><span class="sxs-lookup"><span data-stu-id="c6c59-136">Qualifiers: WmiDataId(5), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-137">Die größte verwendete Größe der virtuellen Seite.</span><span class="sxs-lookup"><span data-stu-id="c6c59-137">Largest virtual page size used.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-138">**PeakWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="c6c59-138">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-139">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c6c59-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-141">Qualifizierer: wmidataid (6), Erweiterung ("sizet")</span><span class="sxs-lookup"><span data-stu-id="c6c59-141">Qualifiers: WmiDataId(6), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-142">Die größte verwendete Workingsetgröße.</span><span class="sxs-lookup"><span data-stu-id="c6c59-142">Largest working set size used.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-143">**PrivatePageCount**</span><span class="sxs-lookup"><span data-stu-id="c6c59-143">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-144">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c6c59-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-146">Qualifizierer: wmidataid (15), Extension ("sizet")</span><span class="sxs-lookup"><span data-stu-id="c6c59-146">Qualifiers: WmiDataId(15), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-147">Aktuelle private physische Seitenanzahl.</span><span class="sxs-lookup"><span data-stu-id="c6c59-147">Current private physical page count.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-148">ProcessId</span><span class="sxs-lookup"><span data-stu-id="c6c59-148">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6c59-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-151">Qualifizierer: wmidataid (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="c6c59-151">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-152">Die globale Prozess-ID, mit der Sie einen Prozess identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="c6c59-152">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="c6c59-153">Der Wert ist gültig ab dem Zeitpunkt, zu dem ein Prozess erstellt wird, bis er beendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6c59-153">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-154">**Quotanonpgedpoolusage**</span><span class="sxs-lookup"><span data-stu-id="c6c59-154">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-155">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c6c59-155">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-157">Qualifizierer: wmidataid (14), Erweiterung ("sizet")</span><span class="sxs-lookup"><span data-stu-id="c6c59-157">Qualifiers: WmiDataId(14), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-158">Aktuell zugesicherte, nicht auslagerbare Speicherauslastung.</span><span class="sxs-lookup"><span data-stu-id="c6c59-158">Current committed non-paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-159">**Quotapgedpoolusage**</span><span class="sxs-lookup"><span data-stu-id="c6c59-159">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-160">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c6c59-160">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-162">Qualifizierer: wmidataid (13), Erweiterung ("sizet")</span><span class="sxs-lookup"><span data-stu-id="c6c59-162">Qualifiers: WmiDataId(13), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-163">Aktuelle zugesicherte auslagerter Speicherauslastung.</span><span class="sxs-lookup"><span data-stu-id="c6c59-163">Current committed paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-164">**Quotapeaknonpgedpoolusage**</span><span class="sxs-lookup"><span data-stu-id="c6c59-164">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-165">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c6c59-165">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-167">Qualifizierer: wmidataid (9), Erweiterung ("sizet")</span><span class="sxs-lookup"><span data-stu-id="c6c59-167">Qualifiers: WmiDataId(9), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-168">Der größte nicht auslagerbare nicht auslagerbare Speicher wurde verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6c59-168">Largest committed non-paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-169">**Quotapeakpgedpoolusage**</span><span class="sxs-lookup"><span data-stu-id="c6c59-169">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-170">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c6c59-170">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-172">Qualifizierer: wmidataid (8), Erweiterung ("sizet")</span><span class="sxs-lookup"><span data-stu-id="c6c59-172">Qualifiers: WmiDataId(8), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-173">Der größte verwendete auslagerter ausgehenster Speicher.</span><span class="sxs-lookup"><span data-stu-id="c6c59-173">Largest committed paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-174">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="c6c59-174">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-175">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6c59-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-177">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="c6c59-177">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-178">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c6c59-178">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-179">**VirtualSize**</span><span class="sxs-lookup"><span data-stu-id="c6c59-179">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-180">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c6c59-180">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-182">Qualifizierer: wmidataid (10), Extension ("sizet")</span><span class="sxs-lookup"><span data-stu-id="c6c59-182">Qualifiers: WmiDataId(10), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-183">Aktuelle Größe der virtuellen Seite.</span><span class="sxs-lookup"><span data-stu-id="c6c59-183">Current virtual page size.</span></span>

</dd> <dt>

<span data-ttu-id="c6c59-184">**Workingsetsize**</span><span class="sxs-lookup"><span data-stu-id="c6c59-184">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c59-185">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c6c59-185">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6c59-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c59-187">Qualifizierer: wmidataid (11), Erweiterung ("sizet")</span><span class="sxs-lookup"><span data-stu-id="c6c59-187">Qualifiers: WmiDataId(11), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="c6c59-188">Aktuelle Workingsetgröße.</span><span class="sxs-lookup"><span data-stu-id="c6c59-188">Current working set size.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6c59-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6c59-189">Remarks</span></span>

<span data-ttu-id="c6c59-190">Diese Ereignisse werden protokolliert, wenn der Prozess beendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6c59-190">These events are logged when the process ends.</span></span> <span data-ttu-id="c6c59-191">Das Ereignis gibt an, wie ein Prozess die Speicherauslastung verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="c6c59-191">The event indicates how a process handled memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c59-192">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c6c59-192">Requirements</span></span>



| <span data-ttu-id="c6c59-193">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6c59-193">Requirement</span></span> | <span data-ttu-id="c6c59-194">Wert</span><span class="sxs-lookup"><span data-stu-id="c6c59-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c6c59-195">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6c59-195">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c59-196">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6c59-196">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c6c59-197">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6c59-197">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c59-198">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6c59-198">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6c59-199">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6c59-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c59-200">**Prozess \_ v2**</span><span class="sxs-lookup"><span data-stu-id="c6c59-200">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




