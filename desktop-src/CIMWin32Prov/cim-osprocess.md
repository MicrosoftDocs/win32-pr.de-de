---
description: Die CIM \_ osprocess-Klasse ordnet das Betriebssystem und einen oder mehrere Prozesse zu, die im Kontext des Betriebssystems ausgeführt werden.
ms.assetid: 59d52b29-9d97-464f-bbbc-4191305df8c7
ms.tgt_platform: multiple
title: CIM_OSProcess-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSProcess
- CIM_OSProcess.PartComponent
- CIM_OSProcess.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b11738669c87b402f12932ad65237a512360427
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860751"
---
# <a name="cim_osprocess-class"></a><span data-ttu-id="69950-103">CIM- \_ osprocess-Klasse</span><span class="sxs-lookup"><span data-stu-id="69950-103">CIM\_OSProcess class</span></span>

<span data-ttu-id="69950-104">Die **CIM \_ osprocess** -Klasse ordnet das Betriebssystem und einen oder mehrere Prozesse zu, die im Kontext des Betriebssystems ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="69950-104">The **CIM\_OSProcess** class associates the operating system and one or more processes running in the context of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69950-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="69950-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="69950-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="69950-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="69950-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="69950-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="69950-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="69950-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="69950-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="69950-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A361A7AE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OSProcess : CIM_Component
{
  CIM_Process         REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="69950-110">Member</span><span class="sxs-lookup"><span data-stu-id="69950-110">Members</span></span>

<span data-ttu-id="69950-111">Die **CIM \_ osprocess** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="69950-111">The **CIM\_OSProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="69950-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69950-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69950-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69950-113">Properties</span></span>

<span data-ttu-id="69950-114">Die **CIM \_ osprocess** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="69950-114">The **CIM\_OSProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="69950-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="69950-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69950-116">Datentyp: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="69950-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="69950-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69950-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69950-118">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="69950-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="69950-119">Ein [**CIM- \_ OperatingSystem**](cim-operatingsystem.md) , das das Betriebssystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="69950-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="69950-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="69950-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69950-121">Datentyp: **CIM- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="69950-121">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="69950-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69950-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69950-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("PartComponent"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="69950-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="69950-124">Ein [**CIM- \_ Prozess**](cim-process.md) , der den Prozess beschreibt, der im Kontext des Betriebssystems ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69950-124">A [**CIM\_Process**](cim-process.md) describing the process running in the context of the operating system</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69950-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69950-125">Remarks</span></span>

<span data-ttu-id="69950-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="69950-126">WMI does not implement this class.</span></span>

<span data-ttu-id="69950-127">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="69950-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="69950-128">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="69950-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="69950-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69950-129">Requirements</span></span>



| <span data-ttu-id="69950-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69950-130">Requirement</span></span> | <span data-ttu-id="69950-131">Wert</span><span class="sxs-lookup"><span data-stu-id="69950-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69950-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69950-132">Minimum supported client</span></span><br/> | <span data-ttu-id="69950-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69950-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="69950-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69950-134">Minimum supported server</span></span><br/> | <span data-ttu-id="69950-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69950-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="69950-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="69950-136">Namespace</span></span><br/>                | <span data-ttu-id="69950-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="69950-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="69950-138">MOF</span><span class="sxs-lookup"><span data-stu-id="69950-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69950-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="69950-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="69950-140">DLL</span><span class="sxs-lookup"><span data-stu-id="69950-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69950-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69950-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69950-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69950-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69950-143">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="69950-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

