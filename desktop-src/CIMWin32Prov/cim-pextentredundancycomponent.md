---
description: Die CIM \_ pextentredundancycomponent-Klasse stellt die physischen Blöcke dar, die Teil einer Speicher Redundanz Gruppe sind.
ms.assetid: 5a4bb1e8-7b99-410a-bba5-2c63beabd00e
ms.tgt_platform: multiple
title: CIM_PExtentRedundancyComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PExtentRedundancyComponent
- CIM_PExtentRedundancyComponent.PartComponent
- CIM_PExtentRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb2b6a88a789e93ca45f8469e0e67449e3473ddc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482934"
---
# <a name="cim_pextentredundancycomponent-class"></a><span data-ttu-id="1eb15-103">CIM \_ pextentredundancycomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="1eb15-103">CIM\_PExtentRedundancyComponent class</span></span>

<span data-ttu-id="1eb15-104">Die **CIM \_ pextentredundancycomponent** -Klasse stellt die physischen Blöcke dar, die Teil einer Speicher Redundanz Gruppe sind.</span><span class="sxs-lookup"><span data-stu-id="1eb15-104">The **CIM\_PExtentRedundancyComponent** class represents the physical extents that participate in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1eb15-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1eb15-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1eb15-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1eb15-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1eb15-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1eb15-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1eb15-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1eb15-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb15-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1eb15-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{AD3C1FA2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_PExtentRedundancyComponent : CIM_RedundancyComponent
{
  CIM_PhysicalExtent         REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="1eb15-110">Member</span><span class="sxs-lookup"><span data-stu-id="1eb15-110">Members</span></span>

<span data-ttu-id="1eb15-111">Die **CIM \_ pextentredundancycomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1eb15-111">The **CIM\_PExtentRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="1eb15-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1eb15-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1eb15-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1eb15-113">Properties</span></span>

<span data-ttu-id="1eb15-114">Die **CIM \_ pextentredundancycomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1eb15-114">The **CIM\_PExtentRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1eb15-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="1eb15-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb15-116">Datentyp: **CIM \_ storageredundancygroup**</span><span class="sxs-lookup"><span data-stu-id="1eb15-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="1eb15-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1eb15-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb15-118">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="1eb15-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="1eb15-119">Eine [**CIM \_ storageredundancygroup**](cim-storageredundancygroup.md) , die die Speicher Redundanz Gruppe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1eb15-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that describes the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="1eb15-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1eb15-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb15-121">Datentyp: **CIM \_ physicalblock**</span><span class="sxs-lookup"><span data-stu-id="1eb15-121">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="1eb15-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1eb15-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb15-123">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="1eb15-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="1eb15-124">Ein [**CIM- \_ physicalblock**](cim-physicalextent.md) , der den physischen Block beschreibt, der Teil der Redundanz Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="1eb15-124">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1eb15-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1eb15-125">Remarks</span></span>

<span data-ttu-id="1eb15-126">Die **CIM- \_ pextentredundancycomponent** -Klasse wird von [**CIM \_ redundant cycomponent**](cim-redundancycomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1eb15-126">The **CIM\_PExtentRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="1eb15-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1eb15-127">WMI does not implement this class.</span></span>

<span data-ttu-id="1eb15-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1eb15-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1eb15-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1eb15-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb15-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1eb15-130">Requirements</span></span>



| <span data-ttu-id="1eb15-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1eb15-131">Requirement</span></span> | <span data-ttu-id="1eb15-132">Wert</span><span class="sxs-lookup"><span data-stu-id="1eb15-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb15-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1eb15-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1eb15-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1eb15-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1eb15-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1eb15-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1eb15-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1eb15-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1eb15-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="1eb15-137">Namespace</span></span><br/>                | <span data-ttu-id="1eb15-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1eb15-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1eb15-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1eb15-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1eb15-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1eb15-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1eb15-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1eb15-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eb15-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1eb15-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eb15-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1eb15-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb15-144">**CIM \_ redundant cycomponent**</span><span class="sxs-lookup"><span data-stu-id="1eb15-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

