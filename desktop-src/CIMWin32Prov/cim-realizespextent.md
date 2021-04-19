---
description: Die CIM- \_ Erweiterung "realizespblock" stellt die Beziehung dar, in der physische Blöcke auf einem physischen Medium realisiert werden. Außerdem wird die Startadresse des physischen Wertebereichs auf dem physischen Medium angegeben.
ms.assetid: 9abe1a7d-8463-4d48-8cec-52bf934ad08b
ms.tgt_platform: multiple
title: CIM_RealizesPExtent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesPExtent
- CIM_RealizesPExtent.Dependent
- CIM_RealizesPExtent.Antecedent
- CIM_RealizesPExtent.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 906861c7bc7a7e09d40d3457d069cdb9dd3a6b11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346223"
---
# <a name="cim_realizespextent-class"></a><span data-ttu-id="9e7ca-104">CIM \_ realizespblock-Klasse</span><span class="sxs-lookup"><span data-stu-id="9e7ca-104">CIM\_RealizesPExtent class</span></span>

<span data-ttu-id="9e7ca-105">Die CIM-Erweiterung " **\_ realizespblock** " stellt die Beziehung dar, in der physische Blöcke auf einem physischen Medium realisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-105">The **CIM\_RealizesPExtent** association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="9e7ca-106">Außerdem wird die Startadresse des physischen Wertebereichs auf dem physischen Medium angegeben.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-106">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e7ca-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9e7ca-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9e7ca-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9e7ca-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9e7ca-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e7ca-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e7ca-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesPExtent : CIM_Realizes
{
  CIM_PhysicalExtent REF Dependent;
  CIM_PhysicalMedia  REF Antecedent;
  uint64                 StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="9e7ca-112">Member</span><span class="sxs-lookup"><span data-stu-id="9e7ca-112">Members</span></span>

<span data-ttu-id="9e7ca-113">Die CIM-Klasse " **\_ realizespblock** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9e7ca-113">The **CIM\_RealizesPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="9e7ca-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e7ca-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e7ca-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e7ca-115">Properties</span></span>

<span data-ttu-id="9e7ca-116">Die CIM-Klasse " **\_ realizespblock** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-116">The **CIM\_RealizesPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e7ca-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="9e7ca-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7ca-118">Datentyp: **CIM \_ physicalmedia**</span><span class="sxs-lookup"><span data-stu-id="9e7ca-118">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="9e7ca-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e7ca-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7ca-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="9e7ca-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9e7ca-121">Ein [**CIM- \_ physicalmedia**](cim-physicalmedia.md) , das das physische Medium beschreibt, auf dem der Block realisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-121">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="9e7ca-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="9e7ca-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7ca-123">Datentyp: **CIM \_ physicalblock**</span><span class="sxs-lookup"><span data-stu-id="9e7ca-123">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="9e7ca-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e7ca-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7ca-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="9e7ca-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9e7ca-126">Ein [**CIM- \_ physicalblock**](cim-physicalextent.md) , der den physischen Block beschreibt, der sich auf dem Medium befindet.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-126">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="9e7ca-127">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="9e7ca-127">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7ca-128">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9e7ca-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9e7ca-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e7ca-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e7ca-130">Startadresse auf dem physischen Medium, an dem der physische Block beginnt.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-130">Starting address on the physical media where the physical extent begins.</span></span> <span data-ttu-id="9e7ca-131">Die Endadresse des physischen Wertebereichs wird mithilfe der Eigenschaften " **zahlofblocks** " und " **BLOCKSIZE** " des [**CIM- \_ physicalblock**](cim-physicalextent.md) -Objekts bestimmt.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-131">The ending address of the physical extent is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_PhysicalExtent**](cim-physicalextent.md) object.</span></span>

<span data-ttu-id="9e7ca-132">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9e7ca-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e7ca-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e7ca-133">Remarks</span></span>

<span data-ttu-id="9e7ca-134">Die CIM-Klasse " **\_ realizespblock** " ist von CIM-Erkenntnissen abgeleitet. [**\_**](cim-realizes.md)</span><span class="sxs-lookup"><span data-stu-id="9e7ca-134">The **CIM\_RealizesPExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="9e7ca-135">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-135">WMI does not implement this class.</span></span>

<span data-ttu-id="9e7ca-136">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9e7ca-137">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9e7ca-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e7ca-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e7ca-138">Requirements</span></span>



| <span data-ttu-id="9e7ca-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e7ca-139">Requirement</span></span> | <span data-ttu-id="9e7ca-140">Wert</span><span class="sxs-lookup"><span data-stu-id="9e7ca-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7ca-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e7ca-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9e7ca-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e7ca-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e7ca-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e7ca-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9e7ca-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e7ca-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e7ca-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e7ca-145">Namespace</span></span><br/>                | <span data-ttu-id="9e7ca-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9e7ca-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e7ca-147">MOF</span><span class="sxs-lookup"><span data-stu-id="9e7ca-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e7ca-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9e7ca-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e7ca-149">DLL</span><span class="sxs-lookup"><span data-stu-id="9e7ca-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e7ca-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e7ca-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e7ca-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e7ca-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e7ca-152">**CIM \_ erkennt**</span><span class="sxs-lookup"><span data-stu-id="9e7ca-152">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

