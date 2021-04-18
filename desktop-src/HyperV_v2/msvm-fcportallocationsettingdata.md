---
description: Stellt den konfigurierten Status eines synthetischen Fibre Channel Ports oder eines Fibre Channel Switchports dar.
ms.assetid: 680badc4-8dba-47e8-859a-0ed472a15eda
title: Msvm_FcPortAllocationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcPortAllocationSettingData
- Msvm_FcPortAllocationSettingData.InstanceID
- Msvm_FcPortAllocationSettingData.Caption
- Msvm_FcPortAllocationSettingData.Description
- Msvm_FcPortAllocationSettingData.ElementName
- Msvm_FcPortAllocationSettingData.ResourceType
- Msvm_FcPortAllocationSettingData.OtherResourceType
- Msvm_FcPortAllocationSettingData.ResourceSubType
- Msvm_FcPortAllocationSettingData.PoolID
- Msvm_FcPortAllocationSettingData.ConsumerVisibility
- Msvm_FcPortAllocationSettingData.HostResource
- Msvm_FcPortAllocationSettingData.AllocationUnits
- Msvm_FcPortAllocationSettingData.VirtualQuantity
- Msvm_FcPortAllocationSettingData.Reservation
- Msvm_FcPortAllocationSettingData.Limit
- Msvm_FcPortAllocationSettingData.Weight
- Msvm_FcPortAllocationSettingData.AutomaticAllocation
- Msvm_FcPortAllocationSettingData.AutomaticDeallocation
- Msvm_FcPortAllocationSettingData.Parent
- Msvm_FcPortAllocationSettingData.Connection
- Msvm_FcPortAllocationSettingData.Address
- Msvm_FcPortAllocationSettingData.MappingBehavior
- Msvm_FcPortAllocationSettingData.AddressOnParent
- Msvm_FcPortAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 824f7077eeb3cb9e00ce8733cb5d2f57761716e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343713"
---
# <a name="msvm_fcportallocationsettingdata-class"></a><span data-ttu-id="1ef03-103">MSVM \_ fcportzugesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="1ef03-103">Msvm\_FcPortAllocationSettingData class</span></span>

<span data-ttu-id="1ef03-104">Stellt den konfigurierten Status eines synthetischen Fibre Channel Ports oder eines Fibre Channel Switchports dar.</span><span class="sxs-lookup"><span data-stu-id="1ef03-104">Represents the configured state of a synthetic Fibre Channel port or a Fibre Channel switch port.</span></span>

