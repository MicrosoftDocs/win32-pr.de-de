---
description: Die CIM- \_ Klasse "realizesdiskpartition" stellt eine Datenträger Partition auf einem physischen Medium dar, die die Erstellung von Partitionen auf einem unformatierten SCSI-oder IDE-Laufwerk modelliert.
ms.assetid: cc317f7d-06cd-4126-8123-6a3eb32f792e
ms.tgt_platform: multiple
title: CIM_RealizesDiskPartition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesDiskPartition
- CIM_RealizesDiskPartition.Dependent
- CIM_RealizesDiskPartition.Antecedent
- CIM_RealizesDiskPartition.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d138aafd179f5fefa40896fe4b9e6a0426b34422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126668"
---
# <a name="cim_realizesdiskpartition-class"></a><span data-ttu-id="2e7c9-103">CIM- \_ Klasse "realizesdiskpartition"</span><span class="sxs-lookup"><span data-stu-id="2e7c9-103">CIM\_RealizesDiskPartition class</span></span>

<span data-ttu-id="2e7c9-104">Die CIM-Klasse " **\_ realizesdiskpartition** " stellt eine Datenträger Partition auf einem physischen Medium dar, die die Erstellung von Partitionen auf einem unformatierten SCSI-oder IDE-Laufwerk modelliert.</span><span class="sxs-lookup"><span data-stu-id="2e7c9-104">The **CIM\_RealizesDiskPartition** class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e7c9-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2e7c9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e7c9-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2e7c9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e7c9-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2e7c9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2e7c9-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2e7c9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e7c9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e7c9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B80-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesDiskPartition : CIM_Realizes
{
  CIM_DiskPartition REF Dependent;
  CIM_PhysicalMedia REF Antecedent;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="2e7c9-110">Member</span><span class="sxs-lookup"><span data-stu-id="2e7c9-110">Members</span></span>

<span data-ttu-id="2e7c9-111">Die CIM-Klasse " **\_ realizesdiskpartition** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2e7c9-111">The **CIM\_RealizesDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="2e7c9-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e7c9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e7c9-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e7c9-113">Properties</span></span>

<span data-ttu-id="2e7c9-114">Die CIM-Klasse " **\_ realizesdiskpartition** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2e7c9-114">The **CIM\_RealizesDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e7c9-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="2e7c9-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e7c9-116">Datentyp: **CIM \_ physicalmedia**</span><span class="sxs-lookup"><span data-stu-id="2e7c9-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="2e7c9-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e7c9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e7c9-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="2e7c9-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="2e7c9-119">Ein [**CIM- \_ physicalmedia**](cim-physicalmedia.md) , das das physische Medium beschreibt, auf dem der Block realisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2e7c9-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="2e7c9-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="2e7c9-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e7c9-121">Datentyp: **CIM \_ Diskpartition**</span><span class="sxs-lookup"><span data-stu-id="2e7c9-121">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="2e7c9-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e7c9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e7c9-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="2e7c9-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2e7c9-124">Eine [**CIM- \_ Diskpartition**](cim-diskpartition.md) , die die auf dem Medium befindliche Datenträger Partition beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2e7c9-124">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="2e7c9-125">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="2e7c9-125">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e7c9-126">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2e7c9-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e7c9-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e7c9-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e7c9-128">Startadresse auf dem physischen Medium, an dem die Datenträger Partition beginnt.</span><span class="sxs-lookup"><span data-stu-id="2e7c9-128">Starting address on the physical media where the disk partition begins.</span></span> <span data-ttu-id="2e7c9-129">Die Endadresse der Partition wird mithilfe der Eigenschaften " **zahlofblocks** " und " **BLOCKSIZE** " des [**CIM \_ Diskpartition**](cim-diskpartition.md) -Objekts ermittelt.</span><span class="sxs-lookup"><span data-stu-id="2e7c9-129">The partition's ending address is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_DiskPartition**](cim-diskpartition.md) object.</span></span>

<span data-ttu-id="2e7c9-130">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2e7c9-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e7c9-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e7c9-131">Remarks</span></span>

<span data-ttu-id="2e7c9-132">Die CIM-Klasse " **\_ realizesdiskpartition** " ist von CIM-Erkenntnissen abgeleitet. [**\_**](cim-realizes.md)</span><span class="sxs-lookup"><span data-stu-id="2e7c9-132">The **CIM\_RealizesDiskPartition** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="2e7c9-133">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2e7c9-133">WMI does not implement this class.</span></span>

<span data-ttu-id="2e7c9-134">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2e7c9-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e7c9-135">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2e7c9-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e7c9-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e7c9-136">Requirements</span></span>



| <span data-ttu-id="2e7c9-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e7c9-137">Requirement</span></span> | <span data-ttu-id="2e7c9-138">Wert</span><span class="sxs-lookup"><span data-stu-id="2e7c9-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e7c9-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e7c9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2e7c9-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e7c9-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e7c9-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e7c9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2e7c9-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e7c9-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e7c9-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e7c9-143">Namespace</span></span><br/>                | <span data-ttu-id="2e7c9-144">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2e7c9-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e7c9-145">MOF</span><span class="sxs-lookup"><span data-stu-id="2e7c9-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e7c9-146"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2e7c9-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e7c9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="2e7c9-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e7c9-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e7c9-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e7c9-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e7c9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e7c9-150">**CIM \_ erkennt**</span><span class="sxs-lookup"><span data-stu-id="2e7c9-150">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

