---
description: Diese Klasse ist die Ereignistyp Klasse für Kontextwechsel Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: Cswitch-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSwitch
- CSwitch.NewThreadId
- CSwitch.OldThreadId
- CSwitch.NewThreadPriority
- CSwitch.OldThreadPriority
- CSwitch.PreviousCState
- CSwitch.SpareByte
- CSwitch.OldThreadWaitReason
- CSwitch.OldThreadWaitMode
- CSwitch.OldThreadState
- CSwitch.OldThreadWaitIdealProcessor
- CSwitch.NewThreadWaitTime
- CSwitch.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 91004ca276140271e8d73c3fc226e83c4e03d1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214867"
---
# <a name="cswitch-class"></a><span data-ttu-id="6fe0f-104">Cswitch-Klasse</span><span class="sxs-lookup"><span data-stu-id="6fe0f-104">CSwitch class</span></span>

<span data-ttu-id="6fe0f-105">Diese Klasse ist die Ereignistyp Klasse für Kontextwechsel Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-105">This class is the event type class for context switch events.</span></span>

<span data-ttu-id="6fe0f-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe0f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fe0f-107">Syntax</span></span>

``` syntax
[EventType{36}, EventTypeName{"CSwitch"}]
class CSwitch : Thread_V2
{
  uint32 NewThreadId;
  uint32 OldThreadId;
  sint8  NewThreadPriority;
  sint8  OldThreadPriority;
  uint8  PreviousCState;
  sint8  SpareByte;
  sint8  OldThreadWaitReason;
  sint8  OldThreadWaitMode;
  sint8  OldThreadState;
  sint8  OldThreadWaitIdealProcessor;
  uint32 NewThreadWaitTime;
  uint32 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="6fe0f-108">Member</span><span class="sxs-lookup"><span data-stu-id="6fe0f-108">Members</span></span>

<span data-ttu-id="6fe0f-109">Die **cswitch** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6fe0f-109">The **CSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="6fe0f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6fe0f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6fe0f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6fe0f-111">Properties</span></span>

<span data-ttu-id="6fe0f-112">Die **cswitch** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-112">The **CSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6fe0f-113">**Newthreadid**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-113">**NewThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fe0f-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-116">Qualifizierer: wmidataid (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="6fe0f-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="6fe0f-117">Neue Thread-ID nach dem Switch.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-117">New thread ID after the switch.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-118">**Newthreadpriority**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-118">**NewThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fe0f-119">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-121">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="6fe0f-122">Thread Priorität des neuen Threads.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-122">Thread priority of the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-123">**Newthreadwaittime**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-123">**NewThreadWaitTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fe0f-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-126">Qualifizierer: wmidataid (11), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="6fe0f-126">Qualifiers: WmiDataId(11), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="6fe0f-127">Die Wartezeit für den neuen Thread.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-127">Wait time for the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-128">**Oldthreadid**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-128">**OldThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fe0f-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-131">Qualifizierer: wmidataid (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="6fe0f-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="6fe0f-132">Vorherige Thread-ID.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-132">Previous thread ID.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-133">**Oldthreadpriority**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-133">**OldThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fe0f-134">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-134">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-136">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-136">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="6fe0f-137">Thread Priorität des vorherigen Threads.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-137">Thread priority of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-138">**Oldthreadstate**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-138">**OldThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fe0f-139">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-139">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-141">Qualifizierer: wmidataid (9)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-141">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="6fe0f-142">Zustand des vorherigen Threads.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-142">State of the previous thread.</span></span> <span data-ttu-id="6fe0f-143">Im folgenden sind die möglichen Zustands Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="6fe0f-143">The following are the possible state values:</span></span>

| <span data-ttu-id="6fe0f-144">State</span><span class="sxs-lookup"><span data-stu-id="6fe0f-144">State</span></span> | <span data-ttu-id="6fe0f-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fe0f-145">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="6fe0f-146">0</span><span class="sxs-lookup"><span data-stu-id="6fe0f-146">0</span></span>     | <span data-ttu-id="6fe0f-147">Initialisiert</span><span class="sxs-lookup"><span data-stu-id="6fe0f-147">Initialized</span></span>                                   |
| <span data-ttu-id="6fe0f-148">1</span><span class="sxs-lookup"><span data-stu-id="6fe0f-148">1</span></span>     | <span data-ttu-id="6fe0f-149">Bereit</span><span class="sxs-lookup"><span data-stu-id="6fe0f-149">Ready</span></span>                                         |
| <span data-ttu-id="6fe0f-150">2</span><span class="sxs-lookup"><span data-stu-id="6fe0f-150">2</span></span>     | <span data-ttu-id="6fe0f-151">Wird ausgeführt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-151">Running</span></span>                                       |
| <span data-ttu-id="6fe0f-152">3</span><span class="sxs-lookup"><span data-stu-id="6fe0f-152">3</span></span>     | <span data-ttu-id="6fe0f-153">Standby</span><span class="sxs-lookup"><span data-stu-id="6fe0f-153">Standby</span></span>                                       |
| <span data-ttu-id="6fe0f-154">4</span><span class="sxs-lookup"><span data-stu-id="6fe0f-154">4</span></span>     | <span data-ttu-id="6fe0f-155">Beendet</span><span class="sxs-lookup"><span data-stu-id="6fe0f-155">Terminated</span></span>                                    |
| <span data-ttu-id="6fe0f-156">5</span><span class="sxs-lookup"><span data-stu-id="6fe0f-156">5</span></span>     | <span data-ttu-id="6fe0f-157">Warten</span><span class="sxs-lookup"><span data-stu-id="6fe0f-157">Waiting</span></span>                                       |
| <span data-ttu-id="6fe0f-158">6</span><span class="sxs-lookup"><span data-stu-id="6fe0f-158">6</span></span>     | <span data-ttu-id="6fe0f-159">Übergang</span><span class="sxs-lookup"><span data-stu-id="6fe0f-159">Transition</span></span>                                    |
| <span data-ttu-id="6fe0f-160">7</span><span class="sxs-lookup"><span data-stu-id="6fe0f-160">7</span></span>     | <span data-ttu-id="6fe0f-161">Deferredready (für Windows Server 2003 hinzugefügt)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-161">DeferredReady (added for Windows Server 2003)</span></span> |



 

</dd> <dt>

<span data-ttu-id="6fe0f-162">**Oldthreadwaitidealprocessor**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-162">**OldThreadWaitIdealProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fe0f-163">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-163">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-165">Qualifizierer: wmidataid (10), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="6fe0f-165">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="6fe0f-166">Die ideale Wartezeit für den vorherigen Thread.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-166">Ideal wait time of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-167">**Oldthreadwaitmode**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-167">**OldThreadWaitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fe0f-168">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-168">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-170">Qualifizierer: wmidataid (8)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-170">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="6fe0f-171">Der Wartemodus für den vorherigen Thread.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-171">Wait mode for the previous thread.</span></span> <span data-ttu-id="6fe0f-172">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="6fe0f-172">The following are the possible values:</span></span>

| <span data-ttu-id="6fe0f-173">State</span><span class="sxs-lookup"><span data-stu-id="6fe0f-173">State</span></span> | <span data-ttu-id="6fe0f-174">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fe0f-174">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="6fe0f-175">0</span><span class="sxs-lookup"><span data-stu-id="6fe0f-175">0</span></span>     | <span data-ttu-id="6fe0f-176">Kernel Mode</span><span class="sxs-lookup"><span data-stu-id="6fe0f-176">KernelMode</span></span>  |
| <span data-ttu-id="6fe0f-177">1</span><span class="sxs-lookup"><span data-stu-id="6fe0f-177">1</span></span>     | <span data-ttu-id="6fe0f-178">UserMode</span><span class="sxs-lookup"><span data-stu-id="6fe0f-178">UserMode</span></span>    |



 

</dd> <dt>

<span data-ttu-id="6fe0f-179">**Oldthreadwaitreason**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-179">**OldThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fe0f-180">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-180">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-182">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-182">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="6fe0f-183">Der Warte Grund für den vorherigen Thread.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-183">Wait reason for the previous thread.</span></span> <span data-ttu-id="6fe0f-184">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="6fe0f-184">The following are the possible values:</span></span>

| <span data-ttu-id="6fe0f-185">State</span><span class="sxs-lookup"><span data-stu-id="6fe0f-185">State</span></span> | <span data-ttu-id="6fe0f-186">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fe0f-186">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="6fe0f-187">0</span><span class="sxs-lookup"><span data-stu-id="6fe0f-187">0</span></span>     | <span data-ttu-id="6fe0f-188">Executive</span><span class="sxs-lookup"><span data-stu-id="6fe0f-188">Executive</span></span>         |
| <span data-ttu-id="6fe0f-189">1</span><span class="sxs-lookup"><span data-stu-id="6fe0f-189">1</span></span>     | <span data-ttu-id="6fe0f-190">Freepage</span><span class="sxs-lookup"><span data-stu-id="6fe0f-190">FreePage</span></span>          |
| <span data-ttu-id="6fe0f-191">2</span><span class="sxs-lookup"><span data-stu-id="6fe0f-191">2</span></span>     | <span data-ttu-id="6fe0f-192">PageIn</span><span class="sxs-lookup"><span data-stu-id="6fe0f-192">PageIn</span></span>            |
| <span data-ttu-id="6fe0f-193">3</span><span class="sxs-lookup"><span data-stu-id="6fe0f-193">3</span></span>     | <span data-ttu-id="6fe0f-194">Poolallocation</span><span class="sxs-lookup"><span data-stu-id="6fe0f-194">PoolAllocation</span></span>    |
| <span data-ttu-id="6fe0f-195">4</span><span class="sxs-lookup"><span data-stu-id="6fe0f-195">4</span></span>     | <span data-ttu-id="6fe0f-196">Delta Execution</span><span class="sxs-lookup"><span data-stu-id="6fe0f-196">DelayExecution</span></span>    |
| <span data-ttu-id="6fe0f-197">5</span><span class="sxs-lookup"><span data-stu-id="6fe0f-197">5</span></span>     | <span data-ttu-id="6fe0f-198">Ausgesetzt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-198">Suspended</span></span>         |
| <span data-ttu-id="6fe0f-199">6</span><span class="sxs-lookup"><span data-stu-id="6fe0f-199">6</span></span>     | <span data-ttu-id="6fe0f-200">Userrequest</span><span class="sxs-lookup"><span data-stu-id="6fe0f-200">UserRequest</span></span>       |
| <span data-ttu-id="6fe0f-201">7</span><span class="sxs-lookup"><span data-stu-id="6fe0f-201">7</span></span>     | <span data-ttu-id="6fe0f-202">Wrexecutive</span><span class="sxs-lookup"><span data-stu-id="6fe0f-202">WrExecutive</span></span>       |
| <span data-ttu-id="6fe0f-203">8</span><span class="sxs-lookup"><span data-stu-id="6fe0f-203">8</span></span>     | <span data-ttu-id="6fe0f-204">Wrfreepage</span><span class="sxs-lookup"><span data-stu-id="6fe0f-204">WrFreePage</span></span>        |
| <span data-ttu-id="6fe0f-205">9</span><span class="sxs-lookup"><span data-stu-id="6fe0f-205">9</span></span>     | <span data-ttu-id="6fe0f-206">Wrpagein</span><span class="sxs-lookup"><span data-stu-id="6fe0f-206">WrPageIn</span></span>          |
| <span data-ttu-id="6fe0f-207">10</span><span class="sxs-lookup"><span data-stu-id="6fe0f-207">10</span></span>    | <span data-ttu-id="6fe0f-208">Wrpoolallocation</span><span class="sxs-lookup"><span data-stu-id="6fe0f-208">WrPoolAllocation</span></span>  |
| <span data-ttu-id="6fe0f-209">11</span><span class="sxs-lookup"><span data-stu-id="6fe0f-209">11</span></span>    | <span data-ttu-id="6fe0f-210">Wrdelta-Ausführungszeit</span><span class="sxs-lookup"><span data-stu-id="6fe0f-210">WrDelayExecution</span></span>  |
| <span data-ttu-id="6fe0f-211">12</span><span class="sxs-lookup"><span data-stu-id="6fe0f-211">12</span></span>    | <span data-ttu-id="6fe0f-212">Wrangeh alten</span><span class="sxs-lookup"><span data-stu-id="6fe0f-212">WrSuspended</span></span>       |
| <span data-ttu-id="6fe0f-213">13</span><span class="sxs-lookup"><span data-stu-id="6fe0f-213">13</span></span>    | <span data-ttu-id="6fe0f-214">Wruserrequest</span><span class="sxs-lookup"><span data-stu-id="6fe0f-214">WrUserRequest</span></span>     |
| <span data-ttu-id="6fe0f-215">14</span><span class="sxs-lookup"><span data-stu-id="6fe0f-215">14</span></span>    | <span data-ttu-id="6fe0f-216">Wreventpair</span><span class="sxs-lookup"><span data-stu-id="6fe0f-216">WrEventPair</span></span>       |
| <span data-ttu-id="6fe0f-217">15</span><span class="sxs-lookup"><span data-stu-id="6fe0f-217">15</span></span>    | <span data-ttu-id="6fe0f-218">Wrqueue</span><span class="sxs-lookup"><span data-stu-id="6fe0f-218">WrQueue</span></span>           |
| <span data-ttu-id="6fe0f-219">16</span><span class="sxs-lookup"><span data-stu-id="6fe0f-219">16</span></span>    | <span data-ttu-id="6fe0f-220">Wrlpcreceive</span><span class="sxs-lookup"><span data-stu-id="6fe0f-220">WrLpcReceive</span></span>      |
| <span data-ttu-id="6fe0f-221">17</span><span class="sxs-lookup"><span data-stu-id="6fe0f-221">17</span></span>    | <span data-ttu-id="6fe0f-222">Wrlpkreply</span><span class="sxs-lookup"><span data-stu-id="6fe0f-222">WrLpcReply</span></span>        |
| <span data-ttu-id="6fe0f-223">18</span><span class="sxs-lookup"><span data-stu-id="6fe0f-223">18</span></span>    | <span data-ttu-id="6fe0f-224">Wrvirtualmemory</span><span class="sxs-lookup"><span data-stu-id="6fe0f-224">WrVirtualMemory</span></span>   |
| <span data-ttu-id="6fe0f-225">19</span><span class="sxs-lookup"><span data-stu-id="6fe0f-225">19</span></span>    | <span data-ttu-id="6fe0f-226">Wrpageout</span><span class="sxs-lookup"><span data-stu-id="6fe0f-226">WrPageOut</span></span>         |
| <span data-ttu-id="6fe0f-227">20</span><span class="sxs-lookup"><span data-stu-id="6fe0f-227">20</span></span>    | <span data-ttu-id="6fe0f-228">Wrrendezvous</span><span class="sxs-lookup"><span data-stu-id="6fe0f-228">WrRendezvous</span></span>      |
| <span data-ttu-id="6fe0f-229">21</span><span class="sxs-lookup"><span data-stu-id="6fe0f-229">21</span></span>    | <span data-ttu-id="6fe0f-230">Wrkeyedebug</span><span class="sxs-lookup"><span data-stu-id="6fe0f-230">WrKeyedEvent</span></span>      |
| <span data-ttu-id="6fe0f-231">22</span><span class="sxs-lookup"><span data-stu-id="6fe0f-231">22</span></span>    | <span data-ttu-id="6fe0f-232">Wrterminiert</span><span class="sxs-lookup"><span data-stu-id="6fe0f-232">WrTerminated</span></span>      |
| <span data-ttu-id="6fe0f-233">23</span><span class="sxs-lookup"><span data-stu-id="6fe0f-233">23</span></span>    | <span data-ttu-id="6fe0f-234">Wrprocessinswap</span><span class="sxs-lookup"><span data-stu-id="6fe0f-234">WrProcessInSwap</span></span>   |
| <span data-ttu-id="6fe0f-235">24</span><span class="sxs-lookup"><span data-stu-id="6fe0f-235">24</span></span>    | <span data-ttu-id="6fe0f-236">Wrcpuratecontrol</span><span class="sxs-lookup"><span data-stu-id="6fe0f-236">WrCpuRateControl</span></span>  |
| <span data-ttu-id="6fe0f-237">25</span><span class="sxs-lookup"><span data-stu-id="6fe0f-237">25</span></span>    | <span data-ttu-id="6fe0f-238">Wrcalloutstack</span><span class="sxs-lookup"><span data-stu-id="6fe0f-238">WrCalloutStack</span></span>    |
| <span data-ttu-id="6fe0f-239">26</span><span class="sxs-lookup"><span data-stu-id="6fe0f-239">26</span></span>    | <span data-ttu-id="6fe0f-240">Wrkernel</span><span class="sxs-lookup"><span data-stu-id="6fe0f-240">WrKernel</span></span>          |
| <span data-ttu-id="6fe0f-241">27</span><span class="sxs-lookup"><span data-stu-id="6fe0f-241">27</span></span>    | <span data-ttu-id="6fe0f-242">Wrresource</span><span class="sxs-lookup"><span data-stu-id="6fe0f-242">WrResource</span></span>        |
| <span data-ttu-id="6fe0f-243">28</span><span class="sxs-lookup"><span data-stu-id="6fe0f-243">28</span></span>    | <span data-ttu-id="6fe0f-244">Wrpushlock</span><span class="sxs-lookup"><span data-stu-id="6fe0f-244">WrPushLock</span></span>        |
| <span data-ttu-id="6fe0f-245">29</span><span class="sxs-lookup"><span data-stu-id="6fe0f-245">29</span></span>    | <span data-ttu-id="6fe0f-246">Wrmutex</span><span class="sxs-lookup"><span data-stu-id="6fe0f-246">WrMutex</span></span>           |
| <span data-ttu-id="6fe0f-247">30</span><span class="sxs-lookup"><span data-stu-id="6fe0f-247">30</span></span>    | <span data-ttu-id="6fe0f-248">Wrquantenend</span><span class="sxs-lookup"><span data-stu-id="6fe0f-248">WrQuantumEnd</span></span>      |
| <span data-ttu-id="6fe0f-249">31</span><span class="sxs-lookup"><span data-stu-id="6fe0f-249">31</span></span>    | <span data-ttu-id="6fe0f-250">Wrdispatchint</span><span class="sxs-lookup"><span data-stu-id="6fe0f-250">WrDispatchInt</span></span>     |
| <span data-ttu-id="6fe0f-251">32</span><span class="sxs-lookup"><span data-stu-id="6fe0f-251">32</span></span>    | <span data-ttu-id="6fe0f-252">Wrpreempted</span><span class="sxs-lookup"><span data-stu-id="6fe0f-252">WrPreempted</span></span>       |
| <span data-ttu-id="6fe0f-253">33</span><span class="sxs-lookup"><span data-stu-id="6fe0f-253">33</span></span>    | <span data-ttu-id="6fe0f-254">Wryieldexecution</span><span class="sxs-lookup"><span data-stu-id="6fe0f-254">WrYieldExecution</span></span>  |
| <span data-ttu-id="6fe0f-255">34</span><span class="sxs-lookup"><span data-stu-id="6fe0f-255">34</span></span>    | <span data-ttu-id="6fe0f-256">Wrfastmutex</span><span class="sxs-lookup"><span data-stu-id="6fe0f-256">WrFastMutex</span></span>       |
| <span data-ttu-id="6fe0f-257">35</span><span class="sxs-lookup"><span data-stu-id="6fe0f-257">35</span></span>    | <span data-ttu-id="6fe0f-258">Wrguardecodmutex</span><span class="sxs-lookup"><span data-stu-id="6fe0f-258">WrGuardedMutex</span></span>    |
| <span data-ttu-id="6fe0f-259">36</span><span class="sxs-lookup"><span data-stu-id="6fe0f-259">36</span></span>    | <span data-ttu-id="6fe0f-260">Wrrundown</span><span class="sxs-lookup"><span data-stu-id="6fe0f-260">WrRundown</span></span>         |
| <span data-ttu-id="6fe0f-261">37</span><span class="sxs-lookup"><span data-stu-id="6fe0f-261">37</span></span>    | <span data-ttu-id="6fe0f-262">Maximumwaitreason</span><span class="sxs-lookup"><span data-stu-id="6fe0f-262">MaximumWaitReason</span></span> |



 

</dd> <dt>

<span data-ttu-id="6fe0f-263">**Previouscstate**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-263">**PreviousCState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fe0f-264">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-264">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-266">Qualifizierer: wmidataid (5)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-266">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="6fe0f-267">Der Index des C-Zustands, der zuletzt vom Prozessor verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-267">The index of the C-state that was last used by the processor.</span></span> <span data-ttu-id="6fe0f-268">Der Wert 0 steht für den leichteren Leerlaufzustand mit höheren Werten, die tiefere C-Zustände darstellen.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-268">A value of 0 represents the lightest idle state with higher values representing deeper C-states.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-269">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-269">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fe0f-270">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-271">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-272">Qualifizierer: wmidataid (12)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-272">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="6fe0f-273">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-273">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-274">**Sparebyte**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-274">**SpareByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fe0f-275">Datentyp: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-275">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fe0f-277">Qualifizierer: wmidataid (6)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-277">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="6fe0f-278">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-278">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fe0f-279">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fe0f-279">Remarks</span></span>

<span data-ttu-id="6fe0f-280">Diese Ereignisse führen zu einer hohen Anzahl von Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-280">These events produce a high volume of events.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fe0f-281">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-281">Requirements</span></span>



| <span data-ttu-id="6fe0f-282">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fe0f-282">Requirement</span></span> | <span data-ttu-id="6fe0f-283">Wert</span><span class="sxs-lookup"><span data-stu-id="6fe0f-283">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6fe0f-284">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-284">Minimum supported client</span></span><br/> | <span data-ttu-id="6fe0f-285">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fe0f-285">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6fe0f-286">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6fe0f-286">Minimum supported server</span></span><br/> | <span data-ttu-id="6fe0f-287">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fe0f-287">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6fe0f-288">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6fe0f-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe0f-289">**Aden**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-289">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="6fe0f-290">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-290">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




