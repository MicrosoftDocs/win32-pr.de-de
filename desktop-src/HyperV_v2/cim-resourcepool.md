---
description: Stellt einen Ressourcenpool dar, bei dem es sich um eine vom Host System bereitgestellte logische Entität zum Zuweisen und Zuweisen von Ressourcen handelt.
ms.assetid: c8e0b701-1814-4409-a073-017f8fea841a
title: CIM_ResourcePool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePool
- CIM_ResourcePool.InstanceID
- CIM_ResourcePool.PoolID
- CIM_ResourcePool.Primordial
- CIM_ResourcePool.Capacity
- CIM_ResourcePool.Reserved
- CIM_ResourcePool.ResourceType
- CIM_ResourcePool.OtherResourceType
- CIM_ResourcePool.ResourceSubType
- CIM_ResourcePool.AllocationUnits
- CIM_ResourcePool.ConsumedResourceUnits
- CIM_ResourcePool.CurrentlyConsumedResource
- CIM_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11a073f817da27dbbd45be26a008486a776470cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129693"
---
# <a name="cim_resourcepool-class"></a><span data-ttu-id="c4d05-103">CIM \_ resourcepool-Klasse</span><span class="sxs-lookup"><span data-stu-id="c4d05-103">CIM\_ResourcePool class</span></span>

<span data-ttu-id="c4d05-104">Stellt einen Ressourcenpool dar, bei dem es sich um eine vom Host System bereitgestellte logische Entität zum Zuweisen und Zuweisen von Ressourcen handelt.</span><span class="sxs-lookup"><span data-stu-id="c4d05-104">Represents a resource pool, which is a logical entity provided by the host system to allocate and assign resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4d05-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4d05-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourcePool : CIM_LogicalElement
{
  string  InstanceID;
  string  PoolID;
  boolean Primordial = FALSE;
  uint64  Capacity;
  uint64  Reserved;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  AllocationUnits;
  string  ConsumedResourceUnits = "count";
  uint64  CurrentlyConsumedResource;
  uint64  MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="c4d05-106">Member</span><span class="sxs-lookup"><span data-stu-id="c4d05-106">Members</span></span>

<span data-ttu-id="c4d05-107">Die **CIM \_ resourcepool** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c4d05-107">The **CIM\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="c4d05-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4d05-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4d05-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4d05-109">Properties</span></span>

<span data-ttu-id="c4d05-110">Die **CIM \_ resourcepool** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c4d05-110">The **CIM\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4d05-111">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="c4d05-111">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4d05-112">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4d05-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4d05-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-114">Qualifizierer: **ispunit**</span><span class="sxs-lookup"><span data-stu-id="c4d05-114">Qualifiers: **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="c4d05-115">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4d05-115">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="c4d05-116">Wenn **ResourceType** beispielsweise auf "Processor" festgelegt ist, kann " **zugcationunits** " auf "Hertz \* 10 ^ 6" oder "Prozent" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c4d05-116">For example, when **ResourceType** is set to "Processor", **AllocationUnits** may be set to "hertz\*10^6" or "percent".</span></span> <span data-ttu-id="c4d05-117">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmatische Einheiten aus Anhang C. 1 von *DSP0004 v 2.4* oder höher sein.</span><span class="sxs-lookup"><span data-stu-id="c4d05-117">The value of this property should be a legal value of the Programmatic Units qualifier from Appendix C.1 of *DSP0004 V2.4* or later.</span></span>

</dd> <dt>

<span data-ttu-id="c4d05-118">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="c4d05-118">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4d05-119">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4d05-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4d05-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4d05-121">Die maximale Menge an Reservierungen, die der Ressourcenpool unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="c4d05-121">The maximum amount of reservations that the resource pool can support.</span></span> <span data-ttu-id="c4d05-122">Die Eigenschaft " **Zuordnungseinheiten** " gibt den Einheitentyp an.</span><span class="sxs-lookup"><span data-stu-id="c4d05-122">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="c4d05-123">**Consumedresourceunits**</span><span class="sxs-lookup"><span data-stu-id="c4d05-123">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4d05-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4d05-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4d05-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-126">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcepool**".**Maxconsumableresource**","**CIM \_ resourcepool**.**Currentlyconsumedresource**"), **ispunit**</span><span class="sxs-lookup"><span data-stu-id="c4d05-126">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**MaxConsumableResource**", "**CIM\_ResourcePool**.**CurrentlyConsumedResource**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="c4d05-127">Die Einheiten für die **maxconsubar** und die **verbrauchten** Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c4d05-127">The units for the **MaxConsumable** and the **Consumed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="c4d05-128">**Currentlyconsumedresource**</span><span class="sxs-lookup"><span data-stu-id="c4d05-128">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4d05-129">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4d05-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4d05-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-131">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcepool**".**Consumedresourceunits**")</span><span class="sxs-lookup"><span data-stu-id="c4d05-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="c4d05-132">Die Menge der Ressource, die der Ressourcenpool derzeit für ressourcenconsumer darstellt.</span><span class="sxs-lookup"><span data-stu-id="c4d05-132">The amount of resource that the resource pool currently presents to resource consumers.</span></span> <span data-ttu-id="c4d05-133">Diese Eigenschaft unterscheidet sich von der **reservierten** Eigenschaft, da Sie die Consumer-Ansicht der Ressource beschreibt, während die **reservierte** Eigenschaft die Producer-Ansicht der Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c4d05-133">This property is different from the **Reserved** property because it describes the consumers view of the resource while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="c4d05-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c4d05-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4d05-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4d05-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4d05-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-137">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="c4d05-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="c4d05-138">Identifiziert eine Instanz dieser Klasse eindeutig innerhalb des Gültigkeits Bereichs des enthaltenden Namespace.</span><span class="sxs-lookup"><span data-stu-id="c4d05-138">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="c4d05-139">Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert der **InstanceId-** Eigenschaft im folgenden Muster erstellt werden: *OrgId*:*localId*</span><span class="sxs-lookup"><span data-stu-id="c4d05-139">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="c4d05-140">*OrgId* muss einen urheberrechtlich geschützten oder anderweitig eindeutigen Namen enthalten, der der Geschäfts Entität gehört, die die **InstanceId-** Eigenschaft definiert, oder eine registrierte ID ist, die von einer anerkannten globalen Autorität zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c4d05-140">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="c4d05-141">*OrgId* darf keinen Doppelpunkt enthalten.</span><span class="sxs-lookup"><span data-stu-id="c4d05-141">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="c4d05-142">Der erste Doppelpunkt in **InstanceId** muss zwischen der *OrgId* und der *Lok-* ID liegen.</span><span class="sxs-lookup"><span data-stu-id="c4d05-142">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="c4d05-143">*LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c4d05-143">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="c4d05-144">Wenn das obige Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceId** -Wert nicht für **InstanceId** -Eigenschaften wieder verwendet wird, die von diesem Anbieter oder von anderen Anbietern für diesen Namespace erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c4d05-144">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="c4d05-145">Für von DMTF definierte Instanzen muss das Muster verwendet werden, wenn die *OrgId* auf "CIM" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c4d05-145">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> <dt>

