---
description: Eine abstrakte Klasse, von der alle Ereignis Ablauf Verfolgungs Klassen abgeleitet werden.
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: EventTrace-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: f04399942b39a2da5b746933884a436a65bb370c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752408"
---
# <a name="eventtrace-class"></a><span data-ttu-id="ff9b6-103">EventTrace-Klasse</span><span class="sxs-lookup"><span data-stu-id="ff9b6-103">EventTrace class</span></span>

<span data-ttu-id="ff9b6-104">Eine abstrakte Klasse, von der alle Ereignis Ablauf Verfolgungs Klassen abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-104">An abstract class from which all event trace classes are derived.</span></span>

<span data-ttu-id="ff9b6-105">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff9b6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff9b6-106">Syntax</span></span>

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a><span data-ttu-id="ff9b6-107">Member</span><span class="sxs-lookup"><span data-stu-id="ff9b6-107">Members</span></span>

<span data-ttu-id="ff9b6-108">Die **EventTrace** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ff9b6-108">The **EventTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="ff9b6-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff9b6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ff9b6-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff9b6-110">Properties</span></span>

<span data-ttu-id="ff9b6-111">Die **EventTrace** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-111">The **EventTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ff9b6-112">**Eventguid**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-112">**EventGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-113">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="ff9b6-113">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-115">Qualifizierer: **wmidataid** (8), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-115">Qualifiers: **WmiDataId** (8), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-116">Die Ereignis-Ablaufverfolgungs-Klassen-GUID dieses Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-116">Event trace class GUID of this event.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-117">**Eventsize**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-117">**EventSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-118">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-120">Qualifizierer: **wmidataid** (1)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-120">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-121">Gesamtanzahl der Bytes des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-121">Total number of bytes of the event.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-122">**EventType**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-122">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-123">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-123">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-125">Qualifizierer: **wmidataid** (3)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-125">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-126">Vom Anbieter definierter Ereignistyp.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-126">Provider-defined event type.</span></span> <span data-ttu-id="ff9b6-127">Gibt Aufschluss darüber, welche Ereignistyp Klasse zum Entschlüsseln der von einem Anbieter definierten Ereignisdaten verwendet werden soll (die Daten, auf die von " **mufdata**" verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-127">Tells you which event type class to use to decipher the provider-defined event data (the data pointed to by **MofData**.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-128">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-128">**InstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-131">Qualifizierer: **wmidataid** (11)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-131">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-132">Der Bezeichner dieser Ereignis Instanz.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-132">Identifier of this event instance.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-133">**Kernelzeit**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-133">**KernelTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-136">Qualifizierer: **wmidataid** (9)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-136">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-137">Verstrichene Ausführungszeit für Kernel Modus-Anweisungen in CPU-Ticks.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-137">Elapsed execution time for kernel-mode instructions, in CPU ticks.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-138">**"MUF"**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-138">**MofData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-141">Qualifizierer: **wmidataid** (14), **Zeiger**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-141">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-142">Zeiger auf die anbieterspezifischen Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-142">Pointer to the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-143">**"Muength"**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-143">**MofLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-146">Qualifizierer: **wmidataid** (15)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-146">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-147">Die Länge der anbieterspezifischen Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-147">Length of the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-148">**Parametriguid**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-148">**ParentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-149">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="ff9b6-149">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-151">Qualifizierer: **wmidataid** (12), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-151">Qualifiers: **WmiDataId** (12), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-152">Die Ereignis-Ablauf Verfolgungs Klassen-GUID der übergeordneten Instanz.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-152">Event trace class GUID of the parent instance.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-153">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-153">**ParentInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-154">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-156">Qualifizierer: **wmidataid** (13)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-156">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-157">Der Bezeichner der übergeordneten Instanzdaten.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-157">Identifier of the parent instance data.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-158">**Reservedheaderfield**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-158">**ReservedHeaderField**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-159">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-161">Qualifizierer: **wmidataid** (2)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-161">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-162">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-162">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-163">**ThreadID**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-163">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-164">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-166">Qualifizierer: **wmidataid** (6), **Zeiger**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-166">Qualifiers: **WmiDataId** (6), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-167">Gibt den Thread an, der das Ereignis generiert hat</span><span class="sxs-lookup"><span data-stu-id="ff9b6-167">Identifies the thread that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-168">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-168">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-169">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-171">Qualifizierer: **wmidataid** (7)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-171">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-172">Enthält das Datum und die Uhrzeit des Auftretens des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-172">Contains the date and time when the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-173">**TraceLevel**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-173">**TraceLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-174">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-176">Qualifizierer: **wmidataid** (4)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-176">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-177">Vom Anbieter definierter Wert, der den Schweregrad definiert, der zum Generieren des Ereignisses verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-177">Provider-defined value that defines the severity level used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-178">**Traceversion**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-178">**TraceVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-179">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-181">Qualifizierer: **wmidataid** (5)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-181">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-182">Anbieter definierte Versionsnummer der Ereignis Ablauf Verfolgungs Klasse, die zum Generieren des Ereignisses verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-182">Provider-defined version number of the event trace class used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="ff9b6-183">**Usertime**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-183">**UserTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff9b6-184">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ff9b6-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff9b6-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff9b6-186">Qualifizierer: **wmidataid** (10)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-186">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="ff9b6-187">Verstrichene Ausführungszeit für benutzermodusanweisungen in CPU-Ticks.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-187">Elapsed execution time for user-mode instructions, in CPU ticks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff9b6-188">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff9b6-188">Remarks</span></span>

<span data-ttu-id="ff9b6-189">Verwenden Sie diese Eigenschaften nicht.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-189">Do not use these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff9b6-190">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-190">Requirements</span></span>



| <span data-ttu-id="ff9b6-191">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff9b6-191">Requirement</span></span> | <span data-ttu-id="ff9b6-192">Wert</span><span class="sxs-lookup"><span data-stu-id="ff9b6-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff9b6-193">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-193">Minimum supported client</span></span><br/> | <span data-ttu-id="ff9b6-194">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff9b6-194">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ff9b6-195">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-195">Minimum supported server</span></span><br/> | <span data-ttu-id="ff9b6-196">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff9b6-196">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ff9b6-197">MOF</span><span class="sxs-lookup"><span data-stu-id="ff9b6-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff9b6-198"><dt>WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ff9b6-198"><dt>Wmi.mof</dt></span></span> </dl> |



 

 




