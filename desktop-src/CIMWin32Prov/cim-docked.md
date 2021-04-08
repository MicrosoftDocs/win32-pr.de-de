---
description: Die in CIM \_ angedockte Zuordnung stellt die Beziehung zwischen zwei Chassis dar. Beispielsweise kann ein Laptop (ein Typ von Chassis) an einer Docking Station (einem anderen Typ von Chassis) angedockt werden. Diese typische Beziehung wird explizit beschrieben.
ms.assetid: 72cb36bb-f79e-4d1a-a859-4024031e4ebc
ms.tgt_platform: multiple
title: CIM_Docked-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Docked
- CIM_Docked.Dependent
- CIM_Docked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 899b85d63293861f0a36df3d3c30610f8cff05ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748489"
---
# <a name="cim_docked-class"></a><span data-ttu-id="8f95c-105">CIM- \_ angedockte Klasse</span><span class="sxs-lookup"><span data-stu-id="8f95c-105">CIM\_Docked class</span></span>

<span data-ttu-id="8f95c-106">Die in **CIM \_ angedockte** Zuordnung stellt die Beziehung zwischen zwei Chassis dar.</span><span class="sxs-lookup"><span data-stu-id="8f95c-106">The **CIM\_Docked** association represents the relationship between two chassis.</span></span> <span data-ttu-id="8f95c-107">Beispielsweise kann ein Laptop (ein Typ von Chassis) an einer Docking Station (einem anderen Typ von Chassis) angedockt werden.</span><span class="sxs-lookup"><span data-stu-id="8f95c-107">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="8f95c-108">Diese typische Beziehung wird explizit beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8f95c-108">This typical relationship is explicitly described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f95c-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8f95c-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8f95c-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8f95c-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8f95c-111">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8f95c-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f95c-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f95c-112">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|Dynamic States|001.2"), UUID("{FAF76B75-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Docked : CIM_Dependency
{
  CIM_Chassis REF Dependent;
  CIM_Chassis REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="8f95c-113">Member</span><span class="sxs-lookup"><span data-stu-id="8f95c-113">Members</span></span>

<span data-ttu-id="8f95c-114">Die **CIM- \_ angedockte** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8f95c-114">The **CIM\_Docked** class has these types of members:</span></span>

-   [<span data-ttu-id="8f95c-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f95c-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f95c-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f95c-116">Properties</span></span>

<span data-ttu-id="8f95c-117">Die von **CIM \_ angedockte** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8f95c-117">The **CIM\_Docked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f95c-118">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="8f95c-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f95c-119">Datentyp: **CIM- \_ Chassis**</span><span class="sxs-lookup"><span data-stu-id="8f95c-119">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="8f95c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f95c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f95c-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8f95c-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8f95c-122">Ein [**CIM- \_ Chassis**](cim-chassis.md) , das die Docking Station beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8f95c-122">A [**CIM\_Chassis**](cim-chassis.md) describing the docking station.</span></span>

</dd> <dt>

<span data-ttu-id="8f95c-123">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="8f95c-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f95c-124">Datentyp: **CIM- \_ Chassis**</span><span class="sxs-lookup"><span data-stu-id="8f95c-124">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="8f95c-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f95c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f95c-126">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8f95c-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8f95c-127">Ein [**CIM- \_ Chassis**](cim-chassis.md) , das den angedockten Laptop beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8f95c-127">A [**CIM\_Chassis**](cim-chassis.md) describing the docked laptop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f95c-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f95c-128">Remarks</span></span>

<span data-ttu-id="8f95c-129">Die **CIM- \_ angedockte** Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8f95c-129">The **CIM\_Docked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="8f95c-130">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8f95c-130">WMI does not implement this class.</span></span>

<span data-ttu-id="8f95c-131">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8f95c-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8f95c-132">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8f95c-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f95c-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f95c-133">Requirements</span></span>



| <span data-ttu-id="8f95c-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f95c-134">Requirement</span></span> | <span data-ttu-id="8f95c-135">Wert</span><span class="sxs-lookup"><span data-stu-id="8f95c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f95c-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f95c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8f95c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f95c-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f95c-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f95c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8f95c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f95c-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f95c-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f95c-140">Namespace</span></span><br/>                | <span data-ttu-id="8f95c-141">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8f95c-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f95c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8f95c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f95c-143"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8f95c-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f95c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8f95c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f95c-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f95c-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f95c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f95c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f95c-147">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="8f95c-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