<span data-ttu-id="c4d05-146">**Maxconsumableresource**</span><span class="sxs-lookup"><span data-stu-id="c4d05-146">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4d05-147">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4d05-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4d05-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-149">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcepool**".**Consumedresourceunits**")</span><span class="sxs-lookup"><span data-stu-id="c4d05-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="c4d05-150">Die maximale Menge an nutzbaren Ressourcen, die der Ressourcenpool für ressourcenconsumer bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c4d05-150">The maximum of amount of consumable resources that the resource pool can present to resource consumers.</span></span> <span data-ttu-id="c4d05-151">Diese Eigenschaft unterscheidet sich von der **Capacity** -Eigenschaft, da Sie die Consumer-Ansicht der Ressource beschreibt, während die **Capacity** -Eigenschaft die Producer-Ansicht der Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c4d05-151">This property is different from the **Capacity** property because it describes the consumers view of the resource while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="c4d05-152">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="c4d05-152">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4d05-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4d05-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4d05-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-155">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcepool**".**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="c4d05-155">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="c4d05-156">Der Ressourcentyp, wenn die **ResourceType** -Eigenschaft auf "0" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c4d05-156">The resource type when the **ResourceType** property is set to "0" (other).</span></span>

</dd> <dt>

<span data-ttu-id="c4d05-157">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="c4d05-157">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4d05-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4d05-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4d05-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-160">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md)".**Poolid**")</span><span class="sxs-lookup"><span data-stu-id="c4d05-160">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="c4d05-161">Ein nicht transparenter Bezeichner für den Pool.</span><span class="sxs-lookup"><span data-stu-id="c4d05-161">An opaque identifier for the pool.</span></span> <span data-ttu-id="c4d05-162">Diese Eigenschaft wird verwendet, um die Korrelation beim Speichern und Wiederherstellen von Konfigurationsdaten im zugrunde liegenden permanenten Speicher bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c4d05-162">This property is used to provide correlation when saving and restoring configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="c4d05-163">**Ursprünglich**</span><span class="sxs-lookup"><span data-stu-id="c4d05-163">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4d05-164">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c4d05-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4d05-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4d05-166">**true** , wenn der Ressourcenpool uralt ist.</span><span class="sxs-lookup"><span data-stu-id="c4d05-166">**true** if the resource pool is primordial.</span></span> <span data-ttu-id="c4d05-167">**false** , wenn der Ressourcenpool ein konkreter Ressourcenpool ist.</span><span class="sxs-lookup"><span data-stu-id="c4d05-167">**false** if the resource pool is a concrete resource pool.</span></span> <span data-ttu-id="c4d05-168">Bei einem ursprünglichen Ressourcenpool handelt es sich um einen Ressourcenpool, der nicht von Kunden der Ressource erstellt oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c4d05-168">A primordial resource pool is a resource pool that is not created or deleted by consumers of the resource.</span></span> <span data-ttu-id="c4d05-169">Ein konkreter Ressourcenpool kann durch Ressourcen Zuordnungs Dienste aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c4d05-169">A concrete resource pool can be updated by resource allocation services.</span></span>

