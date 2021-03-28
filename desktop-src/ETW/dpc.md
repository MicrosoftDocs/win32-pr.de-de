---
description: Diese Klasse ist die Ereignistyp Klasse für Geräte verzögerte Prozedur Aufrufe (DPC). Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: DPC-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862088"
---
# <a name="dpc-class"></a><span data-ttu-id="600a8-104">DPC-Klasse</span><span class="sxs-lookup"><span data-stu-id="600a8-104">DPC class</span></span>

<span data-ttu-id="600a8-105">Diese Klasse ist die Ereignistyp Klasse für Geräte verzögerte Prozedur Aufrufe (DPC).</span><span class="sxs-lookup"><span data-stu-id="600a8-105">This class is the event type class for device deferred procedure call (DPC) events.</span></span>

<span data-ttu-id="600a8-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="600a8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="600a8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="600a8-107">Syntax</span></span>

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a><span data-ttu-id="600a8-108">Member</span><span class="sxs-lookup"><span data-stu-id="600a8-108">Members</span></span>

<span data-ttu-id="600a8-109">Die **DPC** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="600a8-109">The **DPC** class has these types of members:</span></span>

-   [<span data-ttu-id="600a8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="600a8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="600a8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="600a8-111">Properties</span></span>

<span data-ttu-id="600a8-112">Die **DPC** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="600a8-112">The **DPC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="600a8-113">**Initialtime**</span><span class="sxs-lookup"><span data-stu-id="600a8-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600a8-114">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="600a8-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="600a8-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="600a8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600a8-116">Qualifizierer: wmidataid (1), Erweiterung ("wmitime")</span><span class="sxs-lookup"><span data-stu-id="600a8-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="600a8-117">DPC-Eintrags Zeit.</span><span class="sxs-lookup"><span data-stu-id="600a8-117">DPC entry time.</span></span>

</dd> <dt>

<span data-ttu-id="600a8-118">**-Routine zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="600a8-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600a8-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="600a8-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="600a8-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="600a8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600a8-121">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="600a8-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="600a8-122">Adresse der DPC-Routine.</span><span class="sxs-lookup"><span data-stu-id="600a8-122">Address of DPC routine.</span></span> <span data-ttu-id="600a8-123">Verwenden Sie die Adresse mit den Bild Ereignissen, um zu ermitteln, welches Image gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="600a8-123">Use the address with the Image events to find which image started.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="600a8-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="600a8-124">Remarks</span></span>

<span data-ttu-id="600a8-125">Diese Ereignisse werden protokolliert, wenn ein DPC eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="600a8-125">These events are logged when a DPC is entered.</span></span> <span data-ttu-id="600a8-126">Mit diesen Ereignissen können Sie das Verhalten von Treibern und Kernelmoduskomponenten überwachen und überprüfen.</span><span class="sxs-lookup"><span data-stu-id="600a8-126">You use these events to monitor and verify the behavior of drivers and kernel-mode components.</span></span> <span data-ttu-id="600a8-127">Beispielsweise können Sie DPC-, ISR-und Image-Ereignisse verwenden, um die Komponenten zu bestimmen, die zu viel Zeit für hohe Unterbrechungs Stufen aufwenden.</span><span class="sxs-lookup"><span data-stu-id="600a8-127">For example, you can use DPC, ISR, and Image events to determine those components that spend too much time at high interrupt levels.</span></span> <span data-ttu-id="600a8-128">DPC-und ISR-Ereignisse verfügen über einen Eintrags Zeitstempel, der verwendet wird, um die Dauer der Routinen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="600a8-128">DPC and ISR events have an entry time stamp which is used to compute the duration of the routines.</span></span> <span data-ttu-id="600a8-129">Die Bild Ereignisse werden gelesen, um die Speicherbereiche zu erstellen, die bestimmten Modulen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="600a8-129">The image events are read to construct the memory regions that map to certain modules.</span></span> <span data-ttu-id="600a8-130">Sie können die Zuordnung verwenden, um das Modul zu suchen, das die Interruptroutine enthält.</span><span class="sxs-lookup"><span data-stu-id="600a8-130">You can use the mapping to locate the module that contains the interrupt routine.</span></span>

<span data-ttu-id="600a8-131">Das timerdpc-Ereignis zeichnet auf, wenn ein DPC aufgrund eines Zeit Geber Ablaufs und der threaddpc-Ereignisdaten Sätze ausgelöst wird, wenn ein Thread-DPC ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="600a8-131">The TimerDPC event records when a DPC fires as a result of a timer expiration and the ThreadDPC event records when a threaded DPC executes.</span></span>

## <a name="requirements"></a><span data-ttu-id="600a8-132">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="600a8-132">Requirements</span></span>



| <span data-ttu-id="600a8-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="600a8-133">Requirement</span></span> | <span data-ttu-id="600a8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="600a8-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="600a8-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="600a8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="600a8-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="600a8-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="600a8-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="600a8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="600a8-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="600a8-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




