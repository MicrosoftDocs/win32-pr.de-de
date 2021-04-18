---
description: Die CIM-Erweiterung " \_ realizesaggregatepblock" stellt die Beziehung dar, in der die CIM- \_ aggregatepblock-Klasse auf einem physischen Medium realisiert wird.
ms.assetid: 420dde1d-daa8-4cd3-b3fd-c2aefdc1e217
ms.tgt_platform: multiple
title: CIM_RealizesAggregatePExtent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesAggregatePExtent
- CIM_RealizesAggregatePExtent.Dependent
- CIM_RealizesAggregatePExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb80414134534d09a4030e2e87003a660e69fd9f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343971"
---
# <a name="cim_realizesaggregatepextent-class"></a><span data-ttu-id="7d8cb-103">CIM \_ realizesaggregatepblock-Klasse</span><span class="sxs-lookup"><span data-stu-id="7d8cb-103">CIM\_RealizesAggregatePExtent class</span></span>

<span data-ttu-id="7d8cb-104">Die CIM-Erweiterung " **\_ realizesaggregatepblock** " stellt die Beziehung dar, in der die [**CIM- \_ aggregatepblock**](cim-aggregatepextent.md) -Klasse auf einem physischen Medium realisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7d8cb-104">The **CIM\_RealizesAggregatePExtent** association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d8cb-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7d8cb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7d8cb-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7d8cb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7d8cb-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7d8cb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7d8cb-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7d8cb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d8cb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d8cb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B81-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesAggregatePExtent : CIM_Realizes
{
  CIM_AggregatePExtent REF Dependent;
  CIM_PhysicalMedia    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7d8cb-110">Member</span><span class="sxs-lookup"><span data-stu-id="7d8cb-110">Members</span></span>

<span data-ttu-id="7d8cb-111">Die CIM-Klasse " **\_ realizesaggregatepblock** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7d8cb-111">The **CIM\_RealizesAggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="7d8cb-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d8cb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d8cb-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d8cb-113">Properties</span></span>

<span data-ttu-id="7d8cb-114">Die CIM-Klasse " **\_ realizesaggregatepblock** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7d8cb-114">The **CIM\_RealizesAggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d8cb-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="7d8cb-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d8cb-116">Datentyp: **CIM \_ physicalmedia**</span><span class="sxs-lookup"><span data-stu-id="7d8cb-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="7d8cb-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7d8cb-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d8cb-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7d8cb-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7d8cb-119">Ein [**CIM- \_ physicalmedia**](cim-physicalmedia.md) , das das physische Medium beschreibt, auf dem der Block realisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7d8cb-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="7d8cb-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="7d8cb-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d8cb-121">Datentyp: **CIM \_ aggregatepblock**</span><span class="sxs-lookup"><span data-stu-id="7d8cb-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="7d8cb-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7d8cb-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d8cb-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="7d8cb-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7d8cb-124">Der [**CIM- \_ aggregatepblock**](cim-aggregatepextent.md) , der sich auf dem Medium befindet.</span><span class="sxs-lookup"><span data-stu-id="7d8cb-124">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that is located on the media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d8cb-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d8cb-125">Remarks</span></span>

<span data-ttu-id="7d8cb-126">Die CIM-Klasse " **\_ realizesaggregatepblock** " ist von CIM-Erkenntnissen abgeleitet. [**\_**](cim-realizes.md)</span><span class="sxs-lookup"><span data-stu-id="7d8cb-126">The **CIM\_RealizesAggregatePExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="7d8cb-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7d8cb-127">WMI does not implement this class.</span></span>

<span data-ttu-id="7d8cb-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7d8cb-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7d8cb-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7d8cb-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d8cb-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d8cb-130">Requirements</span></span>



| <span data-ttu-id="7d8cb-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d8cb-131">Requirement</span></span> | <span data-ttu-id="7d8cb-132">Wert</span><span class="sxs-lookup"><span data-stu-id="7d8cb-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8cb-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d8cb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7d8cb-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d8cb-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7d8cb-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d8cb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7d8cb-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d8cb-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7d8cb-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d8cb-137">Namespace</span></span><br/>                | <span data-ttu-id="7d8cb-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7d8cb-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7d8cb-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7d8cb-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d8cb-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7d8cb-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d8cb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7d8cb-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d8cb-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d8cb-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d8cb-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d8cb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d8cb-144">**CIM \_ erkennt**</span><span class="sxs-lookup"><span data-stu-id="7d8cb-144">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

