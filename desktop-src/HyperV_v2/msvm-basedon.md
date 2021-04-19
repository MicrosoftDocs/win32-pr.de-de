---
description: Eine Zuordnung, die beschreibt, wie Speicherblöcke aus Blöcken auf niedrigerer Ebene zusammengestellt werden können.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Msvm_BasedOn-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8262ae5e510574bf02630410b584d9df10d64ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362660"
---
# <a name="msvm_basedon-class"></a><span data-ttu-id="7379c-103">MSVM- \_ BasedOn-Klasse</span><span class="sxs-lookup"><span data-stu-id="7379c-103">Msvm\_BasedOn class</span></span>

<span data-ttu-id="7379c-104">Eine Zuordnung, die beschreibt, wie Speicherblöcke aus Blöcken auf niedrigerer Ebene zusammengestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="7379c-104">An association that describes how storage extents can be assembled from lower level extents.</span></span> <span data-ttu-id="7379c-105">Protectedspaceextents sind z. b. Teile von physicalextents, während Volumesets von einem oder mehreren physischen oder protectedspaceextents zusammengestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7379c-105">For example, ProtectedSpaceExtents are parts of PhysicalExtents, while VolumeSets are assembled from one or more Physical or ProtectedSpaceExtents.</span></span> <span data-ttu-id="7379c-106">Ein weiteres Beispiel ist, dass CacheMemory unabhängig voneinander definiert und in einem PhysicalElement realisiert werden kann oder auf flüchtigen oder nicht volatilestorageextents basieren kann.</span><span class="sxs-lookup"><span data-stu-id="7379c-106">As another example, CacheMemory can be defined independently and realized in a PhysicalElement or can be based on Volatile or NonVolatileStorageExtents.</span></span>

<span data-ttu-id="7379c-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7379c-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7379c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7379c-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="7379c-109">Member</span><span class="sxs-lookup"><span data-stu-id="7379c-109">Members</span></span>

<span data-ttu-id="7379c-110">Die **MSVM- \_ BasedOn** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7379c-110">The **Msvm\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="7379c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7379c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7379c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7379c-112">Properties</span></span>

<span data-ttu-id="7379c-113">Die **MSVM- \_ BasedOn** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7379c-113">The **Msvm\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7379c-114">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="7379c-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7379c-115">Datentyp: **[ **CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="7379c-115">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="7379c-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7379c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7379c-117">Der Speicherblock auf niedrigerer Ebene.</span><span class="sxs-lookup"><span data-stu-id="7379c-117">The lower level storage extent.</span></span> <span data-ttu-id="7379c-118">Diese Eigenschaft wird von [**CIM- \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7379c-118">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="7379c-119">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="7379c-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7379c-120">Datentyp: **[ **CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="7379c-120">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="7379c-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7379c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7379c-122">Der Speicherblock auf höherer Ebene.</span><span class="sxs-lookup"><span data-stu-id="7379c-122">The higher level storage extent.</span></span> <span data-ttu-id="7379c-123">Diese Eigenschaft wird von [**CIM- \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7379c-123">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="7379c-124">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="7379c-124">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7379c-125">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7379c-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7379c-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7379c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7379c-127">Die Endadresse, an der sich im Speicher auf niedrigerer Ebene der Umfang der höheren Ebene endet.</span><span class="sxs-lookup"><span data-stu-id="7379c-127">The ending address where, in lower level storage, the higher level extent ends.</span></span> <span data-ttu-id="7379c-128">Diese Eigenschaft ist nützlich, wenn Sie nicht zusammenhängende Blöcke zu einer Gruppierung auf höherer Ebene zuordnen.</span><span class="sxs-lookup"><span data-stu-id="7379c-128">This property is useful when mapping non-contiguous extents into a higher level grouping.</span></span> <span data-ttu-id="7379c-129">Diese Eigenschaft wird von [**CIM- \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7379c-129">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="7379c-130">**Orderindex**</span><span class="sxs-lookup"><span data-stu-id="7379c-130">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7379c-131">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7379c-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7379c-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7379c-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7379c-133">Wenn auf Grundlage von Zuordnungen, die beschreiben, wie ein Speicherblock auf höherer Ebene assembliert wird, eine Bestellung vorhanden ist, gibt die **orderindex** -Eigenschaft dies an.</span><span class="sxs-lookup"><span data-stu-id="7379c-133">If there is an order to the based on associations that describe how a higher level storage extent is assembled, the **OrderIndex** property indicates this.</span></span> <span data-ttu-id="7379c-134">Wenn eine Bestellung vorhanden ist, sollten die Instanzen mit demselben **abhängigen** Wert (dem gleichen höheren Ebenen-Block) eindeutige Werte in der **orderindex** -Eigenschaft platzieren.</span><span class="sxs-lookup"><span data-stu-id="7379c-134">When an order exists, the instances with the same **Dependent** value (the same higher level extent) should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="7379c-135">Der niedrigste Wert impliziert das erste Element der Auflistung von Blöcken auf niedrigerer Ebene, und das Erhöhen der Werte impliziert aufeinander folgende Member der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="7379c-135">The lowest value implies the first member of the collection of lower level extents, and increasing values imply successive members of the collection.</span></span> <span data-ttu-id="7379c-136">Wenn keine geordnete Beziehung vorhanden ist, sollte der Wert 0 (null) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7379c-136">If there is no ordered relationship, a value of zero should be specified.</span></span> <span data-ttu-id="7379c-137">Ein Beispiel für die Verwendung dieser Eigenschaft ist das Definieren eines RAID-0-Stripesets mit drei Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="7379c-137">An example of the use of this property is to define a RAID-0 striped array of three disks.</span></span> <span data-ttu-id="7379c-138">Das resultierende RAID-Array ist ein Speicherblock, der von den Speicherblöcken abhängig ist, die die drei Datenträger beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7379c-138">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the three disks.</span></span> <span data-ttu-id="7379c-139">Der **orderindex** -Wert jeder Zuordnung von der Datenträger Erweiterung zum RAID-Array kann als 1, 2 und 3 angegeben werden, um die Reihenfolge anzugeben, in der die Datenträger Blöcke für den Zugriff auf die RAID-Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7379c-139">The **OrderIndex** of each association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span> <span data-ttu-id="7379c-140">Diese Eigenschaft wird von [**CIM- \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7379c-140">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="7379c-141">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="7379c-141">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7379c-142">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7379c-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7379c-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7379c-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7379c-144">Die Startadresse, an der im Speicher auf niedrigerer Ebene der höhere Ebenen-Block beginnt.</span><span class="sxs-lookup"><span data-stu-id="7379c-144">The starting address where, in lower level storage, the higher level extent begins.</span></span> <span data-ttu-id="7379c-145">Diese Eigenschaft wird von [**CIM- \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7379c-145">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7379c-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7379c-146">Requirements</span></span>



| <span data-ttu-id="7379c-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7379c-147">Requirement</span></span> | <span data-ttu-id="7379c-148">Wert</span><span class="sxs-lookup"><span data-stu-id="7379c-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7379c-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7379c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7379c-150">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7379c-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7379c-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7379c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7379c-152">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7379c-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7379c-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="7379c-153">Namespace</span></span><br/>                | <span data-ttu-id="7379c-154">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7379c-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7379c-155">MOF</span><span class="sxs-lookup"><span data-stu-id="7379c-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7379c-156"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7379c-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7379c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="7379c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7379c-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7379c-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

