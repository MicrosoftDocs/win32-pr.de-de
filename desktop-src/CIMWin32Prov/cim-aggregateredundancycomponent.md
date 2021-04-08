---
description: Die CIM- \_ aggregateredundancycomponent-Klasse beschreibt den aggregierten physischen Block in einer Speicher Redundanz Gruppe.
ms.assetid: 3407e888-e17c-4f65-a33f-056002accbf7
ms.tgt_platform: multiple
title: CIM_AggregateRedundancyComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregateRedundancyComponent
- CIM_AggregateRedundancyComponent.PartComponent
- CIM_AggregateRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9a5e638730578bad8d64f35b29a5152898c23fd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748713"
---
# <a name="cim_aggregateredundancycomponent-class"></a><span data-ttu-id="52093-103">CIM- \_ aggregateredundancycomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="52093-103">CIM\_AggregateRedundancyComponent class</span></span>

<span data-ttu-id="52093-104">Die **CIM- \_ aggregateredundancycomponent** -Klasse beschreibt den aggregierten physischen Block in einer Speicher Redundanz Gruppe.</span><span class="sxs-lookup"><span data-stu-id="52093-104">The **CIM\_AggregateRedundancyComponent** class describes the aggregate physical extent in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52093-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="52093-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="52093-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="52093-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="52093-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="52093-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="52093-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="52093-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="52093-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="52093-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{154E66D8-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AggregateRedundancyComponent : CIM_RedundancyComponent
{
  CIM_AggregatePExtent       REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="52093-110">Member</span><span class="sxs-lookup"><span data-stu-id="52093-110">Members</span></span>

<span data-ttu-id="52093-111">Die **CIM- \_ aggregateredundancycomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="52093-111">The **CIM\_AggregateRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="52093-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52093-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52093-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52093-113">Properties</span></span>

<span data-ttu-id="52093-114">Die **CIM- \_ aggregateredundancycomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="52093-114">The **CIM\_AggregateRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52093-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="52093-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52093-116">Datentyp: **CIM \_ storageredundancygroup**</span><span class="sxs-lookup"><span data-stu-id="52093-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="52093-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52093-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52093-118">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="52093-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="52093-119">Eine [**CIM \_ storageredundancygroup**](cim-storageredundancygroup.md) , die die Speicher Redundanz Gruppe enthält.</span><span class="sxs-lookup"><span data-stu-id="52093-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that contains the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="52093-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="52093-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52093-121">Datentyp: **CIM \_ aggregatepblock**</span><span class="sxs-lookup"><span data-stu-id="52093-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="52093-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52093-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52093-123">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="52093-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="52093-124">Ein [**CIM- \_ aggregatepblock**](cim-aggregatepextent.md) , der den aggregierten physischen Block enthält, der Teil der Redundanz Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="52093-124">A [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that contains the aggregate physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52093-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52093-125">Remarks</span></span>

<span data-ttu-id="52093-126">Die **CIM- \_ aggregateredundancycomponent** -Klasse wird von [**CIM \_ redundant cycomponent**](cim-redundancycomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="52093-126">The **CIM\_AggregateRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="52093-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="52093-127">WMI does not implement this class.</span></span>

<span data-ttu-id="52093-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="52093-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="52093-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="52093-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="52093-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52093-130">Requirements</span></span>



| <span data-ttu-id="52093-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52093-131">Requirement</span></span> | <span data-ttu-id="52093-132">Wert</span><span class="sxs-lookup"><span data-stu-id="52093-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52093-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52093-133">Minimum supported client</span></span><br/> | <span data-ttu-id="52093-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52093-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52093-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52093-135">Minimum supported server</span></span><br/> | <span data-ttu-id="52093-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52093-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52093-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="52093-137">Namespace</span></span><br/>                | <span data-ttu-id="52093-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="52093-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="52093-139">MOF</span><span class="sxs-lookup"><span data-stu-id="52093-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52093-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="52093-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="52093-141">DLL</span><span class="sxs-lookup"><span data-stu-id="52093-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52093-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52093-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52093-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52093-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52093-144">**CIM \_ redundant cycomponent**</span><span class="sxs-lookup"><span data-stu-id="52093-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

