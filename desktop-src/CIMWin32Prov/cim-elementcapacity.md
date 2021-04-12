---
description: Die CIM \_ elementcapacity-Klasse ordnet ein CIM \_ physicalcapacity-Objekt einem oder mehreren physischen Elementen zu. Es ordnet eine Beschreibung der minimalen und maximalen Hardwareanforderungen (bzw.-Funktionen) den physischen Elementen zu, die beschrieben werden.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: CIM_ElementCapacity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c6ecac913f6d4affcd9784a30d85fa08dfe0486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483374"
---
# <a name="cim_elementcapacity-class"></a><span data-ttu-id="c622b-104">CIM \_ elementcapacity-Klasse</span><span class="sxs-lookup"><span data-stu-id="c622b-104">CIM\_ElementCapacity class</span></span>

<span data-ttu-id="c622b-105">Die **CIM \_ elementcapacity** -Klasse ordnet ein [**CIM \_ physicalcapacity**](cim-physicalcapacity.md) -Objekt einem oder mehreren physischen Elementen zu.</span><span class="sxs-lookup"><span data-stu-id="c622b-105">The **CIM\_ElementCapacity** class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="c622b-106">Es ordnet eine Beschreibung der minimalen und maximalen Hardwareanforderungen (bzw.-Funktionen) den physischen Elementen zu, die beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c622b-106">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c622b-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c622b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c622b-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c622b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c622b-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c622b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c622b-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c622b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c622b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c622b-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a><span data-ttu-id="c622b-112">Member</span><span class="sxs-lookup"><span data-stu-id="c622b-112">Members</span></span>

<span data-ttu-id="c622b-113">Die **CIM \_ elementcapacity** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c622b-113">The **CIM\_ElementCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="c622b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c622b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c622b-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c622b-115">Properties</span></span>

<span data-ttu-id="c622b-116">Die **CIM \_ elementcapacity** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c622b-116">The **CIM\_ElementCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c622b-117">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="c622b-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c622b-118">Datentyp: **CIM \_ physicalcapacity**</span><span class="sxs-lookup"><span data-stu-id="c622b-118">Data type: **CIM\_PhysicalCapacity**</span></span>
</dt> <dt>

<span data-ttu-id="c622b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c622b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c622b-120">Verweis auf die [**CIM \_ physicalcapacity**](cim-physicalcapacity.md) -Klasse, die die minimalen und maximalen Anforderungen sowie die Möglichkeit zur Unterstützung verschiedener Hardwaretypen für ein physisches Element beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c622b-120">Reference to the [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class that describes the minimum and maximum requirements and the ability to support different types of hardware for a physical element.</span></span>

</dd> <dt>

<span data-ttu-id="c622b-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="c622b-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c622b-122">Datentyp: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="c622b-122">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="c622b-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c622b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c622b-124">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="c622b-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="c622b-125">Verweis auf das physische Element, das beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c622b-125">Reference to the physical element being described.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c622b-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c622b-126">Remarks</span></span>

<span data-ttu-id="c622b-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c622b-127">WMI does not implement this class.</span></span>

<span data-ttu-id="c622b-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c622b-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c622b-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c622b-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c622b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c622b-130">Requirements</span></span>



| <span data-ttu-id="c622b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c622b-131">Requirement</span></span> | <span data-ttu-id="c622b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c622b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c622b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c622b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c622b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c622b-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c622b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c622b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c622b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c622b-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c622b-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="c622b-137">Namespace</span></span><br/>                | <span data-ttu-id="c622b-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c622b-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c622b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c622b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c622b-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c622b-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c622b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c622b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c622b-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c622b-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

