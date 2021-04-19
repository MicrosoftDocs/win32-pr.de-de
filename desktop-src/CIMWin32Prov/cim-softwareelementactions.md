---
description: Die CIM- \_ softwareelementactions-Zuordnung identifiziert die Aktionen für ein Softwareelement.
ms.assetid: 2f8a584c-dff0-48f8-bc5f-2b833b5c0b18
ms.tgt_platform: multiple
title: CIM_SoftwareElementActions-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementActions
- CIM_SoftwareElementActions.Action
- CIM_SoftwareElementActions.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f51cc122cdf354be9611ca1cca4ebcbe1635d14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338894"
---
# <a name="cim_softwareelementactions-class"></a><span data-ttu-id="2a8c4-103">CIM \_ softwareelementactions-Klasse</span><span class="sxs-lookup"><span data-stu-id="2a8c4-103">CIM\_SoftwareElementActions class</span></span>

<span data-ttu-id="2a8c4-104">Die **CIM- \_ softwareelementactions** -Zuordnung identifiziert die Aktionen für ein Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-104">The **CIM\_SoftwareElementActions** association identifies the actions for a software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a8c4-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2a8c4-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2a8c4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2a8c4-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2a8c4-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a8c4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a8c4-109">Syntax</span></span>

``` syntax
[UUID("{4B82D255-E3CD-11d2-8601-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementActions
{
  CIM_Action          REF Action;
  CIM_SoftwareElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="2a8c4-110">Member</span><span class="sxs-lookup"><span data-stu-id="2a8c4-110">Members</span></span>

<span data-ttu-id="2a8c4-111">Die **CIM- \_ softwareelementactions** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2a8c4-111">The **CIM\_SoftwareElementActions** class has these types of members:</span></span>

-   [<span data-ttu-id="2a8c4-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a8c4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a8c4-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a8c4-113">Properties</span></span>

<span data-ttu-id="2a8c4-114">Die **CIM- \_ softwareelementactions** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-114">The **CIM\_SoftwareElementActions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a8c4-115">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="2a8c4-115">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a8c4-116">Datentyp: **CIM- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="2a8c4-116">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="2a8c4-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a8c4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a8c4-118">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2a8c4-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2a8c4-119">Verweis auf eine [**CIM- \_ Aktions**](cim-action.md) Instanz.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-119">Reference to a [**CIM\_Action**](cim-action.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="2a8c4-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a8c4-120">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a8c4-121">Datentyp: **CIM \_ Softwareelement**</span><span class="sxs-lookup"><span data-stu-id="2a8c4-121">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="2a8c4-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a8c4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a8c4-123">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregat**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2a8c4-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2a8c4-124">Verweis auf eine [**CIM- \_ Softwareelement**](cim-softwareelement.md) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-124">Reference to a [**CIM\_SoftwareElement**](cim-softwareelement.md) instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a8c4-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a8c4-125">Remarks</span></span>

<span data-ttu-id="2a8c4-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-126">WMI does not implement this class.</span></span> <span data-ttu-id="2a8c4-127">Informationen zu WMI-Klassen, die von **CIM \_ Softwareelement Actions** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2a8c4-127">For WMI classes derived from **CIM\_SoftwareElementActions**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2a8c4-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2a8c4-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a8c4-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a8c4-130">Requirements</span></span>



| <span data-ttu-id="2a8c4-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a8c4-131">Requirement</span></span> | <span data-ttu-id="2a8c4-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2a8c4-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a8c4-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a8c4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2a8c4-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a8c4-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2a8c4-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a8c4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2a8c4-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a8c4-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2a8c4-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a8c4-137">Namespace</span></span><br/>                | <span data-ttu-id="2a8c4-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2a8c4-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2a8c4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2a8c4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a8c4-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2a8c4-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a8c4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2a8c4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a8c4-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a8c4-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

