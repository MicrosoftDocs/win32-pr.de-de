---
description: Wird in der Methode queryguestclusterinformation in der MSVM \_ VssService-Klasse verwendet, um Informationen über das Gast Cluster abzurufen, zu dem der virtuelle Computer gehört.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Msvm_GuestClusterInformation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347807"
---
# <a name="msvm_guestclusterinformation-class"></a><span data-ttu-id="4d19d-103">MSVM \_ guestclusterinformation-Klasse</span><span class="sxs-lookup"><span data-stu-id="4d19d-103">Msvm\_GuestClusterInformation class</span></span>

<span data-ttu-id="4d19d-104">Wird in der Methode [**queryguestclusterinformation**](msvm-vssservice-queryguestclusterinformation.md) in der [**MSVM \_ VssService**](msvm-vssservice.md) -Klasse verwendet, um Informationen über das Gast Cluster abzurufen, zu dem der virtuelle Computer gehört.</span><span class="sxs-lookup"><span data-stu-id="4d19d-104">Used in the [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) method in the [**Msvm\_VssService**](msvm-vssservice.md) class to retrieve information about the guest cluster the VM is part of.</span></span>

<span data-ttu-id="4d19d-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4d19d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d19d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d19d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a><span data-ttu-id="4d19d-107">Member</span><span class="sxs-lookup"><span data-stu-id="4d19d-107">Members</span></span>

<span data-ttu-id="4d19d-108">Die **MSVM \_ guestclusterinformation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4d19d-108">The **Msvm\_GuestClusterInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="4d19d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d19d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d19d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d19d-110">Properties</span></span>

<span data-ttu-id="4d19d-111">Die **MSVM \_ guestclusterinformation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4d19d-111">The **Msvm\_GuestClusterInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d19d-112">**ClusterId**</span><span class="sxs-lookup"><span data-stu-id="4d19d-112">**ClusterId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d19d-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d19d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d19d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d19d-115">Der Bezeichner des Failoverclusters, zu dem das Gast Betriebssystem der VM gehört.</span><span class="sxs-lookup"><span data-stu-id="4d19d-115">The identifier of the failover cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="4d19d-116">**Cluster size**</span><span class="sxs-lookup"><span data-stu-id="4d19d-116">**ClusterSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d19d-117">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d19d-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d19d-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d19d-119">Die Anzahl der Knoten im Cluster, zu denen das Gast Betriebssystem der VM gehört.</span><span class="sxs-lookup"><span data-stu-id="4d19d-119">Number of nodes in the cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="4d19d-120">**Isactiveactive**</span><span class="sxs-lookup"><span data-stu-id="4d19d-120">**IsActiveActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d19d-121">Datentyp: **Boolesches** Array</span><span class="sxs-lookup"><span data-stu-id="4d19d-121">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d19d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-123">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4d19d-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4d19d-124">Ein Array von booleschen Werten, die jeder freigegebenen virtuellen Festplatte entsprechen und angeben, ob die zugehörige Datenträger Ressource im Gast Cluster von virtuellen Computern im aktiv/aktiv-Modus gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="4d19d-124">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is shared between VMs in active/active mode.</span></span>

</dd> <dt>

<span data-ttu-id="4d19d-125">**IsClustered**</span><span class="sxs-lookup"><span data-stu-id="4d19d-125">**IsClustered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d19d-126">Datentyp: **Boolesches** Array</span><span class="sxs-lookup"><span data-stu-id="4d19d-126">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d19d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-128">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4d19d-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4d19d-129">Ein Array von booleschen Werten, die jeder freigegebenen virtuellen Festplatte entsprechen und angeben, ob es sich bei dem entsprechenden Datenträger um eine Cluster Ressource im Gast Cluster handelt.</span><span class="sxs-lookup"><span data-stu-id="4d19d-129">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk is a cluster resource in the guest cluster.</span></span>

</dd> <dt>

<span data-ttu-id="4d19d-130">**IsOnline**</span><span class="sxs-lookup"><span data-stu-id="4d19d-130">**IsOnline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d19d-131">Datentyp: **Boolesches** Array</span><span class="sxs-lookup"><span data-stu-id="4d19d-131">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d19d-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-133">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4d19d-133">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4d19d-134">Ein Array von booleschen Werten, die jeder freigegebenen virtuellen Festplatte entsprechen und angeben, ob die entsprechende Datenträger Ressource im Gast Cluster online ist.</span><span class="sxs-lookup"><span data-stu-id="4d19d-134">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is online.</span></span>

</dd> <dt>

<span data-ttu-id="4d19d-135">**Isowned**</span><span class="sxs-lookup"><span data-stu-id="4d19d-135">**IsOwned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d19d-136">Datentyp: **Boolesches** Array</span><span class="sxs-lookup"><span data-stu-id="4d19d-136">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d19d-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-138">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4d19d-138">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4d19d-139">Ein Array von booleschen Werten, die jeder freigegebenen virtuellen Festplatte entsprechen und angeben, ob die zugehörige Datenträger Ressource im Gast Cluster im Besitz dieses virtuellen Computers ist.</span><span class="sxs-lookup"><span data-stu-id="4d19d-139">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is currenly owned by this VM.</span></span>

</dd> <dt>

<span data-ttu-id="4d19d-140">**Lastresourcemuvetime**</span><span class="sxs-lookup"><span data-stu-id="4d19d-140">**LastResourceMoveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d19d-141">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4d19d-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d19d-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d19d-143">Die Takt Anzahl, wenn eine der freigegebenen Datenträger Ressourcen zuletzt verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="4d19d-143">The clock tick count when one of the shared disk resources last moved.</span></span>

> [!Note]  
> <span data-ttu-id="4d19d-144">Diese Eigenschaft wurde in Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4d19d-144">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="4d19d-145">**Sharedvirtualharddiskpath**</span><span class="sxs-lookup"><span data-stu-id="4d19d-145">**SharedVirtualHardDiskPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d19d-146">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4d19d-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d19d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-148">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4d19d-148">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4d19d-149">Ein Array von freigegebenen virtuellen Festplatten Pfaden, die mit dem virtuellen Computer verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="4d19d-149">An array of shared virtual hard disk paths connected to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="4d19d-150">**Sharedvirtualharddisks**</span><span class="sxs-lookup"><span data-stu-id="4d19d-150">**SharedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d19d-151">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4d19d-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d19d-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d19d-153">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4d19d-153">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4d19d-154">Ein Array von Ressourcen Zuordnungs Einstellungsdaten (rasd), die die freigegebenen virtuellen Festplatten darstellen, die mit dem virtuellen Computer verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="4d19d-154">An array of Resource Allocation Setting Data (RASD) representing the shared virtual hard disks connected to the VM.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d19d-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d19d-155">Requirements</span></span>



| <span data-ttu-id="4d19d-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d19d-156">Requirement</span></span> | <span data-ttu-id="4d19d-157">Wert</span><span class="sxs-lookup"><span data-stu-id="4d19d-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d19d-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d19d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="4d19d-159">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d19d-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4d19d-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d19d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="4d19d-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4d19d-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4d19d-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d19d-162">Namespace</span></span><br/>                | <span data-ttu-id="4d19d-163">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4d19d-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4d19d-164">MOF</span><span class="sxs-lookup"><span data-stu-id="4d19d-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d19d-165"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4d19d-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d19d-166">DLL</span><span class="sxs-lookup"><span data-stu-id="4d19d-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d19d-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4d19d-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

