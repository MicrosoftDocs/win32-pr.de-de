---
description: Die CIM \_ productparser-Zuordnung definiert eine Hierarchie mit über-und untergeordneten Elementen zwischen Produkten. Beispielsweise kann ein Produkt mit anderen Produkten gebündelt werden.
ms.assetid: 244576fd-8dae-4554-b80b-0cac58c93037
ms.tgt_platform: multiple
title: CIM_ProductParentChild-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductParentChild
- CIM_ProductParentChild.Child
- CIM_ProductParentChild.Parent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a5fd34cc3dffc6d5c8df7f7a76d9cada7856d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523211"
---
# <a name="cim_productparentchild-class"></a><span data-ttu-id="8cb14-104">CIM \_ productparser-Klasse</span><span class="sxs-lookup"><span data-stu-id="8cb14-104">CIM\_ProductParentChild class</span></span>

<span data-ttu-id="8cb14-105">Die **CIM \_ productparser** -Zuordnung definiert eine Hierarchie mit über-und untergeordneten Elementen zwischen Produkten.</span><span class="sxs-lookup"><span data-stu-id="8cb14-105">The **CIM\_ProductParentChild** association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="8cb14-106">Beispielsweise kann ein Produkt mit anderen Produkten gebündelt werden.</span><span class="sxs-lookup"><span data-stu-id="8cb14-106">For example, a product can come bundled with other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8cb14-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8cb14-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8cb14-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8cb14-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8cb14-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8cb14-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8cb14-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8cb14-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cb14-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cb14-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3E24D5A6-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductParentChild
{
  CIM_Product REF Child;
  CIM_Product REF Parent;
};
```

## <a name="members"></a><span data-ttu-id="8cb14-112">Member</span><span class="sxs-lookup"><span data-stu-id="8cb14-112">Members</span></span>

<span data-ttu-id="8cb14-113">Die **CIM \_ productparser** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8cb14-113">The **CIM\_ProductParentChild** class has these types of members:</span></span>

-   [<span data-ttu-id="8cb14-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cb14-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8cb14-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cb14-115">Properties</span></span>

<span data-ttu-id="8cb14-116">Die **CIM \_ productparser** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8cb14-116">The **CIM\_ProductParentChild** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8cb14-117">**Untergeordnet**</span><span class="sxs-lookup"><span data-stu-id="8cb14-117">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cb14-118">Datentyp: **CIM- \_ Produkt**</span><span class="sxs-lookup"><span data-stu-id="8cb14-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="8cb14-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cb14-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cb14-120">Verweis auf das untergeordnete Produkt in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8cb14-120">Reference to the child product in the association.</span></span>

</dd> <dt>

<span data-ttu-id="8cb14-121">**Parent**</span><span class="sxs-lookup"><span data-stu-id="8cb14-121">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cb14-122">Datentyp: **CIM- \_ Produkt**</span><span class="sxs-lookup"><span data-stu-id="8cb14-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="8cb14-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cb14-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cb14-124">Qualifizierer: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8cb14-124">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8cb14-125">Verweis auf das übergeordnete Produkt in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8cb14-125">Reference to the parent product in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cb14-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cb14-126">Remarks</span></span>

<span data-ttu-id="8cb14-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8cb14-127">WMI does not implement this class.</span></span>

<span data-ttu-id="8cb14-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8cb14-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8cb14-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8cb14-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cb14-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cb14-130">Requirements</span></span>



| <span data-ttu-id="8cb14-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cb14-131">Requirement</span></span> | <span data-ttu-id="8cb14-132">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb14-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cb14-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cb14-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8cb14-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8cb14-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8cb14-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cb14-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8cb14-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cb14-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8cb14-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="8cb14-137">Namespace</span></span><br/>                | <span data-ttu-id="8cb14-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8cb14-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8cb14-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8cb14-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8cb14-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8cb14-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8cb14-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8cb14-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cb14-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cb14-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

