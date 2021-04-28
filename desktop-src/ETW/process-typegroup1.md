---
description: 'Process_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für Prozessereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Process_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_TypeGroup1
- Process_TypeGroup1.UniqueProcessKey
- Process_TypeGroup1.ProcessId
- Process_TypeGroup1.ParentId
- Process_TypeGroup1.SessionId
- Process_TypeGroup1.ExitStatus
- Process_TypeGroup1.DirectoryTableBase
- Process_TypeGroup1.UserSID
- Process_TypeGroup1.ImageFileName
- Process_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd67059f5257dad9b66e1c21f642fef04f03719e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106378"
---
# <a name="process_typegroup1-class"></a><span data-ttu-id="b3449-104">Process \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="b3449-104">Process\_TypeGroup1 class</span></span>

<span data-ttu-id="b3449-105">Diese Klasse ist die Ereignistypklasse für Prozessereignisse.</span><span class="sxs-lookup"><span data-stu-id="b3449-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="b3449-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="b3449-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3449-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3449-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_TypeGroup1 : Process
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  uint32 DirectoryTableBase;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="b3449-108">Member</span><span class="sxs-lookup"><span data-stu-id="b3449-108">Members</span></span>

<span data-ttu-id="b3449-109">Die **Process \_ TypeGroup1-Klasse** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="b3449-109">The **Process\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="b3449-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3449-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3449-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3449-111">Properties</span></span>

<span data-ttu-id="b3449-112">Die **Process \_ TypeGroup1-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b3449-112">The **Process\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3449-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="b3449-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3449-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b3449-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3449-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3449-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3449-116">Qualifizierer: WmiDataId(9), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="b3449-116">Qualifiers: WmiDataId(9), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="b3449-117">Vollständige Befehlszeile des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="b3449-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="b3449-118">DirectoryTableBase</span><span class="sxs-lookup"><span data-stu-id="b3449-118">DirectoryTableBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3449-119">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b3449-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3449-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3449-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3449-121">Qualifizierer: WmiDataId(6), Zeiger</span><span class="sxs-lookup"><span data-stu-id="b3449-121">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b3449-122">Die physische Adresse der Seitentabelle des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="b3449-122">The physical address of the page table of the process.</span></span>

</dd> <dt>

<span data-ttu-id="b3449-123">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="b3449-123">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3449-124">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3449-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3449-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3449-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3449-126">Qualifizierer: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="b3449-126">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="b3449-127">Beendigungsstatus des beendeten Prozesses.</span><span class="sxs-lookup"><span data-stu-id="b3449-127">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="b3449-128">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="b3449-128">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3449-129">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="b3449-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3449-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3449-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3449-131">Qualifizierer: WmiDataId(8), StringTermination("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="b3449-131">Qualifiers: WmiDataId(8), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="b3449-132">Pfad zur ausführbaren Datei des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="b3449-132">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="b3449-133">ParentId</span><span class="sxs-lookup"><span data-stu-id="b3449-133">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3449-134">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b3449-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3449-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3449-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3449-136">Qualifizierer: WmiDataId(3), Format("x")</span><span class="sxs-lookup"><span data-stu-id="b3449-136">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="b3449-137">Eindeutiger Bezeichner des Prozesses, der diesen Prozess erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3449-137">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="b3449-138">Prozessbezeichnernummern werden wiederverwendet, sodass sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b3449-138">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="b3449-139">Es ist möglich, dass der durch ParentProcessId identifizierte Prozess beendet wird, sodass ParentProcessId möglicherweise nicht auf einen ausgeführten Prozess verweist.</span><span class="sxs-lookup"><span data-stu-id="b3449-139">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="b3449-140">Es ist auch möglich, dass ParentProcessId fälschlicherweise auf einen Prozess verweist, der einen Prozessbezeichner wiederverwendet.</span><span class="sxs-lookup"><span data-stu-id="b3449-140">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b3449-141">ProcessId</span><span class="sxs-lookup"><span data-stu-id="b3449-141">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3449-142">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b3449-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3449-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3449-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3449-144">Qualifizierer: WmiDataId(2), Format("x")</span><span class="sxs-lookup"><span data-stu-id="b3449-144">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="b3449-145">Globaler Prozessbezeichner, den Sie zum Identifizieren eines Prozesses verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b3449-145">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="b3449-146">Der Wert ist gültig ab dem Zeitpunkt, zu dem ein Prozess erstellt wird, bis er beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3449-146">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="b3449-147">SessionID</span><span class="sxs-lookup"><span data-stu-id="b3449-147">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3449-148">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b3449-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3449-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3449-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3449-150">Qualifizierer: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="b3449-150">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="b3449-151">Eindeutiger Bezeichner, den ein Betriebssystem generiert, wenn es eine neue Sitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3449-151">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="b3449-152">Eine Sitzung erstreckt sich über einen Zeitraum von der Anmeldung bis zur Abmeldung von einem bestimmten System.</span><span class="sxs-lookup"><span data-stu-id="b3449-152">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="b3449-153">UniqueProcessKey</span><span class="sxs-lookup"><span data-stu-id="b3449-153">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3449-154">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b3449-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3449-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3449-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3449-156">Qualifizierer: WmiDataId(1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="b3449-156">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b3449-157">Die Adresse des Prozessobjekts im Kernel.</span><span class="sxs-lookup"><span data-stu-id="b3449-157">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="b3449-158">UserSID</span><span class="sxs-lookup"><span data-stu-id="b3449-158">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3449-159">Datentyp: **object**</span><span class="sxs-lookup"><span data-stu-id="b3449-159">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b3449-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3449-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3449-161">Qualifizierer: WmiDataId(7), Extension("Sid")</span><span class="sxs-lookup"><span data-stu-id="b3449-161">Qualifiers: WmiDataId(7), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="b3449-162">Sicherheits-ID (SID) für den Benutzerkontext, unter dem das Ereignis eintritt.</span><span class="sxs-lookup"><span data-stu-id="b3449-162">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3449-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3449-163">Remarks</span></span>

<span data-ttu-id="b3449-164">Die DCStart- und DCEnd-Ereignistypen zählen den Prozess auf, der derzeit ausgeführt wird, einschließlich Leerlauf und Systemprozess, zu dem Zeitpunkt, zu dem die Kernelsitzung gestartet bzw. beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3449-164">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3449-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3449-165">Requirements</span></span>



| <span data-ttu-id="b3449-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3449-166">Requirement</span></span> | <span data-ttu-id="b3449-167">Wert</span><span class="sxs-lookup"><span data-stu-id="b3449-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b3449-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3449-168">Minimum supported client</span></span><br/> | <span data-ttu-id="b3449-169">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3449-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b3449-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3449-170">Minimum supported server</span></span><br/> | <span data-ttu-id="b3449-171">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3449-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b3449-172">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b3449-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3449-173">**Prozess**</span><span class="sxs-lookup"><span data-stu-id="b3449-173">**Process**</span></span>](process.md)
</dt> </dl>

 

 




