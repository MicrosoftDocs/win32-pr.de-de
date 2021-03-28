---
description: Diese Klasse ist die Ereignistyp Klasse für Interrupt Service Routine (ISR)-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: ISR-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e27d5aa2712f8493b80ea11884aae1d0ef7abee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979873"
---
# <a name="isr-class"></a><span data-ttu-id="a1624-104">ISR-Klasse</span><span class="sxs-lookup"><span data-stu-id="a1624-104">ISR class</span></span>

<span data-ttu-id="a1624-105">Diese Klasse ist die Ereignistyp Klasse für Interrupt Service Routine (ISR)-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="a1624-105">This class is the event type class for interrupt service routine (ISR) events.</span></span>

<span data-ttu-id="a1624-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="a1624-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1624-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1624-107">Syntax</span></span>

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="a1624-108">Member</span><span class="sxs-lookup"><span data-stu-id="a1624-108">Members</span></span>

<span data-ttu-id="a1624-109">Die **ISR** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a1624-109">The **ISR** class has these types of members:</span></span>

-   [<span data-ttu-id="a1624-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1624-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1624-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1624-111">Properties</span></span>

<span data-ttu-id="a1624-112">Die **ISR** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1624-112">The **ISR** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1624-113">**Initialtime**</span><span class="sxs-lookup"><span data-stu-id="a1624-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1624-114">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="a1624-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a1624-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1624-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1624-116">Qualifizierer: wmidataid (1), Erweiterung ("wmitime")</span><span class="sxs-lookup"><span data-stu-id="a1624-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="a1624-117">ISR-Eintrags Zeit.</span><span class="sxs-lookup"><span data-stu-id="a1624-117">ISR entry time.</span></span>

</dd> <dt>

<span data-ttu-id="a1624-118">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a1624-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1624-119">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1624-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1624-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1624-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1624-121">Qualifizierer: wmidataid (5), Zeiger</span><span class="sxs-lookup"><span data-stu-id="a1624-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a1624-122">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a1624-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a1624-123">**ReturnValue**</span><span class="sxs-lookup"><span data-stu-id="a1624-123">**ReturnValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1624-124">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a1624-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a1624-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1624-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1624-126">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="a1624-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="a1624-127">Boolescher Wert, der angibt, ob der Interrupt beansprucht wurde (ist true, wenn der Interrupt beansprucht wurde).</span><span class="sxs-lookup"><span data-stu-id="a1624-127">Boolean indicating if the interrupt was claimed (is True if the interrupt was claimed).</span></span>

</dd> <dt>

<span data-ttu-id="a1624-128">**-Routine zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="a1624-128">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1624-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1624-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1624-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1624-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1624-131">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="a1624-131">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a1624-132">Die Adresse der ISR-Routine.</span><span class="sxs-lookup"><span data-stu-id="a1624-132">Address of ISR routine.</span></span> <span data-ttu-id="a1624-133">Verwenden Sie die Adresse mit den Bild Ereignissen, um zu ermitteln, welches Image gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="a1624-133">Use the address with the Image events to find which image started.</span></span>

</dd> <dt>

<span data-ttu-id="a1624-134">**Vektor**</span><span class="sxs-lookup"><span data-stu-id="a1624-134">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1624-135">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a1624-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a1624-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1624-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1624-137">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="a1624-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="a1624-138">Vektor aus der Interrupt-Deskriptortabelle, der die ISR-Routine zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a1624-138">Vector from interrupt descriptor table to which ISR routine is assigned.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1624-139">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a1624-139">Requirements</span></span>



| <span data-ttu-id="a1624-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1624-140">Requirement</span></span> | <span data-ttu-id="a1624-141">Wert</span><span class="sxs-lookup"><span data-stu-id="a1624-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1624-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1624-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a1624-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1624-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1624-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1624-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a1624-145">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1624-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




