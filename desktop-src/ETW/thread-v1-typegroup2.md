---
description: Diese Klasse ist die Ereignistyp Klasse für Thread Ende-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Thread_V1_TypeGroup2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3e56590127b2317813d7431a1cc646fbe76e35a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527290"
---
# <a name="thread_v1_typegroup2-class"></a><span data-ttu-id="11990-104">Thread \_ v1 \_ TypeGroup2-Klasse</span><span class="sxs-lookup"><span data-stu-id="11990-104">Thread\_V1\_TypeGroup2 class</span></span>

<span data-ttu-id="11990-105">Diese Klasse ist die Ereignistyp Klasse für Thread Ende-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="11990-105">This class is the event type class for thread end events.</span></span>

<span data-ttu-id="11990-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="11990-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="11990-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="11990-107">Syntax</span></span>

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a><span data-ttu-id="11990-108">Member</span><span class="sxs-lookup"><span data-stu-id="11990-108">Members</span></span>

<span data-ttu-id="11990-109">Die **Thread \_ v1 \_ TypeGroup2** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="11990-109">The **Thread\_V1\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="11990-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11990-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11990-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11990-111">Properties</span></span>

<span data-ttu-id="11990-112">Die **Thread \_ v1 \_ TypeGroup2** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="11990-112">The **Thread\_V1\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11990-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="11990-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11990-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11990-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11990-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11990-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11990-116">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="11990-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="11990-117">Prozess Bezeichner des am Ereignis beteiligten Threads.</span><span class="sxs-lookup"><span data-stu-id="11990-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="11990-118">**Windows Server 2003:** Enthält das Format ("x") Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="11990-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="11990-119">Tthreadid</span><span class="sxs-lookup"><span data-stu-id="11990-119">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11990-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11990-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11990-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11990-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11990-122">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="11990-122">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="11990-123">Thread Bezeichner des am Ereignis beteiligten Threads.</span><span class="sxs-lookup"><span data-stu-id="11990-123">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="11990-124">**Windows Server 2003:** Enthält das Format ("x") Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="11990-124">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11990-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="11990-125">Requirements</span></span>



| <span data-ttu-id="11990-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11990-126">Requirement</span></span> | <span data-ttu-id="11990-127">Wert</span><span class="sxs-lookup"><span data-stu-id="11990-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="11990-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11990-128">Minimum supported client</span></span><br/> | <span data-ttu-id="11990-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11990-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="11990-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11990-130">Minimum supported server</span></span><br/> | <span data-ttu-id="11990-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11990-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11990-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="11990-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11990-133">**Thread \_ v1**</span><span class="sxs-lookup"><span data-stu-id="11990-133">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




