---
description: Die CIM \_ -Klasse "stestedaccesspoint" stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und dem System dar, auf dem es bereitgestellt wird. Jedes System hostet möglicherweise viele SAPS.
ms.assetid: 7da9b781-a5cb-42f5-b03c-4fc818c94e88
ms.tgt_platform: multiple
title: CIM_HostedAccessPoint-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Dependent
- CIM_HostedAccessPoint.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d451cec7ad42fa519b70c576fbd02a32d0289e8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126973"
---
# <a name="cim_hostedaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="eea76-104">CIM_HostedAccessPoint-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="eea76-104">CIM_HostedAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="eea76-105">Die CIM-Klasse " **\_ stestedaccesspoint** " stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und dem System dar, auf dem es bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="eea76-105">The **CIM\_HostedAccessPoint** class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="eea76-106">Jedes System hostet möglicherweise viele SAPS.</span><span class="sxs-lookup"><span data-stu-id="eea76-106">Each system may host many SAPs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eea76-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="eea76-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eea76-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eea76-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eea76-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="eea76-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="eea76-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="eea76-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea76-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="eea76-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{576C3C56-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedAccessPoint : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_System             REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="eea76-112">Member</span><span class="sxs-lookup"><span data-stu-id="eea76-112">Members</span></span>

<span data-ttu-id="eea76-113">Die CIM-Klasse " **\_ tarstedaccesspoint** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eea76-113">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="eea76-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eea76-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eea76-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eea76-115">Properties</span></span>

<span data-ttu-id="eea76-116">Die CIM-Klasse " **\_ stestedaccesspoint** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eea76-116">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eea76-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="eea76-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea76-118">Datentyp: **CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="eea76-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="eea76-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eea76-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eea76-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="eea76-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="eea76-121">Ein [**CIM- \_ System**](cim-system.md) , das das Hostingsystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="eea76-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="eea76-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="eea76-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea76-123">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="eea76-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="eea76-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eea76-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eea76-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eea76-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eea76-126">Ein [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) , der die SAP (s) beschreibt, die auf diesem System gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="eea76-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes The SAP(s) that are hosted on this system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eea76-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eea76-127">Remarks</span></span>

<span data-ttu-id="eea76-128">**CIM \_ "Hustedaccesspoint** " ist von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="eea76-128">**CIM\_HostedAccessPoint** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="eea76-129">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="eea76-129">WMI does not implement this class.</span></span>

<span data-ttu-id="eea76-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="eea76-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eea76-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="eea76-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea76-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eea76-132">Requirements</span></span>



| <span data-ttu-id="eea76-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eea76-133">Requirement</span></span> | <span data-ttu-id="eea76-134">Wert</span><span class="sxs-lookup"><span data-stu-id="eea76-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eea76-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eea76-135">Minimum supported client</span></span><br/> | <span data-ttu-id="eea76-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eea76-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eea76-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eea76-137">Minimum supported server</span></span><br/> | <span data-ttu-id="eea76-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eea76-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eea76-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="eea76-139">Namespace</span></span><br/>                | <span data-ttu-id="eea76-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eea76-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eea76-141">MOF</span><span class="sxs-lookup"><span data-stu-id="eea76-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eea76-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eea76-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eea76-143">DLL</span><span class="sxs-lookup"><span data-stu-id="eea76-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eea76-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eea76-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eea76-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eea76-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea76-146">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="eea76-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

