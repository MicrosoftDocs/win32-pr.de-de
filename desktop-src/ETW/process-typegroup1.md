---
description: Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 4ad2ebcd9a3e1563f6e2f4c82d90dd4d2c80112f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863056"
---
# <a name="process_typegroup1-class"></a><span data-ttu-id="11528-104">Process \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="11528-104">Process\_TypeGroup1 class</span></span>

<span data-ttu-id="11528-105">Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="11528-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="11528-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="11528-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="11528-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="11528-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="11528-108">Member</span><span class="sxs-lookup"><span data-stu-id="11528-108">Members</span></span>

<span data-ttu-id="11528-109">Die **Process \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="11528-109">The **Process\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="11528-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11528-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11528-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11528-111">Properties</span></span>

<span data-ttu-id="11528-112">Die **Process \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="11528-112">The **Process\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11528-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="11528-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11528-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11528-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11528-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11528-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11528-116">Qualifizierer: wmidataid (9), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="11528-116">Qualifiers: WmiDataId(9), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="11528-117">Vollständige Befehlszeile des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="11528-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="11528-118">Directoriytablebase</span><span class="sxs-lookup"><span data-stu-id="11528-118">DirectoryTableBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11528-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11528-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11528-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11528-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11528-121">Qualifizierer: wmidataid (6), Zeiger</span><span class="sxs-lookup"><span data-stu-id="11528-121">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="11528-122">Die physische Adresse der Seiten Tabelle des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="11528-122">The physical address of the page table of the process.</span></span>

</dd> <dt>

<span data-ttu-id="11528-123">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="11528-123">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11528-124">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="11528-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11528-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11528-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11528-126">Qualifizierer: wmidataid (5)</span><span class="sxs-lookup"><span data-stu-id="11528-126">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="11528-127">Beenden Sie den Status des beendeten Prozesses.</span><span class="sxs-lookup"><span data-stu-id="11528-127">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="11528-128">Imagefilename</span><span class="sxs-lookup"><span data-stu-id="11528-128">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11528-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11528-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11528-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11528-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11528-131">Qualifizierer: wmidataid (8), stringbeendigung ("nullterminiert")</span><span class="sxs-lookup"><span data-stu-id="11528-131">Qualifiers: WmiDataId(8), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="11528-132">Pfad zur ausführbaren Datei des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="11528-132">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="11528-133">ParentId</span><span class="sxs-lookup"><span data-stu-id="11528-133">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11528-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11528-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11528-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11528-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11528-136">Qualifizierer: wmidataid (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="11528-136">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="11528-137">Eindeutiger Bezeichner des Prozesses, der diesen Prozess erstellt.</span><span class="sxs-lookup"><span data-stu-id="11528-137">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="11528-138">Die prozesbezeichnernummern werden wieder verwendet, sodass Sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren.</span><span class="sxs-lookup"><span data-stu-id="11528-138">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="11528-139">Es ist möglich, dass der durch "parameterprocessid" identifizierte Prozess beendet wird, sodass "parameterprocessid" möglicherweise nicht auf einen laufenden Prozess verweist.</span><span class="sxs-lookup"><span data-stu-id="11528-139">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="11528-140">Es ist auch möglich, dass "paramedprocessid" fälschlicherweise auf einen Prozess verweist, der einen Prozess Bezeichner wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="11528-140">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="11528-141">ProcessId</span><span class="sxs-lookup"><span data-stu-id="11528-141">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11528-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11528-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11528-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11528-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11528-144">Qualifizierer: wmidataid (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="11528-144">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="11528-145">Die globale Prozess-ID, mit der Sie einen Prozess identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="11528-145">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="11528-146">Der Wert ist gültig ab dem Zeitpunkt, zu dem ein Prozess erstellt wird, bis er beendet wird.</span><span class="sxs-lookup"><span data-stu-id="11528-146">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="11528-147">SessionID</span><span class="sxs-lookup"><span data-stu-id="11528-147">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11528-148">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11528-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11528-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11528-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11528-150">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="11528-150">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="11528-151">Eindeutiger Bezeichner, den ein Betriebssystem generiert, wenn eine neue Sitzung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="11528-151">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="11528-152">Eine Sitzung erstreckt sich über einen Zeitraum von der Anmeldung bis zum Abmelden von einem bestimmten System.</span><span class="sxs-lookup"><span data-stu-id="11528-152">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="11528-153">Uniqueprocesskey</span><span class="sxs-lookup"><span data-stu-id="11528-153">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11528-154">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11528-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11528-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11528-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11528-156">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="11528-156">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="11528-157">Die Adresse des Prozess Objekts im Kernel.</span><span class="sxs-lookup"><span data-stu-id="11528-157">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="11528-158">UserSID</span><span class="sxs-lookup"><span data-stu-id="11528-158">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11528-159">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="11528-159">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="11528-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11528-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11528-161">Qualifizierer: wmidataid (7), Erweiterung ("sid")</span><span class="sxs-lookup"><span data-stu-id="11528-161">Qualifiers: WmiDataId(7), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="11528-162">Sicherheits-ID (SID) für den Benutzer Kontext, in dem das Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="11528-162">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11528-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11528-163">Remarks</span></span>

<span data-ttu-id="11528-164">Die Ereignis Typen DCStart und DCEnd zählen den Prozess, der derzeit ausgeführt wird, einschließlich Leerlauf und System Prozess, zu dem Zeitpunkt, zu dem die Kernel Sitzung beginnt bzw. endet.</span><span class="sxs-lookup"><span data-stu-id="11528-164">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="11528-165">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="11528-165">Requirements</span></span>



| <span data-ttu-id="11528-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11528-166">Requirement</span></span> | <span data-ttu-id="11528-167">Wert</span><span class="sxs-lookup"><span data-stu-id="11528-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="11528-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11528-168">Minimum supported client</span></span><br/> | <span data-ttu-id="11528-169">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11528-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="11528-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11528-170">Minimum supported server</span></span><br/> | <span data-ttu-id="11528-171">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11528-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="11528-172">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="11528-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11528-173">**Prozess**</span><span class="sxs-lookup"><span data-stu-id="11528-173">**Process**</span></span>](process.md)
</dt> </dl>

 

 




