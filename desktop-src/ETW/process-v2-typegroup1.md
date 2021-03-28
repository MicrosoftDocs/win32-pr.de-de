---
description: Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: ff5c1f64-2087-4238-81f9-6283f0f0e68a
title: Process_V2_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup1
- Process_V2_TypeGroup1.UniqueProcessKey
- Process_V2_TypeGroup1.ProcessId
- Process_V2_TypeGroup1.ParentId
- Process_V2_TypeGroup1.SessionId
- Process_V2_TypeGroup1.ExitStatus
- Process_V2_TypeGroup1.UserSID
- Process_V2_TypeGroup1.ImageFileName
- Process_V2_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01da5a8254627d6378c9f99aa2ba36dc6714e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980408"
---
# <a name="process_v2_typegroup1-class"></a><span data-ttu-id="cbfd3-104">Process \_ v2 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="cbfd3-104">Process\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="cbfd3-105">Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="cbfd3-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbfd3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbfd3-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_V2_TypeGroup1 : Process_V2
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="cbfd3-108">Member</span><span class="sxs-lookup"><span data-stu-id="cbfd3-108">Members</span></span>

<span data-ttu-id="cbfd3-109">Die **Process \_ v2 \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cbfd3-109">The **Process\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="cbfd3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbfd3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cbfd3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbfd3-111">Properties</span></span>

<span data-ttu-id="cbfd3-112">Die **Process \_ v2 \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-112">The **Process\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cbfd3-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="cbfd3-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbfd3-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cbfd3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbfd3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-116">Qualifizierer: wmidataid (8), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="cbfd3-116">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="cbfd3-117">Vollständige Befehlszeile des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="cbfd3-118">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="cbfd3-118">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbfd3-119">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cbfd3-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbfd3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-121">Qualifizierer: wmidataid (5)</span><span class="sxs-lookup"><span data-stu-id="cbfd3-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="cbfd3-122">Beenden Sie den Status des beendeten Prozesses.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-122">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="cbfd3-123">Imagefilename</span><span class="sxs-lookup"><span data-stu-id="cbfd3-123">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbfd3-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cbfd3-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbfd3-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-126">Qualifizierer: wmidataid (7), stringbeendigung ("nullterminiert")</span><span class="sxs-lookup"><span data-stu-id="cbfd3-126">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="cbfd3-127">Pfad zur ausführbaren Datei des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-127">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="cbfd3-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="cbfd3-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbfd3-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cbfd3-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbfd3-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-131">Qualifizierer: wmidataid (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="cbfd3-131">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="cbfd3-132">Eindeutiger Bezeichner des Prozesses, der diesen Prozess erstellt.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="cbfd3-133">Die prozesbezeichnernummern werden wieder verwendet, sodass Sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="cbfd3-134">Es ist möglich, dass der durch "parameterprocessid" identifizierte Prozess beendet wird, sodass "parameterprocessid" möglicherweise nicht auf einen laufenden Prozess verweist.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="cbfd3-135">Es ist auch möglich, dass "paramedprocessid" fälschlicherweise auf einen Prozess verweist, der einen Prozess Bezeichner wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="cbfd3-136">ProcessId</span><span class="sxs-lookup"><span data-stu-id="cbfd3-136">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbfd3-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cbfd3-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbfd3-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-139">Qualifizierer: wmidataid (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="cbfd3-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="cbfd3-140">Die globale Prozess-ID, mit der Sie einen Prozess identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-140">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="cbfd3-141">Der Wert ist gültig ab dem Zeitpunkt, zu dem ein Prozess erstellt wird, bis er beendet wird.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-141">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="cbfd3-142">SessionID</span><span class="sxs-lookup"><span data-stu-id="cbfd3-142">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbfd3-143">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cbfd3-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbfd3-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-145">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="cbfd3-145">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="cbfd3-146">Eindeutiger Bezeichner, den ein Betriebssystem generiert, wenn eine neue Sitzung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-146">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="cbfd3-147">Eine Sitzung erstreckt sich über einen Zeitraum von der Anmeldung bis zum Abmelden von einem bestimmten System.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-147">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="cbfd3-148">Uniqueprocesskey</span><span class="sxs-lookup"><span data-stu-id="cbfd3-148">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbfd3-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cbfd3-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbfd3-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-151">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="cbfd3-151">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cbfd3-152">Die Adresse des Prozess Objekts im Kernel.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-152">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="cbfd3-153">UserSID</span><span class="sxs-lookup"><span data-stu-id="cbfd3-153">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbfd3-154">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="cbfd3-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbfd3-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbfd3-156">Qualifizierer: wmidataid (6), Erweiterung ("sid")</span><span class="sxs-lookup"><span data-stu-id="cbfd3-156">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="cbfd3-157">Sicherheits-ID (SID) für den Benutzer Kontext, in dem das Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-157">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbfd3-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbfd3-158">Remarks</span></span>

<span data-ttu-id="cbfd3-159">Die Ereignis Typen DCStart und DCEnd zählen den Prozess, der derzeit ausgeführt wird, einschließlich Leerlauf und System Prozess, zu dem Zeitpunkt, zu dem die Kernel Sitzung beginnt bzw. endet.</span><span class="sxs-lookup"><span data-stu-id="cbfd3-159">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbfd3-160">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cbfd3-160">Requirements</span></span>



| <span data-ttu-id="cbfd3-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbfd3-161">Requirement</span></span> | <span data-ttu-id="cbfd3-162">Wert</span><span class="sxs-lookup"><span data-stu-id="cbfd3-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="cbfd3-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbfd3-163">Minimum supported client</span></span><br/> | <span data-ttu-id="cbfd3-164">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbfd3-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cbfd3-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbfd3-165">Minimum supported server</span></span><br/> | <span data-ttu-id="cbfd3-166">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbfd3-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cbfd3-167">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cbfd3-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbfd3-168">**Prozess \_ v2**</span><span class="sxs-lookup"><span data-stu-id="cbfd3-168">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




