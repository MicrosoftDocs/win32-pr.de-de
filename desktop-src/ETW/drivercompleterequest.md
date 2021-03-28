---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse, die vom Treiber erfüllt werden. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: Drivercompleterequest-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequest
- DriverCompleteRequest.RoutineAddr
- DriverCompleteRequest.Irp
- DriverCompleteRequest.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 57cf49d0e37dc870c0eb46c31ef39e0d81689811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977152"
---
# <a name="drivercompleterequest-class"></a><span data-ttu-id="6cba2-104">Drivercompleterequest-Klasse</span><span class="sxs-lookup"><span data-stu-id="6cba2-104">DriverCompleteRequest class</span></span>

<span data-ttu-id="6cba2-105">Diese Klasse ist die Ereignistyp Klasse für Ereignisse, die vom Treiber erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="6cba2-105">This class is the event type class for driver complete request events.</span></span>

<span data-ttu-id="6cba2-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="6cba2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cba2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cba2-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"DrvComplReq"}]
class DriverCompleteRequest : DiskIo
{
  uint32 RoutineAddr;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="6cba2-108">Member</span><span class="sxs-lookup"><span data-stu-id="6cba2-108">Members</span></span>

<span data-ttu-id="6cba2-109">Die Klasse " **drivercompleterequest** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6cba2-109">The **DriverCompleteRequest** class has these types of members:</span></span>

-   [<span data-ttu-id="6cba2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6cba2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6cba2-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6cba2-111">Properties</span></span>

<span data-ttu-id="6cba2-112">Die Klasse " **drivercompleterequest** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6cba2-112">The **DriverCompleteRequest** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6cba2-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="6cba2-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cba2-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6cba2-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6cba2-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6cba2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cba2-116">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="6cba2-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6cba2-117">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="6cba2-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="6cba2-118">**Routineaddr**</span><span class="sxs-lookup"><span data-stu-id="6cba2-118">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cba2-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6cba2-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6cba2-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6cba2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cba2-121">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="6cba2-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6cba2-122">Adresse der aufgerufenen Treiber Funktion.</span><span class="sxs-lookup"><span data-stu-id="6cba2-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="6cba2-123">**Uniqmatchid**</span><span class="sxs-lookup"><span data-stu-id="6cba2-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cba2-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6cba2-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6cba2-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6cba2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cba2-126">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="6cba2-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="6cba2-127">Ein Bezeichner, der die Anforderung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6cba2-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="6cba2-128">Verwenden Sie diesen Bezeichner, um mit den anderen Treiber Ereignissen, z. b. dem [**drivercompleterequestreturn**](drivercompleterequestreturn.md) -Ereignis, zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="6cba2-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6cba2-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6cba2-129">Requirements</span></span>



| <span data-ttu-id="6cba2-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6cba2-130">Requirement</span></span> | <span data-ttu-id="6cba2-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6cba2-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6cba2-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6cba2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6cba2-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cba2-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6cba2-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6cba2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6cba2-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cba2-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6cba2-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6cba2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cba2-137">**Sowie**</span><span class="sxs-lookup"><span data-stu-id="6cba2-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




