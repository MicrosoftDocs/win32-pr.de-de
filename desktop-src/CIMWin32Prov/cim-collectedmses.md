---
description: Die CIM \_ collectedmses Association-Klasse stellt die Member des Gruppierungs Objekts dar, eine CollectionOfMSEs-Klasse.
ms.assetid: 3dca2094-57f1-447e-809c-f924f88a185a
ms.tgt_platform: multiple
title: CIM_CollectedMSEs-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 154436934e8a8fe417215874ddb98e449b854025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483542"
---
# <a name="cim_collectedmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="3e118-103">CIM_CollectedMSEs-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="3e118-103">CIM_CollectedMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3e118-104">Die **CIM \_ collectedmses** Association-Klasse stellt die Member des Gruppierungs Objekts dar, eine [**CollectionOfMSEs**](cim-collectionofmses.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="3e118-104">The **CIM\_CollectedMSEs** association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e118-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3e118-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3e118-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3e118-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3e118-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="3e118-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3e118-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3e118-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e118-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e118-109">Syntax</span></span>

``` syntax
class CIM_CollectedMSEs
{
  CM_CollectionOfMSEs      REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="3e118-110">Member</span><span class="sxs-lookup"><span data-stu-id="3e118-110">Members</span></span>

<span data-ttu-id="3e118-111">Die **CIM \_ collectedmses** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3e118-111">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="3e118-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e118-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e118-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e118-113">Properties</span></span>

<span data-ttu-id="3e118-114">Die **CIM \_ collectedmses** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3e118-114">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e118-115">**Sammlung**</span><span class="sxs-lookup"><span data-stu-id="3e118-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e118-116">Datentyp: **cm \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="3e118-116">Data type: **CM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="3e118-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3e118-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e118-118">Verweis auf das Gruppierungs-oder "Bag"-Objekt, das die Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="3e118-118">Reference to the grouping or "bag" object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="3e118-119">**Member**</span><span class="sxs-lookup"><span data-stu-id="3e118-119">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e118-120">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="3e118-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="3e118-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3e118-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e118-122">Verweis auf einen Member der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3e118-122">Reference to a member of the collection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e118-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e118-123">Remarks</span></span>

<span data-ttu-id="3e118-124">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3e118-124">WMI does not implement this class.</span></span> <span data-ttu-id="3e118-125">Weitere Informationen zu WMI-Klassen, die von **CIM \_ collectedmses** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3e118-125">For more information about WMI classes derived from **CIM\_CollectedMSEs**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3e118-126">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3e118-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3e118-127">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3e118-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e118-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e118-128">Requirements</span></span>



| <span data-ttu-id="3e118-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e118-129">Requirement</span></span> | <span data-ttu-id="3e118-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3e118-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e118-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e118-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3e118-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e118-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e118-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e118-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3e118-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e118-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e118-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e118-135">Namespace</span></span><br/>                | <span data-ttu-id="3e118-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3e118-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e118-137">MOF</span><span class="sxs-lookup"><span data-stu-id="3e118-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e118-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3e118-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e118-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3e118-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e118-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e118-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




