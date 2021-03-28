---
description: Die Klasse hwconfig \_ logdisk ist die Ereignistyp Klasse für Konfigurations Ereignisse logischer Datenträger. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: HWConfig_LogDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce4faed913d01f76ff23177b2dad42ea74e5c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529885"
---
# <a name="hwconfig_logdisk-class"></a><span data-ttu-id="190a9-104">Hwconfig \_ logdisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="190a9-104">HWConfig\_LogDisk class</span></span>

<span data-ttu-id="190a9-105">Die Klasse **hwconfig \_ logdisk** ist die Ereignistyp Klasse für Konfigurations Ereignisse logischer Datenträger.</span><span class="sxs-lookup"><span data-stu-id="190a9-105">The **HWConfig\_LogDisk** class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="190a9-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="190a9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="190a9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="190a9-107">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a><span data-ttu-id="190a9-108">Member</span><span class="sxs-lookup"><span data-stu-id="190a9-108">Members</span></span>

<span data-ttu-id="190a9-109">Die Klasse " **hwconfig \_ logdisk** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="190a9-109">The **HWConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="190a9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="190a9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="190a9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="190a9-111">Properties</span></span>

<span data-ttu-id="190a9-112">Die **hwconfig \_ logdisk** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="190a9-112">The **HWConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="190a9-113">Disknumber</span><span class="sxs-lookup"><span data-stu-id="190a9-113">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="190a9-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="190a9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="190a9-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="190a9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="190a9-116">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="190a9-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="190a9-117">Index Nummer des Datenträgers, der diese Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="190a9-117">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="190a9-118">Pad</span><span class="sxs-lookup"><span data-stu-id="190a9-118">Pad</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="190a9-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="190a9-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="190a9-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="190a9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="190a9-121">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="190a9-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="190a9-122">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="190a9-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="190a9-123">PartitionSize</span><span class="sxs-lookup"><span data-stu-id="190a9-123">PartitionSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="190a9-124">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="190a9-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="190a9-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="190a9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="190a9-126">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="190a9-126">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="190a9-127">Gesamtgröße der Partition in Bytes.</span><span class="sxs-lookup"><span data-stu-id="190a9-127">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="190a9-128">Starto ffset</span><span class="sxs-lookup"><span data-stu-id="190a9-128">StartOffset</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="190a9-129">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="190a9-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="190a9-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="190a9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="190a9-131">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="190a9-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="190a9-132">Start Offset (in Bytes) der Partition vom Anfang des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="190a9-132">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="190a9-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="190a9-133">Requirements</span></span>



| <span data-ttu-id="190a9-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="190a9-134">Requirement</span></span> | <span data-ttu-id="190a9-135">Wert</span><span class="sxs-lookup"><span data-stu-id="190a9-135">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="190a9-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="190a9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="190a9-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="190a9-137">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="190a9-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="190a9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="190a9-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="190a9-139">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="190a9-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="190a9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="190a9-141">**Hwconfig**</span><span class="sxs-lookup"><span data-stu-id="190a9-141">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




