---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse zum Starten und Beenden von Threads. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Thread_V2_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: c89d573f4eda2580002bedfd0ad17eb9b50c1575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216582"
---
# <a name="thread_v2_typegroup1-class"></a><span data-ttu-id="6222b-104">Thread \_ v2 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="6222b-104">Thread\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="6222b-105">Diese Klasse ist die Ereignistyp Klasse für Ereignisse zum Starten und Beenden von Threads.</span><span class="sxs-lookup"><span data-stu-id="6222b-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="6222b-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="6222b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6222b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6222b-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a><span data-ttu-id="6222b-108">Member</span><span class="sxs-lookup"><span data-stu-id="6222b-108">Members</span></span>

<span data-ttu-id="6222b-109">Die **Thread \_ v2- \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6222b-109">The **Thread\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="6222b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6222b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6222b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6222b-111">Properties</span></span>

<span data-ttu-id="6222b-112">Die **Thread \_ v2- \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6222b-112">The **Thread\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6222b-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="6222b-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6222b-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6222b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6222b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6222b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6222b-116">Qualifizierer: wmidataid (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="6222b-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="6222b-117">Prozess Bezeichner des am Ereignis beteiligten Threads.</span><span class="sxs-lookup"><span data-stu-id="6222b-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="6222b-118">StackBase</span><span class="sxs-lookup"><span data-stu-id="6222b-118">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6222b-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6222b-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6222b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6222b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6222b-121">Qualifizierer: wmidataid (3), Zeiger</span><span class="sxs-lookup"><span data-stu-id="6222b-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6222b-122">Basisadresse des Thread Stapels.</span><span class="sxs-lookup"><span data-stu-id="6222b-122">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="6222b-123">StackLimit</span><span class="sxs-lookup"><span data-stu-id="6222b-123">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6222b-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6222b-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6222b-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6222b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6222b-126">Qualifizierer: wmidataid (4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="6222b-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6222b-127">Grenzwert für den Thread Stapel.</span><span class="sxs-lookup"><span data-stu-id="6222b-127">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="6222b-128">Startaddr</span><span class="sxs-lookup"><span data-stu-id="6222b-128">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6222b-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6222b-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6222b-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6222b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6222b-131">Qualifizierer: wmidataid (7), Zeiger</span><span class="sxs-lookup"><span data-stu-id="6222b-131">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6222b-132">Die Speicheradresse, an der die Ablauf Verfolgung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="6222b-132">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="6222b-133">Subprocesstag</span><span class="sxs-lookup"><span data-stu-id="6222b-133">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6222b-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6222b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6222b-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6222b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6222b-136">Qualifizierer: wmidataid (10), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="6222b-136">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="6222b-137">Identifiziert den Dienst, wenn der Thread einem Dienst gehört. andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6222b-137">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="6222b-138">Tebbase</span><span class="sxs-lookup"><span data-stu-id="6222b-138">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6222b-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6222b-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6222b-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6222b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6222b-141">Qualifizierer: wmidataid (9), Zeiger</span><span class="sxs-lookup"><span data-stu-id="6222b-141">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6222b-142">Basisadresse für Thread Umgebungsblock.</span><span class="sxs-lookup"><span data-stu-id="6222b-142">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="6222b-143">Tthreadid</span><span class="sxs-lookup"><span data-stu-id="6222b-143">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6222b-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6222b-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6222b-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6222b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6222b-146">Qualifizierer: wmidataid (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="6222b-146">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="6222b-147">Thread Bezeichner des am Ereignis beteiligten Threads.</span><span class="sxs-lookup"><span data-stu-id="6222b-147">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="6222b-148">Userstackbase</span><span class="sxs-lookup"><span data-stu-id="6222b-148">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6222b-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6222b-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6222b-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6222b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6222b-151">Qualifizierer: wmidataid (5), Zeiger</span><span class="sxs-lookup"><span data-stu-id="6222b-151">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6222b-152">Basisadresse für den benutzermodusstapel des Threads.</span><span class="sxs-lookup"><span data-stu-id="6222b-152">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="6222b-153">Userstacklimit</span><span class="sxs-lookup"><span data-stu-id="6222b-153">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6222b-154">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6222b-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6222b-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6222b-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6222b-156">Qualifizierer: wmidataid (6), Zeiger</span><span class="sxs-lookup"><span data-stu-id="6222b-156">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6222b-157">Limit für den benutzermodusstapel des Threads.</span><span class="sxs-lookup"><span data-stu-id="6222b-157">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="6222b-158">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="6222b-158">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6222b-159">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6222b-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6222b-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6222b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6222b-161">Qualifizierer: wmidataid (8), Zeiger</span><span class="sxs-lookup"><span data-stu-id="6222b-161">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6222b-162">Die Startadresse der Funktion, die von diesem Thread ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6222b-162">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6222b-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6222b-163">Remarks</span></span>

<span data-ttu-id="6222b-164">Die Ereignis Typen DCStart und DCEnd zählen die Threads, die derzeit zum Zeitpunkt der Kernel Sitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6222b-164">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="6222b-165">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6222b-165">Requirements</span></span>



| <span data-ttu-id="6222b-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6222b-166">Requirement</span></span> | <span data-ttu-id="6222b-167">Wert</span><span class="sxs-lookup"><span data-stu-id="6222b-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6222b-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6222b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="6222b-169">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6222b-169">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6222b-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6222b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="6222b-171">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6222b-171">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6222b-172">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6222b-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6222b-173">**Aden**</span><span class="sxs-lookup"><span data-stu-id="6222b-173">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="6222b-174">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="6222b-174">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




