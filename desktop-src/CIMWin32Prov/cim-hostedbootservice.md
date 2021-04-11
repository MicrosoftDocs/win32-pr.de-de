---
description: Die CIM \_ -Klasse "hostbootservice" ordnet ein Hostingsystem und einen Start Dienst zu. Da diese Beziehung vom CIM \_ -Hostingdienst untergeordnet ist, erbt Sie das für den Dienst definierte Bereichs Schema/Benennungs Schema, bei dem ein Dienst auf das Hostingsystem beschränkt wird.
ms.assetid: 91621288-a231-4423-94df-7601bdf2ebe1
ms.tgt_platform: multiple
title: CIM_HostedBootService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootService
- CIM_HostedBootService.Antecedent
- CIM_HostedBootService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12baa364653feda1400ad15d658e6739859b2521
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126969"
---
# <a name="cim_hostedbootservice-class"></a><span data-ttu-id="9b6d3-104">CIM-Klasse von " \_ hustedbootservice"</span><span class="sxs-lookup"><span data-stu-id="9b6d3-104">CIM\_HostedBootService class</span></span>

<span data-ttu-id="9b6d3-105">Die CIM-Klasse " **\_ hostbootservice** " ordnet ein Hostingsystem und einen Start Dienst zu.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-105">The **CIM\_HostedBootService** class associates a hosting system and a boot service.</span></span> <span data-ttu-id="9b6d3-106">Da diese Beziehung vom [**CIM- \_ Hostingdienst**](cim-hostedservice.md)untergeordnet ist, erbt Sie das für den Dienst definierte Bereichs Schema/Benennungs Schema, bei dem ein Dienst auf das Hostingsystem beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-106">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b6d3-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9b6d3-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9b6d3-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9b6d3-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9b6d3-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b6d3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b6d3-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{6DAE7092-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootService : CIM_HostedService
{
  CIM_System      REF Antecedent;
  CIM_BootService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9b6d3-112">Member</span><span class="sxs-lookup"><span data-stu-id="9b6d3-112">Members</span></span>

<span data-ttu-id="9b6d3-113">Die CIM-Klasse " **\_ hustedbootservice** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9b6d3-113">The **CIM\_HostedBootService** class has these types of members:</span></span>

-   [<span data-ttu-id="9b6d3-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b6d3-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b6d3-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b6d3-115">Properties</span></span>

<span data-ttu-id="9b6d3-116">Die CIM-Klasse " **\_ hustedbootservice** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-116">The **CIM\_HostedBootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b6d3-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="9b6d3-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d3-118">Datentyp: **CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="9b6d3-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d3-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b6d3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d3-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung (Vorgänger)</span><span class="sxs-lookup"><span data-stu-id="9b6d3-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="9b6d3-121">Ein [**CIM- \_ System**](cim-system.md) , das das Hostingsystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d3-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="9b6d3-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b6d3-123">Datentyp: **CIM- \_ Bootservice**</span><span class="sxs-lookup"><span data-stu-id="9b6d3-123">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="9b6d3-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b6d3-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b6d3-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="9b6d3-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9b6d3-126">Ein [**CIM- \_ Bootservice**](cim-bootservice.md) , der den auf dem System gehosteten Start Dienst beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-126">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b6d3-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b6d3-127">Remarks</span></span>

<span data-ttu-id="9b6d3-128">Die CIM-Klasse " **\_ hustedbootservice** " wird vom CIM-Dienst für den [**\_ Dienst**](cim-hostedservice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-128">The **CIM\_HostedBootService** class is derived from [**CIM\_HostedService**](cim-hostedservice.md).</span></span>

<span data-ttu-id="9b6d3-129">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-129">WMI does not implement this class.</span></span>

<span data-ttu-id="9b6d3-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9b6d3-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9b6d3-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b6d3-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b6d3-132">Requirements</span></span>



| <span data-ttu-id="9b6d3-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b6d3-133">Requirement</span></span> | <span data-ttu-id="9b6d3-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9b6d3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b6d3-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b6d3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9b6d3-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b6d3-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b6d3-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b6d3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9b6d3-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b6d3-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b6d3-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b6d3-139">Namespace</span></span><br/>                | <span data-ttu-id="9b6d3-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9b6d3-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b6d3-141">MOF</span><span class="sxs-lookup"><span data-stu-id="9b6d3-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b6d3-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9b6d3-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b6d3-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9b6d3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b6d3-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b6d3-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b6d3-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b6d3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6d3-146">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="9b6d3-146">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> </dl>

 

