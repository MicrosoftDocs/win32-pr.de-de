---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse des Haupt Funktions aufrufdes Treibers. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: Drivermajorfunctioncallklasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionCall
- DriverMajorFunctionCall.MajorFunction
- DriverMajorFunctionCall.MinorFunction
- DriverMajorFunctionCall.RoutineAddr
- DriverMajorFunctionCall.FileObject
- DriverMajorFunctionCall.Irp
- DriverMajorFunctionCall.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c944b11c9019ba5244850f035bfc7c02d5ca3350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977144"
---
# <a name="drivermajorfunctioncall-class"></a><span data-ttu-id="2091b-104">Drivermajorfunctioncallklasse</span><span class="sxs-lookup"><span data-stu-id="2091b-104">DriverMajorFunctionCall class</span></span>

<span data-ttu-id="2091b-105">Diese Klasse ist die Ereignistyp Klasse für Ereignisse des Haupt Funktions aufrufdes Treibers.</span><span class="sxs-lookup"><span data-stu-id="2091b-105">This class is the event type class for driver major function call events.</span></span>

<span data-ttu-id="2091b-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="2091b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2091b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2091b-107">Syntax</span></span>

``` syntax
[EventType{34}, EventTypeName{"DrvMjFnCall"}]
class DriverMajorFunctionCall : DiskIo
{
  uint32 MajorFunction;
  uint32 MinorFunction;
  uint32 RoutineAddr;
  uint32 FileObject;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="2091b-108">Member</span><span class="sxs-lookup"><span data-stu-id="2091b-108">Members</span></span>

<span data-ttu-id="2091b-109">Die **drivermajorfunctioncallklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2091b-109">The **DriverMajorFunctionCall** class has these types of members:</span></span>

-   [<span data-ttu-id="2091b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2091b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2091b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2091b-111">Properties</span></span>

<span data-ttu-id="2091b-112">Die **drivermajorfunctioncallklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2091b-112">The **DriverMajorFunctionCall** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2091b-113">**File Object**</span><span class="sxs-lookup"><span data-stu-id="2091b-113">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2091b-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2091b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2091b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2091b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2091b-116">Qualifizierer: wmidataid (4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="2091b-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2091b-117">Vergleichen Sie den Wert dieses Zeigers mit dem **FileObject** -Zeiger Wert in einem [**diskio \_ TypeGroup1**](diskio-typegroup1.md) -Ereignis, um den Typ des e/a-Vorgangs zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="2091b-117">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="2091b-118">**IRP**</span><span class="sxs-lookup"><span data-stu-id="2091b-118">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2091b-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2091b-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2091b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2091b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2091b-121">Qualifizierer: wmidataid (5), Zeiger</span><span class="sxs-lookup"><span data-stu-id="2091b-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2091b-122">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="2091b-122">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="2091b-123">**Majorfunction**</span><span class="sxs-lookup"><span data-stu-id="2091b-123">**MajorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2091b-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2091b-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2091b-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2091b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2091b-126">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="2091b-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="2091b-127">Code, der die Hauptfunktion identifiziert, die aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2091b-127">Code that identifies the major function being called.</span></span>

</dd> <dt>

<span data-ttu-id="2091b-128">**Minorfunction**</span><span class="sxs-lookup"><span data-stu-id="2091b-128">**MinorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2091b-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2091b-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2091b-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2091b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2091b-131">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="2091b-131">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="2091b-132">Code, der die Nebenfunktion, die aufgerufen wird, identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2091b-132">Code that idenitifies the minor function being called.</span></span>

</dd> <dt>

<span data-ttu-id="2091b-133">**Routineaddr**</span><span class="sxs-lookup"><span data-stu-id="2091b-133">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2091b-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2091b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2091b-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2091b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2091b-136">Qualifizierer: wmidataid (3), Zeiger</span><span class="sxs-lookup"><span data-stu-id="2091b-136">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2091b-137">Adresse der aufgerufenen Treiber Funktion.</span><span class="sxs-lookup"><span data-stu-id="2091b-137">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="2091b-138">**Uniqmatchid**</span><span class="sxs-lookup"><span data-stu-id="2091b-138">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2091b-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2091b-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2091b-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2091b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2091b-141">Qualifizierer: wmidataid (6)</span><span class="sxs-lookup"><span data-stu-id="2091b-141">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="2091b-142">Ein Bezeichner, der die Anforderung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2091b-142">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="2091b-143">Verwenden Sie diesen Bezeichner, um mit den anderen Treiber Ereignissen, z. b. dem [**drivercompleterequest**](drivercompleterequest.md) -Ereignis, zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="2091b-143">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2091b-144">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2091b-144">Requirements</span></span>



| <span data-ttu-id="2091b-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2091b-145">Requirement</span></span> | <span data-ttu-id="2091b-146">Wert</span><span class="sxs-lookup"><span data-stu-id="2091b-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2091b-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2091b-147">Minimum supported client</span></span><br/> | <span data-ttu-id="2091b-148">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2091b-148">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2091b-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2091b-149">Minimum supported server</span></span><br/> | <span data-ttu-id="2091b-150">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2091b-150">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2091b-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2091b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2091b-152">**Sowie**</span><span class="sxs-lookup"><span data-stu-id="2091b-152">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




