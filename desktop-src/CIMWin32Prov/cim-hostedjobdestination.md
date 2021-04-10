---
description: Die CIM \_ -Klasse "hostjobdestination" stellt eine Zuordnung zwischen einem Auftrags Ziel und dem System dar, auf dem es sich befindet. Ein System kann viele Auftrags Warteschlangen hosten. Auftrags Ziele werden an das Hostingsystem zurück verschoben.
ms.assetid: 5d853826-1f27-417b-a053-5e0ee9816376
ms.tgt_platform: multiple
title: CIM_HostedJobDestination-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedJobDestination
- CIM_HostedJobDestination.Dependent
- CIM_HostedJobDestination.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c22e911c6b0adcc38de11fd2410e4797c9381a25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214189"
---
# <a name="cim_hostedjobdestination-class"></a><span data-ttu-id="37583-105">CIM- \_ Klasse "hustedjobdestination"</span><span class="sxs-lookup"><span data-stu-id="37583-105">CIM\_HostedJobDestination class</span></span>

<span data-ttu-id="37583-106">Die CIM-Klasse " **\_ hostjobdestination** " stellt eine Zuordnung zwischen einem Auftrags Ziel und dem System dar, auf dem es sich befindet.</span><span class="sxs-lookup"><span data-stu-id="37583-106">The **CIM\_HostedJobDestination** class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="37583-107">Ein System kann viele Auftrags Warteschlangen hosten.</span><span class="sxs-lookup"><span data-stu-id="37583-107">A system may host many job queues.</span></span> <span data-ttu-id="37583-108">Auftrags Ziele werden an das Hostingsystem zurück verschoben.</span><span class="sxs-lookup"><span data-stu-id="37583-108">Job destinations defer to the hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37583-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="37583-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="37583-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="37583-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="37583-111">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="37583-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="37583-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="37583-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="37583-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="37583-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{7880DD16-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedJobDestination : CIM_Dependency
{
  CIM_JobDestination REF Dependent;
  CIM_System         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="37583-114">Member</span><span class="sxs-lookup"><span data-stu-id="37583-114">Members</span></span>

<span data-ttu-id="37583-115">Die CIM-Klasse " **\_ hustedjobdestination** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="37583-115">The **CIM\_HostedJobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="37583-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37583-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37583-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37583-117">Properties</span></span>

<span data-ttu-id="37583-118">Die CIM-Klasse " **\_ hustedjobdestination** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="37583-118">The **CIM\_HostedJobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37583-119">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="37583-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37583-120">Datentyp: **CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="37583-120">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="37583-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37583-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37583-122">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="37583-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="37583-123">Ein [**CIM- \_ System**](cim-system.md) , das das Hostingsystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="37583-123">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="37583-124">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="37583-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37583-125">Datentyp: **CIM \_ jobdestination**</span><span class="sxs-lookup"><span data-stu-id="37583-125">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="37583-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37583-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37583-127">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="37583-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="37583-128">Ein [**CIM \_ jobdestination**](cim-jobdestination.md) , das das auf dem System gehostete Auftrags Ziel beschreibt.</span><span class="sxs-lookup"><span data-stu-id="37583-128">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37583-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37583-129">Remarks</span></span>

<span data-ttu-id="37583-130">**CIM \_ "Host jobdestination** " ist von [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="37583-130">**CIM\_HostedJobDestination** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="37583-131">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="37583-131">WMI does not implement this class.</span></span>

<span data-ttu-id="37583-132">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="37583-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="37583-133">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="37583-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="37583-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37583-134">Requirements</span></span>



| <span data-ttu-id="37583-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37583-135">Requirement</span></span> | <span data-ttu-id="37583-136">Wert</span><span class="sxs-lookup"><span data-stu-id="37583-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37583-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37583-137">Minimum supported client</span></span><br/> | <span data-ttu-id="37583-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37583-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37583-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37583-139">Minimum supported server</span></span><br/> | <span data-ttu-id="37583-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37583-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37583-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="37583-141">Namespace</span></span><br/>                | <span data-ttu-id="37583-142">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="37583-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="37583-143">MOF</span><span class="sxs-lookup"><span data-stu-id="37583-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37583-144"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="37583-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="37583-145">DLL</span><span class="sxs-lookup"><span data-stu-id="37583-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37583-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37583-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37583-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37583-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37583-148">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="37583-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

