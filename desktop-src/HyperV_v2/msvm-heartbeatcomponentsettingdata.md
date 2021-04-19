---
description: Stellt den konfigurierten Status des Takt dienstankts dar.
ms.assetid: 2946FA02-A751-4576-BB8A-004C80E21E5B
title: Msvm_HeartbeatComponentSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponentSettingData
- Msvm_HeartbeatComponentSettingData.InstanceID
- Msvm_HeartbeatComponentSettingData.Caption
- Msvm_HeartbeatComponentSettingData.Description
- Msvm_HeartbeatComponentSettingData.ElementName
- Msvm_HeartbeatComponentSettingData.ResourceType
- Msvm_HeartbeatComponentSettingData.OtherResourceType
- Msvm_HeartbeatComponentSettingData.ResourceSubType
- Msvm_HeartbeatComponentSettingData.PoolID
- Msvm_HeartbeatComponentSettingData.ConsumerVisibility
- Msvm_HeartbeatComponentSettingData.HostResource
- Msvm_HeartbeatComponentSettingData.AllocationUnits
- Msvm_HeartbeatComponentSettingData.VirtualQuantity
- Msvm_HeartbeatComponentSettingData.Reservation
- Msvm_HeartbeatComponentSettingData.Limit
- Msvm_HeartbeatComponentSettingData.Weight
- Msvm_HeartbeatComponentSettingData.AutomaticAllocation
- Msvm_HeartbeatComponentSettingData.AutomaticDeallocation
- Msvm_HeartbeatComponentSettingData.Parent
- Msvm_HeartbeatComponentSettingData.Connection
- Msvm_HeartbeatComponentSettingData.Address
- Msvm_HeartbeatComponentSettingData.MappingBehavior
- Msvm_HeartbeatComponentSettingData.AddressOnParent
- Msvm_HeartbeatComponentSettingData.VirtualQuantityUnits
- Msvm_HeartbeatComponentSettingData.EnabledState
- Msvm_HeartbeatComponentSettingData.ErrorThreshold
- Msvm_HeartbeatComponentSettingData.Interval
- Msvm_HeartbeatComponentSettingData.Latency
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a36afbd8ab17a3fc2dfddb99b0a648fddbada415
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348810"
---
# <a name="msvm_heartbeatcomponentsettingdata-class"></a><span data-ttu-id="b851e-103">MSVM \_ heartbeatcomponentsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="b851e-103">Msvm\_HeartbeatComponentSettingData class</span></span>

<span data-ttu-id="b851e-104">Stellt den konfigurierten Status des Takt dienstankts dar.</span><span class="sxs-lookup"><span data-stu-id="b851e-104">Represents the configured state of the heartbeat service.</span></span>

