---
description: 'Thread_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für Threadstart- und -endereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: d9e3e33a-0e59-4753-a8d8-5320cbae9d95
title: Thread_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_TypeGroup1
- Thread_TypeGroup1.ProcessId
- Thread_TypeGroup1.TThreadId
- Thread_TypeGroup1.StackBase
- Thread_TypeGroup1.StackLimit
- Thread_TypeGroup1.UserStackBase
- Thread_TypeGroup1.UserStackLimit
- Thread_TypeGroup1.Affinity
- Thread_TypeGroup1.Win32StartAddr
- Thread_TypeGroup1.TebBase
- Thread_TypeGroup1.SubProcessTag
- Thread_TypeGroup1.BasePriority
- Thread_TypeGroup1.PagePriority
- Thread_TypeGroup1.IoPriority
- Thread_TypeGroup1.ThreadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9693bef4449cc076710a74dd9cef88ae608754b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105708"
---
# <a name="thread_typegroup1-class"></a><span data-ttu-id="544d2-104">Thread \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="544d2-104">Thread\_TypeGroup1 class</span></span>

<span data-ttu-id="544d2-105">Diese Klasse ist die Ereignistypklasse für Threadstart- und -endereignisse.</span><span class="sxs-lookup"><span data-stu-id="544d2-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="544d2-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="544d2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="544d2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="544d2-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_TypeGroup1 : Thread
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 Affinity;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
  uint8  BasePriority;
  uint8  PagePriority;
  uint8  IoPriority;
  uint8  ThreadFlags;
};
```

## <a name="members"></a><span data-ttu-id="544d2-108">Member</span><span class="sxs-lookup"><span data-stu-id="544d2-108">Members</span></span>

<span data-ttu-id="544d2-109">Die **Thread \_ TypeGroup1-Klasse** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="544d2-109">The **Thread\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="544d2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="544d2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="544d2-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="544d2-111">Properties</span></span>

<span data-ttu-id="544d2-112">Die **Thread \_ TypeGroup1-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="544d2-112">The **Thread\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="544d2-113">Affinität</span><span class="sxs-lookup"><span data-stu-id="544d2-113">Affinity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-114">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="544d2-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-116">Qualifizierer: WmiDataId(7), Zeiger</span><span class="sxs-lookup"><span data-stu-id="544d2-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="544d2-117">Der Satz von Prozessoren, auf denen der Thread ausgeführt werden darf.</span><span class="sxs-lookup"><span data-stu-id="544d2-117">The set of processors on which the thread is allowed to run.</span></span>

</dd> <dt>

<span data-ttu-id="544d2-118">BasePriority</span><span class="sxs-lookup"><span data-stu-id="544d2-118">BasePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-119">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="544d2-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-121">Qualifizierer: WmiDataId(11)</span><span class="sxs-lookup"><span data-stu-id="544d2-121">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="544d2-122">Die Schedulerpriorität des Threads (siehe [**SetThreadPriority-Funktion).**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)</span><span class="sxs-lookup"><span data-stu-id="544d2-122">The scheduler priority of the thread (see the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function).</span></span>

</dd> <dt>

<span data-ttu-id="544d2-123">IoPriority</span><span class="sxs-lookup"><span data-stu-id="544d2-123">IoPriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-124">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="544d2-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-126">Qualifizierer: WmiDataId(13)</span><span class="sxs-lookup"><span data-stu-id="544d2-126">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="544d2-127">Ein E/A-Prioritätshinweis zum Planen von E/A-Daten, die vom Thread generiert werden.</span><span class="sxs-lookup"><span data-stu-id="544d2-127">An IO priority hint for scheduling IOs generated by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="544d2-128">PagePriority</span><span class="sxs-lookup"><span data-stu-id="544d2-128">PagePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-129">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="544d2-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-131">Qualifizierer: WmiDataId(12)</span><span class="sxs-lookup"><span data-stu-id="544d2-131">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="544d2-132">Ein Speicherseitenprioritätshinweis für Speicherseiten, auf die der Thread zugreift.</span><span class="sxs-lookup"><span data-stu-id="544d2-132">A memory page priority hint for memory pages accessed by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="544d2-133">ProcessId</span><span class="sxs-lookup"><span data-stu-id="544d2-133">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-134">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="544d2-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-136">Qualifizierer: WmiDataId(1), Format("x")</span><span class="sxs-lookup"><span data-stu-id="544d2-136">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="544d2-137">Prozessbezeichner des am Ereignis beteiligten Threads.</span><span class="sxs-lookup"><span data-stu-id="544d2-137">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="544d2-138">StackBase</span><span class="sxs-lookup"><span data-stu-id="544d2-138">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-139">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="544d2-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-141">Qualifizierer: WmiDataId(3), Zeiger</span><span class="sxs-lookup"><span data-stu-id="544d2-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="544d2-142">Basisadresse des Stapels des Threads.</span><span class="sxs-lookup"><span data-stu-id="544d2-142">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="544d2-143">StackLimit</span><span class="sxs-lookup"><span data-stu-id="544d2-143">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-144">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="544d2-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-146">Qualifizierer: WmiDataId(4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="544d2-146">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="544d2-147">Der Grenzwert des Stapels des Threads.</span><span class="sxs-lookup"><span data-stu-id="544d2-147">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="544d2-148">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="544d2-148">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-149">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="544d2-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-151">Qualifizierer: WmiDataId(10), Format("x")</span><span class="sxs-lookup"><span data-stu-id="544d2-151">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="544d2-152">Identifiziert den Dienst, wenn sich der Thread im Besitz eines Diensts befindet. andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="544d2-152">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="544d2-153">TebBase</span><span class="sxs-lookup"><span data-stu-id="544d2-153">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-154">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="544d2-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-156">Qualifizierer: WmiDataId(9), Zeiger</span><span class="sxs-lookup"><span data-stu-id="544d2-156">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="544d2-157">Basisadresse des Threadumgebungsblocks.</span><span class="sxs-lookup"><span data-stu-id="544d2-157">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="544d2-158">ThreadFlags</span><span class="sxs-lookup"><span data-stu-id="544d2-158">ThreadFlags</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-159">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="544d2-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-161">Qualifizierer: WmiDataId(14)</span><span class="sxs-lookup"><span data-stu-id="544d2-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="544d2-162">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="544d2-162">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="544d2-163">TThreadId</span><span class="sxs-lookup"><span data-stu-id="544d2-163">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-164">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="544d2-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-166">Qualifizierer: WmiDataId(2), Format("x")</span><span class="sxs-lookup"><span data-stu-id="544d2-166">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="544d2-167">Threadbezeichner des Threads, der am Ereignis beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="544d2-167">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="544d2-168">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="544d2-168">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-169">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="544d2-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-171">Qualifizierer: WmiDataId(5), Zeiger</span><span class="sxs-lookup"><span data-stu-id="544d2-171">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="544d2-172">Basisadresse des Benutzermodusstapels des Threads.</span><span class="sxs-lookup"><span data-stu-id="544d2-172">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="544d2-173">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="544d2-173">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-174">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="544d2-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-176">Qualifizierer: WmiDataId(6), Zeiger</span><span class="sxs-lookup"><span data-stu-id="544d2-176">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="544d2-177">Limit des Benutzermodusstapels des Threads.</span><span class="sxs-lookup"><span data-stu-id="544d2-177">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="544d2-178">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="544d2-178">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544d2-179">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="544d2-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544d2-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="544d2-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544d2-181">Qualifizierer: WmiDataId(8), Zeiger</span><span class="sxs-lookup"><span data-stu-id="544d2-181">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="544d2-182">Startadresse der Funktion, die von diesem Thread ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="544d2-182">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="544d2-183">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="544d2-183">Remarks</span></span>

<span data-ttu-id="544d2-184">Die DCStart- und DCEnd-Ereignistypen zählen die Threads auf, die derzeit zum Zeitpunkt des Starts bzw. Endes der Kernelsitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="544d2-184">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="544d2-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="544d2-185">Requirements</span></span>



| <span data-ttu-id="544d2-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="544d2-186">Requirement</span></span> | <span data-ttu-id="544d2-187">Wert</span><span class="sxs-lookup"><span data-stu-id="544d2-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="544d2-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="544d2-188">Minimum supported client</span></span><br/> | <span data-ttu-id="544d2-189">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="544d2-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="544d2-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="544d2-190">Minimum supported server</span></span><br/> | <span data-ttu-id="544d2-191">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="544d2-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="544d2-192">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="544d2-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="544d2-193">**Thread**</span><span class="sxs-lookup"><span data-stu-id="544d2-193">**Thread**</span></span>](thread.md)
</dt> </dl>

 

 
