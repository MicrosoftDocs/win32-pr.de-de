---
description: Diese Klasse ist die Ereignistyp Klasse für feste Seiten Fehlerereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 9837cc45-6485-46c3-a5d9-0d33e443cd32
title: PageFault_HardFault-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_HardFault
- PageFault_HardFault.InitialTime
- PageFault_HardFault.ReadOffset
- PageFault_HardFault.VirtualAddress
- PageFault_HardFault.FileObject
- PageFault_HardFault.TThreadId
- PageFault_HardFault.ByteCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 08afd3df20260a8ede63f4d741b3045ce3a39c1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960074"
---
# <a name="pagefault_hardfault-class"></a><span data-ttu-id="018a8-104">Pagefault \_ Hardfault-Klasse</span><span class="sxs-lookup"><span data-stu-id="018a8-104">PageFault\_HardFault class</span></span>

<span data-ttu-id="018a8-105">Diese Klasse ist die Ereignistyp Klasse für feste Seiten Fehlerereignisse.</span><span class="sxs-lookup"><span data-stu-id="018a8-105">This class is the event type class for hard page fault events.</span></span>

<span data-ttu-id="018a8-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="018a8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="018a8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="018a8-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"HardFault"}]
class PageFault_HardFault : PageFault_V2
{
  object InitialTime;
  uint64 ReadOffset;
  uint32 VirtualAddress;
  uint32 FileObject;
  uint32 TThreadId;
  uint32 ByteCount;
};
```

## <a name="members"></a><span data-ttu-id="018a8-108">Member</span><span class="sxs-lookup"><span data-stu-id="018a8-108">Members</span></span>

<span data-ttu-id="018a8-109">Die **Pagefault \_ Hardfault** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="018a8-109">The **PageFault\_HardFault** class has these types of members:</span></span>

-   [<span data-ttu-id="018a8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="018a8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="018a8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="018a8-111">Properties</span></span>

<span data-ttu-id="018a8-112">Die **Pagefault \_ Hardfault** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="018a8-112">The **PageFault\_HardFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="018a8-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="018a8-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="018a8-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="018a8-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="018a8-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="018a8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="018a8-116">Qualifizierer: wmidataid (6)</span><span class="sxs-lookup"><span data-stu-id="018a8-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="018a8-117">Die Menge der aus dem leseoffset gelesenen Daten, um den Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="018a8-117">Amount of data read from ReadOffset to satisfy the fault.</span></span>

</dd> <dt>

<span data-ttu-id="018a8-118">**File Object**</span><span class="sxs-lookup"><span data-stu-id="018a8-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="018a8-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="018a8-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="018a8-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="018a8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="018a8-121">Qualifizierer: wmidataid (4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="018a8-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="018a8-122">Vergleichen Sie den Wert dieses Zeigers mit dem **FileObject** -Zeiger Wert in einem [**FileIO- \_ namens**](fileio-name.md) Ereignis, um den Namen der Datei zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="018a8-122">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="018a8-123">**Initialtime**</span><span class="sxs-lookup"><span data-stu-id="018a8-123">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="018a8-124">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="018a8-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="018a8-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="018a8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="018a8-126">Qualifizierer: wmidataid (1), Erweiterung ("wmitime")</span><span class="sxs-lookup"><span data-stu-id="018a8-126">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="018a8-127">Der Start Zeitstempel, an dem der Seiten Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="018a8-127">Start time stamp at which page fault occurred.</span></span>

</dd> <dt>

<span data-ttu-id="018a8-128">**Read Offset**</span><span class="sxs-lookup"><span data-stu-id="018a8-128">**ReadOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="018a8-129">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="018a8-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="018a8-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="018a8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="018a8-131">Qualifizierer: wmidataid (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="018a8-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="018a8-132">Der Dateioffset, von dem aus Daten gelesen wurden, um Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="018a8-132">File offset from which data was read to satisfy fault.</span></span>

</dd> <dt>

<span data-ttu-id="018a8-133">**Tthreadid**</span><span class="sxs-lookup"><span data-stu-id="018a8-133">**TThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="018a8-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="018a8-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="018a8-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="018a8-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="018a8-136">Qualifizierer: wmidataid (5), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="018a8-136">Qualifiers: WmiDataId(5), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="018a8-137">Thread Bezeichner des Threads, der auf den Seiten Fehler gestoßen ist.</span><span class="sxs-lookup"><span data-stu-id="018a8-137">Thread identifier of the thread that encountered the page fault.</span></span>

</dd> <dt>

<span data-ttu-id="018a8-138">**VirtualAddress**</span><span class="sxs-lookup"><span data-stu-id="018a8-138">**VirtualAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="018a8-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="018a8-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="018a8-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="018a8-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="018a8-141">Qualifizierer: wmidataid (3), Zeiger</span><span class="sxs-lookup"><span data-stu-id="018a8-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="018a8-142">Fehleradressadresse.</span><span class="sxs-lookup"><span data-stu-id="018a8-142">Faulting address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="018a8-143">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="018a8-143">Requirements</span></span>



| <span data-ttu-id="018a8-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="018a8-144">Requirement</span></span> | <span data-ttu-id="018a8-145">Wert</span><span class="sxs-lookup"><span data-stu-id="018a8-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="018a8-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="018a8-146">Minimum supported client</span></span><br/> | <span data-ttu-id="018a8-147">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="018a8-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="018a8-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="018a8-148">Minimum supported server</span></span><br/> | <span data-ttu-id="018a8-149">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="018a8-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="018a8-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="018a8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="018a8-151">**Pagefault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="018a8-151">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




