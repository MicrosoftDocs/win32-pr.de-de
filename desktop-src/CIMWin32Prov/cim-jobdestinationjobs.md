---
description: Die CIM \_ jobdestinationjobs-Zuordnung beschreibt, wo ein Auftrag zur Verarbeitung übermittelt wird (d. h. an welches Auftrags Ziel).
ms.assetid: 6f732d34-2284-4909-a966-6b4066780cb0
ms.tgt_platform: multiple
title: CIM_JobDestinationJobs-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestinationJobs
- CIM_JobDestinationJobs.Dependent
- CIM_JobDestinationJobs.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e59e20f776c410db53294b6f6e98a1b13aef0de
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214185"
---
# <a name="cim_jobdestinationjobs-class"></a><span data-ttu-id="a725d-103">CIM \_ jobdestinationjobs-Klasse</span><span class="sxs-lookup"><span data-stu-id="a725d-103">CIM\_JobDestinationJobs class</span></span>

<span data-ttu-id="a725d-104">Die **CIM \_ jobdestinationjobs-Zuordnung** beschreibt, wo ein Auftrag zur Verarbeitung übermittelt wird (d. h. an welches Auftrags Ziel).</span><span class="sxs-lookup"><span data-stu-id="a725d-104">The **CIM\_JobDestinationJobs** association describes where a job is submitted for processing (that is, to which job destination).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a725d-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a725d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a725d-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a725d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a725d-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a725d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a725d-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a725d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a725d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a725d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D079BEE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestinationJobs : CIM_Dependency
{
  CIM_Job            REF Dependent;
  CIM_JobDestination REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="a725d-110">Member</span><span class="sxs-lookup"><span data-stu-id="a725d-110">Members</span></span>

<span data-ttu-id="a725d-111">Die **CIM \_ jobdestinationjobs** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a725d-111">The **CIM\_JobDestinationJobs** class has these types of members:</span></span>

-   [<span data-ttu-id="a725d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a725d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a725d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a725d-113">Properties</span></span>

<span data-ttu-id="a725d-114">Die **CIM \_ jobdestinationjobs** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a725d-114">The **CIM\_JobDestinationJobs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a725d-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="a725d-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a725d-116">Datentyp: **CIM \_ jobdestination**</span><span class="sxs-lookup"><span data-stu-id="a725d-116">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="a725d-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a725d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a725d-118">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="a725d-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a725d-119">Ein [**CIM \_ jobdestination**](cim-jobdestination.md) , das das Auftrags Ziel beschreibt, möglicherweise eine Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="a725d-119">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination, possibly a queue.</span></span>

</dd> <dt>

<span data-ttu-id="a725d-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="a725d-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a725d-121">Datentyp: **CIM- \_ Auftrag**</span><span class="sxs-lookup"><span data-stu-id="a725d-121">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="a725d-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a725d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a725d-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="a725d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a725d-124">Ein [**CIM- \_ Auftrag**](cim-job.md) , der den Auftrag in der Auftrags Warteschlange/dem Ziel beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a725d-124">A [**CIM\_Job**](cim-job.md) describing the job that is in the job queue/Destination.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a725d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a725d-125">Remarks</span></span>

<span data-ttu-id="a725d-126">**CIM \_ Jobdestinationjobs** wird von [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a725d-126">**CIM\_JobDestinationJobs** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="a725d-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a725d-127">WMI does not implement this class.</span></span>

<span data-ttu-id="a725d-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a725d-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a725d-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a725d-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a725d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a725d-130">Requirements</span></span>



| <span data-ttu-id="a725d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a725d-131">Requirement</span></span> | <span data-ttu-id="a725d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a725d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a725d-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a725d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a725d-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a725d-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a725d-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a725d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a725d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a725d-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a725d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="a725d-137">Namespace</span></span><br/>                | <span data-ttu-id="a725d-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a725d-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a725d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a725d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a725d-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a725d-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a725d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a725d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a725d-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a725d-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a725d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a725d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a725d-144">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="a725d-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

