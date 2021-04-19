---
description: Stellt den konfigurierten Status des Schlüssel-Wert-Paar-Exchange-Dienstanbieter dar.
ms.assetid: B7ED1091-E49A-4C38-9794-E074E6B9EF48
title: Msvm_KvpExchangeComponentSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponentSettingData
- Msvm_KvpExchangeComponentSettingData.DisableHostKVPItems
- Msvm_KvpExchangeComponentSettingData.InstanceID
- Msvm_KvpExchangeComponentSettingData.Caption
- Msvm_KvpExchangeComponentSettingData.Description
- Msvm_KvpExchangeComponentSettingData.ElementName
- Msvm_KvpExchangeComponentSettingData.ResourceType
- Msvm_KvpExchangeComponentSettingData.OtherResourceType
- Msvm_KvpExchangeComponentSettingData.ResourceSubType
- Msvm_KvpExchangeComponentSettingData.PoolID
- Msvm_KvpExchangeComponentSettingData.ConsumerVisibility
- Msvm_KvpExchangeComponentSettingData.HostResource
- Msvm_KvpExchangeComponentSettingData.AllocationUnits
- Msvm_KvpExchangeComponentSettingData.VirtualQuantity
- Msvm_KvpExchangeComponentSettingData.Reservation
- Msvm_KvpExchangeComponentSettingData.Limit
- Msvm_KvpExchangeComponentSettingData.Weight
- Msvm_KvpExchangeComponentSettingData.AutomaticAllocation
- Msvm_KvpExchangeComponentSettingData.AutomaticDeallocation
- Msvm_KvpExchangeComponentSettingData.Parent
- Msvm_KvpExchangeComponentSettingData.Connection
- Msvm_KvpExchangeComponentSettingData.Address
- Msvm_KvpExchangeComponentSettingData.MappingBehavior
- Msvm_KvpExchangeComponentSettingData.AddressOnParent
- Msvm_KvpExchangeComponentSettingData.VirtualQuantityUnits
- Msvm_KvpExchangeComponentSettingData.EnabledState
- Msvm_KvpExchangeComponentSettingData.HostExchangeItems
- Msvm_KvpExchangeComponentSettingData.HostOnlyItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2fe2ef128d3212ba2dfd47a3d71f713c26ba2435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349202"
---
# <a name="msvm_kvpexchangecomponentsettingdata-class"></a><span data-ttu-id="c829e-103">MSVM- \_ kvpexchangecomponentsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="c829e-103">Msvm\_KvpExchangeComponentSettingData class</span></span>

<span data-ttu-id="c829e-104">Stellt den konfigurierten Status des Schlüssel-Wert-Paar-Exchange-Dienstanbieter dar.</span><span class="sxs-lookup"><span data-stu-id="c829e-104">Represents the configured state of the key/value pair exchange service.</span></span>

