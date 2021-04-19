---
description: Stellt die Einstellungen des virtuellen Prozessors für eine virtuelle Maschine dar.
ms.assetid: 2B299793-E1CD-49D4-898C-AE60B49F44F5
title: Msvm_ProcessorSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorSettingData
- Msvm_ProcessorSettingData.InstanceID
- Msvm_ProcessorSettingData.Caption
- Msvm_ProcessorSettingData.Description
- Msvm_ProcessorSettingData.ElementName
- Msvm_ProcessorSettingData.ResourceType
- Msvm_ProcessorSettingData.OtherResourceType
- Msvm_ProcessorSettingData.ResourceSubType
- Msvm_ProcessorSettingData.PoolID
- Msvm_ProcessorSettingData.ConsumerVisibility
- Msvm_ProcessorSettingData.HostResource
- Msvm_ProcessorSettingData.AllocationUnits
- Msvm_ProcessorSettingData.VirtualQuantity
- Msvm_ProcessorSettingData.Reservation
- Msvm_ProcessorSettingData.Limit
- Msvm_ProcessorSettingData.Weight
- Msvm_ProcessorSettingData.AutomaticAllocation
- Msvm_ProcessorSettingData.AutomaticDeallocation
- Msvm_ProcessorSettingData.Parent
- Msvm_ProcessorSettingData.Connection
- Msvm_ProcessorSettingData.Address
- Msvm_ProcessorSettingData.MappingBehavior
- Msvm_ProcessorSettingData.AddressOnParent
- Msvm_ProcessorSettingData.VirtualQuantityUnits
- Msvm_ProcessorSettingData.LimitCPUID
- Msvm_ProcessorSettingData.HwThreadsPerCore
- Msvm_ProcessorSettingData.LimitProcessorFeatures
- Msvm_ProcessorSettingData.MaxProcessorsPerNumaNode
- Msvm_ProcessorSettingData.MaxNumaNodesPerSocket
- Msvm_ProcessorSettingData.EnableHostResourceProtection
- Msvm_ProcessorSettingData.CpuGroupId
- Msvm_ProcessorSettingData.HideHypervisorPresent
- Msvm_ProcessorSettingData.ExposeVirtualizationExtensions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5154105c4deab13f93bb65078a5c9527283620e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367976"
---
# <a name="msvm_processorsettingdata-class"></a><span data-ttu-id="26363-103">MSVM \_ processorsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="26363-103">Msvm\_ProcessorSettingData class</span></span>

<span data-ttu-id="26363-104">Stellt die Einstellungen des virtuellen Prozessors für eine virtuelle Maschine dar.</span><span class="sxs-lookup"><span data-stu-id="26363-104">Represents the virtual processor settings for a virtual machine.</span></span>

