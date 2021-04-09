---
description: Die CIM \_ collectedcollections-Klasse ist eine Aggregations Zuordnung, die eine Auflistung verwalteter System Elemente (MSE) darstellt, die in einer Auflistung von MSES enthalten sind.
ms.assetid: 7baaf429-1211-4545-ace2-c6312d53c0f6
ms.tgt_platform: multiple
title: CIM_CollectedCollections-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedCollections
- CIM_CollectedCollections.Collection
- CIM_CollectedCollections.CollectionInCollection
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e592c7799efc8c280d4cd64c2b54ed8a3ea328f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958453"
---
# <a name="cim_collectedcollections-class"></a><span data-ttu-id="6498a-103">CIM \_ collectedcollections-Klasse</span><span class="sxs-lookup"><span data-stu-id="6498a-103">CIM\_CollectedCollections class</span></span>

<span data-ttu-id="6498a-104">Die **CIM \_ collectedcollections** -Klasse ist eine Aggregations Zuordnung, die eine Auflistung verwalteter System Elemente (MSE) darstellt, die in einer Auflistung von MSES enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6498a-104">The **CIM\_CollectedCollections** class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6498a-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6498a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6498a-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6498a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6498a-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="6498a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6498a-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6498a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6498a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6498a-109">Syntax</span></span>

``` syntax
class CIM_CollectedCollections
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_CollectionOfMSEs REF CollectionInCollection;
};
```

## <a name="members"></a><span data-ttu-id="6498a-110">Member</span><span class="sxs-lookup"><span data-stu-id="6498a-110">Members</span></span>

<span data-ttu-id="6498a-111">Die **CIM \_ collectedcollections** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6498a-111">The **CIM\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="6498a-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6498a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6498a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6498a-113">Properties</span></span>

<span data-ttu-id="6498a-114">Die **CIM \_ collectedcollections** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6498a-114">The **CIM\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6498a-115">**Sammlung**</span><span class="sxs-lookup"><span data-stu-id="6498a-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6498a-116">Datentyp: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="6498a-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="6498a-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6498a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6498a-118">Verweis auf die "höhere Ebene" oder das übergeordnete Element in der Aggregation.</span><span class="sxs-lookup"><span data-stu-id="6498a-118">Reference to the "higher level" or parent element in the aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="6498a-119">**Collectionincollection**</span><span class="sxs-lookup"><span data-stu-id="6498a-119">**CollectionInCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6498a-120">Datentyp: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="6498a-120">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="6498a-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6498a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6498a-122">Verweis auf die **Sammlung**"gesammelt".</span><span class="sxs-lookup"><span data-stu-id="6498a-122">Reference to the "collected" **Collection**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6498a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6498a-123">Remarks</span></span>

<span data-ttu-id="6498a-124">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6498a-124">WMI does not implement this class.</span></span>

<span data-ttu-id="6498a-125">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6498a-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6498a-126">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6498a-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6498a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6498a-127">Requirements</span></span>



| <span data-ttu-id="6498a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6498a-128">Requirement</span></span> | <span data-ttu-id="6498a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="6498a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6498a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6498a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6498a-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6498a-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6498a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6498a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6498a-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6498a-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6498a-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="6498a-134">Namespace</span></span><br/>                | <span data-ttu-id="6498a-135">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6498a-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6498a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6498a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6498a-137"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6498a-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6498a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6498a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6498a-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6498a-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




