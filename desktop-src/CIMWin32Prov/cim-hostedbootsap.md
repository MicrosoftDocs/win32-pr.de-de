---
description: Die CIM- \_ Klasse "shostedbootsap" definiert das Hosting-einheitliche Computersystem für eine CIM- \_ bootsap-Klasse.
ms.assetid: 2113de13-e7af-4a1c-ba80-27e2c57af8a0
ms.tgt_platform: multiple
title: CIM_HostedBootSAP-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootSAP
- CIM_HostedBootSAP.Dependent
- CIM_HostedBootSAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12e801f420ca2c56cc8960175391cdd9a669a00d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958402"
---
# <a name="cim_hostedbootsap-class"></a><span data-ttu-id="116e8-103">CIM- \_ Klasse "hustedbootsap"</span><span class="sxs-lookup"><span data-stu-id="116e8-103">CIM\_HostedBootSAP class</span></span>

<span data-ttu-id="116e8-104">Die CIM-Klasse " **\_ shostedbootsap** " definiert das Hosting-einheitliche Computersystem für eine [**CIM- \_ bootsap**](cim-bootsap.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="116e8-104">The **CIM\_HostedBootSAP** class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="116e8-105">Da diese Beziehung von [**CIM \_ hostspoint**](cim-hostedaccesspoint.md)untergeordnet ist, erbt Sie das für [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)definierte Bereichs Schema/Benennungs Schema, bei dem ein Zugriffspunkt dem Hostingsystem entspricht.</span><span class="sxs-lookup"><span data-stu-id="116e8-105">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="116e8-106">In diesem Fall muss **CIM \_ bootsap** auf seine hostende [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md) -Klasse zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="116e8-106">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="116e8-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="116e8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="116e8-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="116e8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="116e8-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="116e8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="116e8-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="116e8-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="116e8-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="116e8-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{625B4512-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootSAP : CIM_HostedAccessPoint
{
  CIM_BootSAP               REF Dependent;
  CIM_UnitaryComputerSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="116e8-112">Member</span><span class="sxs-lookup"><span data-stu-id="116e8-112">Members</span></span>

<span data-ttu-id="116e8-113">Die CIM-Klasse " **\_ hustedbootsap** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="116e8-113">The **CIM\_HostedBootSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="116e8-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="116e8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="116e8-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="116e8-115">Properties</span></span>

<span data-ttu-id="116e8-116">Die CIM-Klasse " **\_ hustedbootsap** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="116e8-116">The **CIM\_HostedBootSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="116e8-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="116e8-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="116e8-118">Datentyp: **CIM \_ unitarycomputersystem**</span><span class="sxs-lookup"><span data-stu-id="116e8-118">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="116e8-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="116e8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="116e8-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="116e8-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="116e8-121">Ein [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md) , das das einheitliche Computersystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="116e8-121">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="116e8-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="116e8-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="116e8-123">Datentyp: **CIM \_ bootsap**</span><span class="sxs-lookup"><span data-stu-id="116e8-123">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="116e8-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="116e8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="116e8-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="116e8-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="116e8-126">Ein [**CIM- \_ bootsap**](cim-bootsap.md) , der den auf dem einheitlichen Computersystem gehosteten Start-SAP beschreibt.</span><span class="sxs-lookup"><span data-stu-id="116e8-126">A [**CIM\_BootSAP**](cim-bootsap.md) that describes the Boot SAP hosted on the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="116e8-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="116e8-127">Remarks</span></span>

<span data-ttu-id="116e8-128">Die CIM-Klasse " **\_ hustedbootsap** " wird von [**CIM " \_ hustedaccesspoint**](cim-hostedaccesspoint.md)" abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="116e8-128">The **CIM\_HostedBootSAP** class is derived from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md).</span></span>

<span data-ttu-id="116e8-129">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="116e8-129">WMI does not implement this class.</span></span>

<span data-ttu-id="116e8-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="116e8-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="116e8-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="116e8-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="116e8-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="116e8-132">Requirements</span></span>



| <span data-ttu-id="116e8-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="116e8-133">Requirement</span></span> | <span data-ttu-id="116e8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="116e8-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="116e8-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="116e8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="116e8-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="116e8-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="116e8-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="116e8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="116e8-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="116e8-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="116e8-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="116e8-139">Namespace</span></span><br/>                | <span data-ttu-id="116e8-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="116e8-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="116e8-141">MOF</span><span class="sxs-lookup"><span data-stu-id="116e8-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="116e8-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="116e8-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="116e8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="116e8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="116e8-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="116e8-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="116e8-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="116e8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="116e8-146">**CIM- \_ hubspoint**</span><span class="sxs-lookup"><span data-stu-id="116e8-146">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> </dl>

 

