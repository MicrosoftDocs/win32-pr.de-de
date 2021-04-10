---
description: Stellt den konfigurierten Status der Remotedesktop Virtualisierungskomponente (RDV) dar. Der Standardstatus ist "aktiviert".
ms.assetid: 058432d7-4439-47ec-9909-82a405d69a6e
title: Msvm_RdvComponentSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponentSettingData
- Msvm_RdvComponentSettingData.InstanceID
- Msvm_RdvComponentSettingData.Caption
- Msvm_RdvComponentSettingData.Description
- Msvm_RdvComponentSettingData.ElementName
- Msvm_RdvComponentSettingData.ResourceType
- Msvm_RdvComponentSettingData.OtherResourceType
- Msvm_RdvComponentSettingData.ResourceSubType
- Msvm_RdvComponentSettingData.PoolID
- Msvm_RdvComponentSettingData.ConsumerVisibility
- Msvm_RdvComponentSettingData.HostResource
- Msvm_RdvComponentSettingData.AllocationUnits
- Msvm_RdvComponentSettingData.VirtualQuantity
- Msvm_RdvComponentSettingData.Reservation
- Msvm_RdvComponentSettingData.Limit
- Msvm_RdvComponentSettingData.Weight
- Msvm_RdvComponentSettingData.AutomaticAllocation
- Msvm_RdvComponentSettingData.AutomaticDeallocation
- Msvm_RdvComponentSettingData.Parent
- Msvm_RdvComponentSettingData.Connection
- Msvm_RdvComponentSettingData.Address
- Msvm_RdvComponentSettingData.MappingBehavior
- Msvm_RdvComponentSettingData.AddressOnParent
- Msvm_RdvComponentSettingData.VirtualQuantityUnits
- Msvm_RdvComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dfc8decda2bf0c505331c9d681069d55f40687f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865527"
---
# <a name="msvm_rdvcomponentsettingdata-class"></a><span data-ttu-id="07bd5-104">MSVM \_ rdvcomponentsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="07bd5-104">Msvm\_RdvComponentSettingData class</span></span>

<span data-ttu-id="07bd5-105">Stellt den konfigurierten Status der Remotedesktop Virtualisierungskomponente (RDV) dar.</span><span class="sxs-lookup"><span data-stu-id="07bd5-105">Represents the configured state of the Remote Desktop Virtualization (RDV) component.</span></span> <span data-ttu-id="07bd5-106">Der Standardstatus ist "aktiviert".</span><span class="sxs-lookup"><span data-stu-id="07bd5-106">The default state is Enabled.</span></span>

