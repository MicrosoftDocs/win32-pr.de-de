---
description: Diese Klasse ist die Ereignistyp Klasse für Routine Ereignisse, die Treiber vervollständigen. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: deb4f0b2-d73f-4ccf-b39b-6e92b32489fb
title: Drivercompletionroutine-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompletionRoutine
- DriverCompletionRoutine.Routine
- DriverCompletionRoutine.Irp
- DriverCompletionRoutine.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2b43862169cbe8f192f8fb9db561c2e101f377b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862087"
---
# <a name="drivercompletionroutine-class"></a><span data-ttu-id="013db-104">Drivercompletionroutine-Klasse</span><span class="sxs-lookup"><span data-stu-id="013db-104">DriverCompletionRoutine class</span></span>

<span data-ttu-id="013db-105">Diese Klasse ist die Ereignistyp Klasse für Routine Ereignisse, die Treiber vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="013db-105">This class is the event type class for driver complete routine events.</span></span>

<span data-ttu-id="013db-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="013db-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="013db-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="013db-107">Syntax</span></span>

``` syntax
[EventType{37}, EventTypeName{"DrvComplRout"}]
class DriverCompletionRoutine : DiskIo
{
  uint32 Routine;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="013db-108">Member</span><span class="sxs-lookup"><span data-stu-id="013db-108">Members</span></span>

<span data-ttu-id="013db-109">Die **drivercompletionroutine** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="013db-109">The **DriverCompletionRoutine** class has these types of members:</span></span>

-   [<span data-ttu-id="013db-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="013db-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="013db-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="013db-111">Properties</span></span>

<span data-ttu-id="013db-112">Die **drivercompletionroutine** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="013db-112">The **DriverCompletionRoutine** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="013db-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="013db-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="013db-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="013db-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="013db-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="013db-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="013db-116">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="013db-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="013db-117">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="013db-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="013db-118">**-Routine zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="013db-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="013db-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="013db-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="013db-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="013db-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="013db-121">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="013db-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="013db-122">Adresse der aufgerufenen Treiber Funktion.</span><span class="sxs-lookup"><span data-stu-id="013db-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="013db-123">**Uniqmatchid**</span><span class="sxs-lookup"><span data-stu-id="013db-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="013db-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="013db-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="013db-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="013db-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="013db-126">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="013db-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="013db-127">Ein Bezeichner, der die Anforderung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="013db-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="013db-128">Verwenden Sie diesen Bezeichner, um mit den anderen Treiber Ereignissen, z. b. dem [**drivercompleterequest**](drivercompleterequest.md) -Ereignis, zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="013db-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="013db-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="013db-129">Requirements</span></span>



| <span data-ttu-id="013db-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="013db-130">Requirement</span></span> | <span data-ttu-id="013db-131">Wert</span><span class="sxs-lookup"><span data-stu-id="013db-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="013db-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="013db-132">Minimum supported client</span></span><br/> | <span data-ttu-id="013db-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="013db-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="013db-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="013db-134">Minimum supported server</span></span><br/> | <span data-ttu-id="013db-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="013db-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="013db-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="013db-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="013db-137">**Sowie**</span><span class="sxs-lookup"><span data-stu-id="013db-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




