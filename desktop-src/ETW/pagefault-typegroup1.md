---
description: 'PageFault_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für Seitenfehlerereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
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
ms.openlocfilehash: 4a69e74a086ecd594d83c932beea4fd7d62724db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106408"
---
# <a name="pagefault_typegroup1-class"></a><span data-ttu-id="02a36-104">PageFault \_ TypeGroup1-Klasse</span><span class="sxs-lookup"><span data-stu-id="02a36-104">PageFault\_TypeGroup1 class</span></span>

<span data-ttu-id="02a36-105">Diese Klasse ist die Ereignistypklasse für Seitenfehlerereignisse.</span><span class="sxs-lookup"><span data-stu-id="02a36-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="02a36-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="02a36-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="02a36-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="02a36-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="02a36-108">Member</span><span class="sxs-lookup"><span data-stu-id="02a36-108">Members</span></span>

<span data-ttu-id="02a36-109">Die **PageFault \_ TypeGroup1-Klasse** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="02a36-109">The **PageFault\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="02a36-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02a36-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02a36-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02a36-111">Properties</span></span>

<span data-ttu-id="02a36-112">Die **PageFault \_ TypeGroup1-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02a36-112">The **PageFault\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02a36-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="02a36-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02a36-114">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="02a36-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02a36-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02a36-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02a36-116">Qualifizierer: WmiDataId(2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="02a36-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="02a36-117">Zeiger auf die aktuelle Anweisung, die ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02a36-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="02a36-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="02a36-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02a36-119">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="02a36-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02a36-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02a36-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02a36-121">Qualifizierer: WmiDataId(1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="02a36-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="02a36-122">Virtuelle Adresse der Seite, die den Seitenfehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="02a36-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02a36-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02a36-123">Remarks</span></span>

<span data-ttu-id="02a36-124">Ein Seitenfehler tritt auf, wenn eine seite, die im Arbeitsspeichercache gesucht wird, dort nicht gefunden wird und von einer anderen Stelle im Arbeitsspeicher (ein weicher Fehler) oder vom Datenträger (ein harter Fehler) abgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="02a36-124">A page fault occurs when a page sought in the memory cache is not found there and must be retrieved from elsewhere in memory (a soft fault) or from disk (a hard fault).</span></span>

## <a name="requirements"></a><span data-ttu-id="02a36-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02a36-125">Requirements</span></span>



| <span data-ttu-id="02a36-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02a36-126">Requirement</span></span> | <span data-ttu-id="02a36-127">Wert</span><span class="sxs-lookup"><span data-stu-id="02a36-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="02a36-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02a36-128">Minimum supported client</span></span><br/> | <span data-ttu-id="02a36-129">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02a36-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="02a36-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02a36-130">Minimum supported server</span></span><br/> | <span data-ttu-id="02a36-131">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02a36-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02a36-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="02a36-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a36-133">**PageFault \_ V2**</span><span class="sxs-lookup"><span data-stu-id="02a36-133">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




