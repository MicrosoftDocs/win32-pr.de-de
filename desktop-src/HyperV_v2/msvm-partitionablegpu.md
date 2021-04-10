---
description: Stellt eine Partitionier Bare GPU dar. Jede GPU kann in eine Reihe von GPU-Partitionen aufgeteilt werden, die einem virtuellen Computer als vgpu zugewiesen werden können.
ms.assetid: a32dfc03-6967-4fa3-ae32-bf074137740b
title: Msvm_PartitionableGpu-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PartitionableGpu
- Msvm_PartitionableGpu.ValidPartitionCounts
- Msvm_PartitionableGpu.PartitionCount
- Msvm_PartitionableGpu.TotalVRAM
- Msvm_PartitionableGpu.AvailableVRAM
- Msvm_PartitionableGpu.MinPartitionVRAM
- Msvm_PartitionableGpu.MaxPartitionVRAM
- Msvm_PartitionableGpu.OptimalPartitionVRAM
- Msvm_PartitionableGpu.TotalEncode
- Msvm_PartitionableGpu.AvailableEncode
- Msvm_PartitionableGpu.MinPartitionEncode
- Msvm_PartitionableGpu.MaxPartitionEncode
- Msvm_PartitionableGpu.OptimalPartitionEncode
- Msvm_PartitionableGpu.TotalDecode
- Msvm_PartitionableGpu.AvailableDecode
- Msvm_PartitionableGpu.MinPartitionDecode
- Msvm_PartitionableGpu.MaxPartitionDecode
- Msvm_PartitionableGpu.OptimalPartitionDecode
- Msvm_PartitionableGpu.TotalCompute
- Msvm_PartitionableGpu.AvailableCompute
- Msvm_PartitionableGpu.MinPartitionCompute
- Msvm_PartitionableGpu.MaxPartitionCompute
- Msvm_PartitionableGpu.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f82904608a8e2ee4dfa13942066d57d35d511f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868495"
---
# <a name="msvm_partitionablegpu-class"></a><span data-ttu-id="a5bbf-104">MSVM \_ partitionablegpu-Klasse</span><span class="sxs-lookup"><span data-stu-id="a5bbf-104">Msvm\_PartitionableGpu class</span></span>

<span data-ttu-id="a5bbf-105">Stellt eine Partitionier Bare GPU dar.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-105">Represents a partitionable GPU.</span></span> <span data-ttu-id="a5bbf-106">Jede GPU kann in eine Reihe von GPU-Partitionen aufgeteilt werden, die einem virtuellen Computer als vgpu zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-106">Each GPU can be sliced into a number of GPU partitions, which can be assigned to a virtual machine as a vGPU.</span></span>