<span data-ttu-id="26363-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="26363-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26363-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="26363-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Processor";
  string  Description = "A logical processor of the hypervisor running on the host computer system.";
  string  ElementName;
  uint16  ResourceType = 3;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Processor";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits = "percent / 1000";
  uint64  VirtualQuantity = "count";
  uint64  Reservation = 0;
  uint64  Limit = 100000;
  uint32  Weight = 100;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  boolean LimitCPUID;
  uint64  HwThreadsPerCore;
  boolean LimitProcessorFeatures;
  uint64  MaxProcessorsPerNumaNode;
  uint64  MaxNumaNodesPerSocket;
  boolean EnableHostResourceProtection;
  string  CpuGroupId;
  boolean HideHypervisorPresent;
  boolean ExposeVirtualizationExtensions;
};
```

## <a name="members"></a><span data-ttu-id="26363-107">Member</span><span class="sxs-lookup"><span data-stu-id="26363-107">Members</span></span>

<span data-ttu-id="26363-108">Die **MSVM \_ processorsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="26363-108">The **Msvm\_ProcessorSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="26363-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26363-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26363-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26363-110">Properties</span></span>

<span data-ttu-id="26363-111">Die **MSVM \_ processorsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="26363-111">The **Msvm\_ProcessorSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26363-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="26363-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-115">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="26363-115">The address of the resource.</span></span> <span data-ttu-id="26363-116">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-117">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="26363-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-120">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="26363-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="26363-121">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="26363-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="26363-122">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-123">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="26363-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-126">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26363-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="26363-127">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-128">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="26363-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="26363-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26363-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-131">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="26363-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="26363-132">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-133">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="26363-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="26363-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26363-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-136">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="26363-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="26363-137">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="26363-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26363-141">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="26363-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="26363-142">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="26363-142">A short description of the object.</span></span> <span data-ttu-id="26363-143">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="26363-144">**Connection**</span><span class="sxs-lookup"><span data-stu-id="26363-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-145">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="26363-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="26363-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-147">Das Gerät, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="26363-147">The device to which this resource is connected.</span></span> <span data-ttu-id="26363-148">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-149">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="26363-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-150">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26363-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26363-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-152">Beschreibt die Sichtbarkeit der Consumer der zugeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="26363-152">Describes the consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="26363-153">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-154">**Cpugroupid**</span><span class="sxs-lookup"><span data-stu-id="26363-154">**CpuGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-157">Die CPU-Gruppen-ID, an die diese VM gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="26363-157">The Cpu Group Id this VM is bound to.</span></span> <span data-ttu-id="26363-158">Wenn der Wert 0 ist, bedeutet dies, dass er nicht an eine bestimmte CPU-Gruppe gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="26363-158">When value is 0 it means is not bound to a specific CPU group.</span></span>

> [!Note]  
> <span data-ttu-id="26363-159">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="26363-159">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="26363-160">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26363-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-163">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="26363-163">A description of the object.</span></span> <span data-ttu-id="26363-164">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="26363-165">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="26363-165">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-168">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="26363-168">A display name for the object.</span></span> <span data-ttu-id="26363-169">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-169">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="26363-170">Durch Ändern dieser Eigenschaft wird der **ElementName** der zugeordneten logischen Geräte Ableitung geändert.</span><span class="sxs-lookup"><span data-stu-id="26363-170">Changing this property will change the **ElementName** of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="26363-171">**Enablehustresourceprotection**</span><span class="sxs-lookup"><span data-stu-id="26363-171">**EnableHostResourceProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-172">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="26363-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26363-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-174">Gibt an, ob die VM Features aktivieren soll, mit denen der Schutz von Host Ressourcen von der Arbeitsauslastung auf dem virtuellen Computer erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="26363-174">Indicates whether the VM should enable features that increase the protection of host resources from workload running in the VM.</span></span>

> [!Note]  
> <span data-ttu-id="26363-175">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="26363-175">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="26363-176">**Expoabvirtualizationextensions**</span><span class="sxs-lookup"><span data-stu-id="26363-176">**ExposeVirtualizationExtensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-177">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="26363-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26363-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-179">Gibt an, ob Hyper-V virtualisierte hardwarevirtualisierungserweiterungen für die VM verfügbar machen soll.</span><span class="sxs-lookup"><span data-stu-id="26363-179">Indicates whether Hyper-V should expose virtualized hardware virtualization extensions to the VM.</span></span>

> [!Note]  
> <span data-ttu-id="26363-180">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="26363-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="26363-181">**Hidehypervisorpresent**</span><span class="sxs-lookup"><span data-stu-id="26363-181">**HideHypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-182">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="26363-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26363-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-184">Gibt an, ob Hyper-V angeben soll, dass ein Hypervisor für den verbundenen Gast vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="26363-184">Indicates whether Hyper-V should report that a hypervisor is present to the nested guest.</span></span>

> [!Note]  
> <span data-ttu-id="26363-185">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="26363-185">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="26363-186">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="26363-186">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-187">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="26363-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="26363-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-189">Macht eine bestimmte Zuweisung zum Hosten von oder zugrunde liegenden Ressourcen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26363-189">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="26363-190">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="26363-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="26363-191">**Hwthreadspercore**</span><span class="sxs-lookup"><span data-stu-id="26363-191">**HwThreadsPerCore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-192">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26363-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26363-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-194">Gibt die Anzahl der SMT-Threads pro Kern an, die dem Gast gemeldet wurden.</span><span class="sxs-lookup"><span data-stu-id="26363-194">Indicates the number of SMT threads per core reported to the guest.</span></span> <span data-ttu-id="26363-195">Diese Berichterstellung ist unabhängig davon, ob die Hardware für SMT vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="26363-195">This reporting is independent of whether the hardware for SMT is present.</span></span>

> [!Note]  
> <span data-ttu-id="26363-196">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="26363-196">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="26363-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="26363-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26363-200">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="26363-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="26363-201">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="26363-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="26363-202">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="26363-203">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="26363-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-204">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26363-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26363-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-206">Die maximale Menge an CPU-Ressourcen, die vom virtuellen Computer genutzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="26363-206">The maximum amount of CPU resources that may be consumed by the virtual machine.</span></span> <span data-ttu-id="26363-207">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="26363-208">100.000</span><span class="sxs-lookup"><span data-stu-id="26363-208">100000</span></span>

<span data-ttu-id="26363-209">Bereich: 0 100000</span><span class="sxs-lookup"><span data-stu-id="26363-209">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="26363-210">**Limitcpuid**</span><span class="sxs-lookup"><span data-stu-id="26363-210">**LimitCPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-211">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="26363-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26363-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-213">Gibt an, ob der virtuelle Computer den CPU-Bezeichner verringern soll.</span><span class="sxs-lookup"><span data-stu-id="26363-213">Indicates whether the virtual machine should lower the CPU identifier.</span></span> <span data-ttu-id="26363-214">Bei einigen älteren Betriebssystemen ist es möglicherweise erforderlich, die Prozessor Funktionalität auf diese Weise zu begrenzen, damit Sie ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="26363-214">Some older operating systems may require you to limit processor functionality in this way in order to run.</span></span>

</dd> <dt>

<span data-ttu-id="26363-215">**Limitprocessorfeatures**</span><span class="sxs-lookup"><span data-stu-id="26363-215">**LimitProcessorFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-216">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="26363-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26363-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-218">Gibt an, ob der virtuelle Computer die für das Betriebssystem verfügbar gemachten CPU-Features einschränken soll.</span><span class="sxs-lookup"><span data-stu-id="26363-218">Indicates whether the virtual machine should limit the CPU features exposed to the operating system.</span></span> <span data-ttu-id="26363-219">Durch das Einschränken der Prozessor Features kann der virtuelle Computer auf unterschiedliche Host Computersysteme mit unterschiedlichen Prozessoren migriert werden.</span><span class="sxs-lookup"><span data-stu-id="26363-219">Limiting the processor features enables the virtual machine to be migrated to different host computer systems with different processors.</span></span> <span data-ttu-id="26363-220">Das Migrieren virtueller Maschinen zwischen Computern mit Prozessoren von unterschiedlichen Anbietern wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="26363-220">Migrating virtual machines between computers with processors from different vendors is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="26363-221">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="26363-221">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-222">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26363-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26363-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-224">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="26363-224">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="26363-225">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-226">**Maxnumanodespersocket**</span><span class="sxs-lookup"><span data-stu-id="26363-226">**MaxNumaNodesPerSocket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-227">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26363-227">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26363-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-229">Die maximale Anzahl von NUMA-Knoten, die innerhalb des virtuellen Computers beobachtet werden können, wenn er zu einem einzelnen Prozessor Socket gehört.</span><span class="sxs-lookup"><span data-stu-id="26363-229">The maximum number of NUMA nodes that can be observed within the virtual machine as belonging to a single processor socket.</span></span>

</dd> <dt>

<span data-ttu-id="26363-230">**Maxprocessorspernumanode**</span><span class="sxs-lookup"><span data-stu-id="26363-230">**MaxProcessorsPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-231">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26363-231">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26363-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-233">Die maximale Anzahl virtueller Prozessoren, die innerhalb des virtuellen Computers beobachtet werden können, wenn Sie zu einem einzelnen virtuellen NUMA-Knoten gehören.</span><span class="sxs-lookup"><span data-stu-id="26363-233">The maximum number of virtual processors that can be observed within the virtual machine as belonging to a single virtual NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="26363-234">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="26363-234">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-235">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-237">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="26363-237">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="26363-238">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-239">**Parent**</span><span class="sxs-lookup"><span data-stu-id="26363-239">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-242">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="26363-242">The parent of the resource.</span></span> <span data-ttu-id="26363-243">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-244">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="26363-244">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-245">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-247">Der Bezeichner des Ressourcenpools, von dem diese Ressource zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="26363-247">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="26363-248">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-249">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="26363-249">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-250">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26363-250">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26363-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-252">Die Menge der CPU-Ressourcen, die für die Verwendung durch den virtuellen Computer reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="26363-252">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="26363-253">Diese Ressourcen sind garantiert für den Verbrauch durch den virtuellen Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26363-253">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="26363-254">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="26363-255">0</span><span class="sxs-lookup"><span data-stu-id="26363-255">0</span></span>

<span data-ttu-id="26363-256">Bereich: 0 100000</span><span class="sxs-lookup"><span data-stu-id="26363-256">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="26363-257">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="26363-257">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-260">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="26363-260">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="26363-261">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="26363-261">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="26363-262">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-263">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="26363-263">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-264">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26363-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26363-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-266">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="26363-266">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="26363-267">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="26363-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-269">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26363-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26363-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-271">Die Gesamtanzahl der Kerne auf dem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="26363-271">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="26363-272">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-273">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="26363-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-274">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="26363-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26363-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-276">Gibt die Maßeinheit für diese Ressourcenzuweisung an.</span><span class="sxs-lookup"><span data-stu-id="26363-276">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="26363-277">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="26363-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="26363-278">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="26363-279">**Weight**</span><span class="sxs-lookup"><span data-stu-id="26363-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26363-280">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26363-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26363-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26363-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26363-282">Die Gewichtung für jeden Prozessor der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="26363-282">The weight for each virtual machine processor.</span></span> <span data-ttu-id="26363-283">Nachdem alle Reserven erfüllt wurden, wird die verbleibende physische Prozessor Kapazität der Hostingplattform virtuellen Computern basierend auf ihren relativen Gewichtungen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="26363-283">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="26363-284">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="26363-284">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="26363-285">100</span><span class="sxs-lookup"><span data-stu-id="26363-285">100</span></span>

<span data-ttu-id="26363-286">Bereich: 0 10000</span><span class="sxs-lookup"><span data-stu-id="26363-286">Range: 0 10000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26363-287">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26363-287">Remarks</span></span>

<span data-ttu-id="26363-288">Der Zugriff auf die **MSVM \_ processorsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="26363-288">Access to the **Msvm\_ProcessorSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="26363-289">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="26363-289">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="26363-290">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26363-290">Requirements</span></span>



| <span data-ttu-id="26363-291">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26363-291">Requirement</span></span> | <span data-ttu-id="26363-292">Wert</span><span class="sxs-lookup"><span data-stu-id="26363-292">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26363-293">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26363-293">Minimum supported client</span></span><br/> | <span data-ttu-id="26363-294">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26363-294">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="26363-295">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26363-295">Minimum supported server</span></span><br/> | <span data-ttu-id="26363-296">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26363-296">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26363-297">Namespace</span><span class="sxs-lookup"><span data-stu-id="26363-297">Namespace</span></span><br/>                | <span data-ttu-id="26363-298">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="26363-298">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="26363-299">MOF</span><span class="sxs-lookup"><span data-stu-id="26363-299">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26363-300"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="26363-300"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="26363-301">DLL</span><span class="sxs-lookup"><span data-stu-id="26363-301">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26363-302"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="26363-302"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="26363-303">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26363-303">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26363-304">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="26363-304">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="26363-305">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="26363-305">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="26363-306">Prozessor Klassen</span><span class="sxs-lookup"><span data-stu-id="26363-306">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

