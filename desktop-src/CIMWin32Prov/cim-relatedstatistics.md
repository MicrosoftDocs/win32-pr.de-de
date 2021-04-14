---
description: Die CIM \_ relatedstatistics-Zuordnung stellt Hierarchien und Abhängigkeiten verwandter CIM \_ statisticalinformation-Klassen dar.
ms.assetid: f5cea01d-7854-4ad4-a89e-db0ce9f4a83f
ms.tgt_platform: multiple
title: CIM_RelatedStatistics-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RelatedStatistics
- CIM_RelatedStatistics.RelatedStats
- CIM_RelatedStatistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01fb70535a4ae8f84d637cf92a06eee4fe318a49
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523115"
---
# <a name="cim_relatedstatistics-class"></a><span data-ttu-id="97f14-103">CIM \_ relatedstatistics-Klasse</span><span class="sxs-lookup"><span data-stu-id="97f14-103">CIM\_RelatedStatistics class</span></span>

<span data-ttu-id="97f14-104">Die **CIM \_ relatedstatistics** -Zuordnung stellt Hierarchien und Abhängigkeiten verwandter [**CIM \_ statisticalinformation**](cim-statisticalinformation.md) -Klassen dar.</span><span class="sxs-lookup"><span data-stu-id="97f14-104">The **CIM\_RelatedStatistics** association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97f14-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="97f14-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="97f14-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="97f14-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="97f14-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="97f14-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="97f14-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="97f14-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="97f14-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="97f14-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A4-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_RelatedStatistics
{
  CIM_StatisticalInformation REF RelatedStats;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="97f14-110">Member</span><span class="sxs-lookup"><span data-stu-id="97f14-110">Members</span></span>

<span data-ttu-id="97f14-111">Die **CIM \_ relatedstatistics** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="97f14-111">The **CIM\_RelatedStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="97f14-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="97f14-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97f14-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="97f14-113">Properties</span></span>

<span data-ttu-id="97f14-114">Die **CIM \_ relatedstatistics** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="97f14-114">The **CIM\_RelatedStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97f14-115">**Relatedstats**</span><span class="sxs-lookup"><span data-stu-id="97f14-115">**RelatedStats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f14-116">Datentyp: **CIM \_ statisticalinformation**</span><span class="sxs-lookup"><span data-stu-id="97f14-116">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="97f14-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="97f14-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97f14-118">Verweis auf die zugehörigen Statistiken oder Metriken.</span><span class="sxs-lookup"><span data-stu-id="97f14-118">Reference to the related statistics or metrics.</span></span>

</dd> <dt>

<span data-ttu-id="97f14-119">**Stats**</span><span class="sxs-lookup"><span data-stu-id="97f14-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f14-120">Datentyp: **CIM \_ statisticalinformation**</span><span class="sxs-lookup"><span data-stu-id="97f14-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="97f14-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="97f14-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97f14-122">Verweis auf die statistischen Informationen oder das Objekt.</span><span class="sxs-lookup"><span data-stu-id="97f14-122">Reference to the statistic information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97f14-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97f14-123">Remarks</span></span>

<span data-ttu-id="97f14-124">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="97f14-124">WMI does not implement this class.</span></span>

<span data-ttu-id="97f14-125">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="97f14-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="97f14-126">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="97f14-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="97f14-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97f14-127">Requirements</span></span>



| <span data-ttu-id="97f14-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97f14-128">Requirement</span></span> | <span data-ttu-id="97f14-129">Wert</span><span class="sxs-lookup"><span data-stu-id="97f14-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97f14-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97f14-130">Minimum supported client</span></span><br/> | <span data-ttu-id="97f14-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97f14-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97f14-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97f14-132">Minimum supported server</span></span><br/> | <span data-ttu-id="97f14-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97f14-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97f14-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="97f14-134">Namespace</span></span><br/>                | <span data-ttu-id="97f14-135">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="97f14-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="97f14-136">MOF</span><span class="sxs-lookup"><span data-stu-id="97f14-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97f14-137"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="97f14-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="97f14-138">DLL</span><span class="sxs-lookup"><span data-stu-id="97f14-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97f14-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97f14-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




