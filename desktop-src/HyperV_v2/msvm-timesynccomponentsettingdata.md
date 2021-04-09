---
description: Stellt den konfigurierten Status des Zeit Synchronisierungs dienstants dar.
ms.assetid: AACEDE11-3F5B-42AB-A16F-0474FA98D3FD
title: Msvm_TimeSyncComponentSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponentSettingData
- Msvm_TimeSyncComponentSettingData.InstanceID
- Msvm_TimeSyncComponentSettingData.Caption
- Msvm_TimeSyncComponentSettingData.Description
- Msvm_TimeSyncComponentSettingData.ElementName
- Msvm_TimeSyncComponentSettingData.ResourceType
- Msvm_TimeSyncComponentSettingData.OtherResourceType
- Msvm_TimeSyncComponentSettingData.ResourceSubType
- Msvm_TimeSyncComponentSettingData.PoolID
- Msvm_TimeSyncComponentSettingData.ConsumerVisibility
- Msvm_TimeSyncComponentSettingData.HostResource
- Msvm_TimeSyncComponentSettingData.AllocationUnits
- Msvm_TimeSyncComponentSettingData.VirtualQuantity
- Msvm_TimeSyncComponentSettingData.Reservation
- Msvm_TimeSyncComponentSettingData.Limit
- Msvm_TimeSyncComponentSettingData.Weight
- Msvm_TimeSyncComponentSettingData.AutomaticAllocation
- Msvm_TimeSyncComponentSettingData.AutomaticDeallocation
- Msvm_TimeSyncComponentSettingData.Parent
- Msvm_TimeSyncComponentSettingData.Connection
- Msvm_TimeSyncComponentSettingData.Address
- Msvm_TimeSyncComponentSettingData.MappingBehavior
- Msvm_TimeSyncComponentSettingData.AddressOnParent
- Msvm_TimeSyncComponentSettingData.VirtualQuantityUnits
- Msvm_TimeSyncComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 063c0f7904976d50d7c1914f810e71ff84f740b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959189"
---
# <a name="msvm_timesynccomponentsettingdata-class"></a><span data-ttu-id="fb441-103">MSVM \_ timesynccomponentsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="fb441-103">Msvm\_TimeSyncComponentSettingData class</span></span>

<span data-ttu-id="fb441-104">Stellt den konfigurierten Status des Zeit Synchronisierungs dienstants dar.</span><span class="sxs-lookup"><span data-stu-id="fb441-104">Represents the configured state of the time synchronization service.</span></span>

<span data-ttu-id="fb441-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fb441-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb441-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb441-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Time Synchronization";
  string  Description = "Microsoft Time Synchronization Service Setting Data";
  string  ElementName = "Time Synchronization";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Time Synchronization Component";
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

## <a name="members"></a><span data-ttu-id="fb441-107">Member</span><span class="sxs-lookup"><span data-stu-id="fb441-107">Members</span></span>

<span data-ttu-id="fb441-108">Die **MSVM \_ timesynccomponentsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fb441-108">The **Msvm\_TimeSyncComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fb441-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb441-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb441-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb441-110">Properties</span></span>

<span data-ttu-id="fb441-111">Die **MSVM \_ timesynccomponentsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fb441-111">The **Msvm\_TimeSyncComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb441-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="fb441-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb441-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-115">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="fb441-115">The address of the resource.</span></span> <span data-ttu-id="fb441-116">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-117">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="fb441-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb441-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-120">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="fb441-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="fb441-121">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="fb441-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="fb441-122">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-123">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="fb441-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb441-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-126">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb441-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="fb441-127">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-128">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="fb441-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fb441-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-131">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fb441-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="fb441-132">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-133">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="fb441-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fb441-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-136">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="fb441-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="fb441-137">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fb441-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb441-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-141">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fb441-141">A short description of the object.</span></span> <span data-ttu-id="fb441-142">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="fb441-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-144">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fb441-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fb441-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-146">Das, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="fb441-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="fb441-147">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-148">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="fb441-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-149">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb441-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-151">Die Consumer, die für die zugeordnete Ressource sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="fb441-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="fb441-152">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="fb441-153">Wert</span><span class="sxs-lookup"><span data-stu-id="fb441-153">Value</span></span>                                                                        | <span data-ttu-id="fb441-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fb441-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="fb441-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fb441-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="fb441-156">Virtualisierten</span><span class="sxs-lookup"><span data-stu-id="fb441-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fb441-157">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb441-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb441-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-160">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="fb441-160">A description of the object.</span></span> <span data-ttu-id="fb441-161">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fb441-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb441-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-165">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fb441-165">A display name for the object.</span></span> <span data-ttu-id="fb441-166">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="fb441-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-168">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb441-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-170">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="fb441-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="fb441-171">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span></span>

