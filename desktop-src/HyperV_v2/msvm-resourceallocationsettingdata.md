---
description: Stellt die aktuellen und aufgezeichneten Zuordnungs Zustände einer virtuellen Ressource dar.
ms.assetid: 5C180933-2013-4E16-A9BD-653D5426F468
title: Msvm_ResourceAllocationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationSettingData
- Msvm_ResourceAllocationSettingData.InstanceID
- Msvm_ResourceAllocationSettingData.Caption
- Msvm_ResourceAllocationSettingData.Description
- Msvm_ResourceAllocationSettingData.ElementName
- Msvm_ResourceAllocationSettingData.ResourceType
- Msvm_ResourceAllocationSettingData.OtherResourceType
- Msvm_ResourceAllocationSettingData.ResourceSubType
- Msvm_ResourceAllocationSettingData.PoolID
- Msvm_ResourceAllocationSettingData.ConsumerVisibility
- Msvm_ResourceAllocationSettingData.HostResource
- Msvm_ResourceAllocationSettingData.AllocationUnits
- Msvm_ResourceAllocationSettingData.VirtualQuantity
- Msvm_ResourceAllocationSettingData.Reservation
- Msvm_ResourceAllocationSettingData.Limit
- Msvm_ResourceAllocationSettingData.Weight
- Msvm_ResourceAllocationSettingData.AutomaticAllocation
- Msvm_ResourceAllocationSettingData.AutomaticDeallocation
- Msvm_ResourceAllocationSettingData.Parent
- Msvm_ResourceAllocationSettingData.Connection
- Msvm_ResourceAllocationSettingData.Address
- Msvm_ResourceAllocationSettingData.MappingBehavior
- Msvm_ResourceAllocationSettingData.AddressOnParent
- Msvm_ResourceAllocationSettingData.VirtualQuantityUnits
- Msvm_ResourceAllocationSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6d1cb2f97dcb3fa144db5cf27c1a82690214b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346049"
---
# <a name="msvm_resourceallocationsettingdata-class"></a><span data-ttu-id="533f4-103">MSVM \_ resourcezucationsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="533f4-103">Msvm\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="533f4-104">Stellt die aktuellen und aufgezeichneten Zuordnungs Zustände einer virtuellen Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="533f4-104">Represents the current and recorded allocation states of a virtual resource.</span></span>

