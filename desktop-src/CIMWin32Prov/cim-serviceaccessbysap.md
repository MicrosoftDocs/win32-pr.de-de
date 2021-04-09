---
description: Die CIM \_ serviceaccessbysap Association-Klasse stellt die Zugriffspunkte für einen Dienst dar. Beispielsweise kann auf einen Drucker über NetWare, Macintosh oder Windows-Dienst Zugriffspunkte (SAPS) zugegriffen werden, die potenziell auf unterschiedlichen Systemen gehostet werden.
ms.assetid: 68311a56-b034-4a30-a885-74a745a738d8
ms.tgt_platform: multiple
title: CIM_ServiceAccessBySAP-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessBySAP
- CIM_ServiceAccessBySAP.Dependent
- CIM_ServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e34b2af50a6475461ae4d39d156d26143fcb75f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958342"
---
# <a name="cim_serviceaccessbysap-class"></a><span data-ttu-id="a4d13-104">CIM \_ serviceaccessbysap-Klasse</span><span class="sxs-lookup"><span data-stu-id="a4d13-104">CIM\_ServiceAccessBySAP class</span></span>

<span data-ttu-id="a4d13-105">Die **CIM \_ serviceaccessbysap** Association-Klasse stellt die Zugriffspunkte für einen Dienst dar.</span><span class="sxs-lookup"><span data-stu-id="a4d13-105">The **CIM\_ServiceAccessBySAP** association class represents the access points for a service.</span></span> <span data-ttu-id="a4d13-106">Beispielsweise kann auf einen Drucker über NetWare, Macintosh oder Windows-Dienst Zugriffspunkte (SAPS) zugegriffen werden, die potenziell auf unterschiedlichen Systemen gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="a4d13-106">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a4d13-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a4d13-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a4d13-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a4d13-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a4d13-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a4d13-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a4d13-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a4d13-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d13-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4d13-111">Syntax</span></span>

``` syntax
[UUID("{714C00BA-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessBySAP : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_Service            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="a4d13-112">Member</span><span class="sxs-lookup"><span data-stu-id="a4d13-112">Members</span></span>

<span data-ttu-id="a4d13-113">Die **CIM \_ serviceaccessbysap** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a4d13-113">The **CIM\_ServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="a4d13-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4d13-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4d13-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4d13-115">Properties</span></span>

<span data-ttu-id="a4d13-116">Die **CIM \_ serviceaccessbysap** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a4d13-116">The **CIM\_ServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4d13-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="a4d13-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d13-118">Datentyp: **CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="a4d13-118">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="a4d13-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a4d13-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4d13-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="a4d13-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a4d13-121">Ein [**CIM- \_ Dienst**](cim-service.md) , der den Dienst beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a4d13-121">A [**CIM\_Service**](cim-service.md) that describes the service.</span></span>

</dd> <dt>

<span data-ttu-id="a4d13-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="a4d13-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d13-123">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="a4d13-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="a4d13-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a4d13-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4d13-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="a4d13-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a4d13-126">Ein [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) , der einen Zugriffspunkt für einen Dienst beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a4d13-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes an access point for a service.</span></span> <span data-ttu-id="a4d13-127">Zugriffspunkte sind von dieser Beziehung abhängig, da Sie keine Funktion ohne entsprechenden Dienst haben.</span><span class="sxs-lookup"><span data-stu-id="a4d13-127">Access points are dependent in this relationship since they have no function without a corresponding service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4d13-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4d13-128">Remarks</span></span>

<span data-ttu-id="a4d13-129">Die **CIM- \_ serviceaccessbysap** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a4d13-129">The **CIM\_ServiceAccessBySAP** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="a4d13-130">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a4d13-130">WMI does not implement this class.</span></span> <span data-ttu-id="a4d13-131">Informationen zu WMI-Klassen, die von **CIM \_ serviceaccessbysap** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a4d13-131">For WMI classes that are derived from **CIM\_ServiceAccessBySAP**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a4d13-132">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a4d13-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a4d13-133">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a4d13-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4d13-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4d13-134">Requirements</span></span>



| <span data-ttu-id="a4d13-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4d13-135">Requirement</span></span> | <span data-ttu-id="a4d13-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a4d13-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d13-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4d13-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a4d13-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4d13-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4d13-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4d13-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a4d13-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4d13-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4d13-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4d13-141">Namespace</span></span><br/>                | <span data-ttu-id="a4d13-142">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a4d13-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a4d13-143">MOF</span><span class="sxs-lookup"><span data-stu-id="a4d13-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4d13-144"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a4d13-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4d13-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a4d13-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4d13-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4d13-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4d13-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4d13-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d13-148">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="a4d13-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

