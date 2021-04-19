---
description: Die CIM- \_ Klasse stellt die Zuordnung dar, die die Zuordnung zwischen einem logischen Gerät und der physischen Komponente definiert, die das Gerät implementiert.
ms.assetid: 3bddb0c8-dca5-4877-9e30-322516a8d388
ms.tgt_platform: multiple
title: CIM_Realizes-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Realizes
- CIM_Realizes.Dependent
- CIM_Realizes.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b37b2f5f3fe9cfce78e16530df8b94e4333e9a33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343166"
---
# <a name="cim_realizes-class"></a><span data-ttu-id="ac7ba-103">CIM \_ erkennt Klasse</span><span class="sxs-lookup"><span data-stu-id="ac7ba-103">CIM\_Realizes class</span></span>

<span data-ttu-id="ac7ba-104">Die **CIM \_** -Klasse stellt die Zuordnung dar, die die Zuordnung zwischen einem logischen Gerät und der physischen Komponente definiert, die das Gerät implementiert.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-104">The **CIM\_Realizes** class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac7ba-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ac7ba-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ac7ba-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ac7ba-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ac7ba-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac7ba-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac7ba-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B62-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Realizes : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_PhysicalElement REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ac7ba-110">Member</span><span class="sxs-lookup"><span data-stu-id="ac7ba-110">Members</span></span>

<span data-ttu-id="ac7ba-111">Die **CIM \_** -Klasse "wird realisiert" hat folgende Member:</span><span class="sxs-lookup"><span data-stu-id="ac7ba-111">The **CIM\_Realizes** class has these types of members:</span></span>

-   [<span data-ttu-id="ac7ba-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac7ba-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac7ba-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac7ba-113">Properties</span></span>

<span data-ttu-id="ac7ba-114">Die **CIM \_** -Klasse hat diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-114">The **CIM\_Realizes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac7ba-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="ac7ba-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac7ba-116">Datentyp: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="ac7ba-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="ac7ba-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac7ba-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac7ba-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="ac7ba-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ac7ba-119">Ein [**CIM \_ PhysicalElement**](cim-physicalelement.md) , das die physische Komponente beschreibt, die das Gerät implementiert.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-119">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical component that implements the device.</span></span>

</dd> <dt>

<span data-ttu-id="ac7ba-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="ac7ba-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac7ba-121">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="ac7ba-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ac7ba-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac7ba-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac7ba-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="ac7ba-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ac7ba-124">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac7ba-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac7ba-125">Remarks</span></span>

<span data-ttu-id="ac7ba-126">Die **CIM \_** -Klasse "wird realisiert" ist von [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-126">The **CIM\_Realizes** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="ac7ba-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-127">WMI does not implement this class.</span></span>

<span data-ttu-id="ac7ba-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ac7ba-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ac7ba-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac7ba-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac7ba-130">Requirements</span></span>



| <span data-ttu-id="ac7ba-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac7ba-131">Requirement</span></span> | <span data-ttu-id="ac7ba-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ac7ba-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac7ba-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac7ba-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ac7ba-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac7ba-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ac7ba-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac7ba-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ac7ba-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac7ba-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ac7ba-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac7ba-137">Namespace</span></span><br/>                | <span data-ttu-id="ac7ba-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ac7ba-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ac7ba-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ac7ba-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac7ba-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ac7ba-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac7ba-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ac7ba-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac7ba-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac7ba-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac7ba-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac7ba-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac7ba-144">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="ac7ba-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

