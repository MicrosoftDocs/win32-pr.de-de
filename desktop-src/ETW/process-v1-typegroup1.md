---
description: Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: b114d7fd-c308-4f21-8f1a-ab27dc93abc5
title: Process_V1_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V1_TypeGroup1
- Process_V1_TypeGroup1.PageDirectoryBase
- Process_V1_TypeGroup1.ProcessId
- Process_V1_TypeGroup1.ParentId
- Process_V1_TypeGroup1.SessionId
- Process_V1_TypeGroup1.ExitStatus
- Process_V1_TypeGroup1.UserSID
- Process_V1_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: fc2308965de5c06a25858a138d4536763613a4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347839"
---
# <a name="process_v1_typegroup1-class"></a><span data-ttu-id="6c2a0-104">Process \_ v1 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="6c2a0-104">Process\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="6c2a0-105">Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="6c2a0-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c2a0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c2a0-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V1_TypeGroup1 : Process_V1
{
  uint32 PageDirectoryBase;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="6c2a0-108">Member</span><span class="sxs-lookup"><span data-stu-id="6c2a0-108">Members</span></span>

<span data-ttu-id="6c2a0-109">Die **Process \_ v1 \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6c2a0-109">The **Process\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="6c2a0-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c2a0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c2a0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c2a0-111">Properties</span></span>

<span data-ttu-id="6c2a0-112">Die **Process \_ v1 \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-112">The **Process\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c2a0-113">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="6c2a0-113">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2a0-114">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6c2a0-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c2a0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-116">Qualifizierer: wmidataid (5)</span><span class="sxs-lookup"><span data-stu-id="6c2a0-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="6c2a0-117">Beenden Sie den Status des beendeten Prozesses.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-117">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="6c2a0-118">Imagefilename</span><span class="sxs-lookup"><span data-stu-id="6c2a0-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2a0-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c2a0-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c2a0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-121">Qualifizierer: wmidataid (7), stringbeendigung ("nullterminiert")</span><span class="sxs-lookup"><span data-stu-id="6c2a0-121">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="6c2a0-122">Pfad zur ausführbaren Datei des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-122">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="6c2a0-123">Pagedirectoriybase</span><span class="sxs-lookup"><span data-stu-id="6c2a0-123">PageDirectoryBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2a0-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c2a0-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c2a0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-126">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="6c2a0-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6c2a0-127">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6c2a0-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="6c2a0-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2a0-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c2a0-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c2a0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-131">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="6c2a0-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="6c2a0-132">Eindeutiger Bezeichner des Prozesses, der diesen Prozess erstellt.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="6c2a0-133">Die prozesbezeichnernummern werden wieder verwendet, sodass Sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="6c2a0-134">Es ist möglich, dass der durch "parameterprocessid" identifizierte Prozess beendet wird, sodass "parameterprocessid" möglicherweise nicht auf einen laufenden Prozess verweist.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="6c2a0-135">Es ist auch möglich, dass "paramedprocessid" fälschlicherweise auf einen Prozess verweist, der einen Prozess Bezeichner wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

<span data-ttu-id="6c2a0-136">**Windows Server 2003:** Schließt den Format Bezeichner "x" ein.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-136">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="6c2a0-137">ProcessId</span><span class="sxs-lookup"><span data-stu-id="6c2a0-137">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2a0-138">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c2a0-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c2a0-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-140">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="6c2a0-140">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="6c2a0-141">Die globale Prozess-ID, mit der Sie einen Prozess identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-141">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="6c2a0-142">Der Wert ist gültig ab dem Zeitpunkt, zu dem ein Prozess erstellt wird, bis er beendet wird.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-142">The value is valid from the time a process is created until it is terminated.</span></span>

<span data-ttu-id="6c2a0-143">**Windows Server 2003:** Schließt den Format Bezeichner "x" ein.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-143">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="6c2a0-144">SessionID</span><span class="sxs-lookup"><span data-stu-id="6c2a0-144">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2a0-145">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c2a0-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c2a0-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-147">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="6c2a0-147">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="6c2a0-148">Eindeutiger Bezeichner, den ein Betriebssystem generiert, wenn eine neue Sitzung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-148">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="6c2a0-149">Eine Sitzung erstreckt sich über einen Zeitraum von der Anmeldung bis zum Abmelden von einem bestimmten System.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-149">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="6c2a0-150">UserSID</span><span class="sxs-lookup"><span data-stu-id="6c2a0-150">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2a0-151">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="6c2a0-151">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c2a0-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c2a0-153">Qualifizierer: wmidataid (6), Erweiterung ("sid")</span><span class="sxs-lookup"><span data-stu-id="6c2a0-153">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="6c2a0-154">Sicherheits-ID (SID) für den Benutzer Kontext, in dem das Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="6c2a0-154">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c2a0-155">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6c2a0-155">Requirements</span></span>



| <span data-ttu-id="6c2a0-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c2a0-156">Requirement</span></span> | <span data-ttu-id="6c2a0-157">Wert</span><span class="sxs-lookup"><span data-stu-id="6c2a0-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c2a0-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c2a0-158">Minimum supported client</span></span><br/> | <span data-ttu-id="6c2a0-159">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c2a0-159">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6c2a0-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c2a0-160">Minimum supported server</span></span><br/> | <span data-ttu-id="6c2a0-161">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c2a0-161">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c2a0-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6c2a0-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c2a0-163">**Prozess \_ v1**</span><span class="sxs-lookup"><span data-stu-id="6c2a0-163">**Process\_V1**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="6c2a0-164">**Prozess \_ v1**</span><span class="sxs-lookup"><span data-stu-id="6c2a0-164">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 




