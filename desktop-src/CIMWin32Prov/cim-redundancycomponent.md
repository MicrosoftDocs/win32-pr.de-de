---
description: Die CIM \_ RedundancyComponent-Klasse ordnet eine Redundanz Gruppe zu, die aus verwalteten Systemelementen besteht, und gibt an, dass die Elemente zusammen Redundanz bereitstellen.
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: CIM_RedundancyComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyComponent
- CIM_RedundancyComponent.GroupComponent
- CIM_RedundancyComponent.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bcd1c16417ba0c02e13579f9e471076d4c61818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860647"
---
# <a name="cim_redundancycomponent-class"></a><span data-ttu-id="2f38d-103">CIM \_ redundant cycomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="2f38d-103">CIM\_RedundancyComponent class</span></span>

<span data-ttu-id="2f38d-104">Die **CIM \_ RedundancyComponent** -Klasse ordnet eine Redundanz Gruppe zu, die aus verwalteten Systemelementen besteht, und gibt an, dass die Elemente zusammen Redundanz bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2f38d-104">The **CIM\_RedundancyComponent** class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="2f38d-105">Alle Elemente, die in einer Redundanz Gruppe aggregiert werden, sollten Instanziierungen der gleichen Objektklasse sein.</span><span class="sxs-lookup"><span data-stu-id="2f38d-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f38d-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2f38d-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2f38d-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2f38d-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2f38d-108">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2f38d-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2f38d-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2f38d-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f38d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f38d-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FB9D6E62-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyComponent : CIM_Component
{
  CIM_RedundancyGroup      REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="2f38d-111">Member</span><span class="sxs-lookup"><span data-stu-id="2f38d-111">Members</span></span>

<span data-ttu-id="2f38d-112">Die **CIM \_ redundant cycomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2f38d-112">The **CIM\_RedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="2f38d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f38d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f38d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f38d-114">Properties</span></span>

<span data-ttu-id="2f38d-115">Die **CIM \_ redundant cycomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2f38d-115">The **CIM\_RedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f38d-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2f38d-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f38d-117">Datentyp: **CIM \_ redundant cygroup**</span><span class="sxs-lookup"><span data-stu-id="2f38d-117">Data type: **CIM\_RedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="2f38d-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f38d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f38d-119">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="2f38d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2f38d-120">Die **CIM \_ redundant cycomponent** -Zuordnung gibt an, dass diese Gruppe von Fans oder diese physischen Blöcke an einer einzelnen Redundanz Gruppe teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="2f38d-120">The **CIM\_RedundancyComponent** association indicates that 'this set of fans' or 'these physical extents' participate in a single redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="2f38d-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2f38d-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f38d-122">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="2f38d-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="2f38d-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f38d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f38d-124">Ein [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) , das das untergeordnete Element in der Zuordnung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2f38d-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

<span data-ttu-id="2f38d-125">Diese Eigenschaft wird von der [**CIM- \_ Komponente**](cim-component.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2f38d-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f38d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f38d-126">Remarks</span></span>

<span data-ttu-id="2f38d-127">**CIM \_ Redundant cycomponent** wird von der [**CIM- \_ Komponente**](cim-component.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2f38d-127">**CIM\_RedundancyComponent** is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="2f38d-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2f38d-128">WMI does not implement this class.</span></span>

<span data-ttu-id="2f38d-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2f38d-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2f38d-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2f38d-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f38d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f38d-131">Requirements</span></span>



| <span data-ttu-id="2f38d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f38d-132">Requirement</span></span> | <span data-ttu-id="2f38d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="2f38d-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f38d-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f38d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2f38d-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f38d-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f38d-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f38d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2f38d-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f38d-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f38d-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f38d-138">Namespace</span></span><br/>                | <span data-ttu-id="2f38d-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2f38d-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2f38d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="2f38d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f38d-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2f38d-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f38d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2f38d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f38d-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f38d-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f38d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f38d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f38d-145">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="2f38d-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

