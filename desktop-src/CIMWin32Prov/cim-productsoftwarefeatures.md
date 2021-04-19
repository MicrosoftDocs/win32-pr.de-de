---
description: Die CIM \_ productsoftwarefeatures-Zuordnung identifiziert die Software Features für ein bestimmtes Produkt.
ms.assetid: cd6190f8-d86e-44c8-b506-48016a7c22e1
ms.tgt_platform: multiple
title: CIM_ProductSoftwareFeatures-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSoftwareFeatures
- CIM_ProductSoftwareFeatures.Component
- CIM_ProductSoftwareFeatures.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d891d9465688d92c016217cecd8324588026535
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346215"
---
# <a name="cim_productsoftwarefeatures-class"></a><span data-ttu-id="0e2c2-103">CIM \_ productsoftwarefeatures-Klasse</span><span class="sxs-lookup"><span data-stu-id="0e2c2-103">CIM\_ProductSoftwareFeatures class</span></span>

<span data-ttu-id="0e2c2-104">Die **CIM \_ productsoftwarefeatures** -Zuordnung identifiziert die Software Features für ein bestimmtes Produkt.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-104">The **CIM\_ProductSoftwareFeatures** association identifies the software features for a particular product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e2c2-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0e2c2-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0e2c2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0e2c2-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0e2c2-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e2c2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e2c2-109">Syntax</span></span>

``` syntax
[UUID("{7C39D12A-DB2B-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_ProductSoftwareFeatures
{
  CIM_SoftwareFeature REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="0e2c2-110">Member</span><span class="sxs-lookup"><span data-stu-id="0e2c2-110">Members</span></span>

<span data-ttu-id="0e2c2-111">Die **CIM \_ productsoftwarefeatures** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0e2c2-111">The **CIM\_ProductSoftwareFeatures** class has these types of members:</span></span>

-   [<span data-ttu-id="0e2c2-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0e2c2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e2c2-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0e2c2-113">Properties</span></span>

<span data-ttu-id="0e2c2-114">Die **CIM \_ productsoftwarefeatures** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-114">The **CIM\_ProductSoftwareFeatures** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e2c2-115">**Komponente**</span><span class="sxs-lookup"><span data-stu-id="0e2c2-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2c2-116">Datentyp: **CIM \_ Softwarefeature**</span><span class="sxs-lookup"><span data-stu-id="0e2c2-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="0e2c2-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0e2c2-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e2c2-118">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0e2c2-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0e2c2-119">Verweis auf die Komponente.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-119">Reference to the component.</span></span>

</dd> <dt>

<span data-ttu-id="0e2c2-120">**Produkt**</span><span class="sxs-lookup"><span data-stu-id="0e2c2-120">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e2c2-121">Datentyp: **CIM- \_ Produkt**</span><span class="sxs-lookup"><span data-stu-id="0e2c2-121">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="0e2c2-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0e2c2-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e2c2-123">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0e2c2-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0e2c2-124">Verweis auf das Produkt.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-124">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e2c2-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e2c2-125">Remarks</span></span>

<span data-ttu-id="0e2c2-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-126">WMI does not implement this class.</span></span> <span data-ttu-id="0e2c2-127">Informationen zu WMI-Klassen, die von **CIM \_ productsoftwarefeatures** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0e2c2-127">For WMI classes derived from **CIM\_ProductSoftwareFeatures**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0e2c2-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0e2c2-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e2c2-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e2c2-130">Requirements</span></span>



| <span data-ttu-id="0e2c2-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e2c2-131">Requirement</span></span> | <span data-ttu-id="0e2c2-132">Wert</span><span class="sxs-lookup"><span data-stu-id="0e2c2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e2c2-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e2c2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0e2c2-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e2c2-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e2c2-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e2c2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0e2c2-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e2c2-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e2c2-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e2c2-137">Namespace</span></span><br/>                | <span data-ttu-id="0e2c2-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0e2c2-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e2c2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="0e2c2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e2c2-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0e2c2-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e2c2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0e2c2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e2c2-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e2c2-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

