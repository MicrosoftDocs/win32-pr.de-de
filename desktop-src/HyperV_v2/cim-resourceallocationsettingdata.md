---
description: Stellt Einstellungen für eine zugeordnete Ressource dar, die sich außerhalb des Bereichs der CIM-Klasse befinden, die normalerweise zur Darstellung der Ressource selbst verwendet wird.
ms.assetid: 6261bab9-aa51-479e-bd6a-43c4a9b294a6
title: CIM_ResourceAllocationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationSettingData
- CIM_ResourceAllocationSettingData.ResourceType
- CIM_ResourceAllocationSettingData.OtherResourceType
- CIM_ResourceAllocationSettingData.ResourceSubType
- CIM_ResourceAllocationSettingData.PoolID
- CIM_ResourceAllocationSettingData.ConsumerVisibility
- CIM_ResourceAllocationSettingData.HostResource
- CIM_ResourceAllocationSettingData.AllocationUnits
- CIM_ResourceAllocationSettingData.VirtualQuantity
- CIM_ResourceAllocationSettingData.Reservation
- CIM_ResourceAllocationSettingData.Limit
- CIM_ResourceAllocationSettingData.Weight
- CIM_ResourceAllocationSettingData.AutomaticAllocation
- CIM_ResourceAllocationSettingData.AutomaticDeallocation
- CIM_ResourceAllocationSettingData.Parent
- CIM_ResourceAllocationSettingData.Connection
- CIM_ResourceAllocationSettingData.Address
- CIM_ResourceAllocationSettingData.MappingBehavior
- CIM_ResourceAllocationSettingData.AddressOnParent
- CIM_ResourceAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22289511f454e0d3b128d0e73d32687924c7a7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348023"
---
# <a name="cim_resourceallocationsettingdata-class"></a><span data-ttu-id="58f72-103">CIM \_ resourcezucationsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="58f72-103">CIM\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="58f72-104">Stellt Einstellungen für eine zugeordnete Ressource dar, die sich außerhalb des Bereichs der CIM-Klasse befinden, die normalerweise zur Darstellung der Ressource selbst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58f72-104">Represents settings for an allocated resource that are outside the scope of the CIM class typically used to represent the resource itself.</span></span> <span data-ttu-id="58f72-105">Diese Einstellungen enthalten spezifische Informationen für die Zuordnung, die für den Consumer der Ressource möglicherweise nicht sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="58f72-105">These settings include information specific to the allocation that may not be visible to the consumer of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f72-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="58f72-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourceAllocationSettingData : CIM_SettingData
{
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

## <a name="members"></a><span data-ttu-id="58f72-107">Member</span><span class="sxs-lookup"><span data-stu-id="58f72-107">Members</span></span>

<span data-ttu-id="58f72-108">Die **CIM \_ resourcezucationsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="58f72-108">The **CIM\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="58f72-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58f72-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58f72-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58f72-110">Properties</span></span>

<span data-ttu-id="58f72-111">Die **CIM \_ resourcezucationsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="58f72-111">The **CIM\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58f72-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="58f72-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58f72-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58f72-115">Die Adresse der Ressource, z. b. die Mac-Adresse eines Ethernet-Ports.</span><span class="sxs-lookup"><span data-stu-id="58f72-115">The address of the resource, for example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-116">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="58f72-116">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58f72-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58f72-119">Die Adresse dieser Ressource aus dem Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="58f72-119">The address of this resource from the context of the parent.</span></span> <span data-ttu-id="58f72-120">Diese Eigenschaft wird verwendet, um eine Controller Beziehung und die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="58f72-120">This property is used to describe a controller relationship and the ordering of devices on a controller.</span></span> <span data-ttu-id="58f72-121">Wenn das übergeordnete Element z. b. ein PCI-Controller ist, würde diese Eigenschaft den PCI-Slot dieses untergeordneten Geräts angeben.</span><span class="sxs-lookup"><span data-stu-id="58f72-121">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-122">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="58f72-122">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58f72-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f72-125">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcezucationsettingdata**".**Reservierung**","**CIM \_ resourcezucationsettingdata**.**Limit**"), **ispunit**</span><span class="sxs-lookup"><span data-stu-id="58f72-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**Reservation**", "**CIM\_ResourceAllocationSettingData**.**Limit**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="58f72-126">Die von den **Reservierungs** -und **Limit** -Eigenschaften verwendeten Zuordnungs Einheiten.</span><span class="sxs-lookup"><span data-stu-id="58f72-126">The allocation units used by the **Reservation** and **Limit** properties.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-127">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="58f72-127">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="58f72-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58f72-130">" **true** ", um die Ressource automatisch zuzuordnen. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="58f72-130">**true** to automatically allocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-131">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="58f72-131">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-132">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="58f72-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58f72-134">**true** , um die Zuteilung der Ressource automatisch zu verringern. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="58f72-134">**true** to automatically deallocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-135">**Connection**</span><span class="sxs-lookup"><span data-stu-id="58f72-135">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-136">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="58f72-136">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="58f72-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58f72-138">Ein Array, das die Objekte angibt, die mit der Ressource verbunden sind, z. b. ein benanntes Netzwerk oder Switchport.</span><span class="sxs-lookup"><span data-stu-id="58f72-138">An array that indicates the objects connected to the resource, such as a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-139">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="58f72-139">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-140">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58f72-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58f72-142">Die Consumer, die für die zugeordnete Ressource sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="58f72-142">The consumers visibility to the allocated resource.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="58f72-143">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="58f72-143">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>