<span data-ttu-id="a5bbf-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5bbf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5bbf-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PartitionableGpu : CIM_ComputerSystem
{
  uint16 ValidPartitionCounts[];
  uint16 PartitionCount;
  uint64 TotalVRAM;
  uint64 AvailableVRAM;
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 TotalEncode;
  uint64 AvailableEncode;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 TotalDecode;
  uint64 AvailableDecode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 TotalCompute;
  uint64 AvailableCompute;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="a5bbf-109">Member</span><span class="sxs-lookup"><span data-stu-id="a5bbf-109">Members</span></span>

<span data-ttu-id="a5bbf-110">Die **MSVM \_ partitionablegpu** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a5bbf-110">The **Msvm\_PartitionableGpu** class has these types of members:</span></span>

-   [<span data-ttu-id="a5bbf-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5bbf-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5bbf-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5bbf-112">Properties</span></span>

<span data-ttu-id="a5bbf-113">Die **MSVM \_ partitionablegpu** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-113">The **Msvm\_PartitionableGpu** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5bbf-114">**Availablecompute**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-114">**AvailableCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-115">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-117">Die verfügbare Menge an computeengines, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-117">The available amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-118">**Availabledecode**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-118">**AvailableDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-119">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-121">Die verfügbare Anzahl von decodieren-Engines, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-121">The available amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-122">**Availablecodieren**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-122">**AvailableEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-123">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-125">Die verfügbare Anzahl der codierungsmodule, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-125">The available amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-126">**Availablevram**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-126">**AvailableVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-127">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-127">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-129">Die verfügbare VRAM-Größe, die in der GPU-Partition angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-129">The available amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-130">**Maxpartitioncompute**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-130">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-131">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-133">Die maximale Menge an computeengines, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-133">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-134">**Maxpartitiondecode**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-134">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-135">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-137">Die maximale Anzahl von decodieren-Engines, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-137">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-138">**Maxpartitioncocode**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-138">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-139">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-139">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-141">Die maximale Anzahl der codierungsmodule, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-141">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-142">**Maxpartitionvram**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-142">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-143">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-145">Die maximale VRAM-Größe, die in der GPU-Partition angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-145">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-146">**Minpartitioncompute**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-146">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-147">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-149">Die minimale Menge an computeengines, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-149">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-150">**Minpartitiondecode**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-150">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-151">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-153">Die minimale Anzahl von decodieren-Engines, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-153">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-154">**Minpartitioncocode**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-154">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-155">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-157">Der minimale Betrag der Codierungs-Engines, der in der GPU-Partition angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-157">The minumum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-158">**Minpartitionvram**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-158">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-159">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-161">Die minimale VRAM-Größe, die in der GPU-Partition angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-161">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-162">**Optimalpartitioncompute**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-162">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-163">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-165">Die optimale Menge an computeengines, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-165">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-166">**Optimalpartitiondecode**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-166">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-167">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-169">Die optimale Menge an Decodieren von Modulen, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-169">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-170">**Optimalpartitioncocode**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-170">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-171">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-173">Die optimale Menge der codierungsmodule, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-173">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-174">**Optimalpartitionvram**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-174">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-175">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-177">Die optimale VRAM-Größe, die in der GPU-Partition angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-177">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-178">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-178">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-179">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-180">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a5bbf-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-181">Die Menge der GPU-Partitionen, in die die physische GPU aufgeteilt ist.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-181">The amount of GPU partitions the physical GPU is sliced into.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-182">**Totalcompute**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-182">**TotalCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-183">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-185">Die Gesamtmenge der computemodule, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-185">The total amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-186">**Totaldecode**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-186">**TotalDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-187">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-189">Die Gesamtmenge der decodierungsmodule, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-189">The total amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-190">**Totalcodieren**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-190">**TotalEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-191">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-193">Die Gesamtmenge der codierungsmodule, die in der GPU-Partition angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-193">The total amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-194">**Totalvram**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-194">**TotalVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-195">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5bbf-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-197">Die Gesamtmenge des VRAM, der in der GPU-Partition angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-197">The total amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a5bbf-198">**Validpartitioncounts**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-198">**ValidPartitionCounts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bbf-199">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a5bbf-199">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a5bbf-200">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a5bbf-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a5bbf-201">Ein Array gültiger GPU-Partitions Optionen, in die die physische GPU aufgeteilt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a5bbf-201">An array of valid GPU partition options the physical GPU can be sliced into.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5bbf-202">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5bbf-202">Requirements</span></span>



| <span data-ttu-id="a5bbf-203">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5bbf-203">Requirement</span></span> | <span data-ttu-id="a5bbf-204">Wert</span><span class="sxs-lookup"><span data-stu-id="a5bbf-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5bbf-205">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5bbf-205">Minimum supported client</span></span><br/> | <span data-ttu-id="a5bbf-206">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5bbf-206">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a5bbf-207">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5bbf-207">Minimum supported server</span></span><br/> | <span data-ttu-id="a5bbf-208">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a5bbf-208">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a5bbf-209">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5bbf-209">Namespace</span></span><br/>                | <span data-ttu-id="a5bbf-210">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a5bbf-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a5bbf-211">MOF</span><span class="sxs-lookup"><span data-stu-id="a5bbf-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5bbf-212"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a5bbf-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5bbf-213">DLL</span><span class="sxs-lookup"><span data-stu-id="a5bbf-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5bbf-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a5bbf-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a5bbf-215">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5bbf-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5bbf-216">**CIM- \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="a5bbf-216">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




