---
description: Die CIM \_ computersystempackage-Klasse stellt eine Zuordnung dar, die explizit die Beziehung zwischen einheitlichen Computersystemen und einem oder mehreren physischen Paketen definiert.
ms.assetid: a91bf09d-0768-4d2a-a0e5-16237b2e6ddc
ms.tgt_platform: multiple
title: CIM_ComputerSystemPackage-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemPackage
- CIM_ComputerSystemPackage.Dependent
- CIM_ComputerSystemPackage.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a2f166c4494b6120bfc5e2aaedeaba4721b155
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958449"
---
# <a name="cim_computersystempackage-class"></a><span data-ttu-id="a8026-103">CIM \_ computersystempackage-Klasse</span><span class="sxs-lookup"><span data-stu-id="a8026-103">CIM\_ComputerSystemPackage class</span></span>

<span data-ttu-id="a8026-104">Die **CIM \_ computersystempackage** -Klasse stellt eine Zuordnung dar, die explizit die Beziehung zwischen einheitlichen Computersystemen und einem oder mehreren physischen Paketen definiert.</span><span class="sxs-lookup"><span data-stu-id="a8026-104">The **CIM\_ComputerSystemPackage** class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="a8026-105">Die Zuordnung ähnelt der Art und Weise, in der logische Geräte durch physische Elemente realisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a8026-105">The association is similar to the way that logical devices are realized by physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8026-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a8026-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a8026-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a8026-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a8026-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a8026-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a8026-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a8026-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8026-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8026-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystemPackage : CIM_Dependency
{
  CIM_UnitaryComputerSystem REF Dependent;
  CIM_PhysicalPackage       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="a8026-111">Member</span><span class="sxs-lookup"><span data-stu-id="a8026-111">Members</span></span>

<span data-ttu-id="a8026-112">Die **CIM \_ computersystempackage** -Klasse verfügt über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a8026-112">The **CIM\_ComputerSystemPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="a8026-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8026-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8026-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8026-114">Properties</span></span>

<span data-ttu-id="a8026-115">Die **CIM \_ computersystempackage** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a8026-115">The **CIM\_ComputerSystemPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8026-116">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="a8026-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8026-117">Datentyp: **CIM \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="a8026-117">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="a8026-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a8026-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8026-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="a8026-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a8026-120">Ein [**CIM- \_ physicalpackage**](cim-physicalpackage.md) , das die physischen Pakete beschreibt, die ein einheitliches Computersystem realisieren.</span><span class="sxs-lookup"><span data-stu-id="a8026-120">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package(s) that realize a unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="a8026-121">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="a8026-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8026-122">Datentyp: **CIM \_ unitarycomputersystem**</span><span class="sxs-lookup"><span data-stu-id="a8026-122">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a8026-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a8026-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8026-124">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="a8026-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a8026-125">Ein [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md) , das das einheitliche Computersystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a8026-125">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8026-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8026-126">Remarks</span></span>

<span data-ttu-id="a8026-127">Die **CIM \_ computersystempackage** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a8026-127">The **CIM\_ComputerSystemPackage** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="a8026-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a8026-128">WMI does not implement this class.</span></span>

<span data-ttu-id="a8026-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a8026-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a8026-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a8026-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8026-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8026-131">Requirements</span></span>



| <span data-ttu-id="a8026-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8026-132">Requirement</span></span> | <span data-ttu-id="a8026-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a8026-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8026-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8026-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a8026-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8026-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8026-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8026-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a8026-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8026-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8026-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8026-138">Namespace</span></span><br/>                | <span data-ttu-id="a8026-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a8026-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a8026-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a8026-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8026-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a8026-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8026-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a8026-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8026-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8026-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8026-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8026-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8026-145">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="a8026-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

