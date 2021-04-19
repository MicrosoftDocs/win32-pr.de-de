---
description: Die CIM \_ elementslinked Association stellt physische Elemente dar, die von einem physischen Link miteinander verkabelt werden.
ms.assetid: b9e1d11e-6f89-4d7a-9b5c-01161e7c1bdf
ms.tgt_platform: multiple
title: CIM_ElementsLinked-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementsLinked
- CIM_ElementsLinked.Dependent
- CIM_ElementsLinked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353809056d1ca3bae710272b02c2636a3f02eef1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346235"
---
# <a name="cim_elementslinked-class"></a><span data-ttu-id="d669a-103">CIM \_ elementslinked-Klasse</span><span class="sxs-lookup"><span data-stu-id="d669a-103">CIM\_ElementsLinked class</span></span>

<span data-ttu-id="d669a-104">Die **CIM \_ elementslinked** Association stellt physische Elemente dar, die von einem physischen Link miteinander verkabelt werden.</span><span class="sxs-lookup"><span data-stu-id="d669a-104">The **CIM\_ElementsLinked** association represents physical elements that are cabled together by a physical link.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d669a-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d669a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d669a-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d669a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d669a-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d669a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d669a-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d669a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d669a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d669a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B83-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementsLinked : CIM_Dependency
{
  CIM_PhysicalElement REF Dependent;
  CIM_PhysicalLink    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d669a-110">Member</span><span class="sxs-lookup"><span data-stu-id="d669a-110">Members</span></span>

<span data-ttu-id="d669a-111">Die **CIM \_ elementslinked** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d669a-111">The **CIM\_ElementsLinked** class has these types of members:</span></span>

-   [<span data-ttu-id="d669a-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d669a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d669a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d669a-113">Properties</span></span>

<span data-ttu-id="d669a-114">Die **CIM \_ elementslinked** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d669a-114">The **CIM\_ElementsLinked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d669a-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="d669a-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669a-116">Datentyp: **CIM \_ physicallink**</span><span class="sxs-lookup"><span data-stu-id="d669a-116">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="d669a-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d669a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d669a-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="d669a-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d669a-119">Ein [**CIM- \_ physicallink**](cim-physicallink.md) , der den physischen Link beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d669a-119">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link.</span></span>

</dd> <dt>

<span data-ttu-id="d669a-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="d669a-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669a-121">Datentyp: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="d669a-121">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="d669a-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d669a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d669a-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="d669a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d669a-124">Ein [**CIM \_ PhysicalElement**](cim-physicalelement.md) , das das physische Element beschreibt, das verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="d669a-124">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element that is linked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d669a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d669a-125">Remarks</span></span>

<span data-ttu-id="d669a-126">Die **CIM- \_ elementslinked** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d669a-126">The **CIM\_ElementsLinked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="d669a-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d669a-127">WMI does not implement this class.</span></span>

<span data-ttu-id="d669a-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d669a-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d669a-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d669a-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d669a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d669a-130">Requirements</span></span>



| <span data-ttu-id="d669a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d669a-131">Requirement</span></span> | <span data-ttu-id="d669a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="d669a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d669a-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d669a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d669a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d669a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d669a-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d669a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d669a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d669a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d669a-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="d669a-137">Namespace</span></span><br/>                | <span data-ttu-id="d669a-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d669a-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d669a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d669a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d669a-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d669a-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d669a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d669a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d669a-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d669a-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d669a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d669a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d669a-144">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="d669a-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

