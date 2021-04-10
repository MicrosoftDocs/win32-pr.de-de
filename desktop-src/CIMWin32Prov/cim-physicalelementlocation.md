---
description: Die CIM \_ physicalelementlocation-Klasse ordnet ein physisches Element einem CIM- \_ Speicherort Objekt zu Inventur-oder Ersetzungs Zwecken zu.
ms.assetid: d1698c1a-0eda-4e32-9a29-fb741b987671
ms.tgt_platform: multiple
title: CIM_PhysicalElementLocation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElementLocation
- CIM_PhysicalElementLocation.Element
- CIM_PhysicalElementLocation.PhysicalLocation
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e47460a3563d9b7a86aa6ee65704fcb0a422c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127384"
---
# <a name="cim_physicalelementlocation-class"></a><span data-ttu-id="f86a3-103">CIM \_ physicalelementlocation-Klasse</span><span class="sxs-lookup"><span data-stu-id="f86a3-103">CIM\_PhysicalElementLocation class</span></span>

<span data-ttu-id="f86a3-104">Die **CIM \_ physicalelementlocation** -Klasse ordnet ein physisches Element einem [**CIM- \_ Speicherort**](cim-location.md) Objekt zu Inventur-oder Ersetzungs Zwecken zu.</span><span class="sxs-lookup"><span data-stu-id="f86a3-104">The **CIM\_PhysicalElementLocation** class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f86a3-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f86a3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f86a3-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f86a3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f86a3-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f86a3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f86a3-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f86a3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f86a3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f86a3-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B68-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElementLocation
{
  CIM_PhysicalElement REF Element;
  CIM_Location        REF PhysicalLocation;
};
```

## <a name="members"></a><span data-ttu-id="f86a3-110">Member</span><span class="sxs-lookup"><span data-stu-id="f86a3-110">Members</span></span>

<span data-ttu-id="f86a3-111">Die **CIM \_ physicalelementlocation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f86a3-111">The **CIM\_PhysicalElementLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="f86a3-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f86a3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f86a3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f86a3-113">Properties</span></span>

<span data-ttu-id="f86a3-114">Die **CIM \_ physicalelementlocation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f86a3-114">The **CIM\_PhysicalElementLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f86a3-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="f86a3-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f86a3-116">Datentyp: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="f86a3-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="f86a3-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f86a3-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f86a3-118">Verweis auf das physische Element, dessen Speicherort angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f86a3-118">Reference to the physical element whose location is specified.</span></span>

</dd> <dt>

<span data-ttu-id="f86a3-119">**PhysicalLocation**</span><span class="sxs-lookup"><span data-stu-id="f86a3-119">**PhysicalLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f86a3-120">Datentyp: **CIM- \_ Speicherort**</span><span class="sxs-lookup"><span data-stu-id="f86a3-120">Data type: **CIM\_Location**</span></span>
</dt> <dt>

<span data-ttu-id="f86a3-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f86a3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f86a3-122">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f86a3-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f86a3-123">Verweis auf den Speicherort des physischen Elements.</span><span class="sxs-lookup"><span data-stu-id="f86a3-123">Reference to the physical element's location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f86a3-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f86a3-124">Remarks</span></span>

<span data-ttu-id="f86a3-125">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f86a3-125">WMI does not implement this class.</span></span>

<span data-ttu-id="f86a3-126">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f86a3-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f86a3-127">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f86a3-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f86a3-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f86a3-128">Requirements</span></span>



| <span data-ttu-id="f86a3-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f86a3-129">Requirement</span></span> | <span data-ttu-id="f86a3-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f86a3-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f86a3-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f86a3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f86a3-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f86a3-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f86a3-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f86a3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f86a3-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f86a3-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f86a3-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="f86a3-135">Namespace</span></span><br/>                | <span data-ttu-id="f86a3-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f86a3-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f86a3-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f86a3-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f86a3-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f86a3-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f86a3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f86a3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f86a3-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f86a3-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

