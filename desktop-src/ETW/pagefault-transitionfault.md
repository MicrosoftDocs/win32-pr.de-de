---
description: Diese Klasse ist die Ereignistyp Klasse für Seiten Fehlerereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 4721e2d342750b12baa58bb69f72606511c14143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866424"
---
# <a name="pagefault_transitionfault-class"></a><span data-ttu-id="8355e-104">Pagefault \_ transitionfault-Klasse</span><span class="sxs-lookup"><span data-stu-id="8355e-104">PageFault\_TransitionFault class</span></span>

<span data-ttu-id="8355e-105">Diese Klasse ist die Ereignistyp Klasse für Seiten Fehlerereignisse.</span><span class="sxs-lookup"><span data-stu-id="8355e-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="8355e-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="8355e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8355e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8355e-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="8355e-108">Member</span><span class="sxs-lookup"><span data-stu-id="8355e-108">Members</span></span>

<span data-ttu-id="8355e-109">Die **Pagefault \_ transitionfault** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8355e-109">The **PageFault\_TransitionFault** class has these types of members:</span></span>

-   [<span data-ttu-id="8355e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8355e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8355e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8355e-111">Properties</span></span>

<span data-ttu-id="8355e-112">Die **Pagefault \_ transitionfault** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8355e-112">The **PageFault\_TransitionFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8355e-113">Programm Counter</span><span class="sxs-lookup"><span data-stu-id="8355e-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8355e-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8355e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8355e-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8355e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8355e-116">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="8355e-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8355e-117">Zeiger auf die aktuell ausgeführte Anweisung.</span><span class="sxs-lookup"><span data-stu-id="8355e-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="8355e-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="8355e-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8355e-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8355e-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8355e-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8355e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8355e-121">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="8355e-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8355e-122">Die virtuelle Adresse der Seite, die den Seiten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="8355e-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8355e-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8355e-123">Requirements</span></span>



| <span data-ttu-id="8355e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8355e-124">Requirement</span></span> | <span data-ttu-id="8355e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="8355e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8355e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8355e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8355e-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8355e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8355e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8355e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8355e-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8355e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8355e-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8355e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8355e-131">**Pagefault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="8355e-131">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