<span data-ttu-id="58f72-144">Pass **-through** (2)</span><span class="sxs-lookup"><span data-stu-id="58f72-144">**Passed-Through** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>

<span data-ttu-id="58f72-145">**Virtualisiert** (3)</span><span class="sxs-lookup"><span data-stu-id="58f72-145">**Virtualized** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>

<span data-ttu-id="58f72-146">**Nicht dargestellt** (4)</span><span class="sxs-lookup"><span data-stu-id="58f72-146">**Not represented** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="58f72-147">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="58f72-147">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="58f72-148">**Hersteller reserviert** (32767.65535)</span><span class="sxs-lookup"><span data-stu-id="58f72-148">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="58f72-149">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="58f72-149">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-150">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="58f72-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="58f72-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f72-152">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcezucationsettingdata**".**Consumervisibility**","**CIM \_ resourcezucationsettingdata**.**Mappingbehavior**")</span><span class="sxs-lookup"><span data-stu-id="58f72-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ConsumerVisibility**", "**CIM\_ResourceAllocationSettingData**.**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="58f72-153">Ein Array, das die Zuweisung der zugeordneten Ressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="58f72-153">An array that contains the assignment of the allocated resources.</span></span> <span data-ttu-id="58f72-154">Jeder Wert, der nicht NULL ist, muss als RFC3986 basierter URI formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="58f72-154">Each non-null value of this property must be formated as an RFC3986 based URI.</span></span> <span data-ttu-id="58f72-155">Wenn die Ressource modelliert ist, sollte der Wert ein WBEM-URI sein.</span><span class="sxs-lookup"><span data-stu-id="58f72-155">If the resource is modeled, then the value should be a WBEM URI.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-156">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="58f72-156">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-157">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58f72-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f72-159">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcezucationsettingdata**".**"Zuweisung Einheiten**")</span><span class="sxs-lookup"><span data-stu-id="58f72-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="58f72-160">Die maximale Ressourcen Menge, die der Zuordnung gewährt werden soll.</span><span class="sxs-lookup"><span data-stu-id="58f72-160">The maximum amount of resource to grant to the allocation.</span></span> <span data-ttu-id="58f72-161">Der Einheitstyp dieser Eigenschaft wird durch die Eigenschaft " **Zuordnungseinheiten** " angegeben.</span><span class="sxs-lookup"><span data-stu-id="58f72-161">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-162">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="58f72-162">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-163">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58f72-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58f72-165">Gibt an, wie die Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="58f72-165">Indicates how the resource maps to underlying resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="58f72-166">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="58f72-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="58f72-167">**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="58f72-167">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="58f72-168">**Dediziert** (3)</span><span class="sxs-lookup"><span data-stu-id="58f72-168">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="58f72-169">**Weiche Affinität** (4)</span><span class="sxs-lookup"><span data-stu-id="58f72-169">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="58f72-170">**Harte Affinität** (5)</span><span class="sxs-lookup"><span data-stu-id="58f72-170">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="58f72-171">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="58f72-171">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="58f72-172">**Hersteller reserviert** (32767.65535)</span><span class="sxs-lookup"><span data-stu-id="58f72-172">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="58f72-173">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="58f72-173">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58f72-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f72-176">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcezucationsettingdata**".**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="58f72-176">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="58f72-177">Eine Beschreibung des Ressourcentyps, wenn die **ResourceType** -Eigenschaft auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="58f72-177">A description of the resource type when the **ResourceType** property is set to 1 (other).</span></span>

