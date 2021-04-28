---
description: 'PageFault_TransitionFault Klasse: Diese Klasse ist die Ereignistypklasse für Seitenfehlerereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: cc2b7a93-6974-4872-98f3-d6cb81861ae5
title: PageFault_TransitionFault-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TransitionFault
- PageFault_TransitionFault.VirtualAddress
- PageFault_TransitionFault.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6c8ee12cf201b9ee83d231bf1f5e499550aa3cd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106458"
---
# <a name="pagefault_transitionfault-class"></a><span data-ttu-id="c2063-104">PageFault \_ TransitionFault-Klasse</span><span class="sxs-lookup"><span data-stu-id="c2063-104">PageFault\_TransitionFault class</span></span>

<span data-ttu-id="c2063-105">Diese Klasse ist die Ereignistypklasse für Seitenfehlerereignisse.</span><span class="sxs-lookup"><span data-stu-id="c2063-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="c2063-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c2063-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2063-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2063-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="c2063-108">Member</span><span class="sxs-lookup"><span data-stu-id="c2063-108">Members</span></span>

<span data-ttu-id="c2063-109">Die **PageFault \_ TransitionFault-Klasse** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="c2063-109">The **PageFault\_TransitionFault** class has these types of members:</span></span>

-   [<span data-ttu-id="c2063-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2063-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2063-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2063-111">Properties</span></span>

<span data-ttu-id="c2063-112">Die **PageFault \_ TransitionFault-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2063-112">The **PageFault\_TransitionFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2063-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="c2063-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2063-114">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c2063-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2063-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2063-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2063-116">Qualifizierer: WmiDataId(2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="c2063-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c2063-117">Zeiger auf die aktuelle Anweisung, die ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2063-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="c2063-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="c2063-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2063-119">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c2063-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2063-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2063-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2063-121">Qualifizierer: WmiDataId(1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="c2063-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c2063-122">Virtuelle Adresse der Seite, die den Seitenfehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="c2063-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2063-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2063-123">Requirements</span></span>



| <span data-ttu-id="c2063-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2063-124">Requirement</span></span> | <span data-ttu-id="c2063-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c2063-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c2063-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2063-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c2063-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2063-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c2063-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2063-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c2063-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2063-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c2063-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2063-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2063-131">**PageFault \_ V2**</span><span class="sxs-lookup"><span data-stu-id="c2063-131">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




