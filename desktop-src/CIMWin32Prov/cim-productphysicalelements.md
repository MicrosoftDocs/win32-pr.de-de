---
description: Die CIM \_ productphysicalelements-Klasse stellt die physischen Elemente dar, die ein Produkt bilden.
ms.assetid: cf23098a-f61e-4778-883e-1a5138af3da0
ms.tgt_platform: multiple
title: CIM_ProductPhysicalElements-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductPhysicalElements
- CIM_ProductPhysicalElements.Component
- CIM_ProductPhysicalElements.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a581293426c421de0dd76636a9f446f245f6ab32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126302"
---
# <a name="cim_productphysicalelements-class"></a><span data-ttu-id="25378-103">CIM \_ productphysicalelements-Klasse</span><span class="sxs-lookup"><span data-stu-id="25378-103">CIM\_ProductPhysicalElements class</span></span>

<span data-ttu-id="25378-104">Die **CIM \_ productphysicalelements** -Klasse stellt die physischen Elemente dar, die ein Produkt bilden.</span><span class="sxs-lookup"><span data-stu-id="25378-104">The **CIM\_ProductPhysicalElements** class represents the physical elements that make up a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25378-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="25378-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="25378-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="25378-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="25378-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="25378-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="25378-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="25378-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="25378-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="25378-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{502F00A0-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="25378-110">Member</span><span class="sxs-lookup"><span data-stu-id="25378-110">Members</span></span>

<span data-ttu-id="25378-111">Die **CIM \_ productphysicalelements** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="25378-111">The **CIM\_ProductPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="25378-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25378-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25378-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25378-113">Properties</span></span>

<span data-ttu-id="25378-114">Die **CIM \_ productphysicalelements** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="25378-114">The **CIM\_ProductPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25378-115">**Komponente**</span><span class="sxs-lookup"><span data-stu-id="25378-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25378-116">Datentyp: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="25378-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="25378-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="25378-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25378-118">Verweis auf das physische Element, das Bestandteil des Produkts ist.</span><span class="sxs-lookup"><span data-stu-id="25378-118">Reference to the physical element that is part of the product.</span></span>

</dd> <dt>

<span data-ttu-id="25378-119">**Produkt**</span><span class="sxs-lookup"><span data-stu-id="25378-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25378-120">Datentyp: **CIM- \_ Produkt**</span><span class="sxs-lookup"><span data-stu-id="25378-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="25378-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="25378-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25378-122">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="25378-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="25378-123">Verweis auf das Produkt.</span><span class="sxs-lookup"><span data-stu-id="25378-123">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25378-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25378-124">Remarks</span></span>

<span data-ttu-id="25378-125">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="25378-125">WMI does not implement this class.</span></span>

<span data-ttu-id="25378-126">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="25378-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="25378-127">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="25378-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="25378-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25378-128">Requirements</span></span>



| <span data-ttu-id="25378-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25378-129">Requirement</span></span> | <span data-ttu-id="25378-130">Wert</span><span class="sxs-lookup"><span data-stu-id="25378-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25378-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25378-131">Minimum supported client</span></span><br/> | <span data-ttu-id="25378-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25378-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25378-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25378-133">Minimum supported server</span></span><br/> | <span data-ttu-id="25378-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25378-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25378-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="25378-135">Namespace</span></span><br/>                | <span data-ttu-id="25378-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="25378-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="25378-137">MOF</span><span class="sxs-lookup"><span data-stu-id="25378-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25378-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="25378-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="25378-139">DLL</span><span class="sxs-lookup"><span data-stu-id="25378-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25378-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25378-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

