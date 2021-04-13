---
description: Die CIM- \_ Klasse "fruincludesproduct" zeigt an, dass eine ersetzbare Feld Einheit (FRU) aus anderen Produkten bestehen kann.
ms.assetid: e57dc7f5-4c5b-4ec4-9300-e080053955cb
ms.tgt_platform: multiple
title: CIM_FRUIncludesProduct-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUIncludesProduct
- CIM_FRUIncludesProduct.Component
- CIM_FRUIncludesProduct.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 196f0cc1f2e81312e5e695c34e0a492ac7c05389
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104218999"
---
# <a name="cim_fruincludesproduct-class"></a><span data-ttu-id="15681-103">CIM \_ fruincludesproduct-Klasse</span><span class="sxs-lookup"><span data-stu-id="15681-103">CIM\_FRUIncludesProduct class</span></span>

<span data-ttu-id="15681-104">Die CIM-Klasse " **\_ fruincludesproduct** " zeigt an, dass eine ersetzbare Feld Einheit (FRU) aus anderen Produkten bestehen kann.</span><span class="sxs-lookup"><span data-stu-id="15681-104">The **CIM\_FRUIncludesProduct** class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15681-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="15681-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="15681-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="15681-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="15681-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="15681-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="15681-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="15681-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="15681-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="15681-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{87FEEDCA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUIncludesProduct
{
  CIM_Product REF Component;
  CIM_FRU     REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="15681-110">Member</span><span class="sxs-lookup"><span data-stu-id="15681-110">Members</span></span>

<span data-ttu-id="15681-111">Die **CIM \_ fruincludesproduct** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="15681-111">The **CIM\_FRUIncludesProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="15681-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15681-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15681-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15681-113">Properties</span></span>

<span data-ttu-id="15681-114">Die **CIM \_ fruincludesproduct** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="15681-114">The **CIM\_FRUIncludesProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15681-115">**Komponente**</span><span class="sxs-lookup"><span data-stu-id="15681-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15681-116">Datentyp: **CIM- \_ Produkt**</span><span class="sxs-lookup"><span data-stu-id="15681-116">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="15681-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="15681-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15681-118">Verweis auf das Produkt, das Teil der FRU ist.</span><span class="sxs-lookup"><span data-stu-id="15681-118">Reference to the product that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="15681-119">**FRU**</span><span class="sxs-lookup"><span data-stu-id="15681-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15681-120">Datentyp: **CIM \_ FRU**</span><span class="sxs-lookup"><span data-stu-id="15681-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="15681-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="15681-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15681-122">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="15681-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="15681-123">Verweis auf das FRU-.</span><span class="sxs-lookup"><span data-stu-id="15681-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15681-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15681-124">Remarks</span></span>

<span data-ttu-id="15681-125">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="15681-125">WMI does not implement this class.</span></span>

<span data-ttu-id="15681-126">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="15681-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="15681-127">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="15681-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="15681-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15681-128">Requirements</span></span>



| <span data-ttu-id="15681-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15681-129">Requirement</span></span> | <span data-ttu-id="15681-130">Wert</span><span class="sxs-lookup"><span data-stu-id="15681-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15681-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15681-131">Minimum supported client</span></span><br/> | <span data-ttu-id="15681-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15681-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15681-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15681-133">Minimum supported server</span></span><br/> | <span data-ttu-id="15681-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15681-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15681-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="15681-135">Namespace</span></span><br/>                | <span data-ttu-id="15681-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="15681-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15681-137">MOF</span><span class="sxs-lookup"><span data-stu-id="15681-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15681-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="15681-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15681-139">DLL</span><span class="sxs-lookup"><span data-stu-id="15681-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15681-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15681-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