<dt>



 <span data-ttu-id="fb441-172">(2)</span><span class="sxs-lookup"><span data-stu-id="fb441-172">(2)</span></span>


</dt> <dd>

<span data-ttu-id="fb441-173">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="fb441-173">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="fb441-174">3</span><span class="sxs-lookup"><span data-stu-id="fb441-174">3</span></span>
</dt> <dd>

<span data-ttu-id="fb441-175">Disabled</span><span class="sxs-lookup"><span data-stu-id="fb441-175">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fb441-176">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="fb441-176">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-177">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fb441-177">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fb441-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-179">Macht eine bestimmte Zuweisung zum Hosten von oder zugrunde liegenden Ressourcen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fb441-179">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="fb441-180">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fb441-180">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fb441-181">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fb441-181">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb441-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb441-184">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="fb441-184">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fb441-185">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="fb441-185">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fb441-186">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-187">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="fb441-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-188">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fb441-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-190">Die obere Grenze oder die maximale Ressourcen Menge, die für diese Zuweisung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="fb441-190">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="fb441-191">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-192">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="fb441-192">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-193">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb441-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-195">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="fb441-195">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="fb441-196">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-197">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="fb441-197">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb441-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-200">Der Ressourcentyp, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** den Wert "Other" hat.</span><span class="sxs-lookup"><span data-stu-id="fb441-200">The resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="fb441-201">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-202">**Parent**</span><span class="sxs-lookup"><span data-stu-id="fb441-202">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb441-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-205">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="fb441-205">The parent of the resource.</span></span> <span data-ttu-id="fb441-206">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-207">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="fb441-207">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb441-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-210">Die ID des Ressourcenpools, dem die Ressource zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fb441-210">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="fb441-211">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-212">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="fb441-212">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-213">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fb441-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-215">Die Menge der Ressource, die für diese Zuordnung garantiert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fb441-215">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="fb441-216">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-217">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="fb441-217">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-218">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb441-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-220">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fb441-220">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="fb441-221">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fb441-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fb441-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="fb441-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-223">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb441-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-225">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb441-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="fb441-226">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="fb441-227">Wert</span><span class="sxs-lookup"><span data-stu-id="fb441-227">Value</span></span>                                                                        | <span data-ttu-id="fb441-228">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fb441-228">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="fb441-229"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fb441-229"><dt>1</dt></span></span> </dl> | <span data-ttu-id="fb441-230">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="fb441-230">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fb441-231">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="fb441-231">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-232">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fb441-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-234">Die Menge der Ressourcen, die dem Consumer vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fb441-234">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="fb441-235">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-236">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="fb441-236">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb441-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-239">Gibt die Maßeinheit für diese Ressourcenzuweisung an.</span><span class="sxs-lookup"><span data-stu-id="fb441-239">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="fb441-240">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="fb441-240">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="fb441-241">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fb441-242">**Weight**</span><span class="sxs-lookup"><span data-stu-id="fb441-242">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb441-243">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fb441-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb441-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb441-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb441-245">Eine relative Priorität für diese Zuordnung in Bezug auf andere Zuordnungen desselben Ressourcenpools.</span><span class="sxs-lookup"><span data-stu-id="fb441-245">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="fb441-246">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fb441-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb441-247">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb441-247">Remarks</span></span>

<span data-ttu-id="fb441-248">Der Zugriff auf die **MSVM \_ timesynccomponentsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="fb441-248">Access to the **Msvm\_TimeSyncComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fb441-249">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fb441-249">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb441-250">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb441-250">Requirements</span></span>



| <span data-ttu-id="fb441-251">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb441-251">Requirement</span></span> | <span data-ttu-id="fb441-252">Wert</span><span class="sxs-lookup"><span data-stu-id="fb441-252">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb441-253">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb441-253">Minimum supported client</span></span><br/> | <span data-ttu-id="fb441-254">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb441-254">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fb441-255">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb441-255">Minimum supported server</span></span><br/> | <span data-ttu-id="fb441-256">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb441-256">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb441-257">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb441-257">Namespace</span></span><br/>                | <span data-ttu-id="fb441-258">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="fb441-258">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fb441-259">MOF</span><span class="sxs-lookup"><span data-stu-id="fb441-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb441-260"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fb441-260"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb441-261">DLL</span><span class="sxs-lookup"><span data-stu-id="fb441-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb441-262"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fb441-262"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fb441-263">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb441-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb441-264">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="fb441-264">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="fb441-265">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="fb441-265">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

