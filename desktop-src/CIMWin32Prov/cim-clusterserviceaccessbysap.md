---
description: Die CIM \_ clusterserviceaccessbysap-Klasse stellt die Beziehung zwischen einem Clustering-Dienst und seinen Zugriffs Punkten dar.
ms.assetid: b1e03ef1-909c-4836-a75f-c8d88a4d0087
ms.tgt_platform: multiple
title: CIM_ClusterServiceAccessBySAP-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusterServiceAccessBySAP
- CIM_ClusterServiceAccessBySAP.Dependent
- CIM_ClusterServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b6e6f0df20f182be392de3fbb0cb13068cbeffc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958454"
---
# <a name="cim_clusterserviceaccessbysap-class"></a><span data-ttu-id="1cb5c-103">CIM \_ clusterserviceaccessbysap-Klasse</span><span class="sxs-lookup"><span data-stu-id="1cb5c-103">CIM\_ClusterServiceAccessBySAP class</span></span>

<span data-ttu-id="1cb5c-104">Die **CIM \_ clusterserviceaccessbysap** -Klasse stellt die Beziehung zwischen einem Clustering-Dienst und seinen Zugriffs Punkten dar.</span><span class="sxs-lookup"><span data-stu-id="1cb5c-104">The **CIM\_ClusterServiceAccessBySAP** class represents the relationship between a clustering service and its access points.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1cb5c-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1cb5c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1cb5c-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1cb5c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1cb5c-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1cb5c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1cb5c-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1cb5c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cb5c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cb5c-109">Syntax</span></span>

``` syntax
[UUID("{88F073D8-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ClusterServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_ClusteringSAP     REF Dependent;
  CIM_ClusteringService REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="1cb5c-110">Member</span><span class="sxs-lookup"><span data-stu-id="1cb5c-110">Members</span></span>

<span data-ttu-id="1cb5c-111">Die **CIM \_ clusterserviceaccessbysap** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1cb5c-111">The **CIM\_ClusterServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="1cb5c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1cb5c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1cb5c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1cb5c-113">Properties</span></span>

<span data-ttu-id="1cb5c-114">Die **CIM \_ clusterserviceaccessbysap** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1cb5c-114">The **CIM\_ClusterServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1cb5c-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="1cb5c-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cb5c-116">Datentyp: **CIM \_ clusteringservice**</span><span class="sxs-lookup"><span data-stu-id="1cb5c-116">Data type: **CIM\_ClusteringService**</span></span>
</dt> <dt>

<span data-ttu-id="1cb5c-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cb5c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cb5c-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="1cb5c-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="1cb5c-119">Ein [**CIM- \_ clusteringservice**](cim-clusteringservice.md) , der den Clustering-Dienst beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1cb5c-119">A [**CIM\_ClusteringService**](cim-clusteringservice.md) that describes the clustering service.</span></span>

</dd> <dt>

<span data-ttu-id="1cb5c-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="1cb5c-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cb5c-121">Datentyp: **CIM \_ clusteringsap**</span><span class="sxs-lookup"><span data-stu-id="1cb5c-121">Data type: **CIM\_ClusteringSAP**</span></span>
</dt> <dt>

<span data-ttu-id="1cb5c-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1cb5c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cb5c-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="1cb5c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1cb5c-124">Ein [**CIM \_ clusteringsap**](cim-clusteringsap.md) , das einen Zugriffspunkt für den Clustering-Dienst beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1cb5c-124">A [**CIM\_ClusteringSAP**](cim-clusteringsap.md) that describes an access point for the clustering service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cb5c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cb5c-125">Remarks</span></span>

<span data-ttu-id="1cb5c-126">Die **CIM \_ clusterserviceaccessbysap** -Klasse wird von [**CIM \_ serviceaccessbysap**](cim-serviceaccessbysap.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1cb5c-126">The **CIM\_ClusterServiceAccessBySAP** class is derived from [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span></span>

<span data-ttu-id="1cb5c-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1cb5c-127">WMI does not implement this class.</span></span>

<span data-ttu-id="1cb5c-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1cb5c-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1cb5c-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1cb5c-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cb5c-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cb5c-130">Requirements</span></span>



| <span data-ttu-id="1cb5c-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1cb5c-131">Requirement</span></span> | <span data-ttu-id="1cb5c-132">Wert</span><span class="sxs-lookup"><span data-stu-id="1cb5c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb5c-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1cb5c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1cb5c-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1cb5c-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1cb5c-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1cb5c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1cb5c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cb5c-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1cb5c-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="1cb5c-137">Namespace</span></span><br/>                | <span data-ttu-id="1cb5c-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1cb5c-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1cb5c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1cb5c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cb5c-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1cb5c-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1cb5c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1cb5c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cb5c-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cb5c-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cb5c-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cb5c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cb5c-144">**CIM \_ serviceaccessbysap**</span><span class="sxs-lookup"><span data-stu-id="1cb5c-144">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> </dl>

 

