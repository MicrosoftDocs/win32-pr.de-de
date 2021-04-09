---
description: Die CIM- \_ Klasse "fruphysicalelements" stellt die physischen Elemente dar, die eine ersetzbare (Feld) Einheit (FRU) bilden.
ms.assetid: ecdb19a8-5169-4370-8d2d-a21a0021ea5b
ms.tgt_platform: multiple
title: CIM_FRUPhysicalElements-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUPhysicalElements
- CIM_FRUPhysicalElements.Component
- CIM_FRUPhysicalElements.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c47160b9053a323f693d76f5b84d922c5120992
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958404"
---
# <a name="cim_fruphysicalelements-class"></a><span data-ttu-id="adbb3-103">CIM \_ fruphysicalelements-Klasse</span><span class="sxs-lookup"><span data-stu-id="adbb3-103">CIM\_FRUPhysicalElements class</span></span>

<span data-ttu-id="adbb3-104">Die CIM-Klasse " **\_ fruphysicalelements** " stellt die physischen Elemente dar, die eine ersetzbare (Feld) Einheit (FRU) bilden.</span><span class="sxs-lookup"><span data-stu-id="adbb3-104">The **CIM\_FRUPhysicalElements** class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="adbb3-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="adbb3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="adbb3-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="adbb3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="adbb3-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="adbb3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="adbb3-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="adbb3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="adbb3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="adbb3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{977E36CA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_FRU             REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="adbb3-110">Member</span><span class="sxs-lookup"><span data-stu-id="adbb3-110">Members</span></span>

<span data-ttu-id="adbb3-111">Die CIM-Klasse " **\_ fruphysicalelements** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="adbb3-111">The **CIM\_FRUPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="adbb3-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="adbb3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="adbb3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="adbb3-113">Properties</span></span>

<span data-ttu-id="adbb3-114">Die CIM-Klasse " **\_ fruphysicalelements** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="adbb3-114">The **CIM\_FRUPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="adbb3-115">**Komponente**</span><span class="sxs-lookup"><span data-stu-id="adbb3-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbb3-116">Datentyp: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="adbb3-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="adbb3-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adbb3-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adbb3-118">Verweis auf ein physisches Element, das Teil der FRU ist.</span><span class="sxs-lookup"><span data-stu-id="adbb3-118">Reference to a physical element that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="adbb3-119">**FRU**</span><span class="sxs-lookup"><span data-stu-id="adbb3-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbb3-120">Datentyp: **CIM \_ FRU**</span><span class="sxs-lookup"><span data-stu-id="adbb3-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="adbb3-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adbb3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adbb3-122">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="adbb3-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="adbb3-123">Verweis auf das FRU-.</span><span class="sxs-lookup"><span data-stu-id="adbb3-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adbb3-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="adbb3-124">Remarks</span></span>

<span data-ttu-id="adbb3-125">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="adbb3-125">WMI does not implement this class.</span></span>

<span data-ttu-id="adbb3-126">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="adbb3-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="adbb3-127">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="adbb3-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="adbb3-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adbb3-128">Requirements</span></span>



| <span data-ttu-id="adbb3-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adbb3-129">Requirement</span></span> | <span data-ttu-id="adbb3-130">Wert</span><span class="sxs-lookup"><span data-stu-id="adbb3-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adbb3-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="adbb3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="adbb3-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="adbb3-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="adbb3-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="adbb3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="adbb3-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adbb3-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="adbb3-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="adbb3-135">Namespace</span></span><br/>                | <span data-ttu-id="adbb3-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="adbb3-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="adbb3-137">MOF</span><span class="sxs-lookup"><span data-stu-id="adbb3-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adbb3-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="adbb3-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="adbb3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="adbb3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adbb3-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adbb3-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

