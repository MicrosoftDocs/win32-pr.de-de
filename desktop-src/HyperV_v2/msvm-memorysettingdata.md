---
description: Stellt den konfigurierten Zustand des Arbeitsspeichers für einen virtuellen Computer dar.
ms.assetid: 4B6FEE50-1C5F-4F41-B14A-E10B40400A1B
title: Msvm_MemorySettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MemorySettingData
- Msvm_MemorySettingData.InstanceID
- Msvm_MemorySettingData.Caption
- Msvm_MemorySettingData.Description
- Msvm_MemorySettingData.ElementName
- Msvm_MemorySettingData.ResourceType
- Msvm_MemorySettingData.OtherResourceType
- Msvm_MemorySettingData.ResourceSubType
- Msvm_MemorySettingData.PoolID
- Msvm_MemorySettingData.ConsumerVisibility
- Msvm_MemorySettingData.HostResource
- Msvm_MemorySettingData.HugePagesEnabled
- Msvm_MemorySettingData.AllocationUnits
- Msvm_MemorySettingData.VirtualQuantity
- Msvm_MemorySettingData.Reservation
- Msvm_MemorySettingData.Limit
- Msvm_MemorySettingData.Weight
- Msvm_MemorySettingData.AutomaticAllocation
- Msvm_MemorySettingData.AutomaticDeallocation
- Msvm_MemorySettingData.Parent
- Msvm_MemorySettingData.Connection
- Msvm_MemorySettingData.Address
- Msvm_MemorySettingData.MappingBehavior
- Msvm_MemorySettingData.AddressOnParent
- Msvm_MemorySettingData.VirtualQuantityUnits
- Msvm_MemorySettingData.DynamicMemoryEnabled
- Msvm_MemorySettingData.TargetMemoryBuffer
- Msvm_MemorySettingData.IsVirtualized
- Msvm_MemorySettingData.SwapFilesInUse
- Msvm_MemorySettingData.MaxMemoryBlocksPerNumaNode
- Msvm_MemorySettingData.SgxSize
- Msvm_MemorySettingData.SgxEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47309fead7ee45936f34e1e4286ee94437823df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959676"
---
# <a name="msvm_memorysettingdata-class"></a><span data-ttu-id="ef871-103">MSVM \_ memorysettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="ef871-103">Msvm\_MemorySettingData class</span></span>

<span data-ttu-id="ef871-104">Stellt den konfigurierten Zustand des Arbeitsspeichers für einen virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="ef871-104">Represents the configured state of the memory for a virtual machine.</span></span>

