---
description: Diese Klasse ist die Ereignistyp Klasse für virtuelle Zuordnungs Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: PageFault_VirtualAlloc-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_VirtualAlloc
- PageFault_VirtualAlloc.BaseAddress
- PageFault_VirtualAlloc.RegionSize
- PageFault_VirtualAlloc.ProcessId
- PageFault_VirtualAlloc.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: f9e754bc3dc09f492682d5a522a6489cfde27ceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343999"
---
# <a name="pagefault_virtualalloc-class"></a><span data-ttu-id="0465f-104">Pagefault- \_ virtualzuweisung-Klasse</span><span class="sxs-lookup"><span data-stu-id="0465f-104">PageFault\_VirtualAlloc class</span></span>

<span data-ttu-id="0465f-105">Diese Klasse ist die Ereignistyp Klasse für virtuelle Zuordnungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="0465f-105">This class is the event type class for virtual allocation events.</span></span>

<span data-ttu-id="0465f-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="0465f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0465f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0465f-107">Syntax</span></span>

``` syntax
[EventType{98, 99}, EventTypeName{"VirtualAlloc", "VirtualFree"}]
class PageFault_VirtualAlloc : PageFault_V2
{
  uint32 BaseAddress;
  object RegionSize;
  uint32 ProcessId;
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="0465f-108">Member</span><span class="sxs-lookup"><span data-stu-id="0465f-108">Members</span></span>

<span data-ttu-id="0465f-109">Die **Pagefault- \_ virtualordc** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0465f-109">The **PageFault\_VirtualAlloc** class has these types of members:</span></span>

-   [<span data-ttu-id="0465f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0465f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0465f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0465f-111">Properties</span></span>

<span data-ttu-id="0465f-112">Die **Pagefault- \_ virtualordc** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0465f-112">The **PageFault\_VirtualAlloc** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0465f-113">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="0465f-113">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0465f-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0465f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0465f-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0465f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0465f-116">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="0465f-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0465f-117">Die Startadresse, an der der Arbeitsspeicher zugeordnet oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0465f-117">The starting address at which memory was allocated or freed.</span></span>

</dd> <dt>

<span data-ttu-id="0465f-118">**Flags**</span><span class="sxs-lookup"><span data-stu-id="0465f-118">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0465f-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0465f-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0465f-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0465f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0465f-121">Qualifizierer: wmidataid (4), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="0465f-121">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="0465f-122">Der Typ der Speicher Belegung, der ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0465f-122">The type of memory allocation that was performed.</span></span> <span data-ttu-id="0465f-123">Mögliche Werte finden Sie unter der *fltypcationtype* -Parameter der [**virtualzuweisung**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0465f-123">For possible values, see the *flAllocationType* parameter of the [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) function.</span></span>

</dd> <dt>

<span data-ttu-id="0465f-124">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="0465f-124">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0465f-125">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0465f-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0465f-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0465f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0465f-127">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="0465f-127">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="0465f-128">Der Prozess, der den Arbeitsspeicher besaß (kann sich von dem Thread unterscheiden, der die Zuordnung durchgeführt hat).</span><span class="sxs-lookup"><span data-stu-id="0465f-128">The process that owned the memory (can be different from the thread that performed the allocation).</span></span>

</dd> <dt>

<span data-ttu-id="0465f-129">**Regionsize**</span><span class="sxs-lookup"><span data-stu-id="0465f-129">**RegionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0465f-130">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="0465f-130">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0465f-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0465f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0465f-132">Qualifizierer: wmidataid (2), Erweiterung ("sizet")</span><span class="sxs-lookup"><span data-stu-id="0465f-132">Qualifiers: WmiDataId(2), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="0465f-133">Die Größe (in Bytes) des Arbeitsspeichers, der zugeordnet oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0465f-133">The size, in bytes, of the memory that was allocated or freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0465f-134">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0465f-134">Requirements</span></span>



| <span data-ttu-id="0465f-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0465f-135">Requirement</span></span> | <span data-ttu-id="0465f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="0465f-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0465f-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0465f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0465f-138">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0465f-138">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0465f-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0465f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0465f-140">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0465f-140">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0465f-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0465f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0465f-142">**Pagefault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="0465f-142">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 
