---
description: Stellt die Funktionen und die Verwaltung eines Band Laufwerks dar.
ms.assetid: 8140fd9a-8a12-43b4-bc61-ec143e5d754c
title: CIM_TapeDrive-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.Padding
- CIM_TapeDrive.MaxRewindTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b92360388b71abcb0b67d30fddea9b4f5ed7920f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349777"
---
# <a name="cim_tapedrive-class-hyper-v-management"></a><span data-ttu-id="b6574-103">CIM_TapeDrive-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="b6574-103">CIM_TapeDrive class (Hyper-V management)</span></span>

<span data-ttu-id="b6574-104">Stellt die Funktionen und die Verwaltung eines Band Laufwerks dar.</span><span class="sxs-lookup"><span data-stu-id="b6574-104">Represents the capabilities and management of a tape drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6574-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6574-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices")]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint32 EOTWarningZoneSize;
  uint32 MaxPartitionCount;
  uint32 Padding;
  uint64 MaxRewindTime;
};
```

## <a name="members"></a><span data-ttu-id="b6574-106">Member</span><span class="sxs-lookup"><span data-stu-id="b6574-106">Members</span></span>

<span data-ttu-id="b6574-107">Die **CIM \_ TapeDrive** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b6574-107">The **CIM\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="b6574-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6574-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6574-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6574-109">Properties</span></span>

<span data-ttu-id="b6574-110">Die **CIM \_ TapeDrive** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b6574-110">The **CIM\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6574-111">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="b6574-111">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6574-112">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6574-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6574-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6574-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6574-114">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="b6574-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="b6574-115">Die Größe (in Bytes) des Bereichs, der als "Ende des Bands" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b6574-115">The size, in bytes, of the area designated as "end of tape".</span></span> <span data-ttu-id="b6574-116">Der Zugriff in diesem Bereich generiert die Warnung "Ende des Bands".</span><span class="sxs-lookup"><span data-stu-id="b6574-116">Access in this area generates an "end of tape" warning.</span></span>

</dd> <dt>

<span data-ttu-id="b6574-117">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="b6574-117">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6574-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6574-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6574-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6574-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6574-120">Die maximale Partitions Anzahl für das Bandlaufwerk.</span><span class="sxs-lookup"><span data-stu-id="b6574-120">The maximum partition count for the tape drive.</span></span>

</dd> <dt>

<span data-ttu-id="b6574-121">**Maxrewindtime**</span><span class="sxs-lookup"><span data-stu-id="b6574-121">**MaxRewindTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6574-122">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b6574-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b6574-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6574-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6574-124">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden"), **Punit** ("Second \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="b6574-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="b6574-125">Die Zeit (in Millisekunden), die vom physisch entfernten Punkt auf dem Band an den Anfang verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6574-125">The time, in milliseconds, to move from the most physically distant point on the tape to the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="b6574-126">**Auffüllen**</span><span class="sxs-lookup"><span data-stu-id="b6574-126">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6574-127">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6574-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6574-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6574-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6574-129">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="b6574-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="b6574-130">Die Anzahl von Bytes, die zwischen Blöcken auf Bandmedien eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b6574-130">The number of bytes inserted between blocks on tape media.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6574-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6574-131">Requirements</span></span>



| <span data-ttu-id="b6574-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6574-132">Requirement</span></span> | <span data-ttu-id="b6574-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b6574-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6574-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6574-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b6574-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b6574-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b6574-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6574-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b6574-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b6574-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b6574-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6574-138">Namespace</span></span><br/>                | <span data-ttu-id="b6574-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b6574-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b6574-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b6574-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6574-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b6574-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6574-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b6574-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6574-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b6574-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b6574-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6574-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6574-145">**CIM \_ mediaaccessdevice**</span><span class="sxs-lookup"><span data-stu-id="b6574-145">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

