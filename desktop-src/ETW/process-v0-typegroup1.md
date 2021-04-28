---
description: 'Process_V0_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für Prozessereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Process_V0_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 524d3c7da9f8ff76608da120834c5365eb1deb41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106358"
---
# <a name="process_v0_typegroup1-class"></a><span data-ttu-id="cd054-104">Process \_ V0 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="cd054-104">Process\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="cd054-105">Diese Klasse ist die Ereignistypklasse für Prozessereignisse.</span><span class="sxs-lookup"><span data-stu-id="cd054-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="cd054-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="cd054-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd054-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd054-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="cd054-108">Member</span><span class="sxs-lookup"><span data-stu-id="cd054-108">Members</span></span>

<span data-ttu-id="cd054-109">Die **Process \_ V0 \_ TypeGroup1-Klasse** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="cd054-109">The **Process\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="cd054-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd054-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd054-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd054-111">Properties</span></span>

<span data-ttu-id="cd054-112">Die **Klasse Process \_ V0 \_ TypeGroup1** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cd054-112">The **Process\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd054-113">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="cd054-113">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd054-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cd054-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd054-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd054-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd054-116">Qualifizierer: WmiDataId(4), StringTermination("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="cd054-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="cd054-117">Pfad zur ausführbaren Datei des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="cd054-117">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="cd054-118">ParentId</span><span class="sxs-lookup"><span data-stu-id="cd054-118">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd054-119">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="cd054-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd054-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd054-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd054-121">Qualifizierer: WmiDataId(2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="cd054-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cd054-122">Eindeutiger Bezeichner des Prozesses, der einen Prozess erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd054-122">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="cd054-123">Prozessbezeichnernummern werden wiederverwendet, sodass sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cd054-123">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="cd054-124">Es ist möglich, dass der von ParentProcessId identifizierte Prozess beendet wird, sodass ParentProcessId möglicherweise nicht auf einen ausgeführten Prozess verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="cd054-124">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="cd054-125">Es ist auch möglich, dass ParentProcessId fälschlicherweise auf einen Prozess verweist, der einen Prozessbezeichner wiederverwendet.</span><span class="sxs-lookup"><span data-stu-id="cd054-125">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="cd054-126">ProcessId</span><span class="sxs-lookup"><span data-stu-id="cd054-126">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd054-127">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="cd054-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd054-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd054-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd054-129">Qualifizierer: WmiDataId(1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="cd054-129">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cd054-130">Globaler Prozessbezeichner, den Sie zum Identifizieren eines Prozesses verwenden können.</span><span class="sxs-lookup"><span data-stu-id="cd054-130">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="cd054-131">Der Wert ist gültig ab dem Zeitpunkt, zu dem ein Prozess erstellt wird, bis er beendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd054-131">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="cd054-132">UserSID</span><span class="sxs-lookup"><span data-stu-id="cd054-132">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd054-133">Datentyp: **object**</span><span class="sxs-lookup"><span data-stu-id="cd054-133">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cd054-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd054-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd054-135">Qualifizierer: WmiDataId(3), Extension("Sid")</span><span class="sxs-lookup"><span data-stu-id="cd054-135">Qualifiers: WmiDataId(3), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="cd054-136">Sicherheits-ID (SID) für den Benutzerkontext, unter dem das Ereignis eintritt.</span><span class="sxs-lookup"><span data-stu-id="cd054-136">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd054-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd054-137">Requirements</span></span>



| <span data-ttu-id="cd054-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd054-138">Requirement</span></span> | <span data-ttu-id="cd054-139">Wert</span><span class="sxs-lookup"><span data-stu-id="cd054-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd054-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd054-140">Minimum supported client</span></span><br/> | <span data-ttu-id="cd054-141">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd054-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="cd054-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd054-142">Minimum supported server</span></span><br/> | <span data-ttu-id="cd054-143">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd054-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd054-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cd054-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd054-145">**Verarbeiten \_ von V0**</span><span class="sxs-lookup"><span data-stu-id="cd054-145">**Process\_V0**</span></span>](process-v0.md)
</dt> </dl>

 

 




