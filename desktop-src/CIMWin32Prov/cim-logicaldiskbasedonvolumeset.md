---
description: Die CIM \_ logicaldiskbasedonvolumeset-Zuordnung bezieht logische Datenträger mit dem Volume, auf dem Sie gefunden werden. Logische Datenträger können auf einem einzelnen Volume (z. b. von einem Software Volume-Manager verfügbar gemacht) oder auf einer Datenträger Partition basieren.
ms.assetid: 15a588c9-a6b0-4393-927f-8e8818315542
ms.tgt_platform: multiple
title: CIM_LogicalDiskBasedOnVolumeSet-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnVolumeSet
- CIM_LogicalDiskBasedOnVolumeSet.EndingAddress
- CIM_LogicalDiskBasedOnVolumeSet.StartingAddress
- CIM_LogicalDiskBasedOnVolumeSet.Dependent
- CIM_LogicalDiskBasedOnVolumeSet.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2af4c141fe0b64979c6fb6e5b7b0e6068d018d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126152"
---
# <a name="cim_logicaldiskbasedonvolumeset-class"></a><span data-ttu-id="ed74f-104">CIM \_ logicaldiskbasedonvolumeset-Klasse</span><span class="sxs-lookup"><span data-stu-id="ed74f-104">CIM\_LogicalDiskBasedOnVolumeSet class</span></span>

<span data-ttu-id="ed74f-105">Die **CIM \_ logicaldiskbasedonvolumeset** -Zuordnung bezieht logische Datenträger mit dem Volume, auf dem Sie gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="ed74f-105">The **CIM\_LogicalDiskBasedOnVolumeSet** association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="ed74f-106">Logische Datenträger können auf einem einzelnen Volume (z. b. von einem Software Volume-Manager verfügbar gemacht) oder auf einer Datenträger Partition basieren.</span><span class="sxs-lookup"><span data-stu-id="ed74f-106">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed74f-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ed74f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ed74f-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ed74f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ed74f-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ed74f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ed74f-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ed74f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed74f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed74f-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3A608798-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LogicalDiskBasedOnVolumeSet : CIM_BasedOn
{
  uint64              EndingAddress;
  uint64              StartingAddress;
  CIM_LogicalDisk REF Dependent;
  CIM_VolumeSet   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ed74f-112">Member</span><span class="sxs-lookup"><span data-stu-id="ed74f-112">Members</span></span>

<span data-ttu-id="ed74f-113">Die **CIM \_ logicaldiskbasedonvolumeset** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ed74f-113">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="ed74f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed74f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed74f-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed74f-115">Properties</span></span>

<span data-ttu-id="ed74f-116">Die **CIM \_ logicaldiskbasedonvolumeset** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ed74f-116">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed74f-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="ed74f-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed74f-118">Datentyp: **CIM \_ volumeset**</span><span class="sxs-lookup"><span data-stu-id="ed74f-118">Data type: **CIM\_VolumeSet**</span></span>
</dt> <dt>

<span data-ttu-id="ed74f-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed74f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed74f-120">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="ed74f-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ed74f-121">Ein [**CIM- \_ volumeset**](cim-volumeset.md) , das den Volumesatz beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ed74f-121">A [**CIM\_VolumeSet**](cim-volumeset.md) that describes the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="ed74f-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="ed74f-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed74f-123">Datentyp: **CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="ed74f-123">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="ed74f-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed74f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed74f-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="ed74f-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ed74f-126">Ein [**CIM \_ LogicalDisk**](cim-logicaldisk.md) , der den auf dem Volumesatz erstellten logischen Datenträger beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ed74f-126">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="ed74f-127">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="ed74f-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed74f-128">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ed74f-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ed74f-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed74f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed74f-130">Gibt das Ende des hohen Wertebereichs in niedrigerer Speicher Ebene an.</span><span class="sxs-lookup"><span data-stu-id="ed74f-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="ed74f-131">Diese Eigenschaft ist nützlich, wenn Sie nicht zusammenhängende Blöcke einer Gruppierung auf höherer Ebene zuordnen.</span><span class="sxs-lookup"><span data-stu-id="ed74f-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="ed74f-132">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ed74f-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="ed74f-133">Diese Eigenschaft wird von [**CIM- \_ BasedOn**](cim-basedon.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ed74f-133">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed74f-134">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="ed74f-134">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed74f-135">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ed74f-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ed74f-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed74f-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed74f-137">Gibt den Anfang des hohen Bereichs in einem Speicher auf niedrigerer Ebene an.</span><span class="sxs-lookup"><span data-stu-id="ed74f-137">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="ed74f-138">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ed74f-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="ed74f-139">Diese Eigenschaft wird von [**CIM- \_ BasedOn**](cim-basedon.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ed74f-139">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed74f-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed74f-140">Remarks</span></span>

<span data-ttu-id="ed74f-141">Die **CIM \_ logicaldiskbasedonvolumeset** -Klasse wird von [**CIM \_ BasedOn**](cim-basedon.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ed74f-141">The **CIM\_LogicalDiskBasedOnVolumeSet** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="ed74f-142">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ed74f-142">WMI does not implement this class.</span></span>

<span data-ttu-id="ed74f-143">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ed74f-143">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ed74f-144">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ed74f-144">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed74f-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed74f-145">Requirements</span></span>



| <span data-ttu-id="ed74f-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed74f-146">Requirement</span></span> | <span data-ttu-id="ed74f-147">Wert</span><span class="sxs-lookup"><span data-stu-id="ed74f-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed74f-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed74f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ed74f-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed74f-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ed74f-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed74f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ed74f-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed74f-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ed74f-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed74f-152">Namespace</span></span><br/>                | <span data-ttu-id="ed74f-153">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ed74f-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ed74f-154">MOF</span><span class="sxs-lookup"><span data-stu-id="ed74f-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed74f-155"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ed74f-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed74f-156">DLL</span><span class="sxs-lookup"><span data-stu-id="ed74f-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed74f-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed74f-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed74f-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed74f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed74f-159">**CIM- \_ BasedOn**</span><span class="sxs-lookup"><span data-stu-id="ed74f-159">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

