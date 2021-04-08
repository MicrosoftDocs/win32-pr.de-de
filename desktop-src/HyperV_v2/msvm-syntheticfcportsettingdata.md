---
description: Stellt den konfigurierten Status eines synthetischen Fibre Channel Ports dar.
ms.assetid: 5d47dd80-de34-4ae4-a300-c16da1cd4974
title: Msvm_SyntheticFcPortSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPortSettingData
- Msvm_SyntheticFcPortSettingData.InstanceID
- Msvm_SyntheticFcPortSettingData.Caption
- Msvm_SyntheticFcPortSettingData.Description
- Msvm_SyntheticFcPortSettingData.ElementName
- Msvm_SyntheticFcPortSettingData.ResourceType
- Msvm_SyntheticFcPortSettingData.OtherResourceType
- Msvm_SyntheticFcPortSettingData.ResourceSubType
- Msvm_SyntheticFcPortSettingData.PoolID
- Msvm_SyntheticFcPortSettingData.ConsumerVisibility
- Msvm_SyntheticFcPortSettingData.HostResource
- Msvm_SyntheticFcPortSettingData.AllocationUnits
- Msvm_SyntheticFcPortSettingData.VirtualQuantity
- Msvm_SyntheticFcPortSettingData.Reservation
- Msvm_SyntheticFcPortSettingData.Limit
- Msvm_SyntheticFcPortSettingData.Weight
- Msvm_SyntheticFcPortSettingData.AutomaticAllocation
- Msvm_SyntheticFcPortSettingData.AutomaticDeallocation
- Msvm_SyntheticFcPortSettingData.Parent
- Msvm_SyntheticFcPortSettingData.Connection
- Msvm_SyntheticFcPortSettingData.Address
- Msvm_SyntheticFcPortSettingData.MappingBehavior
- Msvm_SyntheticFcPortSettingData.AddressOnParent
- Msvm_SyntheticFcPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticFcPortSettingData.VirtualPortWWPN
- Msvm_SyntheticFcPortSettingData.VirtualPortWWNN
- Msvm_SyntheticFcPortSettingData.SecondaryWWPN
- Msvm_SyntheticFcPortSettingData.SecondaryWWNN
- Msvm_SyntheticFcPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticFcPortSettingData.ChapEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdd0342f5429f5314f5c744a3a760101dbaa043b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750200"
---
# <a name="msvm_syntheticfcportsettingdata-class"></a><span data-ttu-id="5f2bb-103">MSVM \_ syntheticfcportsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="5f2bb-103">Msvm\_SyntheticFcPortSettingData class</span></span>

