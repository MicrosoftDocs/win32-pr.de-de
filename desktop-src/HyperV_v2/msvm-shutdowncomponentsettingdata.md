---
description: Stellt den konfigurierten Status des herunter Fahr Dienstanbieter dar.
ms.assetid: 434DE26A-E78A-403A-AFAB-2F9272426A16
title: Msvm_ShutdownComponentSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponentSettingData
- Msvm_ShutdownComponentSettingData.InstanceID
- Msvm_ShutdownComponentSettingData.Caption
- Msvm_ShutdownComponentSettingData.Description
- Msvm_ShutdownComponentSettingData.ElementName
- Msvm_ShutdownComponentSettingData.ResourceType
- Msvm_ShutdownComponentSettingData.OtherResourceType
- Msvm_ShutdownComponentSettingData.ResourceSubType
- Msvm_ShutdownComponentSettingData.PoolID
- Msvm_ShutdownComponentSettingData.ConsumerVisibility
- Msvm_ShutdownComponentSettingData.HostResource
- Msvm_ShutdownComponentSettingData.AllocationUnits
- Msvm_ShutdownComponentSettingData.VirtualQuantity
- Msvm_ShutdownComponentSettingData.Reservation
- Msvm_ShutdownComponentSettingData.Limit
- Msvm_ShutdownComponentSettingData.Weight
- Msvm_ShutdownComponentSettingData.AutomaticAllocation
- Msvm_ShutdownComponentSettingData.AutomaticDeallocation
- Msvm_ShutdownComponentSettingData.Parent
- Msvm_ShutdownComponentSettingData.Connection
- Msvm_ShutdownComponentSettingData.Address
- Msvm_ShutdownComponentSettingData.MappingBehavior
- Msvm_ShutdownComponentSettingData.AddressOnParent
- Msvm_ShutdownComponentSettingData.VirtualQuantityUnits
- Msvm_ShutdownComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8ee2fcb910dc788b01a58544bbfe6a06ba215585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215130"
---
# <a name="msvm_shutdowncomponentsettingdata-class"></a><span data-ttu-id="a1623-103">MSVM \_ shutdowncomponentsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="a1623-103">Msvm\_ShutdownComponentSettingData class</span></span>

<span data-ttu-id="a1623-104">Stellt den konfigurierten Status des herunter Fahr Dienstanbieter dar.</span><span class="sxs-lookup"><span data-stu-id="a1623-104">Represents the configured state of the shutdown service.</span></span>

<span data-ttu-id="a1623-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1623-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1623-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1623-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Shutdown";
  string  Description = "Microsoft Shutdown Service Setting Data";
  string  ElementName = "Shutdown";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Shutdown Component";
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

## <a name="members"></a><span data-ttu-id="a1623-107">Member</span><span class="sxs-lookup"><span data-stu-id="a1623-107">Members</span></span>

<span data-ttu-id="a1623-108">Die **MSVM \_ shutdowncomponentsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a1623-108">The **Msvm\_ShutdownComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a1623-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1623-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1623-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1623-110">Properties</span></span>

<span data-ttu-id="a1623-111">Die **MSVM \_ shutdowncomponentsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1623-111">The **Msvm\_ShutdownComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1623-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="a1623-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1623-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-115">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a1623-115">The address of the resource.</span></span> <span data-ttu-id="a1623-116">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-117">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="a1623-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1623-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-120">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="a1623-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="a1623-121">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a1623-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="a1623-122">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-123">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="a1623-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1623-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-126">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1623-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="a1623-127">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-128">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="a1623-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a1623-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-131">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a1623-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="a1623-132">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-133">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="a1623-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a1623-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-136">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="a1623-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="a1623-137">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a1623-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1623-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-141">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1623-141">A short description of the object.</span></span> <span data-ttu-id="a1623-142">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Herunterfahren" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a1623-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Shutdown".</span></span>

</dd> <dt>