<span data-ttu-id="533f4-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="533f4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="533f4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="533f4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption;
  string  Description;
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  string  VirtualSystemIdentifiers[] = { "GUID" };
};
```

## <a name="members"></a><span data-ttu-id="533f4-107">Member</span><span class="sxs-lookup"><span data-stu-id="533f4-107">Members</span></span>

<span data-ttu-id="533f4-108">Die **MSVM \_ resourcezucationsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="533f4-108">The **Msvm\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="533f4-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="533f4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="533f4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="533f4-110">Properties</span></span>

<span data-ttu-id="533f4-111">Die **MSVM \_ resourcezucationsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="533f4-111">The **Msvm\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="533f4-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="533f4-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="533f4-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-115">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="533f4-115">The address of the resource.</span></span> <span data-ttu-id="533f4-116">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="533f4-117">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, wenn die **ResourceType** -Eigenschaft jedoch 20 (Grafikcontroller) ist, kann Sie mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden.</span><span class="sxs-lookup"><span data-stu-id="533f4-117">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="533f4-118">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="533f4-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="533f4-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-121">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="533f4-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="533f4-122">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="533f4-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="533f4-123">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-124">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="533f4-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="533f4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-127">Die Zuordnungs Einheit, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="533f4-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="533f4-128">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-129">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="533f4-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-130">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="533f4-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-132">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="533f4-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="533f4-133">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-134">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="533f4-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-135">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="533f4-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-137">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="533f4-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="533f4-138">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="533f4-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="533f4-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="533f4-142">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="533f4-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="533f4-143">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="533f4-143">A short description of the object.</span></span> <span data-ttu-id="533f4-144">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-145">**Connection**</span><span class="sxs-lookup"><span data-stu-id="533f4-145">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-146">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="533f4-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="533f4-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-148">Das Gerät, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="533f4-148">The device to which this resource is connected.</span></span> <span data-ttu-id="533f4-149">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-149">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="533f4-150">Dies ist eine schreibgeschützte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="533f4-150">This is a read-only property.</span></span> <span data-ttu-id="533f4-151">Wenn die **ResourceType** -Eigenschaft jedoch 21 (Serial Port) und die **resourcesubtype** -Eigenschaft "Microsoft: Hyper-V: Serial Port" ist, kann die **Connection** -Eigenschaft mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden.</span><span class="sxs-lookup"><span data-stu-id="533f4-151">But if the **ResourceType** property is 21 (Serial port) and the **ResourceSubType** property is "Microsoft:Hyper-V:Serial Port", the **Connection** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="533f4-152">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="533f4-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-153">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="533f4-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-155">Die Sichtbarkeit des Consumers für die zugeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="533f4-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="533f4-156">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-157">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="533f4-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="533f4-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-160">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="533f4-160">A description of the object.</span></span> <span data-ttu-id="533f4-161">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="533f4-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="533f4-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-165">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="533f4-165">A display name for the object.</span></span> <span data-ttu-id="533f4-166">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="533f4-167">Durch Ändern dieser Eigenschaft wird der Elementname der zugeordneten logischen Geräte Ableitung geändert.</span><span class="sxs-lookup"><span data-stu-id="533f4-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="533f4-168">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="533f4-168">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="533f4-169">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="533f4-169">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-170">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="533f4-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="533f4-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-172">Jedem Gerät auf dem virtuellen Computer kann nur eine Host Ressource zugewiesen werden, sodass nur das erste Element dieses Arrays festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="533f4-172">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="533f4-173">Legen Sie für Geräte, die diese Funktion unterstützen, das erste Element des **hostresource** -Arrays so fest, dass es einen Verweis auf die zugrunde liegende Host Ressource enthält, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="533f4-173">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="533f4-174">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-174">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="533f4-175">Dies ist eine schreibgeschützte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="533f4-175">This is a read-only property.</span></span> <span data-ttu-id="533f4-176">Wenn die **ResourceType** -Eigenschaft jedoch 17 (Disk) und die **resourcesubtype** -Eigenschaft "Microsoft: Hyper-V: physisches Laufwerk" ist, kann die Eigenschaft " **hoststresource** " mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM-Klasse " \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) " geändert werden.</span><span class="sxs-lookup"><span data-stu-id="533f4-176">But if the **ResourceType** property is 17 (Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Physical Disk Drive", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="533f4-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="533f4-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="533f4-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="533f4-180">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="533f4-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="533f4-181">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="533f4-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="533f4-182">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt und ist immer auf "Microsoft:*GUID* Geräte-ID- \\ *Daten*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="533f4-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="533f4-183">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="533f4-183">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-184">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="533f4-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-186">Die maximale Ressourcen Menge, die für diese Zuweisung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="533f4-186">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="533f4-187">Die Maßeinheit für diese Eigenschaft wird durch die **virtualquantityunits** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="533f4-187">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="533f4-188">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-189">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="533f4-189">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-190">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="533f4-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-192">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="533f4-192">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="533f4-193">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-194">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="533f4-194">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="533f4-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-197">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und [**ResourceType**](msvm-processorsettingdata.md) den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="533f4-197">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="533f4-198">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-198">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-199">**Parent**</span><span class="sxs-lookup"><span data-stu-id="533f4-199">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="533f4-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-202">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="533f4-202">The parent of the resource.</span></span> <span data-ttu-id="533f4-203">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-203">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-204">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="533f4-204">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-205">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="533f4-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-207">Der Bezeichner des Ressourcenpools, von dem diese Ressource zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="533f4-207">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="533f4-208">Bei Instanzen, die einem virtuellen Computer zugeordnet sind, ist dies "Microsoft:*GUID* \\ *gerätespezifische Daten*".</span><span class="sxs-lookup"><span data-stu-id="533f4-208">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="533f4-209">Für Instanzen, die mögliche Einstellungen für eine virtuelle Maschine definieren, ist dies "Microsoft: Definition \\ *GUID* \\ *Type*", wobei der *Typ* "Maximum", "Minimal", "Default" oder "increment" sein kann.</span><span class="sxs-lookup"><span data-stu-id="533f4-209">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="533f4-210">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-211">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="533f4-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-212">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="533f4-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-214">Die Menge der Ressource, die für diese Zuordnung garantiert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="533f4-214">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="533f4-215">Die Maßeinheit für diese Eigenschaft wird durch die **virtualquantityunits** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="533f4-215">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="533f4-216">Diese Ressourcen sind garantiert für den Verbrauch durch den virtuellen Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="533f4-216">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="533f4-217">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-218">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="533f4-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="533f4-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-221">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="533f4-221">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="533f4-222">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="533f4-222">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="533f4-223">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-223">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-224">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="533f4-224">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-225">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="533f4-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-227">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="533f4-227">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="533f4-228">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-228">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="533f4-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="533f4-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="533f4-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Prozessor** (3)</span><span class="sxs-lookup"><span data-stu-id="533f4-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>Arbeits **Speicher** (4)</span><span class="sxs-lookup"><span data-stu-id="533f4-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="533f4-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Paralleler SCSI-HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="533f4-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC-HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="533f4-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI-HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="533f4-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="533f4-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-Adapter** (10)</span><span class="sxs-lookup"><span data-stu-id="533f4-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Anderer Netzwerk Adapter** (11)</span><span class="sxs-lookup"><span data-stu-id="533f4-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>E **/a-Slot** (12)</span><span class="sxs-lookup"><span data-stu-id="533f4-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>E **/a-Gerät** (13)</span><span class="sxs-lookup"><span data-stu-id="533f4-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskettenlaufwerk** (14)</span><span class="sxs-lookup"><span data-stu-id="533f4-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD-Laufwerk** (15)</span><span class="sxs-lookup"><span data-stu-id="533f4-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-Laufwerk** (16)</span><span class="sxs-lookup"><span data-stu-id="533f4-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Laufwerk (17** )</span><span class="sxs-lookup"><span data-stu-id="533f4-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Bandlaufwerk** (18)</span><span class="sxs-lookup"><span data-stu-id="533f4-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Speicher** Block (19)</span><span class="sxs-lookup"><span data-stu-id="533f4-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Anderes Speichergerät** (20)</span><span class="sxs-lookup"><span data-stu-id="533f4-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Seriellen Anschluss** (21)</span><span class="sxs-lookup"><span data-stu-id="533f4-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Paralleler Anschluss** (22)</span><span class="sxs-lookup"><span data-stu-id="533f4-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-Controller** (23)</span><span class="sxs-lookup"><span data-stu-id="533f4-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Grafikcontroller** (24)</span><span class="sxs-lookup"><span data-stu-id="533f4-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394-Controller** (25)</span><span class="sxs-lookup"><span data-stu-id="533f4-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionier Bare Einheit** (26)</span><span class="sxs-lookup"><span data-stu-id="533f4-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Partitionier bare Basiseinheit** (27)</span><span class="sxs-lookup"><span data-stu-id="533f4-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Netzteil** (28)</span><span class="sxs-lookup"><span data-stu-id="533f4-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Kühl Gerät** (29)</span><span class="sxs-lookup"><span data-stu-id="533f4-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet-Switchport** (30)</span><span class="sxs-lookup"><span data-stu-id="533f4-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logischer** Datenträger (31)</span><span class="sxs-lookup"><span data-stu-id="533f4-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Speicher Volume** (32)</span><span class="sxs-lookup"><span data-stu-id="533f4-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet-Verbindung** (33)</span><span class="sxs-lookup"><span data-stu-id="533f4-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="533f4-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="533f4-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="533f4-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="533f4-264">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="533f4-264">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-265">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="533f4-265">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-267">Gibt die Menge der Ressourcen an, die dem Consumer vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="533f4-267">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="533f4-268">Die Maßeinheit für diese Eigenschaft wird durch die **virtualquantityunits** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="533f4-268">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="533f4-269">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-269">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-270">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="533f4-270">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-271">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="533f4-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-273">Gibt die Maßeinheit für diese Ressourcenzuweisung an.</span><span class="sxs-lookup"><span data-stu-id="533f4-273">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="533f4-274">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="533f4-274">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="533f4-275">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="533f4-276">**Virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="533f4-276">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-277">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="533f4-277">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="533f4-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="533f4-279">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="533f4-279">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="533f4-280">Ein Zeichen folgen Array mit Bezeichners dieser Ressource, die dem Betriebssystem des virtuellen Computers vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="533f4-280">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="533f4-281">Diese Werte werden nur verwendet, wenn die **ResourceType** -Eigenschaft auf "6" festgelegt ist (paralleler SCSI-HBA) und die **resourcesubtype** -Eigenschaft auf "Microsoft synthetischer SCSI-Controller" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="533f4-281">These values are used only if the **ResourceType** property is set to 6 (Parallel SCSI HBA) and the **ResourceSubType** property is set to "Microsoft Synthetic SCSI Controller".</span></span> <span data-ttu-id="533f4-282">Diese Eigenschaft wird auf "*GUID*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="533f4-282">This property is set to "*GUID*".</span></span>

<span data-ttu-id="533f4-283">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="533f4-283">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="533f4-284">**Weight**</span><span class="sxs-lookup"><span data-stu-id="533f4-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f4-285">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="533f4-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="533f4-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="533f4-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f4-287">Eine ganze Zahl, die die relative Gewichtung für jeden Prozessor der virtuellen Maschine definiert.</span><span class="sxs-lookup"><span data-stu-id="533f4-287">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="533f4-288">Nachdem alle Reserven erfüllt wurden, wird die verbleibende physische Prozessor Kapazität der Hostingplattform virtuellen Computern basierend auf ihren relativen Gewichtungen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="533f4-288">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="533f4-289">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="533f4-289">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="533f4-290">Bereich: 0 1000</span><span class="sxs-lookup"><span data-stu-id="533f4-290">Range: 0 1000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="533f4-291">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="533f4-291">Remarks</span></span>

<span data-ttu-id="533f4-292">Der Zugriff auf die **MSVM \_ resourcezucationsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="533f4-292">Access to the **Msvm\_ResourceAllocationSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="533f4-293">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="533f4-293">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="533f4-294">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="533f4-294">Requirements</span></span>



| <span data-ttu-id="533f4-295">Anforderung</span><span class="sxs-lookup"><span data-stu-id="533f4-295">Requirement</span></span> | <span data-ttu-id="533f4-296">Wert</span><span class="sxs-lookup"><span data-stu-id="533f4-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="533f4-297">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="533f4-297">Minimum supported client</span></span><br/> | <span data-ttu-id="533f4-298">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="533f4-298">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="533f4-299">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="533f4-299">Minimum supported server</span></span><br/> | <span data-ttu-id="533f4-300">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="533f4-300">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="533f4-301">Namespace</span><span class="sxs-lookup"><span data-stu-id="533f4-301">Namespace</span></span><br/>                | <span data-ttu-id="533f4-302">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="533f4-302">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="533f4-303">MOF</span><span class="sxs-lookup"><span data-stu-id="533f4-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="533f4-304"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="533f4-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="533f4-305">DLL</span><span class="sxs-lookup"><span data-stu-id="533f4-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="533f4-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="533f4-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="533f4-307">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="533f4-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="533f4-308">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="533f4-308">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="533f4-309">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="533f4-309">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="533f4-310">**MSVM \_ resourcezucationsettingdata (v1)**</span><span class="sxs-lookup"><span data-stu-id="533f4-310">**Msvm\_ResourceAllocationSettingData (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="533f4-311">Ressourcen Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="533f4-311">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

