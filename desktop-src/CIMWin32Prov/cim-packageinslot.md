---
description: Die CIM \_ packageinslot-Zuordnung stellt die Beziehung zwischen den Geräte Karten und dem Gehäuse dar, in dem Sie eingebunden werden.
ms.assetid: 439f28a8-24fd-4a53-9d42-48fabb58e84a
ms.tgt_platform: multiple
title: CIM_PackageInSlot-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInSlot
- CIM_PackageInSlot.Dependent
- CIM_PackageInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a17e133f16f838d6353b6d74ee2054bd5ec52cd0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126140"
---
# <a name="cim_packageinslot-class"></a><span data-ttu-id="ed114-103">CIM \_ packageinslot-Klasse</span><span class="sxs-lookup"><span data-stu-id="ed114-103">CIM\_PackageInSlot class</span></span>

<span data-ttu-id="ed114-104">Die **CIM \_ packageinslot** -Zuordnung stellt die Beziehung zwischen den Geräte Karten und dem Gehäuse dar, in dem Sie eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="ed114-104">The **CIM\_PackageInSlot** association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed114-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ed114-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ed114-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ed114-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ed114-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ed114-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ed114-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ed114-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed114-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed114-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B89-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInSlot : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_Slot            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ed114-110">Member</span><span class="sxs-lookup"><span data-stu-id="ed114-110">Members</span></span>

<span data-ttu-id="ed114-111">Die **CIM \_ packageinslot** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ed114-111">The **CIM\_PackageInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="ed114-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed114-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed114-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed114-113">Properties</span></span>

<span data-ttu-id="ed114-114">Die **CIM \_ packageinslot** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ed114-114">The **CIM\_PackageInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed114-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="ed114-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed114-116">Datentyp: **CIM- \_ Slot**</span><span class="sxs-lookup"><span data-stu-id="ed114-116">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="ed114-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed114-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed114-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="ed114-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ed114-119">Ein [**CIM- \_ Slot**](cim-slot.md) , der den Slot beschreibt, in den das physische Paket eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ed114-119">A [**CIM\_Slot**](cim-slot.md) describing the slot into which the physical package is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="ed114-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="ed114-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed114-121">Datentyp: **CIM \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="ed114-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="ed114-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed114-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed114-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="ed114-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ed114-124">Ein [**CIM- \_ physicalpackage**](cim-physicalpackage.md) , das das Paket im Slot beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ed114-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the package in the slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed114-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed114-125">Remarks</span></span>

<span data-ttu-id="ed114-126">**CIM \_ Packageinslot** ist von [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ed114-126">**CIM\_PackageInSlot** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="ed114-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ed114-127">WMI does not implement this class.</span></span>

<span data-ttu-id="ed114-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ed114-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ed114-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ed114-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed114-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed114-130">Requirements</span></span>



| <span data-ttu-id="ed114-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed114-131">Requirement</span></span> | <span data-ttu-id="ed114-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ed114-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed114-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed114-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ed114-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed114-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ed114-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed114-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ed114-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed114-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ed114-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed114-137">Namespace</span></span><br/>                | <span data-ttu-id="ed114-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ed114-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ed114-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ed114-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed114-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ed114-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed114-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ed114-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed114-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed114-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed114-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed114-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed114-144">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="ed114-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

