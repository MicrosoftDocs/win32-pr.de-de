---
description: Stellt den konfigurierten Status des Volumeschattenkopie-Dienst-Diensts (VSS) dar.
ms.assetid: FAE8E8F7-525A-4E5A-91B3-B73343337352
title: Msvm_VssComponentSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponentSettingData
- Msvm_VssComponentSettingData.InstanceID
- Msvm_VssComponentSettingData.Caption
- Msvm_VssComponentSettingData.Description
- Msvm_VssComponentSettingData.ElementName
- Msvm_VssComponentSettingData.ResourceType
- Msvm_VssComponentSettingData.OtherResourceType
- Msvm_VssComponentSettingData.ResourceSubType
- Msvm_VssComponentSettingData.PoolID
- Msvm_VssComponentSettingData.ConsumerVisibility
- Msvm_VssComponentSettingData.HostResource
- Msvm_VssComponentSettingData.AllocationUnits
- Msvm_VssComponentSettingData.VirtualQuantity
- Msvm_VssComponentSettingData.Reservation
- Msvm_VssComponentSettingData.Limit
- Msvm_VssComponentSettingData.Weight
- Msvm_VssComponentSettingData.AutomaticAllocation
- Msvm_VssComponentSettingData.AutomaticDeallocation
- Msvm_VssComponentSettingData.Parent
- Msvm_VssComponentSettingData.Connection
- Msvm_VssComponentSettingData.Address
- Msvm_VssComponentSettingData.MappingBehavior
- Msvm_VssComponentSettingData.AddressOnParent
- Msvm_VssComponentSettingData.VirtualQuantityUnits
- Msvm_VssComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d37f46c10cc702c66a30fb484553a8c5da03d8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346903"
---
# <a name="msvm_vsscomponentsettingdata-class"></a><span data-ttu-id="b9306-103">MSVM \_ vsscomponentsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="b9306-103">Msvm\_VssComponentSettingData class</span></span>

<span data-ttu-id="b9306-104">Stellt den konfigurierten Status des Volumeschattenkopie-Dienst-Diensts (VSS) dar.</span><span class="sxs-lookup"><span data-stu-id="b9306-104">Represents the configured state of the Volume Shadow Copy Service (VSS) service.</span></span>

<span data-ttu-id="b9306-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9306-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9306-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9306-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "VSS";
  string  Description = "Microsoft VSS Service Setting Data";
  string  ElementName = "VSS";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:VSS Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource;
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

## <a name="members"></a><span data-ttu-id="b9306-107">Member</span><span class="sxs-lookup"><span data-stu-id="b9306-107">Members</span></span>

<span data-ttu-id="b9306-108">Die **MSVM \_ vsscomponentsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b9306-108">The **Msvm\_VssComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b9306-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9306-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9306-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9306-110">Properties</span></span>

<span data-ttu-id="b9306-111">Die **MSVM \_ vsscomponentsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9306-111">The **Msvm\_VssComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9306-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="b9306-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-115">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b9306-115">The address of the resource.</span></span> <span data-ttu-id="b9306-116">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-117">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="b9306-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-120">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="b9306-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="b9306-121">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b9306-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="b9306-122">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-123">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="b9306-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-126">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9306-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="b9306-127">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-128">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="b9306-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9306-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-131">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b9306-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="b9306-132">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-133">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="b9306-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b9306-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-136">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="b9306-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="b9306-137">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b9306-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-141">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b9306-141">A short description of the object.</span></span> <span data-ttu-id="b9306-142">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="b9306-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-144">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b9306-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b9306-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-146">Das, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b9306-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="b9306-147">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-148">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="b9306-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-149">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9306-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-151">Die Consumer, die für die zugeordnete Ressource sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="b9306-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="b9306-152">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="b9306-153">Wert</span><span class="sxs-lookup"><span data-stu-id="b9306-153">Value</span></span>                                                                        | <span data-ttu-id="b9306-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b9306-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="b9306-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b9306-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="b9306-156">Virtualisierten</span><span class="sxs-lookup"><span data-stu-id="b9306-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b9306-157">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b9306-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-160">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b9306-160">A description of the object.</span></span> <span data-ttu-id="b9306-161">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b9306-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-165">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b9306-165">A display name for the object.</span></span> <span data-ttu-id="b9306-166">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b9306-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-168">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9306-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-170">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="b9306-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b9306-171">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und hat den Standardwert 2 (aktiviert).</span><span class="sxs-lookup"><span data-stu-id="b9306-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and has a default value of 2 (Enabled).</span></span>

