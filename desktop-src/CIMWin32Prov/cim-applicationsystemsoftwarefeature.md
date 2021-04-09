---
description: Die CIM \_ applicationsystemsoftwarefeature-Klasse stellt eine Zuordnung dar, mit der die Software Features identifiziert werden, die ein bestimmtes Anwendungssystem bilden. Die Software Features können in verschiedene Produkte eingeschlossen werden.
ms.assetid: e40d0d64-f9f0-4c05-aef6-c759256e408b
ms.tgt_platform: multiple
title: CIM_ApplicationSystemSoftwareFeature-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystemSoftwareFeature
- CIM_ApplicationSystemSoftwareFeature.PartComponent
- CIM_ApplicationSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b13a15370b19583eef61fb36fda2d63fcb61989
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861424"
---
# <a name="cim_applicationsystemsoftwarefeature-class"></a><span data-ttu-id="bf624-104">CIM \_ applicationsystemsoftwarefeature-Klasse</span><span class="sxs-lookup"><span data-stu-id="bf624-104">CIM\_ApplicationSystemSoftwareFeature class</span></span>

<span data-ttu-id="bf624-105">Die **CIM \_ applicationsystemsoftwarefeature** -Klasse stellt eine Zuordnung dar, mit der die Software Features identifiziert werden, die ein bestimmtes Anwendungssystem bilden.</span><span class="sxs-lookup"><span data-stu-id="bf624-105">The **CIM\_ApplicationSystemSoftwareFeature** class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="bf624-106">Die Software Features können in verschiedene Produkte eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="bf624-106">The software features can be included in different products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf624-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bf624-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bf624-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bf624-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bf624-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="bf624-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bf624-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bf624-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf624-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf624-111">Syntax</span></span>

``` syntax
[UUID("{0E17B9EA-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ApplicationSystemSoftwareFeature : CIM_SystemComponent
{
  CIM_SoftwareFeature   REF PartComponent;
  CIM_ApplicationSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="bf624-112">Member</span><span class="sxs-lookup"><span data-stu-id="bf624-112">Members</span></span>

<span data-ttu-id="bf624-113">Die **CIM- \_ applicationsystemsoftwarefeature** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bf624-113">The **CIM\_ApplicationSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="bf624-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf624-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf624-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf624-115">Properties</span></span>

<span data-ttu-id="bf624-116">Die **CIM \_ applicationsystemsoftwarefeature** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bf624-116">The **CIM\_ApplicationSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf624-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="bf624-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf624-118">Datentyp: **CIM \_ applicationsystem**</span><span class="sxs-lookup"><span data-stu-id="bf624-118">Data type: **CIM\_ApplicationSystem**</span></span>
</dt> <dt>

<span data-ttu-id="bf624-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf624-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf624-120">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="bf624-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="bf624-121">Ein [**CIM- \_ applicationsystem**](cim-applicationsystem.md) , das das übergeordnete System in der Zuordnung enthält.</span><span class="sxs-lookup"><span data-stu-id="bf624-121">A [**CIM\_ApplicationSystem**](cim-applicationsystem.md) that contains the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="bf624-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="bf624-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf624-123">Datentyp: **CIM \_ Softwarefeature**</span><span class="sxs-lookup"><span data-stu-id="bf624-123">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="bf624-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf624-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf624-125">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="bf624-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="bf624-126">Ein [**CIM- \_ Softwarefeature**](cim-softwarefeature.md) , das das untergeordnete Element enthält, das eine Komponente eines Systems ist.</span><span class="sxs-lookup"><span data-stu-id="bf624-126">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that contain the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf624-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf624-127">Remarks</span></span>

<span data-ttu-id="bf624-128">Die **CIM- \_ applicationsystemsoftwarefeature** -Klasse wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bf624-128">The **CIM\_ApplicationSystemSoftwareFeature** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="bf624-129">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="bf624-129">WMI does not implement this class.</span></span>

<span data-ttu-id="bf624-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bf624-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bf624-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bf624-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf624-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf624-132">Requirements</span></span>



| <span data-ttu-id="bf624-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf624-133">Requirement</span></span> | <span data-ttu-id="bf624-134">Wert</span><span class="sxs-lookup"><span data-stu-id="bf624-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf624-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf624-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bf624-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf624-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf624-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf624-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bf624-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf624-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf624-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf624-139">Namespace</span></span><br/>                | <span data-ttu-id="bf624-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bf624-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bf624-141">MOF</span><span class="sxs-lookup"><span data-stu-id="bf624-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf624-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bf624-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf624-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bf624-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf624-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf624-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf624-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf624-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf624-146">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="bf624-146">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