<span data-ttu-id="b851e-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b851e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b851e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b851e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Heartbeat";
  string  Description = "Microsoft Heartbeat Service Setting Data";
  string  ElementName = "Heartbeat";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft Heartbeat Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Integration Components";
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
  uint32  ErrorThreshold = 2;
  uint32  Interval = 2000;
  uint32  Latency = 1000;
};
```

## <a name="members"></a><span data-ttu-id="b851e-107">Member</span><span class="sxs-lookup"><span data-stu-id="b851e-107">Members</span></span>

<span data-ttu-id="b851e-108">Die **MSVM \_ heartbeatcomponentsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b851e-108">The **Msvm\_HeartbeatComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b851e-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b851e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b851e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b851e-110">Properties</span></span>

<span data-ttu-id="b851e-111">Die **MSVM \_ heartbeatcomponentsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b851e-111">The **Msvm\_HeartbeatComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b851e-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="b851e-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b851e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-115">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b851e-115">The address of the resource.</span></span> <span data-ttu-id="b851e-116">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-117">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="b851e-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b851e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-120">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="b851e-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="b851e-121">Die über **geordneten** / **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung und die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b851e-121">The **Parent**/**AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="b851e-122">Wenn das übergeordnete Element z. b. ein PCI-Controller ist, würde diese Eigenschaft den PCI-Slot dieses untergeordneten Geräts angeben.</span><span class="sxs-lookup"><span data-stu-id="b851e-122">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span> <span data-ttu-id="b851e-123">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-124">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="b851e-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b851e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-127">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b851e-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="b851e-128">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf "Integrations Komponenten" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Integration Components".</span></span>

</dd> <dt>

<span data-ttu-id="b851e-129">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="b851e-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-130">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b851e-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-132">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b851e-132">Indicates whether the resource is automatically allocated.</span></span> <span data-ttu-id="b851e-133">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-134">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="b851e-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-135">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b851e-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-137">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="b851e-137">Indicates whether the resource is automatically de-allocated.</span></span> <span data-ttu-id="b851e-138">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b851e-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b851e-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-142">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b851e-142">A short description of the object.</span></span> <span data-ttu-id="b851e-143">Diese Eigenschaft wird von der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse geerbt und ist immer auf "Heartbeat" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-143">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="b851e-144">**Connection**</span><span class="sxs-lookup"><span data-stu-id="b851e-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-145">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b851e-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b851e-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-147">Das, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b851e-147">The thing to which this resource is connected.</span></span> <span data-ttu-id="b851e-148">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-149">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="b851e-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-150">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b851e-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-152">Beschreibt die Sichtbarkeit der Kunden für die zugeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="b851e-152">Describes the consumers' visibility to the allocated resource.</span></span> <span data-ttu-id="b851e-153">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf 3 (virtualisiert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="b851e-154">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b851e-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b851e-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-157">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b851e-157">A description of the object.</span></span> <span data-ttu-id="b851e-158">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft Heartbeat Service Setting Data" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="b851e-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b851e-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b851e-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-162">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b851e-162">A display name for the object.</span></span> <span data-ttu-id="b851e-163">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt und ist immer auf "Heartbeat" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Heartbeat".</span></span> <span data-ttu-id="b851e-164">Durch Ändern dieser Eigenschaft wird die **ElementName** -Eigenschaft der zugeordneten [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -Ableitung geändert.</span><span class="sxs-lookup"><span data-stu-id="b851e-164">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="b851e-165">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b851e-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-166">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b851e-166">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b851e-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-169">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="b851e-169">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="b851e-170">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b851e-170">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b851e-171">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="b851e-171">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b851e-172">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="b851e-172">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b851e-173">**Errorthreshold**</span><span class="sxs-lookup"><span data-stu-id="b851e-173">**ErrorThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-174">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b851e-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-176">Die Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="b851e-176">An administrator's startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="b851e-177">Diese Eigenschaft ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-177">This property is always set to 2 (Enabled).</span></span>

<span data-ttu-id="b851e-178">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b851e-178">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-179">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="b851e-179">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-180">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b851e-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b851e-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-182">Macht eine bestimmte Zuweisung zum Hosten von oder zugrunde liegenden Ressourcen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b851e-182">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="b851e-183">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-184">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b851e-184">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b851e-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b851e-187">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="b851e-187">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b851e-188">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b851e-188">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b851e-189">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) geerbt und ist immer auf "Microsoft:*GUID* Geräte-ID- \\ *Daten*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="b851e-190">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="b851e-190">**Interval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-191">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b851e-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-193">Das Intervall (in Millisekunden) zwischen Ping-versuchen.</span><span class="sxs-lookup"><span data-stu-id="b851e-193">The interval, in milliseconds, between ping attempts.</span></span> <span data-ttu-id="b851e-194">Diese ist immer auf 2000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-194">This is always set to 2000.</span></span>

<span data-ttu-id="b851e-195">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b851e-195">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-196">**Latenz**</span><span class="sxs-lookup"><span data-stu-id="b851e-196">**Latency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-197">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b851e-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-199">Die maximale erwartete Latenzzeit (in Millisekunden) zwischen einem Anforderungs Ping und einer Antwort, bevor eine bestimmte Anforderung als gelöscht angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="b851e-199">The maximum expected latency, in milliseconds, between a request ping and a response before a given request is considered dropped.</span></span> <span data-ttu-id="b851e-200">Diese Eigenschaft ist immer auf 1000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-200">This property is always set to 1000.</span></span>

<span data-ttu-id="b851e-201">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b851e-201">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-202">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="b851e-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-203">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b851e-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-205">Die obere Grenze oder die maximale Ressourcen Menge, die für diese Zuweisung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="b851e-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="b851e-206">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-207">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="b851e-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-208">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b851e-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-210">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="b851e-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="b851e-211">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-212">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="b851e-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b851e-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-215">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und die **ResourceType** -Eigenschaft den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="b851e-215">A string that describes the resource type when a well-defined value is not available and the **ResourceType** property has the value 1 (Other).</span></span> <span data-ttu-id="b851e-216">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf "Microsoft Heartbeat Component" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Microsoft Heartbeat Component".</span></span>

</dd> <dt>

<span data-ttu-id="b851e-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="b851e-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-218">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b851e-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-220">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b851e-220">The parent of the resource.</span></span> <span data-ttu-id="b851e-221">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-222">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="b851e-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b851e-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-225">Die ID des Ressourcenpools, dem die Ressource zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b851e-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="b851e-226">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b851e-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b851e-227">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="b851e-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-228">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b851e-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-230">Die Menge der Ressource, die für diese Zuordnung garantiert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b851e-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="b851e-231">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-232">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="b851e-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-233">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b851e-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-235">Ein Implementierungs spezifischer Untertyp für diese Ressource.</span><span class="sxs-lookup"><span data-stu-id="b851e-235">An implementation specific subtype for this resource.</span></span> <span data-ttu-id="b851e-236">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="b851e-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-238">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b851e-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-240">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="b851e-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="b851e-241">Diese Eigenschaft wird von der [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Klasse geerbt und ist immer auf 1 (sonstige) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-241">This property is inherited from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class and is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="b851e-242">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="b851e-242">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-243">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b851e-243">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-245">Die Menge der Ressourcen, die dem Consumer vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b851e-245">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="b851e-246">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="b851e-247">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="b851e-247">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-248">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b851e-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-250">Gibt die Einheiten an, die von der **virtualmenge** -Eigenschaft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b851e-250">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="b851e-251">Wenn z. b. ResourceType = Processor ist, kann der Wert der **virtualquantityunits** -Eigenschaft auf "count" festgelegt werden, um anzugeben, dass der Wert der **virtualmenge** -Eigenschaft als "count" ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="b851e-251">For example, if ResourceType=Processor, the value of the **VirtualQuantityUnits** property can be set to "count", indicating that the value of the **VirtualQuantity** property is expressed as a count.</span></span> <span data-ttu-id="b851e-252">Wenn ResourceType = Memory, kann der Wert der **virtualquantityunits** -Eigenschaft auf "Bytes \* 10 ^ 3" festgelegt werden, um anzugeben, dass der Wert der **virtualmenge** -Eigenschaft in Kilobyte ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="b851e-252">If ResourceType=Memory, the value of the **VirtualQuantityUnits** property can be set to "bytes\*10^3", indicating that the value of the **VirtualQuantity** property is expressed in kilobytes.</span></span> <span data-ttu-id="b851e-253">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf "count" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-253">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "count".</span></span>

</dd> <dt>

<span data-ttu-id="b851e-254">**Weight**</span><span class="sxs-lookup"><span data-stu-id="b851e-254">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b851e-255">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b851e-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b851e-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b851e-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b851e-257">Die relative Priorität für diese Zuordnung in Bezug auf andere Zuordnungen desselben Ressourcenpools.</span><span class="sxs-lookup"><span data-stu-id="b851e-257">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="b851e-258">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b851e-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b851e-259">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b851e-259">Remarks</span></span>

<span data-ttu-id="b851e-260">Der Zugriff auf die **MSVM-Klasse " \_ heartbeatcomponentsettingdata** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="b851e-260">Access to the **Msvm\_HeartbeatComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b851e-261">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b851e-261">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b851e-262">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b851e-262">Requirements</span></span>



| <span data-ttu-id="b851e-263">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b851e-263">Requirement</span></span> | <span data-ttu-id="b851e-264">Wert</span><span class="sxs-lookup"><span data-stu-id="b851e-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b851e-265">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b851e-265">Minimum supported client</span></span><br/> | <span data-ttu-id="b851e-266">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b851e-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b851e-267">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b851e-267">Minimum supported server</span></span><br/> | <span data-ttu-id="b851e-268">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b851e-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b851e-269">Namespace</span><span class="sxs-lookup"><span data-stu-id="b851e-269">Namespace</span></span><br/>                | <span data-ttu-id="b851e-270">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b851e-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b851e-271">MOF</span><span class="sxs-lookup"><span data-stu-id="b851e-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b851e-272"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b851e-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b851e-273">DLL</span><span class="sxs-lookup"><span data-stu-id="b851e-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b851e-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b851e-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b851e-275">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b851e-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b851e-276">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="b851e-276">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="b851e-277">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="b851e-277">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="b851e-278">**MSVM \_ heartbeatcomponentsettingdata**</span><span class="sxs-lookup"><span data-stu-id="b851e-278">**Msvm\_HeartbeatComponentSettingData**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponentsettingdata)
</dt> </dl>

 