</dd> <dt>

<span data-ttu-id="58f72-178">**Parent**</span><span class="sxs-lookup"><span data-stu-id="58f72-178">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58f72-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58f72-181">Das übergeordnete Element der Ressource, z. b. ein Controller für die aktuelle Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="58f72-181">The parent of the resource, for example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-182">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="58f72-182">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58f72-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f72-185">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ resourcepool**](cim-resourcepool.md)".**Poolid**")</span><span class="sxs-lookup"><span data-stu-id="58f72-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="58f72-186">Die ID des Ressourcenpools, der die Ressource generiert hat.</span><span class="sxs-lookup"><span data-stu-id="58f72-186">The ID of the resource pool that generated the resource.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-187">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="58f72-187">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-188">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58f72-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f72-190">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcezucationsettingdata**".**"Zuweisung Einheiten**")</span><span class="sxs-lookup"><span data-stu-id="58f72-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="58f72-191">Die Anzahl der Ressourcen, die für diese Zuordnung garantiert verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="58f72-191">The number of resource that are guaranteed to be available for this allocation.</span></span> <span data-ttu-id="58f72-192">Auf Systemen, die eine über-und Ressourcen übereinbindung unterstützen, wird dieser Wert in der Regel für die Zugangskontrolle verwendet.</span><span class="sxs-lookup"><span data-stu-id="58f72-192">On systems that support over-commitment of resources, this value is typically used for admission control.</span></span>