<span data-ttu-id="ef871-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ef871-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef871-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef871-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MemorySettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Memory Default Settings";
  string  Description = "Describes the default settings for the memory resources.";
  string  ElementName;
  uint16  ResourceType = 4;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Memory";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  boolean HugePagesEnabled;
  string  AllocationUnits = "byte * 2^20";
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "byte * 2^20";
  boolean DynamicMemoryEnabled;
  uint32  TargetMemoryBuffer;
  boolean IsVirtualized = True;
  boolean SwapFilesInUse;
  uint64  MaxMemoryBlocksPerNumaNode;
  uint64  SgxSize;
  boolean SgxEnabled;
};
```

## <a name="members"></a><span data-ttu-id="ef871-107">Member</span><span class="sxs-lookup"><span data-stu-id="ef871-107">Members</span></span>

<span data-ttu-id="ef871-108">Die **MSVM \_ memorysettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ef871-108">The **Msvm\_MemorySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ef871-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef871-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef871-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef871-110">Properties</span></span>

<span data-ttu-id="ef871-111">Die **MSVM \_ memorysettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ef871-111">The **Msvm\_MemorySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef871-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="ef871-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef871-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-115">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ef871-115">The address of the resource.</span></span> <span data-ttu-id="ef871-116">Beispielsweise die Mac-Adresse eines Ethernet-Ports.</span><span class="sxs-lookup"><span data-stu-id="ef871-116">For example, the MAC address of an Ethernet port.</span></span> <span data-ttu-id="ef871-117">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-118">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="ef871-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef871-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-121">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="ef871-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="ef871-122">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ef871-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="ef871-123">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-124">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="ef871-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef871-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-127">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef871-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="ef871-128">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-129">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="ef871-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-130">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef871-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-132">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ef871-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="ef871-133">Wenn diese Eigenschaft beispielsweise auf " **true** " festgelegt ist und der verarbeitende virtuelle Computer eingeschaltet ist, wird diese Ressource zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ef871-133">For example, when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="ef871-134">Der Wert **false** gibt an, dass die Ressource explizit zugewiesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="ef871-134">A value of **False** indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="ef871-135">Die Einstellung kann z. b. ein Wechselmedium (z. b. eine CD-ROM oder eine Diskette) darstellen, bei dem das Medium beim Start nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ef871-135">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="ef871-136">Ein expliziter Vorgang ist erforderlich, um die Ressource zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="ef871-136">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="ef871-137">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-138">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="ef871-138">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-139">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef871-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-141">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ef871-141">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="ef871-142">Wenn diese Eigenschaft beispielsweise auf " **true** " festgelegt ist und der verarbeitende virtuelle Computer eingeschaltet ist, wird diese Ressource zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ef871-142">For example when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="ef871-143">Wenn diese Eigenschaft **false** ist, muss die Ressource explizit zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="ef871-143">When this property is **False**, the resource must be explicitly allocated.</span></span> <span data-ttu-id="ef871-144">Die Einstellung kann z. b. ein Wechselmedium (z. b. eine CD-ROM oder eine Diskette) darstellen, bei dem das Medium beim Start nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ef871-144">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="ef871-145">Ein expliziter Vorgang ist erforderlich, um die Ressource zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="ef871-145">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="ef871-146">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-147">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ef871-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef871-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef871-150">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="ef871-150">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ef871-151">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef871-151">A short description of the object.</span></span> <span data-ttu-id="ef871-152">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-153">**Connection**</span><span class="sxs-lookup"><span data-stu-id="ef871-153">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-154">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ef871-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef871-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-156">Das Gerät, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ef871-156">The device to which this resource is connected.</span></span> <span data-ttu-id="ef871-157">Beispielsweise ein benanntes Netzwerk oder ein Switchport.</span><span class="sxs-lookup"><span data-stu-id="ef871-157">For example, a named network or switch port.</span></span> <span data-ttu-id="ef871-158">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-158">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-159">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="ef871-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-160">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef871-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-162">Beschreibt die Benutzer Sichtbarkeit der zugeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="ef871-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="ef871-163">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-164">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef871-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef871-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-167">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef871-167">A description of the object.</span></span> <span data-ttu-id="ef871-168">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-169">**DynamicMemoryEnabled**</span><span class="sxs-lookup"><span data-stu-id="ef871-169">**DynamicMemoryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-170">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef871-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-172">Gibt an, ob dynamischer Arbeitsspeicher für den virtuellen Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ef871-172">Indicates whether dynamic memory is enabled for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ef871-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ef871-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef871-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-176">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ef871-176">A display name for the object.</span></span> <span data-ttu-id="ef871-177">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-178">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="ef871-178">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-179">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ef871-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef871-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-181">Das erste Element dieses Arrays enthält einen Verweis auf die zugrunde liegende Host Ressource, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef871-181">The first element of this array contains a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="ef871-182">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef871-182">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but it is not used.</span></span>

</dd> <dt>
  
<span data-ttu-id="ef871-183">**HugePagesEnabled**</span><span class="sxs-lookup"><span data-stu-id="ef871-183">**HugePagesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-184">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef871-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-186">Gibt an, ob der Arbeitsspeicher durch 1-GB-Seiten unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ef871-186">Whether the memory is backed by 1GB pages or not.</span></span>

</dd> <dt>

<span data-ttu-id="ef871-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ef871-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef871-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef871-190">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="ef871-190">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ef871-191">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ef871-191">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ef871-192">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-193">**Isvirtualisiert**</span><span class="sxs-lookup"><span data-stu-id="ef871-193">**IsVirtualized**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-194">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef871-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-196">Gibt an, ob dieses Gerät virtualisiert oder durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="ef871-196">Indicates whether this device is virtualized or passed through.</span></span> <span data-ttu-id="ef871-197">Wenn **false** festgelegt ist, wird die zugrunde liegende-oder-Host Ressource verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef871-197">When set to **False**, the underlying or host resource is used.</span></span> <span data-ttu-id="ef871-198">In **der Eigenschaft** "Eigenschaft" sollte mindestens ein Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ef871-198">At least one item should be present in the **DeviceID** property.</span></span> <span data-ttu-id="ef871-199">Wenn diese Einstellung auf " **true**" festgelegt ist, wird die Ressource virtualisiert und darf einer zugrunde liegenden/Host Ressource nicht direkt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ef871-199">When set to **True**, the resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="ef871-200">Einige Implementierungen unterstützen möglicherweise eine bestimmte Zuweisung für virtualisierte Ressourcen. in diesem Fall werden die Host Ressourcen mithilfe der **DeviceID** -Eigenschaft verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="ef871-200">Some implementations may support specific assignment for virtualized resources, in which case the host resources are exposed by using the **DeviceID** property.</span></span> <span data-ttu-id="ef871-201">Diese Eigenschaft ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ef871-201">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="ef871-202">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="ef871-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-203">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ef871-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-205">Die maximale Arbeitsspeicher Menge, die vom virtuellen Computer genutzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef871-205">The maximum amount of memory that may be consumed by the virtual machine.</span></span> <span data-ttu-id="ef871-206">Für einen virtuellen Computer mit aktiviertem dynamischen Arbeitsspeicher ist dies die maximale Arbeitsspeicher Einstellung.</span><span class="sxs-lookup"><span data-stu-id="ef871-206">For a virtual machine with dynamic memory enabled, this represents the maximum memory setting.</span></span> <span data-ttu-id="ef871-207">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-208">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="ef871-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-209">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef871-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-211">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="ef871-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="ef871-212">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-213">**Maxmemoryblockspernumanode**</span><span class="sxs-lookup"><span data-stu-id="ef871-213">**MaxMemoryBlocksPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-214">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ef871-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-216">Die maximale Arbeitsspeicher Menge, die innerhalb des virtuellen Computers beobachtet werden kann, wenn er zu einem einzelnen NUMA-Knoten gehört.</span><span class="sxs-lookup"><span data-stu-id="ef871-216">The maximum amount of memory that can be observed within the virtual machine as belonging to a single NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="ef871-217">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="ef871-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-218">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef871-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-220">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** den Wert "Other" hat.</span><span class="sxs-lookup"><span data-stu-id="ef871-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="ef871-221">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-222">**Parent**</span><span class="sxs-lookup"><span data-stu-id="ef871-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef871-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-225">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ef871-225">The parent of the resource.</span></span> <span data-ttu-id="ef871-226">Beispielsweise ein Controller für die aktuelle Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="ef871-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="ef871-227">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-228">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="ef871-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-229">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef871-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-231">Der Bezeichner des Ressourcenpools, von dem diese Ressource zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="ef871-231">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="ef871-232">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-233">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="ef871-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-234">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ef871-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-236">Gibt den Umfang des Arbeitsspeichers an, der für diesen virtuellen Computer garantiert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ef871-236">Specifies the amount of memory guaranteed to be available for this virtual machine.</span></span> <span data-ttu-id="ef871-237">Bei einem virtuellen Computer mit aktiviertem dynamischen Arbeitsspeicher stellt dies die Einstellung für den minimalen Arbeitsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="ef871-237">For a virtual machine with dynamic memory enabled, this represents the minimum memory setting.</span></span> <span data-ttu-id="ef871-238">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-239">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="ef871-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef871-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-242">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ef871-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="ef871-243">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ef871-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="ef871-244">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="ef871-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-246">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef871-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-248">Der Ressourcentyp, den diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ef871-248">The type of resource that this allocation setting represents.</span></span> <span data-ttu-id="ef871-249">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 4 (Arbeitsspeicher) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ef871-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 4 (Memory).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-250">**Sgxfähig**</span><span class="sxs-lookup"><span data-stu-id="ef871-250">**SgxEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-251">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef871-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-253">Gibt an, ob SGX aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ef871-253">Indicates if SGX is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="ef871-254">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ef871-254">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="ef871-255">**Sgxsize**</span><span class="sxs-lookup"><span data-stu-id="ef871-255">**SgxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-256">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ef871-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-258">Die Menge des für die VM zuzuordnenden SGX-Speichers in MB.</span><span class="sxs-lookup"><span data-stu-id="ef871-258">The amount of SGX memory to allocate for the VM, in MB.</span></span>

> [!Note]  
> <span data-ttu-id="ef871-259">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ef871-259">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="ef871-260">**Austauschen von Dateien**</span><span class="sxs-lookup"><span data-stu-id="ef871-260">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-261">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef871-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-263">**True** , wenn das Paging auf zweiter Ebene aktiv ist; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="ef871-263">**True** if second level paging is active; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="ef871-264">**Targetmemorybuffer**</span><span class="sxs-lookup"><span data-stu-id="ef871-264">**TargetMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-265">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef871-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-267">Definiert den zusätzlichen Arbeitsspeicher, der für einen virtuellen Computer zur Laufzeit reserviert werden soll, als Prozentsatz des gesamten Arbeitsspeichers, den der virtuelle Computer benötigt.</span><span class="sxs-lookup"><span data-stu-id="ef871-267">Defines the amount of extra memory that should be reserved for a virtual machine at runtime, as a percentage of the total memory that the virtual machine is thought to need.</span></span> <span data-ttu-id="ef871-268">Dies gilt nur für virtuelle Computer, auf denen dynamischer Arbeitsspeicher aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ef871-268">This only applies to virtual machines with dynamic memory enabled.</span></span>

<span data-ttu-id="ef871-269">Diese Eigenschaft kann im Bereich von 5 bis 2000 liegen.</span><span class="sxs-lookup"><span data-stu-id="ef871-269">This property can be in the range of 5 to 2000.</span></span>

</dd> <dt>

<span data-ttu-id="ef871-270">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="ef871-270">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-271">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ef871-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-273">Die Gesamtgröße des Arbeitsspeichers auf dem virtuellen Computer, wie vom Gast Betriebssystem angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ef871-273">The total amount of RAM in the virtual machine, as seen by the guest operating system.</span></span> <span data-ttu-id="ef871-274">Bei einem virtuellen Computer mit aktiviertem dynamischen Arbeitsspeicher stellt dies den anfänglichen Arbeitsspeicher dar, der beim Start verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ef871-274">For a virtual machine with dynamic memory enabled, this represents the initial memory available at startup.</span></span> <span data-ttu-id="ef871-275">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-276">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="ef871-276">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-277">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef871-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-279">Gibt die Maßeinheit für diese Ressourcenzuweisung an.</span><span class="sxs-lookup"><span data-stu-id="ef871-279">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="ef871-280">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="ef871-280">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="ef871-281">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef871-282">**Weight**</span><span class="sxs-lookup"><span data-stu-id="ef871-282">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef871-283">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef871-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef871-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef871-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef871-285">Definiert den Wert für die Speicher Belegungs Gewichtung für jeden virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ef871-285">Defines the memory allocation weighting value for each virtual machine.</span></span> <span data-ttu-id="ef871-286">Nachdem alle Reserven erreicht wurden, wird der verbleibende Arbeitsspeicher der Hostingplattform virtuellen Computern basierend auf ihren relativen Gewichtungen zugewiesen (sodass der von der Eigenschaft **Limit** angegebene Wert nicht überschritten wird).</span><span class="sxs-lookup"><span data-stu-id="ef871-286">After all reserves have been met, the remaining memory of the hosting platform will be allocated to virtual machines based on their relative weights (not to exceed the value specified by the **Limit** property).</span></span> <span data-ttu-id="ef871-287">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef871-287">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef871-288">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef871-288">Remarks</span></span>

<span data-ttu-id="ef871-289">Der Zugriff auf die **MSVM \_ memorysettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="ef871-289">Access to the **Msvm\_MemorySettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ef871-290">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ef871-290">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ef871-291">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef871-291">Examples</span></span>

```powershell
function WaitForResult
{
  param($result)
  if ($result.ReturnValue -eq 4096)
  {
    while($true)
    {
      $result.Job
      if ($result.Job -ne $null)
      {
        if ($result.Job.JobState -gt 4)
        {
          return $result.Job.ErrorCode
        }
      }
      start-sleep 1
    }
  }
  else
  {
    return $result.ReturnValue
  }
}