<span data-ttu-id="07bd5-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="07bd5-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="07bd5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="07bd5-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Remote Desktop Virtualization Service Default Settings";
  string  Description = "Describes the default settings for the Remote Desktop Virtualization Service resources.";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  EnabledState = 2;
};
```

## <a name="members"></a><span data-ttu-id="07bd5-109">Member</span><span class="sxs-lookup"><span data-stu-id="07bd5-109">Members</span></span>

<span data-ttu-id="07bd5-110">Die **MSVM \_ rdvcomponentsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="07bd5-110">The **Msvm\_RdvComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="07bd5-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07bd5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07bd5-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07bd5-112">Properties</span></span>

<span data-ttu-id="07bd5-113">Die **MSVM \_ rdvcomponentsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="07bd5-113">The **Msvm\_RdvComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07bd5-114">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="07bd5-114">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07bd5-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-117">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="07bd5-117">The address of the resource.</span></span> <span data-ttu-id="07bd5-118">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-118">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-119">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="07bd5-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07bd5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-122">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="07bd5-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="07bd5-123">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="07bd5-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="07bd5-124">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-125">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="07bd5-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07bd5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-128">Die Zuordnungs Einheit, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="07bd5-128">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="07bd5-129">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-130">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="07bd5-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-131">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="07bd5-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-133">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="07bd5-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="07bd5-134">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-135">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="07bd5-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-136">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="07bd5-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-138">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="07bd5-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="07bd5-139">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-140">**Caption**</span><span class="sxs-lookup"><span data-stu-id="07bd5-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07bd5-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-143">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="07bd5-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-144">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="07bd5-144">A short description of the object.</span></span> <span data-ttu-id="07bd5-145">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-switchporteinstellungen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-146">**Connection**</span><span class="sxs-lookup"><span data-stu-id="07bd5-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-147">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="07bd5-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-149">Das Gerät, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="07bd5-149">The device to which this resource is connected.</span></span> <span data-ttu-id="07bd5-150">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-151">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="07bd5-151">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-152">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07bd5-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-154">Die Sichtbarkeit des Consumers für die zugeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="07bd5-154">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="07bd5-155">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 3 (virtualisiert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07bd5-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07bd5-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-159">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="07bd5-159">A description of the object.</span></span> <span data-ttu-id="07bd5-160">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-switchporteinstellungen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-161">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="07bd5-161">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07bd5-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-164">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-164">A display name for the object.</span></span> <span data-ttu-id="07bd5-165">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-165">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="07bd5-166">Durch Ändern dieser Eigenschaft wird der Elementname der zugeordneten logischen Geräte Ableitung geändert.</span><span class="sxs-lookup"><span data-stu-id="07bd5-166">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="07bd5-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-168">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07bd5-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-170">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="07bd5-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="07bd5-171">Gültige Werte sind 2 (aktiviert) und 3 (deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="07bd5-171">Valid values are 2 (enabled) and 3 (disabled).</span></span> <span data-ttu-id="07bd5-172">Der Standardwert ist 2 (aktiviert).</span><span class="sxs-lookup"><span data-stu-id="07bd5-172">The default value is 2 (enabled).</span></span> <span data-ttu-id="07bd5-173">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyvirtualsystemresources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) -Methode der Klasse " [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) " geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="07bd5-173">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-174">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="07bd5-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-175">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="07bd5-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-177">Jedem Gerät im virtuellen Switch kann nur eine Host Ressource zugewiesen werden, sodass nur das erste Element dieses Arrays festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="07bd5-177">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="07bd5-178">Legen Sie für Geräte, die diese Funktion unterstützen, das erste Element des **hostresource** -Arrays so fest, dass es einen Verweis auf die zugrunde liegende Host Ressource enthält, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="07bd5-178">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="07bd5-179">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-179">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="07bd5-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07bd5-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-183">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="07bd5-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-184">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="07bd5-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="07bd5-185">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-186">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="07bd5-186">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-187">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="07bd5-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-189">Die maximale Menge der entsprechenden Host Ressourcen, die vom virtuellen Switch genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="07bd5-189">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="07bd5-190">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-191">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="07bd5-191">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-192">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07bd5-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-194">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="07bd5-194">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="07bd5-195">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-196">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="07bd5-196">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07bd5-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-199">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und [**ResourceType**](msvm-processorsettingdata.md) den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="07bd5-199">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="07bd5-200">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="07bd5-200">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-201">**Parent**</span><span class="sxs-lookup"><span data-stu-id="07bd5-201">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07bd5-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-204">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="07bd5-204">The parent of the resource.</span></span> <span data-ttu-id="07bd5-205">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-205">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-206">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="07bd5-206">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07bd5-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-209">Der Bezeichner des Ressourcenpools, von dem diese Ressource zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="07bd5-209">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="07bd5-210">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-211">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="07bd5-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-212">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="07bd5-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-214">Die Menge der Ressourcen, die für die Verwendung durch den virtuellen Switch reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="07bd5-214">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="07bd5-215">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-215">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-216">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="07bd5-216">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07bd5-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-219">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-219">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="07bd5-220">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="07bd5-220">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="07bd5-221">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="07bd5-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-223">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07bd5-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-225">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="07bd5-226">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 33 (Ethernet-Verbindung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-227">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="07bd5-227">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-228">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="07bd5-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-230">Die Gesamtanzahl der Ports im virtuellen Switch.</span><span class="sxs-lookup"><span data-stu-id="07bd5-230">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="07bd5-231">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-232">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="07bd5-232">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-233">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07bd5-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-235">Gibt die Maßeinheit für die **virtualmenge** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="07bd5-235">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="07bd5-236">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="07bd5-236">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="07bd5-237">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="07bd5-238">**Weight**</span><span class="sxs-lookup"><span data-stu-id="07bd5-238">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07bd5-239">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07bd5-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07bd5-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07bd5-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07bd5-241">Eine ganze Zahl, die die Gewichtung für jeden virtuellen Switch definiert.</span><span class="sxs-lookup"><span data-stu-id="07bd5-241">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="07bd5-242">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07bd5-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="07bd5-243">Bereich: 0 1000</span><span class="sxs-lookup"><span data-stu-id="07bd5-243">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07bd5-244">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07bd5-244">Requirements</span></span>



| <span data-ttu-id="07bd5-245">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07bd5-245">Requirement</span></span> | <span data-ttu-id="07bd5-246">Wert</span><span class="sxs-lookup"><span data-stu-id="07bd5-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07bd5-247">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07bd5-247">Minimum supported client</span></span><br/> | <span data-ttu-id="07bd5-248">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07bd5-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="07bd5-249">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07bd5-249">Minimum supported server</span></span><br/> | <span data-ttu-id="07bd5-250">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07bd5-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07bd5-251">Namespace</span><span class="sxs-lookup"><span data-stu-id="07bd5-251">Namespace</span></span><br/>                | <span data-ttu-id="07bd5-252">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="07bd5-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="07bd5-253">MOF</span><span class="sxs-lookup"><span data-stu-id="07bd5-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07bd5-254"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="07bd5-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="07bd5-255">DLL</span><span class="sxs-lookup"><span data-stu-id="07bd5-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07bd5-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="07bd5-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

