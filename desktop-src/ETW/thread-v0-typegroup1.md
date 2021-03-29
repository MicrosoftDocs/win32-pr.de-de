---
description: Diese Klasse ist die Ereignistyp Klasse für Thread Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: cc668fef-48fe-4948-8fe5-4351f7a033d1
title: Thread_V0_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V0_TypeGroup1
- Thread_V0_TypeGroup1.TThreadId
- Thread_V0_TypeGroup1.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f6fa7ae1f50e005fe8f66e918a4a8360a0e8f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978224"
---
# <a name="thread_v0_typegroup1-class"></a><span data-ttu-id="684fa-104">Thread \_ v0 \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="684fa-104">Thread\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="684fa-105">Diese Klasse ist die Ereignistyp Klasse für Thread Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="684fa-105">This class is the event type class for thread events.</span></span>

<span data-ttu-id="684fa-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="684fa-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="684fa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="684fa-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V0_TypeGroup1 : Thread_V0
{
  uint32 TThreadId;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="684fa-108">Member</span><span class="sxs-lookup"><span data-stu-id="684fa-108">Members</span></span>

<span data-ttu-id="684fa-109">Die Thread-Klasse " **\_ v0 \_ TypeGroup1** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="684fa-109">The **Thread\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="684fa-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="684fa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="684fa-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="684fa-111">Properties</span></span>

<span data-ttu-id="684fa-112">Die **Thread \_ v0 \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="684fa-112">The **Thread\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="684fa-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="684fa-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="684fa-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="684fa-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="684fa-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="684fa-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="684fa-116">Qualifizierer: wmidataid (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="684fa-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="684fa-117">Prozess Bezeichner des am Ereignis beteiligten Threads.</span><span class="sxs-lookup"><span data-stu-id="684fa-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="684fa-118">Tthreadid</span><span class="sxs-lookup"><span data-stu-id="684fa-118">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="684fa-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="684fa-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="684fa-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="684fa-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="684fa-121">Qualifizierer: wmidataid (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="684fa-121">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="684fa-122">Thread Bezeichner des am Ereignis beteiligten Threads.</span><span class="sxs-lookup"><span data-stu-id="684fa-122">Thread identifier of the thread involved in the event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="684fa-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="684fa-123">Requirements</span></span>



| <span data-ttu-id="684fa-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="684fa-124">Requirement</span></span> | <span data-ttu-id="684fa-125">Wert</span><span class="sxs-lookup"><span data-stu-id="684fa-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="684fa-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="684fa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="684fa-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="684fa-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="684fa-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="684fa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="684fa-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="684fa-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="684fa-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="684fa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="684fa-131">**Thread \_ v0**</span><span class="sxs-lookup"><span data-stu-id="684fa-131">**Thread\_V0**</span></span>](thread-v0.md)
</dt> </dl>

 

 