<span data-ttu-id="1ef03-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1ef03-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef03-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ef03-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel VDev Default Settings";
  string  Description = "The default settings for the virtual Fibre Channel connection pool.";
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
};
```

## <a name="members"></a><span data-ttu-id="1ef03-107">Member</span><span class="sxs-lookup"><span data-stu-id="1ef03-107">Members</span></span>

<span data-ttu-id="1ef03-108">Die **MSVM \_ fcportzugecationsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1ef03-108">The **Msvm\_FcPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1ef03-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ef03-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ef03-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ef03-110">Properties</span></span>

<span data-ttu-id="1ef03-111">Die **MSVM \_ fcportzuweisung** -Klasse hat diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1ef03-111">The **Msvm\_FcPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ef03-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="1ef03-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ef03-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-115">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="1ef03-115">The address of the resource.</span></span> <span data-ttu-id="1ef03-116">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-117">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="1ef03-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ef03-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-120">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="1ef03-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="1ef03-121">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1ef03-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="1ef03-122">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-123">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="1ef03-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ef03-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-126">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ef03-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="1ef03-127">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-128">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="1ef03-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1ef03-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-131">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1ef03-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="1ef03-132">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-133">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="1ef03-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1ef03-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-136">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="1ef03-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="1ef03-137">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1ef03-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ef03-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-141">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="1ef03-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-142">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1ef03-142">A short description of the object.</span></span> <span data-ttu-id="1ef03-143">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-144">**Connection**</span><span class="sxs-lookup"><span data-stu-id="1ef03-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-145">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1ef03-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-147">Das Gerät, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="1ef03-147">The device to which this resource is connected.</span></span> <span data-ttu-id="1ef03-148">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-149">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="1ef03-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-150">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ef03-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-152">Die Sichtbarkeit des Consumers für die zugeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="1ef03-152">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="1ef03-153">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-154">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ef03-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ef03-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-157">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1ef03-157">A description of the object.</span></span> <span data-ttu-id="1ef03-158">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1ef03-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ef03-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-162">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-162">A display name for the object.</span></span> <span data-ttu-id="1ef03-163">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="1ef03-164">Durch Ändern dieser Eigenschaft wird der Elementname der zugeordneten logischen Geräte Ableitung geändert.</span><span class="sxs-lookup"><span data-stu-id="1ef03-164">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="1ef03-165">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1ef03-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-166">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="1ef03-166">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-167">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1ef03-167">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-169">Jedem Gerät auf dem virtuellen Computer kann nur eine Host Ressource zugewiesen werden, sodass nur das erste Element dieses Arrays festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1ef03-169">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="1ef03-170">Legen Sie für Geräte, die diese Funktion unterstützen, das erste Element des **hostresource** -Arrays so fest, dass es einen Verweis auf die zugrunde liegende Host Ressource enthält, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ef03-170">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="1ef03-171">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-171">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="1ef03-172">Dies ist eine schreibgeschützte Eigenschaft. wenn die **ResourceType** -Eigenschaft jedoch 22 (Disk) und die **resourcesubtype** -Eigenschaft "Microsoft Physical Disk Drive" ist, kann Sie mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1ef03-172">This is a read-only property, but if the **ResourceType** property is 22 (Disk) and the **ResourceSubType** property is "Microsoft Physical Disk Drive", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1ef03-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ef03-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-176">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="1ef03-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-177">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1ef03-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1ef03-178">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-178">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-179">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="1ef03-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-180">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ef03-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-182">Die maximale Ressourcen Menge, die für diese Zuweisung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="1ef03-182">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="1ef03-183">Die Maßeinheit für diese Eigenschaft wird durch die **virtualquantityunits** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="1ef03-183">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="1ef03-184">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-184">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-185">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="1ef03-185">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-186">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ef03-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-188">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="1ef03-188">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="1ef03-189">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-190">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="1ef03-190">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ef03-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-193">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und [**ResourceType**](msvm-processorsettingdata.md) den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="1ef03-193">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="1ef03-194">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-195">**Parent**</span><span class="sxs-lookup"><span data-stu-id="1ef03-195">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ef03-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-198">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="1ef03-198">The parent of the resource.</span></span> <span data-ttu-id="1ef03-199">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-200">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="1ef03-200">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ef03-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-203">Der Bezeichner des Ressourcenpools, von dem diese Ressource zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="1ef03-203">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="1ef03-204">Bei Instanzen, die einem virtuellen Computer zugeordnet sind, ist dies "Microsoft:*GUID* \\ *gerätespezifische Daten*".</span><span class="sxs-lookup"><span data-stu-id="1ef03-204">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="1ef03-205">Für Instanzen, die mögliche Einstellungen für eine virtuelle Maschine definieren, ist dies "Microsoft: Definition \\ *GUID* \\ *Type*", wobei der *Typ* "Maximum", "Minimal", "Default" oder "increment" sein kann.</span><span class="sxs-lookup"><span data-stu-id="1ef03-205">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="1ef03-206">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-207">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="1ef03-207">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-208">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ef03-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-210">Die Menge der Ressource, die für diese Zuordnung garantiert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1ef03-210">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="1ef03-211">Die Maßeinheit für diese Eigenschaft wird durch die **virtualquantityunits** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="1ef03-211">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="1ef03-212">Diese Ressourcen sind garantiert für den Verbrauch durch den virtuellen Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1ef03-212">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="1ef03-213">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-214">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="1ef03-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-215">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ef03-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-217">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="1ef03-218">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="1ef03-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="1ef03-219">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="1ef03-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-221">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ef03-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-223">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="1ef03-224">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="1ef03-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="1ef03-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="1ef03-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Prozessor** (3)</span><span class="sxs-lookup"><span data-stu-id="1ef03-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>Arbeits **Speicher** (4)</span><span class="sxs-lookup"><span data-stu-id="1ef03-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="1ef03-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Paralleler SCSI-HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="1ef03-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC-HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="1ef03-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI-HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="1ef03-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="1ef03-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-Adapter** (10)</span><span class="sxs-lookup"><span data-stu-id="1ef03-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Anderer Netzwerk Adapter** (11)</span><span class="sxs-lookup"><span data-stu-id="1ef03-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>E **/a-Slot** (12)</span><span class="sxs-lookup"><span data-stu-id="1ef03-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>E **/a-Gerät** (13)</span><span class="sxs-lookup"><span data-stu-id="1ef03-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Diskettenlaufwerk** (14)</span><span class="sxs-lookup"><span data-stu-id="1ef03-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD-Laufwerk** (15)</span><span class="sxs-lookup"><span data-stu-id="1ef03-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-Laufwerk** (16)</span><span class="sxs-lookup"><span data-stu-id="1ef03-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Seriellen Anschluss** (17)</span><span class="sxs-lookup"><span data-stu-id="1ef03-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Paralleler Anschluss** (18)</span><span class="sxs-lookup"><span data-stu-id="1ef03-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-Controller** (19)</span><span class="sxs-lookup"><span data-stu-id="1ef03-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Grafikcontroller** (20)</span><span class="sxs-lookup"><span data-stu-id="1ef03-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Speicher** Block (21)</span><span class="sxs-lookup"><span data-stu-id="1ef03-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>Daten **Träger (22** )</span><span class="sxs-lookup"><span data-stu-id="1ef03-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Band** (23)</span><span class="sxs-lookup"><span data-stu-id="1ef03-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Anderes Speichergerät** (24)</span><span class="sxs-lookup"><span data-stu-id="1ef03-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire-Controller** (25)</span><span class="sxs-lookup"><span data-stu-id="1ef03-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionier Bare Einheit** (26)</span><span class="sxs-lookup"><span data-stu-id="1ef03-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Partitionier bare Basiseinheit** (27)</span><span class="sxs-lookup"><span data-stu-id="1ef03-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Netzteil** (28)</span><span class="sxs-lookup"><span data-stu-id="1ef03-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Kühl Gerät** (29)</span><span class="sxs-lookup"><span data-stu-id="1ef03-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="1ef03-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="1ef03-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ef03-256">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="1ef03-256">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-257">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ef03-257">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-259">Gibt die Menge der Ressourcen an, die dem Consumer vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1ef03-259">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="1ef03-260">Die Maßeinheit für diese Eigenschaft wird durch die **virtualquantityunits** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="1ef03-260">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="1ef03-261">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-262">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="1ef03-262">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-263">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ef03-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-265">Gibt die Maßeinheit für diese Ressourcenzuweisung an.</span><span class="sxs-lookup"><span data-stu-id="1ef03-265">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="1ef03-266">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="1ef03-266">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="1ef03-267">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ef03-268">**Weight**</span><span class="sxs-lookup"><span data-stu-id="1ef03-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef03-269">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ef03-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef03-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ef03-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ef03-271">Eine ganze Zahl, die die relative Gewichtung für jeden Prozessor der virtuellen Maschine definiert.</span><span class="sxs-lookup"><span data-stu-id="1ef03-271">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="1ef03-272">Nachdem alle Reserven erfüllt wurden, wird die verbleibende physische Prozessor Kapazität der Hostingplattform virtuellen Computern basierend auf ihren relativen Gewichtungen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1ef03-272">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="1ef03-273">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ef03-273">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="1ef03-274">Bereich: 0 1000</span><span class="sxs-lookup"><span data-stu-id="1ef03-274">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ef03-275">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ef03-275">Requirements</span></span>



| <span data-ttu-id="1ef03-276">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ef03-276">Requirement</span></span> | <span data-ttu-id="1ef03-277">Wert</span><span class="sxs-lookup"><span data-stu-id="1ef03-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef03-278">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ef03-278">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef03-279">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ef03-279">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1ef03-280">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ef03-280">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef03-281">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ef03-281">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ef03-282">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ef03-282">Namespace</span></span><br/>                | <span data-ttu-id="1ef03-283">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1ef03-283">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1ef03-284">MOF</span><span class="sxs-lookup"><span data-stu-id="1ef03-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ef03-285"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1ef03-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ef03-286">DLL</span><span class="sxs-lookup"><span data-stu-id="1ef03-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ef03-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ef03-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

