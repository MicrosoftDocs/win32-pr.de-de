---
description: Die CIM \_ storagemängel-Aggregation sammelt die Speicherfehler für einen Speicherblock.
ms.assetid: 7acd3d25-4691-43cb-badc-662684989345
ms.tgt_platform: multiple
title: CIM_StorageDefect-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageDefect
- CIM_StorageDefect.Error
- CIM_StorageDefect.Extent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e6c2be45fe2f44afa407dc72e3ae90c486593ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958560"
---
# <a name="cim_storagedefect-class"></a><span data-ttu-id="d4bb5-103">CIM \_ storagemängel-Klasse</span><span class="sxs-lookup"><span data-stu-id="d4bb5-103">CIM\_StorageDefect class</span></span>

<span data-ttu-id="d4bb5-104">Die **CIM \_ storagemängel** -Aggregation sammelt die Speicherfehler für einen Speicherblock.</span><span class="sxs-lookup"><span data-stu-id="d4bb5-104">The **CIM\_StorageDefect** aggregation collects the storage errors for a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4bb5-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4bb5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d4bb5-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d4bb5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d4bb5-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4bb5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d4bb5-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d4bb5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4bb5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4bb5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{5CC70817-DB31-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_StorageDefect
{
  CIM_StorageError  REF Error;
  CIM_StorageExtent REF Extent;
};
```

## <a name="members"></a><span data-ttu-id="d4bb5-110">Member</span><span class="sxs-lookup"><span data-stu-id="d4bb5-110">Members</span></span>

<span data-ttu-id="d4bb5-111">Die **CIM \_ storagemängel** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d4bb5-111">The **CIM\_StorageDefect** class has these types of members:</span></span>

-   [<span data-ttu-id="d4bb5-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4bb5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d4bb5-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4bb5-113">Properties</span></span>

<span data-ttu-id="d4bb5-114">Die **CIM \_ storagemängel** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4bb5-114">The **CIM\_StorageDefect** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4bb5-115">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="d4bb5-115">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4bb5-116">Datentyp: **CIM \_ storageerror**</span><span class="sxs-lookup"><span data-stu-id="d4bb5-116">Data type: **CIM\_StorageError**</span></span>
</dt> <dt>

<span data-ttu-id="d4bb5-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4bb5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4bb5-118">Qualifizierer: [ **schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d4bb5-118">Qualifiers: [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d4bb5-119">Verweis auf das Error-Objekt, das die Anfangs-und Endadressen definiert, die aus dem Speicherblock zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d4bb5-119">Reference to the error object, which defines the starting and ending addresses that are mapped out of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="d4bb5-120">**Extent**</span><span class="sxs-lookup"><span data-stu-id="d4bb5-120">**Extent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4bb5-121">Datentyp: **CIM \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="d4bb5-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="d4bb5-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4bb5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4bb5-123">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="d4bb5-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d4bb5-124">Verweis auf den Speicherblock, in dem die Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="d4bb5-124">Reference to the storage extent on which the errors occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4bb5-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4bb5-125">Remarks</span></span>

<span data-ttu-id="d4bb5-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d4bb5-126">WMI does not implement this class.</span></span>

<span data-ttu-id="d4bb5-127">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d4bb5-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d4bb5-128">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d4bb5-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4bb5-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4bb5-129">Requirements</span></span>



| <span data-ttu-id="d4bb5-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4bb5-130">Requirement</span></span> | <span data-ttu-id="d4bb5-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d4bb5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bb5-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4bb5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d4bb5-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4bb5-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4bb5-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4bb5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d4bb5-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4bb5-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4bb5-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4bb5-136">Namespace</span></span><br/>                | <span data-ttu-id="d4bb5-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d4bb5-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d4bb5-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d4bb5-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4bb5-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d4bb5-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4bb5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d4bb5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4bb5-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4bb5-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

