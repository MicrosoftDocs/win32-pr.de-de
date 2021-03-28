---
description: Bei dieser Klasse handelt es sich um die Ereignistyp Klasse für zurückgegebene Ereignisse der Treiber Complete Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 04505f8c-a11e-4bf7-91c0-fca1b5846d80
title: Drivercompleterequestreturn-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequestReturn
- DriverCompleteRequestReturn.Irp
- DriverCompleteRequestReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c147573578e067b7fb1b588545a1d9f231e35f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525256"
---
# <a name="drivercompleterequestreturn-class"></a><span data-ttu-id="50eed-104">Drivercompleterequestreturn-Klasse</span><span class="sxs-lookup"><span data-stu-id="50eed-104">DriverCompleteRequestReturn class</span></span>

<span data-ttu-id="50eed-105">Bei dieser Klasse handelt es sich um die Ereignistyp Klasse für zurückgegebene Ereignisse der Treiber Complete</span><span class="sxs-lookup"><span data-stu-id="50eed-105">This class is the event type class for driver complete request return events.</span></span>

<span data-ttu-id="50eed-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="50eed-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="50eed-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="50eed-107">Syntax</span></span>

``` syntax
[EventType{53}, EventTypeName{"DrvComplReqRet"}]
class DriverCompleteRequestReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="50eed-108">Member</span><span class="sxs-lookup"><span data-stu-id="50eed-108">Members</span></span>

<span data-ttu-id="50eed-109">Die **drivercompleterequestreturn** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="50eed-109">The **DriverCompleteRequestReturn** class has these types of members:</span></span>

-   [<span data-ttu-id="50eed-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50eed-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50eed-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50eed-111">Properties</span></span>

<span data-ttu-id="50eed-112">Die **drivercompleterequestreturn** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="50eed-112">The **DriverCompleteRequestReturn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50eed-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="50eed-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50eed-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50eed-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50eed-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50eed-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50eed-116">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="50eed-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="50eed-117">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="50eed-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="50eed-118">**Uniqmatchid**</span><span class="sxs-lookup"><span data-stu-id="50eed-118">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50eed-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50eed-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50eed-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50eed-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50eed-121">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="50eed-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="50eed-122">Ein Bezeichner, der die Anforderung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="50eed-122">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="50eed-123">Verwenden Sie diesen Bezeichner, um mit den anderen Treiber Ereignissen, z. b. dem [**drivercompleterequest**](drivercompleterequest.md) -Ereignis, zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="50eed-123">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50eed-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="50eed-124">Requirements</span></span>



| <span data-ttu-id="50eed-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50eed-125">Requirement</span></span> | <span data-ttu-id="50eed-126">Wert</span><span class="sxs-lookup"><span data-stu-id="50eed-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50eed-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50eed-127">Minimum supported client</span></span><br/> | <span data-ttu-id="50eed-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50eed-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="50eed-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50eed-129">Minimum supported server</span></span><br/> | <span data-ttu-id="50eed-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50eed-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50eed-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="50eed-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50eed-132">**Sowie**</span><span class="sxs-lookup"><span data-stu-id="50eed-132">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




