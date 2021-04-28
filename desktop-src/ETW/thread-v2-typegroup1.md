---
description: 'Thread_V2_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für Threadstart- und -endereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
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
ms.openlocfilehash: 24ac4655fc374c40eb530828229a319f9ee1375e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105658"
---
# <a name="thread_v2_typegroup1-class"></a><span data-ttu-id="b5d3e-104">Thread \_ V2 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="b5d3e-104">Thread\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="b5d3e-105">Diese Klasse ist die Ereignistypklasse für Threadstart- und -endereignisse.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="b5d3e-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d3e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5d3e-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b5d3e-108">Member</span><span class="sxs-lookup"><span data-stu-id="b5d3e-108">Members</span></span>

<span data-ttu-id="b5d3e-109">Die **Klasse Thread \_ V2 \_ TypeGroup1** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="b5d3e-109">The **Thread\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="b5d3e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5d3e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5d3e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5d3e-111">Properties</span></span>

<span data-ttu-id="b5d3e-112">Die **Klasse Thread \_ V2 \_ TypeGroup1** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-112">The **Thread\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5d3e-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="b5d3e-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5d3e-114">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b5d3e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5d3e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-116">Qualifizierer: WmiDataId(1), Format("x")</span><span class="sxs-lookup"><span data-stu-id="b5d3e-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="b5d3e-117">Prozessbezeichner des threads, der am Ereignis beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="b5d3e-118">StackBase</span><span class="sxs-lookup"><span data-stu-id="b5d3e-118">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5d3e-119">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b5d3e-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5d3e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-121">Qualifizierer: WmiDataId(3), Zeiger</span><span class="sxs-lookup"><span data-stu-id="b5d3e-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b5d3e-122">Basisadresse des Threadstapels.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-122">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="b5d3e-123">StackLimit</span><span class="sxs-lookup"><span data-stu-id="b5d3e-123">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5d3e-124">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b5d3e-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5d3e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-126">Qualifizierer: WmiDataId(4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="b5d3e-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b5d3e-127">Limit des Threadstapels.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-127">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="b5d3e-128">StartAddr</span><span class="sxs-lookup"><span data-stu-id="b5d3e-128">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5d3e-129">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b5d3e-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5d3e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-131">Qualifizierer: WmiDataId(7), Zeiger</span><span class="sxs-lookup"><span data-stu-id="b5d3e-131">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b5d3e-132">Speicheradresse, an der die Ablaufverfolgung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-132">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="b5d3e-133">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="b5d3e-133">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5d3e-134">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b5d3e-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5d3e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-136">Qualifizierer: WmiDataId(10), Format("x")</span><span class="sxs-lookup"><span data-stu-id="b5d3e-136">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="b5d3e-137">Identifiziert den Dienst, wenn sich der Thread im Besitz eines Diensts befindet. andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b5d3e-137">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="b5d3e-138">TebBase</span><span class="sxs-lookup"><span data-stu-id="b5d3e-138">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5d3e-139">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b5d3e-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5d3e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-141">Qualifizierer: WmiDataId(9), Zeiger</span><span class="sxs-lookup"><span data-stu-id="b5d3e-141">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b5d3e-142">Basisadresse des Threadumgebungsblocks.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-142">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="b5d3e-143">TThreadId</span><span class="sxs-lookup"><span data-stu-id="b5d3e-143">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5d3e-144">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b5d3e-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5d3e-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-146">Qualifizierer: WmiDataId(2), Format("x")</span><span class="sxs-lookup"><span data-stu-id="b5d3e-146">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="b5d3e-147">Threadbezeichner des Threads, der am Ereignis beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-147">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="b5d3e-148">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="b5d3e-148">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5d3e-149">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b5d3e-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5d3e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-151">Qualifizierer: WmiDataId(5), Zeiger</span><span class="sxs-lookup"><span data-stu-id="b5d3e-151">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b5d3e-152">Basisadresse des Benutzermodusstapels des Threads.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-152">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="b5d3e-153">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="b5d3e-153">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5d3e-154">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b5d3e-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5d3e-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-156">Qualifizierer: WmiDataId(6), Zeiger</span><span class="sxs-lookup"><span data-stu-id="b5d3e-156">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b5d3e-157">Limit des Benutzermodusstapels des Threads.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-157">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="b5d3e-158">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="b5d3e-158">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5d3e-159">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b5d3e-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5d3e-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5d3e-161">Qualifizierer: WmiDataId(8), Zeiger</span><span class="sxs-lookup"><span data-stu-id="b5d3e-161">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b5d3e-162">Startadresse der Funktion, die von diesem Thread ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-162">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5d3e-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5d3e-163">Remarks</span></span>

<span data-ttu-id="b5d3e-164">Die Ereignistypen DCStart und DCEnd aufzählen die Threads, die derzeit zum Zeitpunkt des Starts bzw. Endes der Kernelsitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b5d3e-164">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d3e-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5d3e-165">Requirements</span></span>



| <span data-ttu-id="b5d3e-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5d3e-166">Requirement</span></span> | <span data-ttu-id="b5d3e-167">Wert</span><span class="sxs-lookup"><span data-stu-id="b5d3e-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b5d3e-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5d3e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d3e-169">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5d3e-169">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b5d3e-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5d3e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d3e-171">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5d3e-171">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5d3e-172">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b5d3e-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d3e-173">**Thread**</span><span class="sxs-lookup"><span data-stu-id="b5d3e-173">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="b5d3e-174">**Thread \_ V2**</span><span class="sxs-lookup"><span data-stu-id="b5d3e-174">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




