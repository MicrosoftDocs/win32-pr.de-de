---
description: Diese Klasse ist die Ereignistyp Klasse für Thread Start Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 412de56f-4f54-46e8-ab60-d47371247e79
title: Thread_V1_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup1
- Thread_V1_TypeGroup1.ProcessId
- Thread_V1_TypeGroup1.TThreadId
- Thread_V1_TypeGroup1.StackBase
- Thread_V1_TypeGroup1.StackLimit
- Thread_V1_TypeGroup1.UserStackBase
- Thread_V1_TypeGroup1.UserStackLimit
- Thread_V1_TypeGroup1.StartAddr
- Thread_V1_TypeGroup1.Win32StartAddr
- Thread_V1_TypeGroup1.WaitMode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 13c419b417b614eb9022d1cb7c09a84ca705b3dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959989"
---
# <a name="thread_v1_typegroup1-class"></a><span data-ttu-id="55778-104">Thread \_ v1 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="55778-104">Thread\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="55778-105">Diese Klasse ist die Ereignistyp Klasse für Thread Start Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="55778-105">This class is the event type class for thread start events.</span></span>

<span data-ttu-id="55778-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="55778-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="55778-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="55778-107">Syntax</span></span>

``` syntax
[EventType{1, 3}, EventTypeName{"Start", "DCStart"}]
class Thread_V1_TypeGroup1 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  sint8  WaitMode;
};
```

## <a name="members"></a><span data-ttu-id="55778-108">Member</span><span class="sxs-lookup"><span data-stu-id="55778-108">Members</span></span>

<span data-ttu-id="55778-109">Die **Thread \_ v1 \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="55778-109">The **Thread\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="55778-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55778-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55778-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55778-111">Properties</span></span>

<span data-ttu-id="55778-112">Die **Thread \_ v1 \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="55778-112">The **Thread\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55778-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="55778-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55778-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55778-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55778-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55778-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55778-116">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="55778-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="55778-117">Prozess Bezeichner des am Ereignis beteiligten Threads.</span><span class="sxs-lookup"><span data-stu-id="55778-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="55778-118">**Windows Server 2003:** Enthält das Format ("x") Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="55778-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="55778-119">StackBase</span><span class="sxs-lookup"><span data-stu-id="55778-119">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55778-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55778-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55778-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55778-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55778-122">Qualifizierer: wmidataid (3), Zeiger</span><span class="sxs-lookup"><span data-stu-id="55778-122">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="55778-123">Basisadresse des Thread Stapels.</span><span class="sxs-lookup"><span data-stu-id="55778-123">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="55778-124">StackLimit</span><span class="sxs-lookup"><span data-stu-id="55778-124">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55778-125">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55778-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55778-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55778-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55778-127">Qualifizierer: wmidataid (4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="55778-127">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="55778-128">Grenzwert für den Thread Stapel.</span><span class="sxs-lookup"><span data-stu-id="55778-128">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="55778-129">Startaddr</span><span class="sxs-lookup"><span data-stu-id="55778-129">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55778-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55778-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55778-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55778-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55778-132">Qualifizierer: wmidataid (7), Zeiger</span><span class="sxs-lookup"><span data-stu-id="55778-132">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="55778-133">Die Speicheradresse, an der die Ablauf Verfolgung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="55778-133">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="55778-134">Tthreadid</span><span class="sxs-lookup"><span data-stu-id="55778-134">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55778-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55778-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55778-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55778-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55778-137">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="55778-137">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="55778-138">Thread Bezeichner des am Ereignis beteiligten Threads.</span><span class="sxs-lookup"><span data-stu-id="55778-138">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="55778-139">**Windows Server 2003:** Enthält das Format ("x") Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="55778-139">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="55778-140">Userstackbase</span><span class="sxs-lookup"><span data-stu-id="55778-140">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55778-141">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55778-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55778-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55778-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55778-143">Qualifizierer: wmidataid (5), Zeiger</span><span class="sxs-lookup"><span data-stu-id="55778-143">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="55778-144">Basisadresse für den benutzermodusstapel des Threads.</span><span class="sxs-lookup"><span data-stu-id="55778-144">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="55778-145">Userstacklimit</span><span class="sxs-lookup"><span data-stu-id="55778-145">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55778-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55778-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55778-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55778-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55778-148">Qualifizierer: wmidataid (6), Zeiger</span><span class="sxs-lookup"><span data-stu-id="55778-148">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="55778-149">Limit für den benutzermodusstapel des Threads.</span><span class="sxs-lookup"><span data-stu-id="55778-149">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="55778-150">WaitMode</span><span class="sxs-lookup"><span data-stu-id="55778-150">WaitMode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55778-151">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="55778-151">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="55778-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55778-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55778-153">Qualifizierer: wmidataid (9), Format ("c")</span><span class="sxs-lookup"><span data-stu-id="55778-153">Qualifiers: WmiDataId(9), Format("c")</span></span>
</dt> </dl>

<span data-ttu-id="55778-154">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="55778-154">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="55778-155">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="55778-155">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55778-156">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55778-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55778-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55778-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55778-158">Qualifizierer: wmidataid (8), Zeiger</span><span class="sxs-lookup"><span data-stu-id="55778-158">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="55778-159">Die Startadresse der Funktion, die von diesem Thread ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="55778-159">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55778-160">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="55778-160">Requirements</span></span>



| <span data-ttu-id="55778-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55778-161">Requirement</span></span> | <span data-ttu-id="55778-162">Wert</span><span class="sxs-lookup"><span data-stu-id="55778-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="55778-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55778-163">Minimum supported client</span></span><br/> | <span data-ttu-id="55778-164">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55778-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="55778-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55778-165">Minimum supported server</span></span><br/> | <span data-ttu-id="55778-166">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55778-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="55778-167">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="55778-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55778-168">**Thread \_ v1**</span><span class="sxs-lookup"><span data-stu-id="55778-168">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




