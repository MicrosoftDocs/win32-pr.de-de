---
description: Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 2889feb05bfc396f2c2018ca59d2cf46fba8ec13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977704"
---
# <a name="process_v0_typegroup1-class"></a><span data-ttu-id="1f938-104">Process \_ v0 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="1f938-104">Process\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="1f938-105">Diese Klasse ist die Ereignistyp Klasse für Prozess Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="1f938-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="1f938-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="1f938-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f938-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f938-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="1f938-108">Member</span><span class="sxs-lookup"><span data-stu-id="1f938-108">Members</span></span>

<span data-ttu-id="1f938-109">Die **Process \_ v0 \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1f938-109">The **Process\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="1f938-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f938-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f938-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f938-111">Properties</span></span>

<span data-ttu-id="1f938-112">Die **Process \_ v0 \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1f938-112">The **Process\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f938-113">Imagefilename</span><span class="sxs-lookup"><span data-stu-id="1f938-113">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f938-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f938-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f938-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f938-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f938-116">Qualifizierer: wmidataid (4), stringbeendigung ("nullterminiert")</span><span class="sxs-lookup"><span data-stu-id="1f938-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="1f938-117">Pfad zur ausführbaren Datei des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="1f938-117">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="1f938-118">ParentId</span><span class="sxs-lookup"><span data-stu-id="1f938-118">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f938-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f938-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f938-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f938-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f938-121">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="1f938-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1f938-122">Eindeutiger Bezeichner des Prozesses, von dem ein Prozess erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1f938-122">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="1f938-123">Die prozesbezeichnernummern werden wieder verwendet, sodass Sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1f938-123">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="1f938-124">Es ist möglich, dass der durch "parameterprocessid" identifizierte Prozess beendet wird, sodass "parameterprocessid" möglicherweise nicht auf einen laufenden Prozess verweist.</span><span class="sxs-lookup"><span data-stu-id="1f938-124">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="1f938-125">Es ist auch möglich, dass "paramedprocessid" fälschlicherweise auf einen Prozess verweist, der einen Prozess Bezeichner wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f938-125">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1f938-126">ProcessId</span><span class="sxs-lookup"><span data-stu-id="1f938-126">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f938-127">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f938-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f938-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f938-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f938-129">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="1f938-129">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1f938-130">Die globale Prozess-ID, mit der Sie einen Prozess identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="1f938-130">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="1f938-131">Der Wert ist gültig ab dem Zeitpunkt, zu dem ein Prozess erstellt wird, bis er beendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f938-131">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="1f938-132">UserSID</span><span class="sxs-lookup"><span data-stu-id="1f938-132">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f938-133">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="1f938-133">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1f938-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f938-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f938-135">Qualifizierer: wmidataid (3), Erweiterung ("sid")</span><span class="sxs-lookup"><span data-stu-id="1f938-135">Qualifiers: WmiDataId(3), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="1f938-136">Sicherheits-ID (SID) für den Benutzer Kontext, in dem das Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="1f938-136">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f938-137">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1f938-137">Requirements</span></span>



| <span data-ttu-id="1f938-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f938-138">Requirement</span></span> | <span data-ttu-id="1f938-139">Wert</span><span class="sxs-lookup"><span data-stu-id="1f938-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1f938-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f938-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1f938-141">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f938-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1f938-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f938-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1f938-143">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f938-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f938-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1f938-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f938-145">**Prozess \_ v0**</span><span class="sxs-lookup"><span data-stu-id="1f938-145">**Process\_V0**</span></span>](process-v0.md)
</dt> </dl>

 

 




