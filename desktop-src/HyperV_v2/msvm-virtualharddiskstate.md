---
description: Stellt Zustandsinformationen für ein vorhandenes virtuelles Festplatten Abbild bereit.
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Msvm_VirtualHardDiskState-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15d0a8b150e83c17946a6d1b66c7086383f08466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484355"
---
# <a name="msvm_virtualharddiskstate-class"></a><span data-ttu-id="06a84-103">MSVM \_ virtualharddiskstate-Klasse</span><span class="sxs-lookup"><span data-stu-id="06a84-103">Msvm\_VirtualHardDiskState class</span></span>

<span data-ttu-id="06a84-104">Stellt Zustandsinformationen für ein vorhandenes virtuelles Festplatten Abbild bereit.</span><span class="sxs-lookup"><span data-stu-id="06a84-104">Provides state information for an existing virtual hard disk image.</span></span>

<span data-ttu-id="06a84-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="06a84-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a84-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="06a84-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a><span data-ttu-id="06a84-107">Member</span><span class="sxs-lookup"><span data-stu-id="06a84-107">Members</span></span>

<span data-ttu-id="06a84-108">Die Klasse " **MSVM \_ virtualharddiskstate** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="06a84-108">The **Msvm\_VirtualHardDiskState** class has these types of members:</span></span>

-   [<span data-ttu-id="06a84-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06a84-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06a84-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06a84-110">Properties</span></span>

<span data-ttu-id="06a84-111">Die **MSVM \_ virtualharddiskstate** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="06a84-111">The **Msvm\_VirtualHardDiskState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06a84-112">**Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="06a84-112">**Alignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a84-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06a84-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06a84-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06a84-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a84-115">Gibt den Typ der Ausrichtung der virtuellen Festplatte an.</span><span class="sxs-lookup"><span data-stu-id="06a84-115">Specifies the type of alignment of the virtual hard disk.</span></span> <span data-ttu-id="06a84-116">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="06a84-116">This will be one of the following values.</span></span>



| <span data-ttu-id="06a84-117">Wert</span><span class="sxs-lookup"><span data-stu-id="06a84-117">Value</span></span>                                                                        | <span data-ttu-id="06a84-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="06a84-118">Meaning</span></span>                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="06a84-119"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="06a84-119"><dt>0</dt></span></span> </dl> | <span data-ttu-id="06a84-120">512-Byte-Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="06a84-120">512 byte alignment.</span></span><br/> |
| <dl> <span data-ttu-id="06a84-121"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="06a84-121"><dt>1</dt></span></span> </dl> | <span data-ttu-id="06a84-122">4-KB-Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="06a84-122">4 KB alignment.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="06a84-123">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="06a84-123">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a84-124">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06a84-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06a84-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06a84-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a84-126">Die Größe der virtuellen Festplatten Datei (die tatsächliche Menge an Speicher, die von der Datei belegt wird) in Bytes.</span><span class="sxs-lookup"><span data-stu-id="06a84-126">The size of the virtual hard disk file (the actual amount of storage being consumed by the file), in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="06a84-127">**Fragmentationprozentsatz**</span><span class="sxs-lookup"><span data-stu-id="06a84-127">**FragmentationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a84-128">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06a84-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06a84-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06a84-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a84-130">Ein Näherungswert für den Prozentsatz der virtuellen Festplattenblöcke, die in der virtuellen Festplatten Datei fragmentiert sind.</span><span class="sxs-lookup"><span data-stu-id="06a84-130">An approximation of the percentage of virtual disk blocks that are fragmented in the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="06a84-131">**Derzeit verwendeten**</span><span class="sxs-lookup"><span data-stu-id="06a84-131">**InUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a84-132">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="06a84-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06a84-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06a84-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a84-134">Diese Eigenschaft ist für eine spätere Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="06a84-134">This property is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="06a84-135">**Mininternalsize**</span><span class="sxs-lookup"><span data-stu-id="06a84-135">**MinInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a84-136">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06a84-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06a84-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06a84-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a84-138">Die minimale Größe, auf die die virtuelle Festplatte verkleinert werden kann (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="06a84-138">The minimum size that the virtual hard disk can be shrunk to, in bytes.</span></span> <span data-ttu-id="06a84-139">Diese Größe wird auf das nächstgrößte Vielfache der Sektorgröße aufgerundet.</span><span class="sxs-lookup"><span data-stu-id="06a84-139">This size is rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="06a84-140">**Physicalsector size**</span><span class="sxs-lookup"><span data-stu-id="06a84-140">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a84-141">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06a84-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06a84-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06a84-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a84-143">Die physische Sektorgröße, die vom zugrunde liegenden physischen Datenträger verwendet wird (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="06a84-143">The physical sector size used by the underlying physical disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="06a84-144">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="06a84-144">**Timestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a84-145">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="06a84-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="06a84-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06a84-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a84-147">Der Zeitstempel der virtuellen Festplatte</span><span class="sxs-lookup"><span data-stu-id="06a84-147">The timestamp of the virtual hard disk</span></span>

> [!Note]  
> <span data-ttu-id="06a84-148">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="06a84-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06a84-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06a84-149">Requirements</span></span>



| <span data-ttu-id="06a84-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06a84-150">Requirement</span></span> | <span data-ttu-id="06a84-151">Wert</span><span class="sxs-lookup"><span data-stu-id="06a84-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06a84-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06a84-152">Minimum supported client</span></span><br/> | <span data-ttu-id="06a84-153">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06a84-153">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="06a84-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06a84-154">Minimum supported server</span></span><br/> | <span data-ttu-id="06a84-155">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06a84-155">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06a84-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="06a84-156">Namespace</span></span><br/>                | <span data-ttu-id="06a84-157">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="06a84-157">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="06a84-158">MOF</span><span class="sxs-lookup"><span data-stu-id="06a84-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06a84-159"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="06a84-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06a84-160">DLL</span><span class="sxs-lookup"><span data-stu-id="06a84-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06a84-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06a84-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06a84-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06a84-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a84-163">**Getvirtualharddiskstate**</span><span class="sxs-lookup"><span data-stu-id="06a84-163">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




