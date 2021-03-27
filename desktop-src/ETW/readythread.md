---
description: Diese Klasse ist die Ereignistyp Klasse für bereite Thread Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: "\"Leserythread\"-Klasse"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: e10029c0397c16a5a5eb30be6e3db64c0baec596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862876"
---
# <a name="readythread-class"></a><span data-ttu-id="fe877-104">"Leserythread"-Klasse</span><span class="sxs-lookup"><span data-stu-id="fe877-104">ReadyThread class</span></span>

<span data-ttu-id="fe877-105">Diese Klasse ist die Ereignistyp Klasse für bereite Thread Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="fe877-105">This class is the event type class for ready thread events.</span></span>

<span data-ttu-id="fe877-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="fe877-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe877-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe877-107">Syntax</span></span>

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a><span data-ttu-id="fe877-108">Member</span><span class="sxs-lookup"><span data-stu-id="fe877-108">Members</span></span>

<span data-ttu-id="fe877-109">Die " **leserythread** "-Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fe877-109">The **ReadyThread** class has these types of members:</span></span>

-   [<span data-ttu-id="fe877-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe877-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe877-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe877-111">Properties</span></span>

<span data-ttu-id="fe877-112">Die " **leserythread** "-Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fe877-112">The **ReadyThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe877-113">Anpassung erhöhen</span><span class="sxs-lookup"><span data-stu-id="fe877-113">AdjustIncrement</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe877-114">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="fe877-114">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="fe877-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe877-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe877-116">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="fe877-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="fe877-117">Der Wert, mit dem die Priorität angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="fe877-117">The value by which the priority is being adjusted.</span></span>

</dd> <dt>

<span data-ttu-id="fe877-118">Adjustreason</span><span class="sxs-lookup"><span data-stu-id="fe877-118">AdjustReason</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe877-119">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="fe877-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="fe877-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe877-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe877-121">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="fe877-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="fe877-122">Der Grund für die Prioritäts Erhöhung.</span><span class="sxs-lookup"><span data-stu-id="fe877-122">The reason for the priority boost.</span></span>



| <span data-ttu-id="fe877-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fe877-123">Value</span></span>                                                                        | <span data-ttu-id="fe877-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fe877-124">Meaning</span></span>                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe877-125"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fe877-125"><dt>0</dt></span></span> </dl> | <span data-ttu-id="fe877-126">Das Inkrement wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fe877-126">Ignore the increment.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="fe877-127"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fe877-127"><dt>1</dt></span></span> </dl> | <span data-ttu-id="fe877-128">Wenden Sie das Inkrement an, das am Ende jedes Quantums inkrementell beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="fe877-128">Apply the increment, which will decay incrementally at the end of each quantum.</span></span><br/>                              |
| <dl> <span data-ttu-id="fe877-129"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fe877-129"><dt>2</dt></span></span> </dl> | <span data-ttu-id="fe877-130">Wenden Sie das Inkrement als Verstärkung an, die vollständig bei Quantum (in der Regel für die Prioritäts Spende) verfällt.</span><span class="sxs-lookup"><span data-stu-id="fe877-130">Apply the increment as a boost that will decay in its entirety at quantum (typically for priority donation).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fe877-131">Flag</span><span class="sxs-lookup"><span data-stu-id="fe877-131">Flag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe877-132">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="fe877-132">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="fe877-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe877-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe877-134">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="fe877-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="fe877-135">Im folgenden sind die möglichen Statusflags aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="fe877-135">The following are the possible state flags:</span></span>



| <span data-ttu-id="fe877-136">Wert</span><span class="sxs-lookup"><span data-stu-id="fe877-136">Value</span></span>                                                                          | <span data-ttu-id="fe877-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fe877-137">Meaning</span></span>                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe877-138"><dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="fe877-138"><dt>0x1</dt></span></span> </dl> | <span data-ttu-id="fe877-139">Der Thread wurde von DPC (verzögerter Prozedur aufzurufen) neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="fe877-139">The thread has been readied from DPC (deferred procedure call).</span></span><br/> |
| <dl> <span data-ttu-id="fe877-140"><dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="fe877-140"><dt>0x2</dt></span></span> </dl> | <span data-ttu-id="fe877-141">Der Kernel Stapel wird zurzeit ausgetauscht.</span><span class="sxs-lookup"><span data-stu-id="fe877-141">The kernel stack is currently swapped out.</span></span><br/>                      |
| <dl> <span data-ttu-id="fe877-142"><dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="fe877-142"><dt>0x4</dt></span></span> </dl> | <span data-ttu-id="fe877-143">Der Prozess Adressraum wird ausgetauscht.</span><span class="sxs-lookup"><span data-stu-id="fe877-143">The process address space is swapped out.</span></span><br/>                       |



 

<span data-ttu-id="fe877-144">Beachten Sie Folgendes: Wenn der Kernel Stapel oder der Prozess Adressraum ausgetauscht wird, gibt es nach dem Kernel Stapel ein zusätzliches "Read-Thread"-Ereignis, oder der Prozess Adressraum wird wieder in den Austausch eingefügt, und der Thread wird für die Weiterleitung bereit.</span><span class="sxs-lookup"><span data-stu-id="fe877-144">Note that when the kernel stack or the process address space is swapped out, there will be an additional ReadyThread event after the kernel stack or the process address space has been swapped back in and the thread is made ready to be dispatched.</span></span>

</dd> <dt>

<span data-ttu-id="fe877-145">Reserviert</span><span class="sxs-lookup"><span data-stu-id="fe877-145">Reserved</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe877-146">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="fe877-146">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="fe877-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe877-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe877-148">Qualifizierer: wmidataid (5)</span><span class="sxs-lookup"><span data-stu-id="fe877-148">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="fe877-149">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="fe877-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="fe877-150">Tthreadid</span><span class="sxs-lookup"><span data-stu-id="fe877-150">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe877-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe877-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe877-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe877-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe877-153">Qualifizierer: wmidataid (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="fe877-153">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="fe877-154">Der Thread Bezeichner des Threads, der für die Ausführung neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fe877-154">The thread identifier of the thread being readied for execution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe877-155">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fe877-155">Requirements</span></span>



| <span data-ttu-id="fe877-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe877-156">Requirement</span></span> | <span data-ttu-id="fe877-157">Wert</span><span class="sxs-lookup"><span data-stu-id="fe877-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="fe877-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe877-158">Minimum supported client</span></span><br/> | <span data-ttu-id="fe877-159">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe877-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fe877-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe877-160">Minimum supported server</span></span><br/> | <span data-ttu-id="fe877-161">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe877-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fe877-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fe877-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe877-163">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="fe877-163">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




