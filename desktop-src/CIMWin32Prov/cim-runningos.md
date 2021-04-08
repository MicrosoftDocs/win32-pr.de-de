---
description: Die CIM \_ runningos-Klasse stellt das aktuell ausgeführte Betriebssystem dar. Höchstens ein Betriebssystem kann zu einem beliebigen Zeitpunkt auf einem Computersystem ausgeführt werden. das Computersystem ist möglicherweise nicht gestartet, oder sein Betriebssystem ist unbekannt.
ms.assetid: 93e3d425-d751-4252-aa81-7d6774c8f8c5
ms.tgt_platform: multiple
title: CIM_RunningOS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RunningOS
- CIM_RunningOS.Dependent
- CIM_RunningOS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ff86af88342a1b8f0147ecd9721765794faf39e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748952"
---
# <a name="cim_runningos-class"></a><span data-ttu-id="537ce-104">CIM \_ runningos-Klasse</span><span class="sxs-lookup"><span data-stu-id="537ce-104">CIM\_RunningOS class</span></span>

<span data-ttu-id="537ce-105">Die **CIM \_ runningos** -Klasse stellt das aktuell ausgeführte Betriebssystem dar.</span><span class="sxs-lookup"><span data-stu-id="537ce-105">The **CIM\_RunningOS** class represents the currently executing operating system.</span></span> <span data-ttu-id="537ce-106">Höchstens ein Betriebssystem kann zu einem beliebigen Zeitpunkt auf einem Computersystem ausgeführt werden. das Computersystem ist möglicherweise nicht gestartet, oder sein Betriebssystem ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="537ce-106">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="537ce-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="537ce-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="537ce-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="537ce-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="537ce-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="537ce-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="537ce-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="537ce-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="537ce-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="537ce-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1F2EA300-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RunningOS : CIM_Dependency
{
  CIM_ComputerSystem  REF Dependent;
  CIM_OperatingSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="537ce-112">Member</span><span class="sxs-lookup"><span data-stu-id="537ce-112">Members</span></span>

<span data-ttu-id="537ce-113">Die **CIM \_ runningos** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="537ce-113">The **CIM\_RunningOS** class has these types of members:</span></span>

-   [<span data-ttu-id="537ce-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="537ce-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="537ce-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="537ce-115">Properties</span></span>

<span data-ttu-id="537ce-116">Die **CIM \_ runningos** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="537ce-116">The **CIM\_RunningOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="537ce-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="537ce-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="537ce-118">Datentyp: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="537ce-118">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="537ce-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="537ce-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="537ce-120">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="537ce-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="537ce-121">Ein [**CIM- \_ OperatingSystem**](cim-operatingsystem.md) , das das zurzeit auf dem Computersystem laufende Betriebssystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="537ce-121">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system currently running on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="537ce-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="537ce-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="537ce-123">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="537ce-123">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="537ce-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="537ce-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="537ce-125">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="537ce-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="537ce-126">Ein [**CIM- \_ Computersystem**](cim-computersystem.md) , das das Computersystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="537ce-126">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="537ce-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="537ce-127">Remarks</span></span>

<span data-ttu-id="537ce-128">Die **CIM- \_ runningos** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="537ce-128">The **CIM\_RunningOS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="537ce-129">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="537ce-129">WMI does not implement this class.</span></span>

<span data-ttu-id="537ce-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="537ce-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="537ce-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="537ce-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="537ce-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="537ce-132">Requirements</span></span>



| <span data-ttu-id="537ce-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="537ce-133">Requirement</span></span> | <span data-ttu-id="537ce-134">Wert</span><span class="sxs-lookup"><span data-stu-id="537ce-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="537ce-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="537ce-135">Minimum supported client</span></span><br/> | <span data-ttu-id="537ce-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="537ce-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="537ce-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="537ce-137">Minimum supported server</span></span><br/> | <span data-ttu-id="537ce-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="537ce-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="537ce-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="537ce-139">Namespace</span></span><br/>                | <span data-ttu-id="537ce-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="537ce-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="537ce-141">MOF</span><span class="sxs-lookup"><span data-stu-id="537ce-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="537ce-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="537ce-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="537ce-143">DLL</span><span class="sxs-lookup"><span data-stu-id="537ce-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="537ce-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="537ce-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="537ce-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="537ce-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="537ce-146">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="537ce-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

