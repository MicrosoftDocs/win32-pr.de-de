---
description: Stellt den konfigurierten Status eines GPU-Partitions Geräts dar.
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Msvm_GpuPartitionSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d8c9809b3a062654eaf0fb7a73b75b0188f7284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959040"
---
# <a name="msvm_gpupartitionsettingdata-class"></a><span data-ttu-id="bb3c8-103">MSVM \_ gpupartitionsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="bb3c8-103">Msvm\_GpuPartitionSettingData class</span></span>

<span data-ttu-id="bb3c8-104">Stellt den konfigurierten Status eines GPU-Partitions Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-104">Represents the configured state of a GPU partition device.</span></span>

<span data-ttu-id="bb3c8-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb3c8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb3c8-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="bb3c8-107">Member</span><span class="sxs-lookup"><span data-stu-id="bb3c8-107">Members</span></span>

<span data-ttu-id="bb3c8-108">Die **MSVM-Klasse " \_ gpupartitionsettingdata** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bb3c8-108">The **Msvm\_GpuPartitionSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="bb3c8-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb3c8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb3c8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb3c8-110">Properties</span></span>

<span data-ttu-id="bb3c8-111">Die **MSVM \_ gpupartitionsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-111">The **Msvm\_GpuPartitionSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb3c8-112">**Maxpartitioncompute**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-112">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb3c8-113">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb3c8-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb3c8-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb3c8-115">Die maximale Menge an computeengines, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-115">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="bb3c8-116">**Maxpartitiondecode**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-116">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb3c8-117">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-117">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb3c8-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb3c8-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb3c8-119">Die maximale Anzahl von decodieren-Engines, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-119">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="bb3c8-120">**Maxpartitioncocode**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-120">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb3c8-121">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb3c8-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb3c8-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb3c8-123">Die maximale Anzahl der codierungsmodule, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-123">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="bb3c8-124">**Maxpartitionvram**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-124">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb3c8-125">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb3c8-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb3c8-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb3c8-127">Die maximale VRAM-Größe, die in der GPU-Partition angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-127">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="bb3c8-128">**Minpartitioncompute**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-128">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb3c8-129">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb3c8-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb3c8-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb3c8-131">Die minimale Menge an computeengines, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-131">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="bb3c8-132">**Minpartitiondecode**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-132">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb3c8-133">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb3c8-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb3c8-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb3c8-135">Die minimale Anzahl von decodieren-Engines, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-135">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="bb3c8-136">**Minpartitioncocode**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-136">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb3c8-137">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb3c8-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb3c8-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb3c8-139">Die Mindestanzahl der codiermodule, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-139">The minimum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="bb3c8-140">**Minpartitionvram**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-140">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb3c8-141">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb3c8-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb3c8-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb3c8-143">Die minimale VRAM-Größe, die in der GPU-Partition angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-143">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="bb3c8-144">**Optimalpartitioncompute**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-144">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb3c8-145">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb3c8-146">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb3c8-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb3c8-147">Die optimale Menge an computeengines, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-147">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="bb3c8-148">**Optimalpartitiondecode**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-148">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb3c8-149">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb3c8-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb3c8-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb3c8-151">Die optimale Menge an Decodieren von Modulen, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-151">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="bb3c8-152">**Optimalpartitioncocode**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-152">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb3c8-153">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb3c8-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb3c8-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb3c8-155">Die optimale Menge der codierungsmodule, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-155">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="bb3c8-156">**Optimalpartitionvram**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-156">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb3c8-157">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb3c8-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bb3c8-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb3c8-159">Die optimale VRAM-Größe, die in der GPU-Partition angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bb3c8-159">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb3c8-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb3c8-160">Requirements</span></span>



| <span data-ttu-id="bb3c8-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb3c8-161">Requirement</span></span> | <span data-ttu-id="bb3c8-162">Wert</span><span class="sxs-lookup"><span data-stu-id="bb3c8-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb3c8-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb3c8-163">Minimum supported client</span></span><br/> | <span data-ttu-id="bb3c8-164">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb3c8-164">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bb3c8-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb3c8-165">Minimum supported server</span></span><br/> | <span data-ttu-id="bb3c8-166">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bb3c8-166">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bb3c8-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb3c8-167">Namespace</span></span><br/>                | <span data-ttu-id="bb3c8-168">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="bb3c8-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bb3c8-169">MOF</span><span class="sxs-lookup"><span data-stu-id="bb3c8-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb3c8-170"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bb3c8-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb3c8-171">DLL</span><span class="sxs-lookup"><span data-stu-id="bb3c8-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb3c8-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb3c8-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb3c8-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb3c8-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb3c8-174">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="bb3c8-174">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




