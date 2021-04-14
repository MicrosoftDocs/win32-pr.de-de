---
description: Die CIM \_ LogicalDiskBasedOnPartition-Klasse ordnet der Festplatten Partition, auf der Sie sich befindet, einen logischen Datenträger zu.
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: CIM_LogicalDiskBasedOnPartition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67aac7ae8d295bd6d98e06e0ebb8135d3330f52f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523136"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a><span data-ttu-id="d4ebf-103">CIM \_ LogicalDiskBasedOnPartition-Klasse</span><span class="sxs-lookup"><span data-stu-id="d4ebf-103">CIM\_LogicalDiskBasedOnPartition class</span></span>

<span data-ttu-id="d4ebf-104">Die **CIM \_ LogicalDiskBasedOnPartition** -Klasse ordnet der Festplatten Partition, auf der Sie sich befindet, einen logischen Datenträger zu.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-104">The **CIM\_LogicalDiskBasedOnPartition** class associates a logical disk with the disk partition on which it resides.</span></span>

<span data-ttu-id="d4ebf-105">Beispielsweise kann sich das Laufwerk C eines Computers auf einer Partition auf einem lokalen physischen Medium befinden. Dies stellt fest, dass ein logischer Datenträger nicht mehr als eine Partition umfassen kann.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-105">For example, a computer's drive C can be located on a partition on local physical media, which dictates that a logical disk cannot span more than one partition.</span></span> <span data-ttu-id="d4ebf-106">Wenn ein logischer Datenträger mehr als eine Partition umfassen kann, basiert der logische Datenträger jedoch auf der RAID-Konfiguration (z. b. auf einem Spiegel oder einem Stripeset).</span><span class="sxs-lookup"><span data-stu-id="d4ebf-106">When a logical disk can span more than one partition, however, the logical disk is based on RAID configuration (for example, a mirror or stripe set).</span></span> <span data-ttu-id="d4ebf-107">In diesem Fall basiert der logische Datenträger auf dem Speicher Volume.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-107">In which case, the logical disk is based on storage volume.</span></span> <span data-ttu-id="d4ebf-108">Um zu verhindern, dass die **CIM \_ LogicalDiskBasedOnPartition** ordnungsgemäß verwendet wird, wurde der **Max (1)** -Qualifizierer auf den **Vorgänger** Verweis auf die Datenträger Partition festgestellt.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-108">To prevent using the **CIM\_LogicalDiskBasedOnPartition** association incorrectly, the **Max(1)** qualifier was put on the **Antecedent** reference to the disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4ebf-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d4ebf-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d4ebf-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d4ebf-111">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d4ebf-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ebf-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4ebf-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d4ebf-114">Member</span><span class="sxs-lookup"><span data-stu-id="d4ebf-114">Members</span></span>

<span data-ttu-id="d4ebf-115">Die **CIM \_ LogicalDiskBasedOnPartition** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d4ebf-115">The **CIM\_LogicalDiskBasedOnPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="d4ebf-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4ebf-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d4ebf-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4ebf-117">Properties</span></span>

<span data-ttu-id="d4ebf-118">Die **CIM \_ LogicalDiskBasedOnPartition** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-118">The **CIM\_LogicalDiskBasedOnPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4ebf-119">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="d4ebf-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebf-120">Datentyp: **CIM \_ Diskpartition**</span><span class="sxs-lookup"><span data-stu-id="d4ebf-120">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebf-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4ebf-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4ebf-122">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="d4ebf-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d4ebf-123">Eine [**CIM \_ Diskpartition**](cim-diskpartition.md) , die die Datenträger Partition beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-123">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebf-124">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="d4ebf-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebf-125">Datentyp: **CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="d4ebf-125">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebf-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4ebf-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4ebf-127">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="d4ebf-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d4ebf-128">Ein [**CIM \_ LogicalDisk**](cim-logicaldisk.md) , der den logischen Datenträger beschreibt, der auf der Partition erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-128">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the partition.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebf-129">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="d4ebf-129">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebf-130">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d4ebf-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebf-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4ebf-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebf-132">Gibt das Ende des hohen Wertebereichs in niedrigerer Speicher Ebene an.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-132">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="d4ebf-133">Diese Eigenschaft ist nützlich, wenn Sie nicht zusammenhängende Blöcke einer Gruppierung auf höherer Ebene zuordnen.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-133">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="d4ebf-134">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d4ebf-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d4ebf-135">Diese Eigenschaft wird von [**CIM- \_ BasedOn**](cim-basedon.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-135">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebf-136">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="d4ebf-136">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebf-137">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d4ebf-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebf-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4ebf-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebf-139">Gibt den Anfang des hohen Bereichs in einem Speicher auf niedrigerer Ebene an.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-139">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="d4ebf-140">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d4ebf-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d4ebf-141">Diese Eigenschaft wird von [**CIM- \_ BasedOn**](cim-basedon.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-141">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4ebf-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4ebf-142">Remarks</span></span>

<span data-ttu-id="d4ebf-143">Die **CIM \_ LogicalDiskBasedOnPartition** -Klasse wird von [**CIM \_ BasedOn**](cim-basedon.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-143">The **CIM\_LogicalDiskBasedOnPartition** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="d4ebf-144">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-144">WMI does not implement this class.</span></span> <span data-ttu-id="d4ebf-145">Informationen zu Klassen, die von **CIM \_ LogicalDiskBasedOnPartition** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d4ebf-145">For classes derived from **CIM\_LogicalDiskBasedOnPartition**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d4ebf-146">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d4ebf-147">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d4ebf-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ebf-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4ebf-148">Requirements</span></span>



| <span data-ttu-id="d4ebf-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4ebf-149">Requirement</span></span> | <span data-ttu-id="d4ebf-150">Wert</span><span class="sxs-lookup"><span data-stu-id="d4ebf-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ebf-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4ebf-151">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ebf-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4ebf-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4ebf-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4ebf-153">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ebf-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4ebf-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4ebf-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4ebf-155">Namespace</span></span><br/>                | <span data-ttu-id="d4ebf-156">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d4ebf-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d4ebf-157">MOF</span><span class="sxs-lookup"><span data-stu-id="d4ebf-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4ebf-158"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebf-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4ebf-159">DLL</span><span class="sxs-lookup"><span data-stu-id="d4ebf-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4ebf-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebf-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ebf-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4ebf-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ebf-162">**CIM- \_ BasedOn**</span><span class="sxs-lookup"><span data-stu-id="d4ebf-162">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

