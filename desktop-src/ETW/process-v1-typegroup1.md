---
description: 'Process_V1_TypeGroup1-Klasse: Diese Klasse ist die Ereignistypklasse für Prozessereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
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
ms.openlocfilehash: 8d7f4426f34a97ff79dc41806f1e0070013528d2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106328"
---
# <a name="process_v1_typegroup1-class"></a><span data-ttu-id="701e4-104">Process \_ V1 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="701e4-104">Process\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="701e4-105">Diese Klasse ist die Ereignistypklasse für Prozessereignisse.</span><span class="sxs-lookup"><span data-stu-id="701e4-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="701e4-106">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="701e4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="701e4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="701e4-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="701e4-108">Member</span><span class="sxs-lookup"><span data-stu-id="701e4-108">Members</span></span>

<span data-ttu-id="701e4-109">Die **\_ Process V1 \_ TypeGroup1-Klasse** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="701e4-109">The **Process\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="701e4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="701e4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="701e4-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="701e4-111">Properties</span></span>

<span data-ttu-id="701e4-112">Die **Process \_ V1 \_ TypeGroup1-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="701e4-112">The **Process\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="701e4-113">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="701e4-113">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701e4-114">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="701e4-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="701e4-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="701e4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701e4-116">Qualifizierer: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="701e4-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="701e4-117">Beendigungsstatus des beendeten Prozesses.</span><span class="sxs-lookup"><span data-stu-id="701e4-117">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="701e4-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="701e4-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701e4-119">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="701e4-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701e4-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="701e4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701e4-121">Qualifizierer: WmiDataId(7), StringTermination("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="701e4-121">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="701e4-122">Pfad zur ausführbaren Datei des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="701e4-122">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="701e4-123">PageDirectoryBase</span><span class="sxs-lookup"><span data-stu-id="701e4-123">PageDirectoryBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701e4-124">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="701e4-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="701e4-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="701e4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701e4-126">Qualifizierer: WmiDataId(1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="701e4-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="701e4-127">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="701e4-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="701e4-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="701e4-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701e4-129">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="701e4-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="701e4-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="701e4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701e4-131">Qualifizierer: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="701e4-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="701e4-132">Eindeutiger Bezeichner des Prozesses, der diesen Prozess erstellt.</span><span class="sxs-lookup"><span data-stu-id="701e4-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="701e4-133">Prozessbezeichnernummern werden wiederverwendet, sodass sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren.</span><span class="sxs-lookup"><span data-stu-id="701e4-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="701e4-134">Es ist möglich, dass der von ParentProcessId identifizierte Prozess beendet wird, sodass ParentProcessId möglicherweise nicht auf einen ausgeführten Prozess verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="701e4-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="701e4-135">Es ist auch möglich, dass ParentProcessId fälschlicherweise auf einen Prozess verweist, der einen Prozessbezeichner wiederverwendet.</span><span class="sxs-lookup"><span data-stu-id="701e4-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

<span data-ttu-id="701e4-136">**Windows Server 2003:** Schließt den Format("x")-Qualifizierer ein.</span><span class="sxs-lookup"><span data-stu-id="701e4-136">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="701e4-137">ProcessId</span><span class="sxs-lookup"><span data-stu-id="701e4-137">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701e4-138">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="701e4-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="701e4-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="701e4-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701e4-140">Qualifizierer: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="701e4-140">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="701e4-141">Globaler Prozessbezeichner, den Sie zum Identifizieren eines Prozesses verwenden können.</span><span class="sxs-lookup"><span data-stu-id="701e4-141">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="701e4-142">Der Wert ist ab dem Zeitpunkt gültig, zu dem ein Prozess erstellt wird, bis er beendet wird.</span><span class="sxs-lookup"><span data-stu-id="701e4-142">The value is valid from the time a process is created until it is terminated.</span></span>

<span data-ttu-id="701e4-143">**Windows Server 2003:** Schließt den Format("x")-Qualifizierer ein.</span><span class="sxs-lookup"><span data-stu-id="701e4-143">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="701e4-144">SessionID</span><span class="sxs-lookup"><span data-stu-id="701e4-144">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701e4-145">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="701e4-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="701e4-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="701e4-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701e4-147">Qualifizierer: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="701e4-147">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="701e4-148">Eindeutiger Bezeichner, den ein Betriebssystem generiert, wenn es eine neue Sitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="701e4-148">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="701e4-149">Eine Sitzung erstreckt sich über einen Zeitraum von der Anmeldung bis zur Abmelde von einem bestimmten System.</span><span class="sxs-lookup"><span data-stu-id="701e4-149">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="701e4-150">UserSID</span><span class="sxs-lookup"><span data-stu-id="701e4-150">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701e4-151">Datentyp: **Objekt**</span><span class="sxs-lookup"><span data-stu-id="701e4-151">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="701e4-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="701e4-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701e4-153">Qualifizierer: WmiDataId(6), Extension("Sid")</span><span class="sxs-lookup"><span data-stu-id="701e4-153">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="701e4-154">Sicherheits-ID (SID) für den Benutzerkontext, unter dem das Ereignis eintritt.</span><span class="sxs-lookup"><span data-stu-id="701e4-154">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="701e4-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="701e4-155">Requirements</span></span>



| <span data-ttu-id="701e4-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="701e4-156">Requirement</span></span> | <span data-ttu-id="701e4-157">Wert</span><span class="sxs-lookup"><span data-stu-id="701e4-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="701e4-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="701e4-158">Minimum supported client</span></span><br/> | <span data-ttu-id="701e4-159">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="701e4-159">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="701e4-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="701e4-160">Minimum supported server</span></span><br/> | <span data-ttu-id="701e4-161">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="701e4-161">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="701e4-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="701e4-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="701e4-163">**Prozess \_ V1**</span><span class="sxs-lookup"><span data-stu-id="701e4-163">**Process\_V1**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="701e4-164">**Prozess \_ V1**</span><span class="sxs-lookup"><span data-stu-id="701e4-164">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 