if ($($args.count) -ne 2)
{
  Write-Host "EnableHugePages.ps1 VMName SizeInMB"
  return
}

$vmName = $args[0]
$sizeInMB = $args[1]
 
$namespace = "root\virtualization\v2"
$vm = Get-WmiObject -class MSVM_ComputerSystem -filter "ElementName='$vmName'" -namespace $namespace
$settings = Get-WmiObject -query "Associators of {$vm} where ResultClass = Msvm_VirtualSystemSettingData" -namespace $namespace
$vmSettings = $settings | ? VirtualSystemType -eq "Microsoft:Hyper-V:System:Realized"
$memorySettings = Get-WmiObject -query "Associators of {$vmSettings} where ResultClass = Msvm_MemorySettingData" -namespace $namespace

$memorySettings.MaxMemoryBlocksPerNumaNode = $sizeInMB
$memorySettings.Reservation = $sizeInMB
$memorySettings.Limit = $sizeInMB
$memorySettings.VirtualQuantity = $sizeInMB
$memorySettings.HugePagesEnabled = $True

$vmSvc = Get-WmiObject -class Msvm_VirtualSystemManagementService -namespace $namespace
$res = $vmSvc.ModifyResourceSettings($memorySettings.GetText(2))
if (WaitForResult($res) -ne 0)
{
  Write-Host "Failed."
}
```

## <a name="requirements"></a><span data-ttu-id="ef871-292">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef871-292">Requirements</span></span>



| <span data-ttu-id="ef871-293">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef871-293">Requirement</span></span> | <span data-ttu-id="ef871-294">Wert</span><span class="sxs-lookup"><span data-stu-id="ef871-294">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef871-295">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef871-295">Minimum supported client</span></span><br/> | <span data-ttu-id="ef871-296">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef871-296">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ef871-297">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef871-297">Minimum supported server</span></span><br/> | <span data-ttu-id="ef871-298">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef871-298">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef871-299">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef871-299">Namespace</span></span><br/>                | <span data-ttu-id="ef871-300">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ef871-300">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ef871-301">MOF</span><span class="sxs-lookup"><span data-stu-id="ef871-301">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef871-302"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ef871-302"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef871-303">DLL</span><span class="sxs-lookup"><span data-stu-id="ef871-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef871-304"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef871-304"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef871-305">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef871-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef871-306">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="ef871-306">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="ef871-307">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="ef871-307">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="ef871-308">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="ef871-308">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