<span data-ttu-id="5f2bb-104">Stellt den konfigurierten Status eines synthetischen Fibre Channel Ports dar.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-104">Represents the configured state of a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="5f2bb-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f2bb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f2bb-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPortSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel Port Default Settings";
  string  Description = "Describes the default settings for the virtual Fibre Channel port resources.";
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
  string  VirtualPortWWPN;
  string  VirtualPortWWNN;
  string  SecondaryWWPN;
  string  SecondaryWWNN;
  string  VirtualSystemIdentifiers[];
  boolean ChapEnabled;
};
```

## <a name="members"></a><span data-ttu-id="5f2bb-107">Member</span><span class="sxs-lookup"><span data-stu-id="5f2bb-107">Members</span></span>

<span data-ttu-id="5f2bb-108">Die **MSVM \_ syntheticfcportsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5f2bb-108">The **Msvm\_SyntheticFcPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5f2bb-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f2bb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f2bb-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f2bb-110">Properties</span></span>

<span data-ttu-id="5f2bb-111">Die **MSVM \_ syntheticfcportsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-111">The **Msvm\_SyntheticFcPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f2bb-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-115">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-115">The address of the resource.</span></span> <span data-ttu-id="5f2bb-116">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-117">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-120">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="5f2bb-121">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="5f2bb-122">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-123">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-126">Die Zuordnungs Einheit, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-126">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="5f2bb-127">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-128">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5f2bb-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-131">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="5f2bb-132">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-133">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5f2bb-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-136">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="5f2bb-137">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-141">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="5f2bb-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-142">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-142">A short description of the object.</span></span> <span data-ttu-id="5f2bb-143">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-144">**In chapaktiviertem**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-144">**ChapEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-145">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5f2bb-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-147">Gibt an, dass dieser Port mithilfe von dh-CHAP mit einem gemeinsamen geheimen Schlüssel konfiguriert wurde, der es dem Fibre Channel Fabric ermöglicht, sich zu authentifizieren, dass diese virtuelle Maschine die World Wide Names, die diesem Port zugewiesen sind, rechtmäßig verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-147">Indicates that this port has been configured with a shared secret using DH-CHAP, which allows the Fibre Channel fabric to authenticate that this virtual machine can legitimately use the world wide names that are assigned to this port.</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-148">**Connection**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-148">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-149">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="5f2bb-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-151">Das Gerät, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-151">The device to which this resource is connected.</span></span> <span data-ttu-id="5f2bb-152">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-153">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-153">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-154">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-156">Die Sichtbarkeit des Consumers für die zugeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-156">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="5f2bb-157">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-161">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-161">A description of the object.</span></span> <span data-ttu-id="5f2bb-162">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-166">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-166">A display name for the object.</span></span> <span data-ttu-id="5f2bb-167">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-167">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="5f2bb-168">Durch Ändern dieser Eigenschaft wird der Elementname der zugeordneten logischen Geräte Ableitung geändert.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-168">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="5f2bb-169">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-169">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-170">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-170">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-171">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="5f2bb-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-173">Jedem Gerät auf dem virtuellen Computer kann nur eine Host Ressource zugewiesen werden, sodass nur das erste Element dieses Arrays festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-173">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="5f2bb-174">Legen Sie für Geräte, die diese Funktion unterstützen, das erste Element des **hostresource** -Arrays so fest, dass es einen Verweis auf die zugrunde liegende Host Ressource enthält, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-174">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="5f2bb-175">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-175">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-176">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-176">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-179">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-179">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-180">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-180">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5f2bb-181">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-181">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-182">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-182">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-183">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-185">Die maximale Menge der entsprechenden Host Ressourcen, die von der virtuellen Maschine verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-185">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="5f2bb-186">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-187">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-187">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-188">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-190">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-190">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="5f2bb-191">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-192">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-192">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-195">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und [**ResourceType**](msvm-processorsettingdata.md) den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-195">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="5f2bb-196">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-197">**Parent**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-197">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-200">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-200">The parent of the resource.</span></span> <span data-ttu-id="5f2bb-201">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-202">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-202">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-205">Der Bezeichner des Ressourcenpools, von dem diese Ressource zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-205">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="5f2bb-206">Bei Instanzen, die einem virtuellen Computer zugeordnet sind, ist dies "Microsoft:*GUID* \\ *gerätespezifische Daten*".</span><span class="sxs-lookup"><span data-stu-id="5f2bb-206">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="5f2bb-207">Für Instanzen, die mögliche Einstellungen für eine virtuelle Maschine definieren, ist dies "Microsoft: Definition \\ *GUID* \\ *Type*", wobei der *Typ* "Maximum", "Minimal", "Default" oder "increment" sein kann.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-207">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="5f2bb-208">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-209">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-209">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-210">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-212">Die Menge der Ressourcen, die für die Verwendung durch den virtuellen Computer reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-212">The amount of resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="5f2bb-213">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-214">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-215">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-217">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="5f2bb-218">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="5f2bb-219">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-221">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-223">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="5f2bb-224">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="5f2bb-225">Wert</span><span class="sxs-lookup"><span data-stu-id="5f2bb-225">Value</span></span>                                                                                                                                                                                          | <span data-ttu-id="5f2bb-226">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5f2bb-226">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC_HBA"></span><span id="fc_hba"></span><dl> <span data-ttu-id="5f2bb-227"><dt>**FC HBA**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="5f2bb-227"><dt>**FC HBA**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="5f2bb-228">Fibre Channel</span><span class="sxs-lookup"><span data-stu-id="5f2bb-228">Fibre Channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5f2bb-229">**Secondarywwnn**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-229">**SecondaryWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-232">Gibt den World Wide Node Name des virtuellen HBA-Ports an, der bei der Live Migration des virtuellen Computers verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-232">Indicates the world wide node name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-233">**Secondarywwpn**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-233">**SecondaryWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-234">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-236">Gibt den World Wide Port Name des virtuellen HBA-Ports an, der bei der Live Migration des virtuellen Computers verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-236">Indicates the world wide port name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-237">**Virtualportwwnn**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-237">**VirtualPortWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-238">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-240">Gibt den World Wide Node Name des virtuellen HBA-Ports an.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-240">Indicates the world wide node name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-241">**Virtualportwwpn**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-241">**VirtualPortWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-244">Gibt den World Wide Port Name des virtuellen HBA-Ports an.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-244">Indicates the world wide port name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-245">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-245">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-246">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-246">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-248">Gibt die Menge der Ressourcen an, die dem Consumer vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-248">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="5f2bb-249">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-250">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-250">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-253">Gibt die Maßeinheit für die **virtualmenge** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-253">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="5f2bb-254">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-254">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="5f2bb-255">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-255">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-256">**Virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-256">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-257">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="5f2bb-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-259">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="5f2bb-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-260">Ein Zeichen folgen Array mit Bezeichners dieser Ressource, die dem Betriebssystem des virtuellen Computers vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-260">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="5f2bb-261">Die Indizes und Werte pro Index werden pro Ressource definiert (d. h. für jeden aufgezählten **ResourceType** -Wert).</span><span class="sxs-lookup"><span data-stu-id="5f2bb-261">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="5f2bb-262">Diese Eigenschaft wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-262">This property is not used</span></span>

</dd> <dt>

<span data-ttu-id="5f2bb-263">**Weight**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-263">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f2bb-264">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f2bb-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f2bb-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f2bb-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f2bb-266">Eine ganze Zahl, die die relative Gewichtung für jeden Prozessor der virtuellen Maschine definiert.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-266">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="5f2bb-267">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f2bb-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f2bb-268">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f2bb-268">Requirements</span></span>



| <span data-ttu-id="5f2bb-269">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f2bb-269">Requirement</span></span> | <span data-ttu-id="5f2bb-270">Wert</span><span class="sxs-lookup"><span data-stu-id="5f2bb-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f2bb-271">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f2bb-271">Minimum supported client</span></span><br/> | <span data-ttu-id="5f2bb-272">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f2bb-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5f2bb-273">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f2bb-273">Minimum supported server</span></span><br/> | <span data-ttu-id="5f2bb-274">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f2bb-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f2bb-275">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f2bb-275">Namespace</span></span><br/>                | <span data-ttu-id="5f2bb-276">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5f2bb-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5f2bb-277">MOF</span><span class="sxs-lookup"><span data-stu-id="5f2bb-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f2bb-278"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5f2bb-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f2bb-279">DLL</span><span class="sxs-lookup"><span data-stu-id="5f2bb-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f2bb-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5f2bb-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