<span data-ttu-id="b9306-172">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b9306-172">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>



 <span data-ttu-id="b9306-173">(2)</span><span class="sxs-lookup"><span data-stu-id="b9306-173">(2)</span></span>


</dt> <dd>

<span data-ttu-id="b9306-174">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b9306-174">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="b9306-175">3</span><span class="sxs-lookup"><span data-stu-id="b9306-175">3</span></span>
</dt> <dd>

<span data-ttu-id="b9306-176">Disabled</span><span class="sxs-lookup"><span data-stu-id="b9306-176">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b9306-177">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="b9306-177">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-180">Macht eine bestimmte Zuweisung zum Hosten von oder zugrunde liegenden Ressourcen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b9306-180">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="b9306-181">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9306-181">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b9306-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b9306-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9306-185">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="b9306-185">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b9306-186">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b9306-186">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b9306-187">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-188">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="b9306-188">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-189">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9306-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-191">Die obere Grenze oder die maximale Ressourcen Menge, die für diese Zuweisung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="b9306-191">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="b9306-192">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-193">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="b9306-193">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-194">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9306-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-196">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="b9306-196">Indicates how this resource maps to underlying resources.</span></span> <span data-ttu-id="b9306-197">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-197">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-198">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="b9306-198">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-201">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="b9306-201">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="b9306-202">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-202">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-203">**Parent**</span><span class="sxs-lookup"><span data-stu-id="b9306-203">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-206">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b9306-206">The parent of the resource.</span></span> <span data-ttu-id="b9306-207">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-208">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="b9306-208">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-209">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-211">Die ID des Ressourcenpools, dem die Ressource zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b9306-211">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="b9306-212">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-213">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="b9306-213">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-214">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9306-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-216">Die Menge der Ressource, die für diese Zuordnung garantiert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b9306-216">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="b9306-217">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-218">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="b9306-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-221">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b9306-221">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="b9306-222">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9306-222">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b9306-223">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="b9306-223">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-224">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9306-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-226">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9306-226">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="b9306-227">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf 1 (sonstige) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9306-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1 (Other).</span></span>



| <span data-ttu-id="b9306-228">Wert</span><span class="sxs-lookup"><span data-stu-id="b9306-228">Value</span></span>                                                                        | <span data-ttu-id="b9306-229">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b9306-229">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="b9306-230"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b9306-230"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b9306-231">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="b9306-231">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b9306-232">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="b9306-232">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-233">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9306-233">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-235">Die Menge der Ressourcen, die dem Consumer vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b9306-235">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="b9306-236">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-237">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="b9306-237">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-238">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9306-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-240">Gibt die Maßeinheit für diese Ressourcenzuweisung an.</span><span class="sxs-lookup"><span data-stu-id="b9306-240">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="b9306-241">Der Wert dieser Eigenschaft ist ein gültiger Wert des Qualifizierers für programmatische Einheiten, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="b9306-241">The value of this property is a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="b9306-242">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b9306-243">**Weight**</span><span class="sxs-lookup"><span data-stu-id="b9306-243">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9306-244">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9306-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9306-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9306-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9306-246">Eine relative Priorität für diese Zuordnung in Bezug auf andere Zuordnungen desselben Ressourcenpools.</span><span class="sxs-lookup"><span data-stu-id="b9306-246">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="b9306-247">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9306-247">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9306-248">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9306-248">Remarks</span></span>

<span data-ttu-id="b9306-249">Der Zugriff auf die **MSVM \_ vsscomponentsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="b9306-249">Access to the **Msvm\_VssComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b9306-250">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b9306-250">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9306-251">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9306-251">Requirements</span></span>



| <span data-ttu-id="b9306-252">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9306-252">Requirement</span></span> | <span data-ttu-id="b9306-253">Wert</span><span class="sxs-lookup"><span data-stu-id="b9306-253">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9306-254">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9306-254">Minimum supported client</span></span><br/> | <span data-ttu-id="b9306-255">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9306-255">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b9306-256">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9306-256">Minimum supported server</span></span><br/> | <span data-ttu-id="b9306-257">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9306-257">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9306-258">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9306-258">Namespace</span></span><br/>                | <span data-ttu-id="b9306-259">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b9306-259">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b9306-260">MOF</span><span class="sxs-lookup"><span data-stu-id="b9306-260">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9306-261"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b9306-261"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9306-262">DLL</span><span class="sxs-lookup"><span data-stu-id="b9306-262">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9306-263"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b9306-263"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b9306-264">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9306-264">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9306-265">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="b9306-265">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="b9306-266">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="b9306-266">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

