---
description: Die CIM- \_ BasedOn-Klasse stellt eine Zuordnung dar, die beschreibt, wie Speicherblöcke aus Blöcken auf niedrigerer Ebene zusammengestellt werden können.
ms.assetid: 82132012-5851-4be8-82db-edbdb50b70e5
ms.tgt_platform: multiple
title: CIM_BasedOn-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Dependent
- CIM_BasedOn.Antecedent
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e25cd9a5f194df8c5cbc0c7dc24a4777cee3417
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214230"
---
# <a name="cim_basedon-class-cimwin32-wmi-providers"></a><span data-ttu-id="26af1-103">CIM_BasedOn-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="26af1-103">CIM_BasedOn class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="26af1-104">Die **CIM- \_ BasedOn** -Klasse stellt eine Zuordnung dar, die beschreibt, wie Speicherblöcke aus Blöcken auf niedrigerer Ebene zusammengestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="26af1-104">The **CIM\_BasedOn** class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="26af1-105">Physische Blöcke enthalten beispielsweise Blöcke mit geschütztem Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="26af1-105">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="26af1-106">Volumesätze werden daher aus einem oder mehreren physischen oder geschützten Speicherplatz Blöcken zusammengestellt.</span><span class="sxs-lookup"><span data-stu-id="26af1-106">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="26af1-107">Der Cache Speicher kann unabhängig voneinander definiert und in einem physischen Element realisiert werden. er kann aber auch auf flüchtigen oder nicht flüchtigen Speicherblöcken basieren.</span><span class="sxs-lookup"><span data-stu-id="26af1-107">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26af1-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="26af1-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="26af1-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="26af1-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="26af1-110">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="26af1-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26af1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="26af1-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Dependent;
  CIM_StorageExtent REF Antecedent;
  uint64                EndingAddress;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="26af1-112">Member</span><span class="sxs-lookup"><span data-stu-id="26af1-112">Members</span></span>

<span data-ttu-id="26af1-113">Die **CIM- \_ BasedOn** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="26af1-113">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="26af1-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26af1-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26af1-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26af1-115">Properties</span></span>

<span data-ttu-id="26af1-116">Die **CIM- \_ BasedOn** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="26af1-116">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26af1-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="26af1-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26af1-118">Datentyp: **CIM \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="26af1-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="26af1-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26af1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26af1-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="26af1-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="26af1-121">Ein [**CIM- \_ storageblock**](cim-storageextent.md) , der den Speicherblock auf niedrigerer Ebene beschreibt.</span><span class="sxs-lookup"><span data-stu-id="26af1-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the lower level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="26af1-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="26af1-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26af1-123">Datentyp: **CIM \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="26af1-123">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="26af1-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26af1-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26af1-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="26af1-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="26af1-126">Ein [**CIM- \_ storageblock**](cim-storageextent.md) , der den Speicherblock auf höherer Ebene beschreibt.</span><span class="sxs-lookup"><span data-stu-id="26af1-126">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the higher level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="26af1-127">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="26af1-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26af1-128">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26af1-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26af1-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26af1-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26af1-130">Gibt das Ende des hohen Wertebereichs in niedrigerer Speicher Ebene an.</span><span class="sxs-lookup"><span data-stu-id="26af1-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="26af1-131">Diese Eigenschaft ist nützlich, wenn Sie nicht zusammenhängende Blöcke einer Gruppierung auf höherer Ebene zuordnen.</span><span class="sxs-lookup"><span data-stu-id="26af1-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="26af1-132">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="26af1-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="26af1-133">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="26af1-133">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26af1-134">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26af1-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26af1-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26af1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26af1-136">Gibt den Anfang des hohen Bereichs in einem Speicher auf niedrigerer Ebene an.</span><span class="sxs-lookup"><span data-stu-id="26af1-136">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="26af1-137">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="26af1-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26af1-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26af1-138">Remarks</span></span>

<span data-ttu-id="26af1-139">Die **CIM- \_ BasedOn** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="26af1-139">The **CIM\_BasedOn** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="26af1-140">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="26af1-140">WMI does not implement this class.</span></span>

<span data-ttu-id="26af1-141">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="26af1-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="26af1-142">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="26af1-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="26af1-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26af1-143">Requirements</span></span>



| <span data-ttu-id="26af1-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26af1-144">Requirement</span></span> | <span data-ttu-id="26af1-145">Wert</span><span class="sxs-lookup"><span data-stu-id="26af1-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26af1-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26af1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="26af1-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26af1-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26af1-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26af1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="26af1-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26af1-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26af1-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="26af1-150">Namespace</span></span><br/>                | <span data-ttu-id="26af1-151">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="26af1-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="26af1-152">MOF</span><span class="sxs-lookup"><span data-stu-id="26af1-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26af1-153"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="26af1-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="26af1-154">DLL</span><span class="sxs-lookup"><span data-stu-id="26af1-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26af1-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26af1-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26af1-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26af1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26af1-157">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="26af1-157">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