</dd> <dt>

<span data-ttu-id="c4d05-170">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="c4d05-170">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4d05-171">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4d05-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4d05-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4d05-173">Die aktuelle Anzahl der Reservierungen, die auf alle aktiven Zuweisungen aus diesem Pool verteilt sind.</span><span class="sxs-lookup"><span data-stu-id="c4d05-173">The current number of reservations spread across all active allocations from this pool.</span></span> <span data-ttu-id="c4d05-174">In einer hierarchischen Konfiguration stellt dies die Summe aller aktuellen untergeordneten Reservierungen dar.</span><span class="sxs-lookup"><span data-stu-id="c4d05-174">In a hierarchical configuration, this represents the sum of all current descendant reservations.</span></span> <span data-ttu-id="c4d05-175">Die Eigenschaft " **Zuordnungseinheiten** " gibt den Einheitentyp an.</span><span class="sxs-lookup"><span data-stu-id="c4d05-175">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="c4d05-176">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="c4d05-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4d05-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4d05-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4d05-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-179">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcepool**".**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="c4d05-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="c4d05-180">Der Implementierungs spezifische Untertyp für den Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="c4d05-180">The implementation specific sub-type for the resource pool.</span></span> <span data-ttu-id="c4d05-181">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="c4d05-181">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="c4d05-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="c4d05-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4d05-183">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4d05-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4d05-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4d05-185">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ resourcepool**".**Otherresourcetype**","**CIM \_ resourcepool**.**Resourcesubtype**")</span><span class="sxs-lookup"><span data-stu-id="c4d05-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**OtherResourceType**", "**CIM\_ResourcePool**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="c4d05-186">Der Typ der Ressource, die vom Ressourcenpool zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c4d05-186">The type of resource allocated by the resource pool.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c4d05-187">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c4d05-187">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="c4d05-188">**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="c4d05-188">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="c4d05-189">**Prozessor** (3)</span><span class="sxs-lookup"><span data-stu-id="c4d05-189">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="c4d05-190">Arbeits **Speicher** (4)</span><span class="sxs-lookup"><span data-stu-id="c4d05-190">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="c4d05-191">**IDE-Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="c4d05-191">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="c4d05-192">**Paralleler SCSI-HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="c4d05-192">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="c4d05-193">**FC-HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="c4d05-193">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="c4d05-194">**iSCSI-HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="c4d05-194">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="c4d05-195">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="c4d05-195">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="c4d05-196">**Ethernet-Adapter** (10)</span><span class="sxs-lookup"><span data-stu-id="c4d05-196">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="c4d05-197">**Anderer Netzwerk Adapter** (11)</span><span class="sxs-lookup"><span data-stu-id="c4d05-197">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="c4d05-198">E **/a-Slot** (12)</span><span class="sxs-lookup"><span data-stu-id="c4d05-198">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="c4d05-199">E **/a-Gerät** (13)</span><span class="sxs-lookup"><span data-stu-id="c4d05-199">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="c4d05-200">**Diskettenlaufwerk** (14)</span><span class="sxs-lookup"><span data-stu-id="c4d05-200">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="c4d05-201">**CD-Laufwerk** (15)</span><span class="sxs-lookup"><span data-stu-id="c4d05-201">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="c4d05-202">**DVD-Laufwerk** (16)</span><span class="sxs-lookup"><span data-stu-id="c4d05-202">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="c4d05-203">**Laufwerk (17** )</span><span class="sxs-lookup"><span data-stu-id="c4d05-203">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="c4d05-204">**Bandlaufwerk** (18)</span><span class="sxs-lookup"><span data-stu-id="c4d05-204">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="c4d05-205">**Speicher** Block (19)</span><span class="sxs-lookup"><span data-stu-id="c4d05-205">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="c4d05-206">**Anderes Speichergerät** (20)</span><span class="sxs-lookup"><span data-stu-id="c4d05-206">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="c4d05-207">**Seriellen Anschluss** (21)</span><span class="sxs-lookup"><span data-stu-id="c4d05-207">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="c4d05-208">**Paralleler Anschluss** (22)</span><span class="sxs-lookup"><span data-stu-id="c4d05-208">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="c4d05-209">**USB-Controller** (23)</span><span class="sxs-lookup"><span data-stu-id="c4d05-209">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="c4d05-210">**Grafikcontroller** (24)</span><span class="sxs-lookup"><span data-stu-id="c4d05-210">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="c4d05-211">**IEEE 1394-Controller** (25)</span><span class="sxs-lookup"><span data-stu-id="c4d05-211">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="c4d05-212">**Partitionier Bare Einheit** (26)</span><span class="sxs-lookup"><span data-stu-id="c4d05-212">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="c4d05-213">**Partitionier bare Basiseinheit** (27)</span><span class="sxs-lookup"><span data-stu-id="c4d05-213">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="c4d05-214">**Energie** (28)</span><span class="sxs-lookup"><span data-stu-id="c4d05-214">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="c4d05-215">**Kühlkapazität** (29)</span><span class="sxs-lookup"><span data-stu-id="c4d05-215">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="c4d05-216">**Ethernet-Switchport** (30)</span><span class="sxs-lookup"><span data-stu-id="c4d05-216">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="c4d05-217">**Logischer** Datenträger (31)</span><span class="sxs-lookup"><span data-stu-id="c4d05-217">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="c4d05-218">**Speicher Volume** (32)</span><span class="sxs-lookup"><span data-stu-id="c4d05-218">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="c4d05-219">**Ethernet-Verbindung** (33)</span><span class="sxs-lookup"><span data-stu-id="c4d05-219">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c4d05-220">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="c4d05-220">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c4d05-221">**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="c4d05-221">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="c4d05-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c4d05-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c4d05-223">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4d05-223">Requirements</span></span>



| <span data-ttu-id="c4d05-224">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4d05-224">Requirement</span></span> | <span data-ttu-id="c4d05-225">Wert</span><span class="sxs-lookup"><span data-stu-id="c4d05-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d05-226">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4d05-226">Minimum supported client</span></span><br/> | <span data-ttu-id="c4d05-227">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c4d05-227">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c4d05-228">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4d05-228">Minimum supported server</span></span><br/> | <span data-ttu-id="c4d05-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4d05-229">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c4d05-230">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4d05-230">Namespace</span></span><br/>                | <span data-ttu-id="c4d05-231">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c4d05-231">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c4d05-232">MOF</span><span class="sxs-lookup"><span data-stu-id="c4d05-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4d05-233"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c4d05-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4d05-234">DLL</span><span class="sxs-lookup"><span data-stu-id="c4d05-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4d05-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4d05-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c4d05-236">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4d05-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d05-237">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="c4d05-237">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

