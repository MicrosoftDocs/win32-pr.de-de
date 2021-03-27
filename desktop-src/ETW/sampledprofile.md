---
description: Diese Klasse ist die Ereignistyp Klasse für samplingprofilereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: Sampledprofile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980553"
---
# <a name="sampledprofile-class"></a><span data-ttu-id="ad5bc-104">Sampledprofile-Klasse</span><span class="sxs-lookup"><span data-stu-id="ad5bc-104">SampledProfile class</span></span>

<span data-ttu-id="ad5bc-105">Diese Klasse ist die Ereignistyp Klasse für samplingprofilereignisse.</span><span class="sxs-lookup"><span data-stu-id="ad5bc-105">This class is the event type class for sampled profile events.</span></span>

<span data-ttu-id="ad5bc-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="ad5bc-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad5bc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad5bc-107">Syntax</span></span>

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a><span data-ttu-id="ad5bc-108">Member</span><span class="sxs-lookup"><span data-stu-id="ad5bc-108">Members</span></span>

<span data-ttu-id="ad5bc-109">Die **sampledprofile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ad5bc-109">The **SampledProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="ad5bc-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad5bc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad5bc-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad5bc-111">Properties</span></span>

<span data-ttu-id="ad5bc-112">Die **sampledprofile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ad5bc-112">The **SampledProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad5bc-113">**Count**</span><span class="sxs-lookup"><span data-stu-id="ad5bc-113">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad5bc-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad5bc-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad5bc-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad5bc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad5bc-116">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="ad5bc-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="ad5bc-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad5bc-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad5bc-118">**Instructionpointer**</span><span class="sxs-lookup"><span data-stu-id="ad5bc-118">**InstructionPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad5bc-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad5bc-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad5bc-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad5bc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad5bc-121">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="ad5bc-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ad5bc-122">Adresse des Abbilds, das zum Zeitpunkt des Prozessors für den Prozessor ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad5bc-122">Address of the image that was running at the time the processor was sampled.</span></span>

</dd> <dt>

<span data-ttu-id="ad5bc-123">**ThreadID**</span><span class="sxs-lookup"><span data-stu-id="ad5bc-123">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad5bc-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad5bc-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad5bc-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad5bc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad5bc-126">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="ad5bc-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="ad5bc-127">Thread Bezeichner des Threads, der zum Zeitpunkt der Stichprobenentnahme des Prozessors ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad5bc-127">Thread identifier of the thread that was running at the time the processor was sampled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad5bc-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad5bc-128">Remarks</span></span>

<span data-ttu-id="ad5bc-129">Diese Ereignisse stellen ein erfassten Ausführungsprofil bereit.</span><span class="sxs-lookup"><span data-stu-id="ad5bc-129">These events provide a sampled execution profile.</span></span> <span data-ttu-id="ad5bc-130">Das Ereignis zeichnet auf, was auf dem Prozessor ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad5bc-130">The event records what was being executed on the processor.</span></span> <span data-ttu-id="ad5bc-131">Sie können die Image-Ereignisse verwenden, um das binäre Modul zu identifizieren, das diese Anweisung enthält.</span><span class="sxs-lookup"><span data-stu-id="ad5bc-131">You can use the Image events to identify the binary module containing that instruction.</span></span> <span data-ttu-id="ad5bc-132">Sie können diese Informationen dann verwenden, um ein Ausführungsprofil für die Dauer der Ablauf Verfolgung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad5bc-132">You can then use this information to produce an execution profile for the duration of the trace.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad5bc-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ad5bc-133">Requirements</span></span>



| <span data-ttu-id="ad5bc-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad5bc-134">Requirement</span></span> | <span data-ttu-id="ad5bc-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ad5bc-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ad5bc-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad5bc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ad5bc-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad5bc-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ad5bc-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad5bc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ad5bc-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad5bc-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




