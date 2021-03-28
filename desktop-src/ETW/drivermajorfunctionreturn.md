---
description: Diese Klasse ist die Ereignistyp Klasse für Treiber-Haupt Funktionsaufrufe-Rückgabe Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: b3358935-d6fb-49eb-bdf7-4366b4fd14c5
title: Drivermajorfunctionreturn-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionReturn
- DriverMajorFunctionReturn.Irp
- DriverMajorFunctionReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21340224253d1eb3f3ddc733bf2d43e847844282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525250"
---
# <a name="drivermajorfunctionreturn-class"></a><span data-ttu-id="17e17-104">Drivermajorfunctionreturn-Klasse</span><span class="sxs-lookup"><span data-stu-id="17e17-104">DriverMajorFunctionReturn class</span></span>

<span data-ttu-id="17e17-105">Diese Klasse ist die Ereignistyp Klasse für Treiber-Haupt Funktionsaufrufe-Rückgabe Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="17e17-105">This class is the event type class for driver major function call return events.</span></span>

<span data-ttu-id="17e17-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="17e17-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e17-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="17e17-107">Syntax</span></span>

``` syntax
[EventType{35}, EventTypeName{"DrvMjFnRet"}]
class DriverMajorFunctionReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="17e17-108">Member</span><span class="sxs-lookup"><span data-stu-id="17e17-108">Members</span></span>

<span data-ttu-id="17e17-109">Die **drivermajorfunctionreturn** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="17e17-109">The **DriverMajorFunctionReturn** class has these types of members:</span></span>

-   [<span data-ttu-id="17e17-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17e17-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17e17-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17e17-111">Properties</span></span>

<span data-ttu-id="17e17-112">Die **drivermajorfunctionreturn** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17e17-112">The **DriverMajorFunctionReturn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17e17-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="17e17-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17e17-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17e17-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17e17-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17e17-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17e17-116">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="17e17-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="17e17-117">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="17e17-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="17e17-118">**Uniqmatchid**</span><span class="sxs-lookup"><span data-stu-id="17e17-118">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17e17-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17e17-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17e17-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17e17-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17e17-121">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="17e17-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="17e17-122">Ein Bezeichner, der die Anforderung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="17e17-122">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="17e17-123">Verwenden Sie diesen Bezeichner, um mit den anderen Treiber Ereignissen, z. b. dem [**drivercompleterequest**](drivercompleterequest.md) -Ereignis, zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="17e17-123">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17e17-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="17e17-124">Requirements</span></span>



| <span data-ttu-id="17e17-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17e17-125">Requirement</span></span> | <span data-ttu-id="17e17-126">Wert</span><span class="sxs-lookup"><span data-stu-id="17e17-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="17e17-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17e17-127">Minimum supported client</span></span><br/> | <span data-ttu-id="17e17-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17e17-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="17e17-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17e17-129">Minimum supported server</span></span><br/> | <span data-ttu-id="17e17-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17e17-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17e17-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="17e17-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e17-132">**Sowie**</span><span class="sxs-lookup"><span data-stu-id="17e17-132">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