<span data-ttu-id="58f72-193">Der Einheitstyp dieser Eigenschaft wird durch die Eigenschaft " **Zuordnungseinheiten** " angegeben.</span><span class="sxs-lookup"><span data-stu-id="58f72-193">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-194">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="58f72-194">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58f72-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f72-197">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcezucationsettingdata**".**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="58f72-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="58f72-198">Ein Implementierungs spezifischer Untertyp für diese Ressource.</span><span class="sxs-lookup"><span data-stu-id="58f72-198">An implementation specific sub-type for this resource.</span></span> <span data-ttu-id="58f72-199">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="58f72-199">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-200">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="58f72-200">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-201">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58f72-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f72-203">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcezucationsettingdata**".**Otherresourcetype**","**CIM \_ resourcezucationsettingdata**.**Resourcesubtype**")</span><span class="sxs-lookup"><span data-stu-id="58f72-203">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**OtherResourceType**", "**CIM\_ResourceAllocationSettingData**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="58f72-204">Der Ressourcentyp, der durch die Zuordnungs Einstellungen dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="58f72-204">The type of resource that is represented by the allocation settings.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="58f72-205">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="58f72-205">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="58f72-206">**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="58f72-206">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="58f72-207">**Prozessor** (3)</span><span class="sxs-lookup"><span data-stu-id="58f72-207">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="58f72-208">Arbeits **Speicher** (4)</span><span class="sxs-lookup"><span data-stu-id="58f72-208">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="58f72-209">**IDE-Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="58f72-209">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="58f72-210">**Paralleler SCSI-HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="58f72-210">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="58f72-211">**FC-HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="58f72-211">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="58f72-212">**iSCSI-HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="58f72-212">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="58f72-213">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="58f72-213">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="58f72-214">**Ethernet-Adapter** (10)</span><span class="sxs-lookup"><span data-stu-id="58f72-214">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="58f72-215">**Anderer Netzwerk Adapter** (11)</span><span class="sxs-lookup"><span data-stu-id="58f72-215">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="58f72-216">E **/a-Slot** (12)</span><span class="sxs-lookup"><span data-stu-id="58f72-216">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="58f72-217">E **/a-Gerät** (13)</span><span class="sxs-lookup"><span data-stu-id="58f72-217">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="58f72-218">**Diskettenlaufwerk** (14)</span><span class="sxs-lookup"><span data-stu-id="58f72-218">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="58f72-219">**CD-Laufwerk** (15)</span><span class="sxs-lookup"><span data-stu-id="58f72-219">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="58f72-220">**DVD-Laufwerk** (16)</span><span class="sxs-lookup"><span data-stu-id="58f72-220">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="58f72-221">**Laufwerk (17** )</span><span class="sxs-lookup"><span data-stu-id="58f72-221">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="58f72-222">**Bandlaufwerk** (18)</span><span class="sxs-lookup"><span data-stu-id="58f72-222">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="58f72-223">**Speicher** Block (19)</span><span class="sxs-lookup"><span data-stu-id="58f72-223">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="58f72-224">**Anderes Speichergerät** (20)</span><span class="sxs-lookup"><span data-stu-id="58f72-224">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="58f72-225">**Seriellen Anschluss** (21)</span><span class="sxs-lookup"><span data-stu-id="58f72-225">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="58f72-226">**Paralleler Anschluss** (22)</span><span class="sxs-lookup"><span data-stu-id="58f72-226">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="58f72-227">**USB-Controller** (23)</span><span class="sxs-lookup"><span data-stu-id="58f72-227">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="58f72-228">**Grafikcontroller** (24)</span><span class="sxs-lookup"><span data-stu-id="58f72-228">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="58f72-229">**IEEE 1394-Controller** (25)</span><span class="sxs-lookup"><span data-stu-id="58f72-229">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="58f72-230">**Partitionier Bare Einheit** (26)</span><span class="sxs-lookup"><span data-stu-id="58f72-230">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="58f72-231">**Partitionier bare Basiseinheit** (27)</span><span class="sxs-lookup"><span data-stu-id="58f72-231">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="58f72-232">**Energie** (28)</span><span class="sxs-lookup"><span data-stu-id="58f72-232">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="58f72-233">**Kühlkapazität** (29)</span><span class="sxs-lookup"><span data-stu-id="58f72-233">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="58f72-234">**Ethernet-Switchport** (30)</span><span class="sxs-lookup"><span data-stu-id="58f72-234">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="58f72-235">**Logischer** Datenträger (31)</span><span class="sxs-lookup"><span data-stu-id="58f72-235">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="58f72-236">**Speicher Volume** (32)</span><span class="sxs-lookup"><span data-stu-id="58f72-236">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="58f72-237">**Ethernet-Verbindung** (33)</span><span class="sxs-lookup"><span data-stu-id="58f72-237">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="58f72-238">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="58f72-238">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="58f72-239">**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="58f72-239">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="58f72-240">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="58f72-240">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-241">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58f72-241">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f72-243">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcezucationsettingdata**".**Virtualquantityunits**")</span><span class="sxs-lookup"><span data-stu-id="58f72-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="58f72-244">Die Anzahl der Ressourcen, die dem Consumer der Ressource angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="58f72-244">The number of resources presented to the consumer of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-245">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="58f72-245">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58f72-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f72-248">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcezucationsettingdata**".**Virtualmenge**"), **ispunit**</span><span class="sxs-lookup"><span data-stu-id="58f72-248">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="58f72-249">Die Einheiten, die von der **virtualmenge** -Eigenschaft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58f72-249">The units used by the **VirtualQuantity** property.</span></span>

</dd> <dt>

<span data-ttu-id="58f72-250">**Weight**</span><span class="sxs-lookup"><span data-stu-id="58f72-250">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f72-251">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58f72-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58f72-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58f72-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58f72-253">Die relative Priorität für diese Zuordnung in Bezug auf andere Zuordnungen desselben Ressourcenpools.</span><span class="sxs-lookup"><span data-stu-id="58f72-253">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58f72-254">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58f72-254">Requirements</span></span>



| <span data-ttu-id="58f72-255">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58f72-255">Requirement</span></span> | <span data-ttu-id="58f72-256">Wert</span><span class="sxs-lookup"><span data-stu-id="58f72-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58f72-257">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58f72-257">Minimum supported client</span></span><br/> | <span data-ttu-id="58f72-258">Windows 8</span><span class="sxs-lookup"><span data-stu-id="58f72-258">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="58f72-259">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58f72-259">Minimum supported server</span></span><br/> | <span data-ttu-id="58f72-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="58f72-260">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="58f72-261">Namespace</span><span class="sxs-lookup"><span data-stu-id="58f72-261">Namespace</span></span><br/>                | <span data-ttu-id="58f72-262">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="58f72-262">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="58f72-263">MOF</span><span class="sxs-lookup"><span data-stu-id="58f72-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58f72-264"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="58f72-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58f72-265">DLL</span><span class="sxs-lookup"><span data-stu-id="58f72-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58f72-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58f72-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58f72-267">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58f72-267">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f72-268">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="58f72-268">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

