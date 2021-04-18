---
description: Die CIM \_ -Klasse "Hostdienst" stellt eine Zuordnung zwischen einem Dienst und dem System dar, auf dem sich die Funktionalität befindet.
ms.assetid: 23bb385d-dd22-4126-aea9-d2f22527223e
ms.tgt_platform: multiple
title: CIM_HostedService-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Dependent
- CIM_HostedService.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c63b28fed7977c9fce78fe1030afbe66d5b2d75e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343980"
---
# <a name="cim_hostedservice-class-cimwin32-wmi-providers"></a><span data-ttu-id="23d31-103">CIM_HostedService-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="23d31-103">CIM_HostedService class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="23d31-104">Die CIM-Klasse " **\_ Hostdienst** " stellt eine Zuordnung zwischen einem Dienst und dem System dar, auf dem sich die Funktionalität befindet.</span><span class="sxs-lookup"><span data-stu-id="23d31-104">The **CIM\_HostedService** class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="23d31-105">Ein System kann viele Dienste hosten, die auf das Hostingsystem zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="23d31-105">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="23d31-106">Das Modell stellt keine Dienste dar, die auf mehreren Systemen gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="23d31-106">The model does not represent services hosted across multiple systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23d31-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="23d31-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="23d31-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="23d31-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="23d31-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="23d31-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="23d31-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="23d31-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="23d31-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="23d31-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{83B2A7AA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedService : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_System  REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="23d31-112">Member</span><span class="sxs-lookup"><span data-stu-id="23d31-112">Members</span></span>

<span data-ttu-id="23d31-113">Die CIM-Klasse " **\_ hustedservice** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="23d31-113">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="23d31-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23d31-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23d31-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23d31-115">Properties</span></span>

<span data-ttu-id="23d31-116">Die CIM-Klasse " **\_ hustedservice** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="23d31-116">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23d31-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="23d31-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23d31-118">Datentyp: **CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="23d31-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="23d31-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23d31-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23d31-120">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="23d31-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="23d31-121">Ein [**CIM- \_ System**](cim-system.md) , das das Hostingsystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="23d31-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="23d31-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="23d31-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23d31-123">Datentyp: **CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="23d31-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="23d31-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23d31-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23d31-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="23d31-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="23d31-126">Ein [**CIM- \_ Dienst**](cim-service.md) , der den auf dem System gehosteten Dienst beschreibt.</span><span class="sxs-lookup"><span data-stu-id="23d31-126">A [**CIM\_Service**](cim-service.md) that describes the service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23d31-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23d31-127">Remarks</span></span>

<span data-ttu-id="23d31-128">**CIM \_ Der "hustedservice** " ist von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="23d31-128">**CIM\_HostedService** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="23d31-129">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="23d31-129">WMI does not implement this class.</span></span>

<span data-ttu-id="23d31-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="23d31-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="23d31-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="23d31-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="23d31-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23d31-132">Requirements</span></span>



| <span data-ttu-id="23d31-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23d31-133">Requirement</span></span> | <span data-ttu-id="23d31-134">Wert</span><span class="sxs-lookup"><span data-stu-id="23d31-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23d31-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23d31-135">Minimum supported client</span></span><br/> | <span data-ttu-id="23d31-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23d31-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23d31-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23d31-137">Minimum supported server</span></span><br/> | <span data-ttu-id="23d31-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23d31-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23d31-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="23d31-139">Namespace</span></span><br/>                | <span data-ttu-id="23d31-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="23d31-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="23d31-141">MOF</span><span class="sxs-lookup"><span data-stu-id="23d31-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23d31-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="23d31-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="23d31-143">DLL</span><span class="sxs-lookup"><span data-stu-id="23d31-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23d31-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23d31-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23d31-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23d31-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23d31-146">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="23d31-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

