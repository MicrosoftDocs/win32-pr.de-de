---
description: Die CIM \_ mediapresent-Zuordnung beschreibt eine Beziehung, bei der über ein Medien Zugriffsgerät auf einen Speicherblock zugegriffen werden muss.
ms.assetid: 84c4931c-1dc6-4fc1-b3b9-8252ecb627f5
ms.tgt_platform: multiple
title: CIM_MediaPresent-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d033871a77a0433292c4a2ca1fae185df6aa5015
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869540"
---
# <a name="cim_mediapresent-class-cimwin32-wmi-providers"></a><span data-ttu-id="e09f4-103">CIM_MediaPresent-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="e09f4-103">CIM_MediaPresent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e09f4-104">Die **CIM \_ mediapresent** -Zuordnung beschreibt eine Beziehung, bei der über ein Medien Zugriffsgerät auf einen Speicherblock zugegriffen werden muss.</span><span class="sxs-lookup"><span data-stu-id="e09f4-104">The **CIM\_MediaPresent** association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e09f4-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e09f4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e09f4-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e09f4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e09f4-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e09f4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e09f4-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e09f4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e09f4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e09f4-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C540-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_StorageExtent     REF Dependent;
  CIM_MediaAccessDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e09f4-110">Member</span><span class="sxs-lookup"><span data-stu-id="e09f4-110">Members</span></span>

<span data-ttu-id="e09f4-111">Die **CIM \_ mediapresent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e09f4-111">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="e09f4-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e09f4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e09f4-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e09f4-113">Properties</span></span>

<span data-ttu-id="e09f4-114">Die **CIM \_ mediapresent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e09f4-114">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e09f4-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="e09f4-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e09f4-116">Datentyp: **CIM \_ mediaaccessdevice**</span><span class="sxs-lookup"><span data-stu-id="e09f4-116">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e09f4-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e09f4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e09f4-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="e09f4-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e09f4-119">Ein [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md) , das das Medien Zugriffsgerät beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e09f4-119">A [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) that describes the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="e09f4-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="e09f4-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e09f4-121">Datentyp: **CIM \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="e09f4-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="e09f4-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e09f4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e09f4-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="e09f4-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e09f4-124">Ein [**CIM- \_ storageblock**](cim-storageextent.md) , der den Speicherblock beschreibt, auf den über das Medien Zugriffsgerät zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="e09f4-124">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent accessed using the media access device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e09f4-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e09f4-125">Remarks</span></span>

<span data-ttu-id="e09f4-126">Die **CIM \_ mediapresent** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e09f4-126">The **CIM\_MediaPresent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="e09f4-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="e09f4-127">WMI does not implement this class.</span></span> <span data-ttu-id="e09f4-128">Informationen zu von **CIM \_ mediapresent** abgeleiteten Klassen finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e09f4-128">For classes derived from **CIM\_MediaPresent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e09f4-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e09f4-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e09f4-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e09f4-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e09f4-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e09f4-131">Requirements</span></span>



| <span data-ttu-id="e09f4-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e09f4-132">Requirement</span></span> | <span data-ttu-id="e09f4-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e09f4-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e09f4-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e09f4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e09f4-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e09f4-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e09f4-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e09f4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e09f4-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e09f4-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e09f4-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="e09f4-138">Namespace</span></span><br/>                | <span data-ttu-id="e09f4-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e09f4-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e09f4-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e09f4-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e09f4-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e09f4-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e09f4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e09f4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e09f4-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e09f4-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e09f4-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e09f4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e09f4-145">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="e09f4-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

