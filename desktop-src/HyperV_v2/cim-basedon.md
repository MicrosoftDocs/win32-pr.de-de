---
description: Stellt eine Zuordnung zwischen einem CIM \_ -storageblock-Objekt höherer Ebene und einem CIM-storageblock-Objekt auf niedrigerer Ebene dar \_ . Beispielsweise ist ein CIM \_ protectedspaceblock-Objekt Teil eines CIM- \_ physicalblock-Objekts.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: CIM_BasedOn-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862464"
---
# <a name="cim_basedon-class-hyper-v-management"></a><span data-ttu-id="b754a-104">CIM_BasedOn-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="b754a-104">CIM_BasedOn class (Hyper-V management)</span></span>

<span data-ttu-id="b754a-105">Stellt eine Zuordnung zwischen einem CIM- **\_ storageblock** -Objekt höherer Ebene und einem **CIM- \_ storageblock** -Objekt auf niedrigerer Ebene dar.</span><span class="sxs-lookup"><span data-stu-id="b754a-105">Represents an association between a higher level **CIM\_StorageExtent** object and a lower level **CIM\_StorageExtent** object.</span></span> <span data-ttu-id="b754a-106">Beispielsweise ist ein [**CIM \_ protectedspaceblock**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) -Objekt Teil eines [**CIM- \_ physicalblock**](/windows/desktop/CIMWin32Prov/cim-physicalextent) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b754a-106">For example a [**CIM\_ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) object is a part of a [**CIM\_PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b754a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b754a-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="b754a-108">Member</span><span class="sxs-lookup"><span data-stu-id="b754a-108">Members</span></span>

<span data-ttu-id="b754a-109">Die **CIM- \_ BasedOn** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b754a-109">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="b754a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b754a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b754a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b754a-111">Properties</span></span>

<span data-ttu-id="b754a-112">Die **CIM- \_ BasedOn** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b754a-112">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b754a-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="b754a-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b754a-114">Datentyp: **CIM \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="b754a-114">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="b754a-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b754a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b754a-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="b754a-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b754a-117">Das CIM- **\_ storageblock** -Objekt auf niedrigerer Ebene.</span><span class="sxs-lookup"><span data-stu-id="b754a-117">The lower level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="b754a-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="b754a-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b754a-119">Datentyp: **CIM \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="b754a-119">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="b754a-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b754a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b754a-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="b754a-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b754a-122">Das CIM- **\_ storageblock** -Objekt der höheren Ebene.</span><span class="sxs-lookup"><span data-stu-id="b754a-122">The higher level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="b754a-123">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="b754a-123">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b754a-124">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b754a-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b754a-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b754a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b754a-126">Die Adresse, die angibt, an welcher Stelle im Speicher auf niedrigerer Ebene das **CIM- \_ storageblock** -Objekt der höheren Ebene endet.</span><span class="sxs-lookup"><span data-stu-id="b754a-126">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object ends.</span></span> <span data-ttu-id="b754a-127">Diese Eigenschaft ist nützlich, wenn Sie nicht zusammenhängende **CIM \_ storageblock** -Objekte einer Gruppierung auf höherer Ebene entspricht.</span><span class="sxs-lookup"><span data-stu-id="b754a-127">This property is useful when mapping non-contiguous **CIM\_StorageExtent** objects into a higher level grouping.</span></span>

</dd> <dt>

<span data-ttu-id="b754a-128">**Orderindex**</span><span class="sxs-lookup"><span data-stu-id="b754a-128">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b754a-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b754a-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b754a-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b754a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b754a-131">Ein Index, der verwendet wird, um die Reihenfolge der **CIM- \_ BasedOn** -Zuordnungen in einer Auflistung anzugeben; andernfalls gibt "0" keine Reihenfolge an.</span><span class="sxs-lookup"><span data-stu-id="b754a-131">An index that is used to specify the order of **CIM\_BasedOn** associations in a collection; otherwise "0" indicates no order.</span></span> <span data-ttu-id="b754a-132">**CIM \_ BasedOn** -Instanzen mit demselben abhängigen Wert sollten eindeutige Werte in der **orderindex** -Eigenschaft platzieren.</span><span class="sxs-lookup"><span data-stu-id="b754a-132">**CIM\_BasedOn** instances with the same dependent value should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="b754a-133">Der niedrigste **orderindex** -Wert gibt den ersten Member der Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="b754a-133">The lowest **OrderIndex** value specifies the first member of the collection.</span></span>

<span data-ttu-id="b754a-134">Ein Beispiel für die Verwendung dieser Eigenschaft ist das Definieren eines RAID-0-Stripesets von drei Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="b754a-134">An example of the use of this property is to define a RAID-0 striped array of 3 disks.</span></span> <span data-ttu-id="b754a-135">Das resultierende RAID-Array ist ein Speicherblock, der von den Speicherblöcken abhängig ist, die die drei Datenträger beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b754a-135">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the 3 disks.</span></span> <span data-ttu-id="b754a-136">Der **orderindex** -Wert jeder **CIM- \_ BasedOn** -Zuordnung aus den Datenträger Blöcken zum RAID-Array kann als 1, 2 und 3 angegeben werden, um die Reihenfolge anzugeben, in der die Datenträger Blöcke für den Zugriff auf die RAID-Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b754a-136">The **OrderIndex** value of each **CIM\_BasedOn** association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span>

</dd> <dt>

<span data-ttu-id="b754a-137">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="b754a-137">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b754a-138">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b754a-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b754a-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b754a-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b754a-140">Die Adresse, die angibt, an welcher Stelle im Speicher auf niedrigerer Ebene das **CIM- \_ storageblock** -Objekt der höheren Ebene beginnt.</span><span class="sxs-lookup"><span data-stu-id="b754a-140">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object begins.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b754a-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b754a-141">Requirements</span></span>



| <span data-ttu-id="b754a-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b754a-142">Requirement</span></span> | <span data-ttu-id="b754a-143">Wert</span><span class="sxs-lookup"><span data-stu-id="b754a-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b754a-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b754a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b754a-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b754a-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b754a-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b754a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b754a-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b754a-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b754a-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="b754a-148">Namespace</span></span><br/>                | <span data-ttu-id="b754a-149">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b754a-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b754a-150">MOF</span><span class="sxs-lookup"><span data-stu-id="b754a-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b754a-151"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b754a-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b754a-152">DLL</span><span class="sxs-lookup"><span data-stu-id="b754a-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b754a-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b754a-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b754a-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b754a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b754a-155">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="b754a-155">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