<span data-ttu-id="c829e-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c829e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c829e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c829e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponentSettingData : CIM_ResourceAllocationSettingData
{
  boolean DisableHostKVPItems;
  string  InstanceID;
  string  Caption = "Key-Value Pair Exchange";
  string  Description = "Microsoft Key-Value Pair Exchange Service Setting Data";
  string  ElementName = "Key-Value Pair Exchange";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Key-Value Pair Exchange Component";
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
  String  HostExchangeItems[];
  String  HostOnlyItems[];
};
```

## <a name="members"></a><span data-ttu-id="c829e-107">Member</span><span class="sxs-lookup"><span data-stu-id="c829e-107">Members</span></span>

<span data-ttu-id="c829e-108">Die **MSVM \_ kvpexchangecomponentsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c829e-108">The **Msvm\_KvpExchangeComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c829e-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c829e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c829e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c829e-110">Properties</span></span>

<span data-ttu-id="c829e-111">Die **MSVM- \_ kvpexchangecomponentsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c829e-111">The **Msvm\_KvpExchangeComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c829e-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="c829e-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c829e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-115">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c829e-115">The address of the resource.</span></span> <span data-ttu-id="c829e-116">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c829e-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c829e-117">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="c829e-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c829e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-120">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="c829e-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="c829e-121">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c829e-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="c829e-122">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-123">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="c829e-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c829e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-126">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c829e-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="c829e-127">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-128">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="c829e-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c829e-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-131">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c829e-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="c829e-132">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-133">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="c829e-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c829e-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-136">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="c829e-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="c829e-137">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c829e-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c829e-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-141">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c829e-141">A short description of the object.</span></span> <span data-ttu-id="c829e-142">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="c829e-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-144">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c829e-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c829e-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-146">Das, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c829e-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="c829e-147">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c829e-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c829e-148">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="c829e-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-149">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c829e-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-151">Die Consumer, die für die zugeordnete Ressource sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="c829e-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="c829e-152">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="c829e-153">Wert</span><span class="sxs-lookup"><span data-stu-id="c829e-153">Value</span></span>                                                                        | <span data-ttu-id="c829e-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c829e-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="c829e-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c829e-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="c829e-156">Virtualisierten</span><span class="sxs-lookup"><span data-stu-id="c829e-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c829e-157">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c829e-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c829e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-160">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="c829e-160">A description of the object.</span></span> <span data-ttu-id="c829e-161">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-162">**Disablehostkvpitems**</span><span class="sxs-lookup"><span data-stu-id="c829e-162">**DisableHostKVPItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-163">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c829e-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-164">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c829e-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c829e-165">Mit dieser Eigenschaft wird verhindert, dass der Host automatisch die Hostnamen-und Betriebssysteminformationen im Gast auffüllt.</span><span class="sxs-lookup"><span data-stu-id="c829e-165">This property disables the host from automatically populatinghost name and OS information inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="c829e-166">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c829e-166">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="c829e-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c829e-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c829e-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-170">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c829e-170">A display name for the object.</span></span> <span data-ttu-id="c829e-171">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-172">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c829e-172">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-173">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c829e-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-175">Der aktivierte Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="c829e-175">The enabled state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c829e-176">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="c829e-176">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c829e-177">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="c829e-177">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c829e-178">**Hostexchangeitems**</span><span class="sxs-lookup"><span data-stu-id="c829e-178">**HostExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-179">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c829e-179">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="c829e-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c829e-181">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), **hypervembeddedinstance** ("MSVM \_ kvpexchangedataitem")</span><span class="sxs-lookup"><span data-stu-id="c829e-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="c829e-182">Ein Array von eingebetteten [**MSVM- \_ kvpexchangedataitem**](msvm-kvpexchangedataitem.md) -Instanzen, die die Schlüssel-Wert-Paare darstellen.</span><span class="sxs-lookup"><span data-stu-id="c829e-182">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances that represent the key/value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="c829e-183">**Hostonlyitems**</span><span class="sxs-lookup"><span data-stu-id="c829e-183">**HostOnlyItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-184">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c829e-184">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="c829e-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c829e-186">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), **hypervembeddedinstance** ("MSVM \_ kvpexchangedataitem")</span><span class="sxs-lookup"><span data-stu-id="c829e-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="c829e-187">Ein Array von [**MSVM- \_ kvpexchangedataitem**](msvm-kvpexchangedataitem.md) -Instanzen, das die Schlüssel-Wert-Paare enthält, die in der Konfigurationsdatei gespeichert, aber nicht mit dem Gast Betriebssystem ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="c829e-187">An array of [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances containing the key/value pairs that are stored in the configuration file but not exchanged with the guest operating system.</span></span> <span data-ttu-id="c829e-188">Dies ermöglicht Anwendungen das Speichern von virtuellen computerspezifischen Daten, die für das Gast Betriebssystem nicht sichtbar sein müssen.</span><span class="sxs-lookup"><span data-stu-id="c829e-188">This allows applications to store virtual machine-specific data that does not need to be visible to the guest operating system.</span></span> <span data-ttu-id="c829e-189">Die Elemente werden genauso formatiert wie die Elemente in der **hostexchangeitems** -Eigenschaft, mit der Ausnahme, dass die **Source** -Eigenschaft der **MSVM-Instanz von \_ kvpexchangedataitem** auf 4 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c829e-189">The items are formatted the same as the items in the **HostExchangeItems** property except the **Source** property of the **Msvm\_KvpExchangeDataItem** instance is set to 4.</span></span> <span data-ttu-id="c829e-190">Jede Konfigurationsdatei ist auf 128 Schlüssel/Wert-Paare beschränkt, wobei jedes Wertfeld bis zu 16 KB groß sein darf und das Schlüsselfeld bis zu 512 Byte groß sein darf.</span><span class="sxs-lookup"><span data-stu-id="c829e-190">Each configuration file is limited to 128 key/value pairs, where each value field is allowed to be up to 16 KB in size and the key field is allowed to be up to 512 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c829e-191">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="c829e-191">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-192">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c829e-192">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c829e-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-194">Macht eine bestimmte Zuweisung zum Hosten von oder zugrunde liegenden Ressourcen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c829e-194">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="c829e-195">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c829e-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c829e-196">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c829e-196">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c829e-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c829e-199">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="c829e-199">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c829e-200">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="c829e-200">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c829e-201">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-202">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="c829e-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-203">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c829e-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-205">Die obere Grenze oder die maximale Ressourcen Menge, die für diese Zuweisung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="c829e-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="c829e-206">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-207">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="c829e-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-208">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c829e-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-210">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="c829e-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="c829e-211">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c829e-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c829e-212">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="c829e-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c829e-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-215">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="c829e-215">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="c829e-216">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="c829e-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-218">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c829e-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-220">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c829e-220">The parent of the resource.</span></span> <span data-ttu-id="c829e-221">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c829e-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c829e-222">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="c829e-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c829e-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-225">Die ID des Ressourcenpools, dem die Ressource zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c829e-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="c829e-226">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-227">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="c829e-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-228">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c829e-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-230">Die Menge der Ressource, die für diese Zuordnung garantiert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c829e-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="c829e-231">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-232">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="c829e-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-233">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c829e-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-235">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c829e-235">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="c829e-236">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="c829e-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-238">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c829e-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-240">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="c829e-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="c829e-241">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="c829e-242">Wert</span><span class="sxs-lookup"><span data-stu-id="c829e-242">Value</span></span>                                                                        | <span data-ttu-id="c829e-243">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c829e-243">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="c829e-244"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c829e-244"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c829e-245">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="c829e-245">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c829e-246">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="c829e-246">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-247">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c829e-247">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-249">Die Menge der Ressourcen, die dem Consumer vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c829e-249">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="c829e-250">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-250">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-251">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="c829e-251">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c829e-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-254">Gibt die Maßeinheit für diese Ressourcenzuweisung an.</span><span class="sxs-lookup"><span data-stu-id="c829e-254">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="c829e-255">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="c829e-255">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="c829e-256">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-256">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c829e-257">**Weight**</span><span class="sxs-lookup"><span data-stu-id="c829e-257">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c829e-258">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c829e-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c829e-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c829e-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c829e-260">Eine relative Priorität für diese Zuordnung in Bezug auf andere Zuordnungen desselben Ressourcenpools.</span><span class="sxs-lookup"><span data-stu-id="c829e-260">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="c829e-261">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c829e-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c829e-262">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c829e-262">Remarks</span></span>

<span data-ttu-id="c829e-263">Der Zugriff auf die **MSVM-Klasse " \_ kvpexchangecomponentsettingdata** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="c829e-263">Access to the **Msvm\_KvpExchangeComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c829e-264">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c829e-264">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c829e-265">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c829e-265">Requirements</span></span>



| <span data-ttu-id="c829e-266">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c829e-266">Requirement</span></span> | <span data-ttu-id="c829e-267">Wert</span><span class="sxs-lookup"><span data-stu-id="c829e-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c829e-268">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c829e-268">Minimum supported client</span></span><br/> | <span data-ttu-id="c829e-269">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c829e-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c829e-270">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c829e-270">Minimum supported server</span></span><br/> | <span data-ttu-id="c829e-271">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c829e-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c829e-272">Namespace</span><span class="sxs-lookup"><span data-stu-id="c829e-272">Namespace</span></span><br/>                | <span data-ttu-id="c829e-273">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c829e-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c829e-274">MOF</span><span class="sxs-lookup"><span data-stu-id="c829e-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c829e-275"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c829e-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c829e-276">DLL</span><span class="sxs-lookup"><span data-stu-id="c829e-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c829e-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c829e-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c829e-278">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c829e-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c829e-279">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="c829e-279">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="c829e-280">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="c829e-280">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

