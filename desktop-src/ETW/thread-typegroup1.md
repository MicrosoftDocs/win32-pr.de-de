---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse zum Starten und Beenden von Threads. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 75352efbe044f5fee837c496c394fe28e2dbbbfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130705"
---
# <a name="thread_typegroup1-class"></a><span data-ttu-id="f9aec-104">Thread \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="f9aec-104">Thread\_TypeGroup1 class</span></span>

<span data-ttu-id="f9aec-105">Diese Klasse ist die Ereignistyp Klasse für Ereignisse zum Starten und Beenden von Threads.</span><span class="sxs-lookup"><span data-stu-id="f9aec-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="f9aec-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="f9aec-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9aec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9aec-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="f9aec-108">Member</span><span class="sxs-lookup"><span data-stu-id="f9aec-108">Members</span></span>

<span data-ttu-id="f9aec-109">Die **Thread \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f9aec-109">The **Thread\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="f9aec-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9aec-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9aec-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9aec-111">Properties</span></span>

<span data-ttu-id="f9aec-112">Die **Thread \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f9aec-112">The **Thread\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9aec-113">Affinität</span><span class="sxs-lookup"><span data-stu-id="f9aec-113">Affinity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9aec-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-116">Qualifizierer: wmidataid (7), Zeiger</span><span class="sxs-lookup"><span data-stu-id="f9aec-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-117">Der Satz von Prozessoren, auf denen der Thread ausgeführt werden darf.</span><span class="sxs-lookup"><span data-stu-id="f9aec-117">The set of processors on which the thread is allowed to run.</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-118">BasePriority</span><span class="sxs-lookup"><span data-stu-id="f9aec-118">BasePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-119">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f9aec-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-121">Qualifizierer: wmidataid (11)</span><span class="sxs-lookup"><span data-stu-id="f9aec-121">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-122">Die Zeit Planungs Modul Priorität des Threads (siehe die [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) -Funktion).</span><span class="sxs-lookup"><span data-stu-id="f9aec-122">The scheduler priority of the thread (see the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function).</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-123">Iopriority</span><span class="sxs-lookup"><span data-stu-id="f9aec-123">IoPriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-124">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f9aec-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-126">Qualifizierer: wmidataid (13)</span><span class="sxs-lookup"><span data-stu-id="f9aec-126">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-127">Ein e/a-Prioritäts Hinweis zum Planen von IOS, der vom Thread generiert wird</span><span class="sxs-lookup"><span data-stu-id="f9aec-127">An IO priority hint for scheduling IOs generated by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-128">Pagepriority</span><span class="sxs-lookup"><span data-stu-id="f9aec-128">PagePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-129">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f9aec-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-131">Qualifizierer: wmidataid (12)</span><span class="sxs-lookup"><span data-stu-id="f9aec-131">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-132">Ein Speicherseiten Prioritäts Hinweis für Speicherseiten, auf die der Thread zugreift.</span><span class="sxs-lookup"><span data-stu-id="f9aec-132">A memory page priority hint for memory pages accessed by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-133">ProcessId</span><span class="sxs-lookup"><span data-stu-id="f9aec-133">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9aec-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-136">Qualifizierer: wmidataid (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="f9aec-136">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-137">Prozess Bezeichner des am Ereignis beteiligten Threads.</span><span class="sxs-lookup"><span data-stu-id="f9aec-137">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-138">StackBase</span><span class="sxs-lookup"><span data-stu-id="f9aec-138">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9aec-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-141">Qualifizierer: wmidataid (3), Zeiger</span><span class="sxs-lookup"><span data-stu-id="f9aec-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-142">Basisadresse des Thread Stapels.</span><span class="sxs-lookup"><span data-stu-id="f9aec-142">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-143">StackLimit</span><span class="sxs-lookup"><span data-stu-id="f9aec-143">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9aec-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-146">Qualifizierer: wmidataid (4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="f9aec-146">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-147">Grenzwert für den Thread Stapel.</span><span class="sxs-lookup"><span data-stu-id="f9aec-147">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-148">Subprocesstag</span><span class="sxs-lookup"><span data-stu-id="f9aec-148">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9aec-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-151">Qualifizierer: wmidataid (10), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="f9aec-151">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-152">Identifiziert den Dienst, wenn der Thread einem Dienst gehört. andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f9aec-152">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-153">Tebbase</span><span class="sxs-lookup"><span data-stu-id="f9aec-153">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-154">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9aec-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-156">Qualifizierer: wmidataid (9), Zeiger</span><span class="sxs-lookup"><span data-stu-id="f9aec-156">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-157">Basisadresse für Thread Umgebungsblock.</span><span class="sxs-lookup"><span data-stu-id="f9aec-157">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-158">Threadflags</span><span class="sxs-lookup"><span data-stu-id="f9aec-158">ThreadFlags</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-159">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f9aec-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-161">Qualifizierer: wmidataid (14)</span><span class="sxs-lookup"><span data-stu-id="f9aec-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-162">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9aec-162">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-163">Tthreadid</span><span class="sxs-lookup"><span data-stu-id="f9aec-163">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-164">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9aec-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-166">Qualifizierer: wmidataid (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="f9aec-166">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-167">Thread Bezeichner des am Ereignis beteiligten Threads.</span><span class="sxs-lookup"><span data-stu-id="f9aec-167">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-168">Userstackbase</span><span class="sxs-lookup"><span data-stu-id="f9aec-168">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-169">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9aec-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-171">Qualifizierer: wmidataid (5), Zeiger</span><span class="sxs-lookup"><span data-stu-id="f9aec-171">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-172">Basisadresse für den benutzermodusstapel des Threads.</span><span class="sxs-lookup"><span data-stu-id="f9aec-172">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-173">Userstacklimit</span><span class="sxs-lookup"><span data-stu-id="f9aec-173">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-174">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9aec-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-176">Qualifizierer: wmidataid (6), Zeiger</span><span class="sxs-lookup"><span data-stu-id="f9aec-176">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-177">Limit für den benutzermodusstapel des Threads.</span><span class="sxs-lookup"><span data-stu-id="f9aec-177">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="f9aec-178">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="f9aec-178">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9aec-179">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9aec-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9aec-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9aec-181">Qualifizierer: wmidataid (8), Zeiger</span><span class="sxs-lookup"><span data-stu-id="f9aec-181">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f9aec-182">Die Startadresse der Funktion, die von diesem Thread ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9aec-182">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9aec-183">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9aec-183">Remarks</span></span>

<span data-ttu-id="f9aec-184">Die Ereignis Typen DCStart und DCEnd zählen die Threads, die derzeit zum Zeitpunkt der Kernel Sitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f9aec-184">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9aec-185">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f9aec-185">Requirements</span></span>



| <span data-ttu-id="f9aec-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9aec-186">Requirement</span></span> | <span data-ttu-id="f9aec-187">Wert</span><span class="sxs-lookup"><span data-stu-id="f9aec-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9aec-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9aec-188">Minimum supported client</span></span><br/> | <span data-ttu-id="f9aec-189">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9aec-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9aec-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9aec-190">Minimum supported server</span></span><br/> | <span data-ttu-id="f9aec-191">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9aec-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9aec-192">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f9aec-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9aec-193">**Aden**</span><span class="sxs-lookup"><span data-stu-id="f9aec-193">**Thread**</span></span>](thread.md)
</dt> </dl>

 

 
