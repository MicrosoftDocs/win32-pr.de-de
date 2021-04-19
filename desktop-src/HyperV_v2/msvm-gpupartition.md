---
description: Stellt den Status der GPU-Partition dar.
ms.assetid: 319b37d5-b5f0-4251-9482-316347a9015b
title: Msvm_GpuPartition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartition
- Msvm_GpuPartition.DeviceInstancePath
- Msvm_GpuPartition.PartitionId
- Msvm_GpuPartition.PartitionVfLuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc0975644609832c692f5522cc756240f7a5bff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360075"
---
# <a name="msvm_gpupartition-class"></a><span data-ttu-id="cae4a-103">MSVM- \_ gpupartition-Klasse</span><span class="sxs-lookup"><span data-stu-id="cae4a-103">Msvm\_GpuPartition class</span></span>

<span data-ttu-id="cae4a-104">Stellt den Status der GPU-Partition dar.</span><span class="sxs-lookup"><span data-stu-id="cae4a-104">Represents the state of the GPU partition.</span></span>

<span data-ttu-id="cae4a-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cae4a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae4a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cae4a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartition : CIM_LogicalDevice
{
  string DeviceInstancePath;
  uint16 PartitionId;
  string PartitionVfLuid;
};
```

## <a name="members"></a><span data-ttu-id="cae4a-107">Member</span><span class="sxs-lookup"><span data-stu-id="cae4a-107">Members</span></span>

<span data-ttu-id="cae4a-108">Die **MSVM-Klasse " \_ gpupartition** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cae4a-108">The **Msvm\_GpuPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="cae4a-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cae4a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cae4a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cae4a-110">Properties</span></span>

<span data-ttu-id="cae4a-111">Die **MSVM- \_ gpupartition** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cae4a-111">The **Msvm\_GpuPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cae4a-112">**Gerätepfad**</span><span class="sxs-lookup"><span data-stu-id="cae4a-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cae4a-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cae4a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cae4a-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cae4a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cae4a-115">Eine Zeichenfolge, die den geräteinstanzpfad enthält, der das GPU-Partitions Gerät identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cae4a-115">A string containing the device instance path that identifies the GPU partition device.</span></span>

</dd> <dt>

<span data-ttu-id="cae4a-116">**PartitionId**</span><span class="sxs-lookup"><span data-stu-id="cae4a-116">**PartitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cae4a-117">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cae4a-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cae4a-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cae4a-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cae4a-119">Die Partitions-ID des GPU-Partitions Geräts.</span><span class="sxs-lookup"><span data-stu-id="cae4a-119">The partition ID of the GPU partition device.</span></span>

</dd> <dt>

<span data-ttu-id="cae4a-120">**Partitionvfluid**</span><span class="sxs-lookup"><span data-stu-id="cae4a-120">**PartitionVfLuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cae4a-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cae4a-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cae4a-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cae4a-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cae4a-123">Die virtuelle Funktion LUID, die eine GPU-Partition darstellt.</span><span class="sxs-lookup"><span data-stu-id="cae4a-123">The virtual function LUID, which represents a GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cae4a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cae4a-124">Requirements</span></span>



| <span data-ttu-id="cae4a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cae4a-125">Requirement</span></span> | <span data-ttu-id="cae4a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="cae4a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cae4a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cae4a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cae4a-128">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cae4a-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cae4a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cae4a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cae4a-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cae4a-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cae4a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="cae4a-131">Namespace</span></span><br/>                | <span data-ttu-id="cae4a-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cae4a-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cae4a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="cae4a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cae4a-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cae4a-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cae4a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="cae4a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cae4a-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cae4a-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cae4a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cae4a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae4a-138">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="cae4a-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




