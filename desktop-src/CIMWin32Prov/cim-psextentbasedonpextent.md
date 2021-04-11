---
description: Die CIM \_ psextentbasedonpblock-Klasse ordnet Blöcke mit geschütztem Speicherplatz zu, die auf einem physischen Block basieren.
ms.assetid: 4b89319c-022c-4ff4-91ec-70c435a5888a
ms.tgt_platform: multiple
title: CIM_PSExtentBasedOnPExtent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PSExtentBasedOnPExtent
- CIM_PSExtentBasedOnPExtent.EndingAddress
- CIM_PSExtentBasedOnPExtent.StartingAddress
- CIM_PSExtentBasedOnPExtent.Dependent
- CIM_PSExtentBasedOnPExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d028cb99c2f2ca3c0afd8238a3c0c1c3b2e451a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126673"
---
# <a name="cim_psextentbasedonpextent-class"></a><span data-ttu-id="05785-103">CIM \_ psextentbasedonpblock-Klasse</span><span class="sxs-lookup"><span data-stu-id="05785-103">CIM\_PSExtentBasedOnPExtent class</span></span>

<span data-ttu-id="05785-104">Die **CIM \_ psextentbasedonpblock** -Klasse ordnet Blöcke mit geschütztem Speicherplatz zu, die auf einem physischen Block basieren.</span><span class="sxs-lookup"><span data-stu-id="05785-104">The **CIM\_PSExtentBasedOnPExtent** class associates protected space extents that are based on a physical extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05785-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="05785-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="05785-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="05785-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="05785-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="05785-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="05785-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="05785-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="05785-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="05785-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{451FE14C-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_PSExtentBasedOnPExtent : CIM_BasedOn
{
  uint64                       EndingAddress;
  uint64                       StartingAddress;
  CIM_ProtectedSpaceExtent REF Dependent;
  CIM_PhysicalExtent       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="05785-110">Member</span><span class="sxs-lookup"><span data-stu-id="05785-110">Members</span></span>

<span data-ttu-id="05785-111">Die **CIM \_ psextentbasedonpblock** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="05785-111">The **CIM\_PSExtentBasedOnPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="05785-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="05785-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="05785-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="05785-113">Properties</span></span>

<span data-ttu-id="05785-114">Die **CIM \_ psextentbasedonpblock** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="05785-114">The **CIM\_PSExtentBasedOnPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05785-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="05785-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05785-116">Datentyp: **CIM \_ physicalblock**</span><span class="sxs-lookup"><span data-stu-id="05785-116">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="05785-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05785-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05785-118">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="05785-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="05785-119">Ein [**CIM- \_ physikalischer**](cim-physicalextent.md) Wert, der den physischen Wertebereich beschreibt.</span><span class="sxs-lookup"><span data-stu-id="05785-119">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="05785-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="05785-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05785-121">Datentyp: **CIM \_ protectedspaceblock**</span><span class="sxs-lookup"><span data-stu-id="05785-121">Data type: **CIM\_ProtectedSpaceExtent**</span></span>
</dt> <dt>

<span data-ttu-id="05785-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05785-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05785-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="05785-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="05785-124">Ein [**CIM \_ protectedspaceblock**](cim-protectedspaceextent.md) , der den geschützten Bereichs Bereich beschreibt, der auf dem physischen Block basiert.</span><span class="sxs-lookup"><span data-stu-id="05785-124">A [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) that describes the protected space extent which is built on the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="05785-125">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="05785-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05785-126">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="05785-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="05785-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05785-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05785-128">Gibt das Ende des hohen Wertebereichs in niedrigerer Speicher Ebene an.</span><span class="sxs-lookup"><span data-stu-id="05785-128">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="05785-129">Diese Eigenschaft ist nützlich, wenn Sie nicht zusammenhängende Blöcke einer Gruppierung auf höherer Ebene zuordnen.</span><span class="sxs-lookup"><span data-stu-id="05785-129">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="05785-130">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="05785-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="05785-131">Diese Eigenschaft wird von [**CIM- \_ BasedOn**](cim-basedon.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="05785-131">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="05785-132">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="05785-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05785-133">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="05785-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="05785-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05785-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05785-135">Gibt den Anfang des hohen Bereichs in einem Speicher auf niedrigerer Ebene an.</span><span class="sxs-lookup"><span data-stu-id="05785-135">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="05785-136">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="05785-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="05785-137">Diese Eigenschaft wird von [**CIM- \_ BasedOn**](cim-basedon.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="05785-137">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05785-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05785-138">Remarks</span></span>

<span data-ttu-id="05785-139">Die **CIM \_ psextentbasedonpblock** -Klasse wird von [**CIM \_ BasedOn**](cim-basedon.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="05785-139">The **CIM\_PSExtentBasedOnPExtent** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="05785-140">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="05785-140">WMI does not implement this class.</span></span>

<span data-ttu-id="05785-141">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="05785-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="05785-142">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="05785-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="05785-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05785-143">Requirements</span></span>



| <span data-ttu-id="05785-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05785-144">Requirement</span></span> | <span data-ttu-id="05785-145">Wert</span><span class="sxs-lookup"><span data-stu-id="05785-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05785-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05785-146">Minimum supported client</span></span><br/> | <span data-ttu-id="05785-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05785-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05785-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05785-148">Minimum supported server</span></span><br/> | <span data-ttu-id="05785-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05785-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05785-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="05785-150">Namespace</span></span><br/>                | <span data-ttu-id="05785-151">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="05785-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="05785-152">MOF</span><span class="sxs-lookup"><span data-stu-id="05785-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05785-153"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="05785-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="05785-154">DLL</span><span class="sxs-lookup"><span data-stu-id="05785-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05785-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05785-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05785-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05785-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05785-157">**CIM- \_ BasedOn**</span><span class="sxs-lookup"><span data-stu-id="05785-157">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

