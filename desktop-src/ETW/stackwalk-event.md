---
description: Diese Klasse ist die Ereignistyp Klasse für Stapel Ablauf Verfolgungs Ereignisse.
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: StackWalk_Event-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 746a7f2a9b5f6bb6316bf0d0e20e5645cea15a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980081"
---
# <a name="stackwalk_event-class"></a><span data-ttu-id="ed5fe-103">Stackwalk ( \_ Ereignisklasse)</span><span class="sxs-lookup"><span data-stu-id="ed5fe-103">StackWalk\_Event class</span></span>

<span data-ttu-id="ed5fe-104">Diese Klasse ist die Ereignistyp Klasse für Stapel Ablauf Verfolgungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="ed5fe-104">This class is the event type class for stack tracing events.</span></span>

<span data-ttu-id="ed5fe-105">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ed5fe-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed5fe-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed5fe-106">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a><span data-ttu-id="ed5fe-107">Member</span><span class="sxs-lookup"><span data-stu-id="ed5fe-107">Members</span></span>

<span data-ttu-id="ed5fe-108">Die **Stackwalk- \_ Ereignis** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ed5fe-108">The **StackWalk\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="ed5fe-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed5fe-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed5fe-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed5fe-110">Properties</span></span>

<span data-ttu-id="ed5fe-111">Die **Stackwalk- \_ Ereignis** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ed5fe-111">The **StackWalk\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed5fe-112">**Eventtimestamp**</span><span class="sxs-lookup"><span data-stu-id="ed5fe-112">**EventTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed5fe-113">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ed5fe-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ed5fe-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed5fe-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed5fe-115">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="ed5fe-115">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="ed5fe-116">Ursprünglicher ereigniszeitstempel aus dem Ereignis Header.</span><span class="sxs-lookup"><span data-stu-id="ed5fe-116">Original event time stamp from the event header.</span></span> <span data-ttu-id="ed5fe-117">Verwenden Sie diesen Zeitstempel, um den Stapel mit einem Ereignis zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="ed5fe-117">Use this time stamp to match the stack to an event.</span></span>

</dd> <dt>

<span data-ttu-id="ed5fe-118">**Stack1**</span><span class="sxs-lookup"><span data-stu-id="ed5fe-118">**Stack1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed5fe-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed5fe-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed5fe-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed5fe-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed5fe-121">Qualifizierer: wmidataid (4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="ed5fe-121">Qualifiers: WmiDataId(4), pointer</span></span>
</dt> </dl>

<span data-ttu-id="ed5fe-122">Adresse des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="ed5fe-122">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="ed5fe-123">**Stack192**</span><span class="sxs-lookup"><span data-stu-id="ed5fe-123">**Stack192**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed5fe-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed5fe-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed5fe-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed5fe-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed5fe-126">Qualifizierer: wmidataid (195), Zeiger</span><span class="sxs-lookup"><span data-stu-id="ed5fe-126">Qualifiers: WmiDataId(195), pointer</span></span>
</dt> </dl>

<span data-ttu-id="ed5fe-127">Adresse des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="ed5fe-127">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="ed5fe-128">**Stackprocess**</span><span class="sxs-lookup"><span data-stu-id="ed5fe-128">**StackProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed5fe-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed5fe-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed5fe-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed5fe-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed5fe-131">Qualifizierer: wmidataid (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="ed5fe-131">Qualifiers: WmiDataId(2), format("x")</span></span>
</dt> </dl>

<span data-ttu-id="ed5fe-132">Der Prozess Bezeichner des ursprünglichen Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="ed5fe-132">The process identifier of the original event.</span></span>

</dd> <dt>

<span data-ttu-id="ed5fe-133">**Stackthread**</span><span class="sxs-lookup"><span data-stu-id="ed5fe-133">**StackThread**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed5fe-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed5fe-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed5fe-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed5fe-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed5fe-136">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="ed5fe-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="ed5fe-137">Der Thread Bezeichner des ursprünglichen Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="ed5fe-137">The thread identifier of the original event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed5fe-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed5fe-138">Remarks</span></span>

<span data-ttu-id="ed5fe-139">Beachten Sie, dass die-Klasse nicht alle \*\*Stapel \* n\*\*\*-Eigenschaften anzeigt, die zwischen **Stack1** und **Stack192** vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ed5fe-139">Note that the class does not show all of the **Stack\*n**\* properties that exist between **Stack1** and **Stack192**.</span></span> <span data-ttu-id="ed5fe-140">Verwenden Sie die Größe des Ereignisses, um zu bestimmen, wie viele \*\*Stapel \* n\*\*\*-Eigenschaften gültige Adressen enthalten.</span><span class="sxs-lookup"><span data-stu-id="ed5fe-140">Use the size of the event to determine how many **Stack\*n**\* properties contain valid addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed5fe-141">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ed5fe-141">Requirements</span></span>



| <span data-ttu-id="ed5fe-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed5fe-142">Requirement</span></span> | <span data-ttu-id="ed5fe-143">Wert</span><span class="sxs-lookup"><span data-stu-id="ed5fe-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ed5fe-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed5fe-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ed5fe-145">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed5fe-145">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ed5fe-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed5fe-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ed5fe-147">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed5fe-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




