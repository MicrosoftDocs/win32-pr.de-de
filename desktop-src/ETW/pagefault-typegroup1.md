---
description: Diese Klasse ist die Ereignistyp Klasse für Seiten Fehlerereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: PageFault_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TypeGroup1
- PageFault_TypeGroup1.VirtualAddress
- PageFault_TypeGroup1.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4bf1f49c909833d75af844c8f2f943a01b6a5d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216773"
---
# <a name="pagefault_typegroup1-class"></a><span data-ttu-id="5e301-104">Pagefault \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="5e301-104">PageFault\_TypeGroup1 class</span></span>

<span data-ttu-id="5e301-105">Diese Klasse ist die Ereignistyp Klasse für Seiten Fehlerereignisse.</span><span class="sxs-lookup"><span data-stu-id="5e301-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="5e301-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="5e301-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e301-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e301-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="5e301-108">Member</span><span class="sxs-lookup"><span data-stu-id="5e301-108">Members</span></span>

<span data-ttu-id="5e301-109">Die **Pagefault \_ TypeGroup1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5e301-109">The **PageFault\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="5e301-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e301-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e301-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e301-111">Properties</span></span>

<span data-ttu-id="5e301-112">Die **Pagefault \_ TypeGroup1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5e301-112">The **PageFault\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e301-113">Programm Counter</span><span class="sxs-lookup"><span data-stu-id="5e301-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e301-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e301-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e301-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5e301-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e301-116">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="5e301-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5e301-117">Zeiger auf die aktuell ausgeführte Anweisung.</span><span class="sxs-lookup"><span data-stu-id="5e301-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="5e301-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="5e301-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e301-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e301-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e301-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5e301-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e301-121">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="5e301-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5e301-122">Die virtuelle Adresse der Seite, die den Seiten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="5e301-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e301-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e301-123">Remarks</span></span>

<span data-ttu-id="5e301-124">Ein Seiten Fehler tritt auf, wenn eine im Arbeitsspeicher-Cache gesuchte Seite dort nicht gefunden wird und von einer anderen Stelle im Arbeitsspeicher (einem Soft-Fehler) oder vom Datenträger abgerufen werden muss (ein harter Fehler).</span><span class="sxs-lookup"><span data-stu-id="5e301-124">A page fault occurs when a page sought in the memory cache is not found there and must be retrieved from elsewhere in memory (a soft fault) or from disk (a hard fault).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e301-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5e301-125">Requirements</span></span>



| <span data-ttu-id="5e301-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e301-126">Requirement</span></span> | <span data-ttu-id="5e301-127">Wert</span><span class="sxs-lookup"><span data-stu-id="5e301-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e301-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e301-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5e301-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e301-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e301-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e301-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5e301-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e301-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e301-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5e301-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e301-133">**Pagefault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="5e301-133">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