<span data-ttu-id="a1623-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="a1623-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-144">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a1623-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1623-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-146">Das, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="a1623-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="a1623-147">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-148">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="a1623-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-149">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1623-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-151">Die Consumer, die für die zugeordnete Ressource sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="a1623-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="a1623-152">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="a1623-153">Wert</span><span class="sxs-lookup"><span data-stu-id="a1623-153">Value</span></span>                                                                        | <span data-ttu-id="a1623-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a1623-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="a1623-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a1623-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="a1623-156">Virtualisierten</span><span class="sxs-lookup"><span data-stu-id="a1623-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1623-157">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1623-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1623-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-160">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1623-160">A description of the object.</span></span> <span data-ttu-id="a1623-161">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a1623-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1623-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-165">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a1623-165">A display name for the object.</span></span> <span data-ttu-id="a1623-166">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a1623-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-168">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1623-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-170">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="a1623-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="a1623-171">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a1623-172">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="a1623-172">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a1623-173">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="a1623-173">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a1623-174">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="a1623-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-175">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a1623-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1623-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-177">Macht eine bestimmte Zuweisung zum Hosten von oder zugrunde liegenden Ressourcen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a1623-177">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="a1623-178">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-178">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-179">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a1623-179">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1623-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1623-182">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a1623-182">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a1623-183">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="a1623-183">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a1623-184">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-185">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="a1623-185">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-186">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a1623-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-188">Die obere Grenze oder die maximale Ressourcen Menge, die für diese Zuweisung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="a1623-188">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="a1623-189">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-190">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="a1623-190">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-191">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1623-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-193">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="a1623-193">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="a1623-194">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-195">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="a1623-195">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1623-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-198">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="a1623-198">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="a1623-199">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-200">**Parent**</span><span class="sxs-lookup"><span data-stu-id="a1623-200">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1623-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-203">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a1623-203">The parent of the resource.</span></span> <span data-ttu-id="a1623-204">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-205">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="a1623-205">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-206">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1623-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-208">Die ID des Ressourcenpools, dem die Ressource zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a1623-208">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="a1623-209">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-210">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="a1623-210">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-211">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a1623-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-213">Die Menge der Ressource, die für diese Zuordnung garantiert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a1623-213">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="a1623-214">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-214">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-215">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="a1623-215">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1623-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-218">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a1623-218">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="a1623-219">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="a1623-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-221">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1623-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-223">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="a1623-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="a1623-224">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="a1623-225">Wert</span><span class="sxs-lookup"><span data-stu-id="a1623-225">Value</span></span>                                                                        | <span data-ttu-id="a1623-226">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a1623-226">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="a1623-227"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a1623-227"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a1623-228">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="a1623-228">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1623-229">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="a1623-229">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-230">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a1623-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-232">Die Menge der Ressourcen, die dem Consumer vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a1623-232">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="a1623-233">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-233">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-234">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="a1623-234">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-235">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1623-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-237">Gibt die Maßeinheit für diese Ressourcenzuweisung an.</span><span class="sxs-lookup"><span data-stu-id="a1623-237">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="a1623-238">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="a1623-238">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="a1623-239">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-239">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a1623-240">**Weight**</span><span class="sxs-lookup"><span data-stu-id="a1623-240">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1623-241">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1623-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1623-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1623-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1623-243">Eine relative Priorität für diese Zuordnung in Bezug auf andere Zuordnungen desselben Ressourcenpools.</span><span class="sxs-lookup"><span data-stu-id="a1623-243">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="a1623-244">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1623-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1623-245">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1623-245">Remarks</span></span>

<span data-ttu-id="a1623-246">Der Zugriff auf die **MSVM \_ shutdowncomponentsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="a1623-246">Access to the **Msvm\_ShutdownComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a1623-247">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a1623-247">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1623-248">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1623-248">Requirements</span></span>



| <span data-ttu-id="a1623-249">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1623-249">Requirement</span></span> | <span data-ttu-id="a1623-250">Wert</span><span class="sxs-lookup"><span data-stu-id="a1623-250">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1623-251">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1623-251">Minimum supported client</span></span><br/> | <span data-ttu-id="a1623-252">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1623-252">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a1623-253">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1623-253">Minimum supported server</span></span><br/> | <span data-ttu-id="a1623-254">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1623-254">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a1623-255">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1623-255">Namespace</span></span><br/>                | <span data-ttu-id="a1623-256">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a1623-256">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a1623-257">MOF</span><span class="sxs-lookup"><span data-stu-id="a1623-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1623-258"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a1623-258"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1623-259">DLL</span><span class="sxs-lookup"><span data-stu-id="a1623-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1623-260"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a1623-260"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a1623-261">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1623-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1623-262">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="a1623-262">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="a1623-263">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="a1623-263">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

