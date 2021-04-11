---
description: Die CIM \_ -Klasse "Zuweisungs Klasse" stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar und zeigt an, dass die Ressource dem Gerät zugewiesen ist.
ms.assetid: e1702635-32f5-4280-8c02-3940fd858106
ms.tgt_platform: multiple
title: CIM_AllocatedResource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocatedResource
- CIM_AllocatedResource.Dependent
- CIM_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4191315b76553a8c23b94c04d9649cceb131855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127217"
---
# <a name="cim_allocatedresource-class"></a><span data-ttu-id="8cf8b-103">CIM-Klasse "- \_ Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="8cf8b-103">CIM\_AllocatedResource class</span></span>

<span data-ttu-id="8cf8b-104">Die CIM-Klasse " **\_ Zuweisungs** Klasse" stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar und zeigt an, dass die Ressource dem Gerät zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-104">The **CIM\_AllocatedResource** class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8cf8b-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8cf8b-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8cf8b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8cf8b-107">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf8b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cf8b-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C579-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="8cf8b-109">Member</span><span class="sxs-lookup"><span data-stu-id="8cf8b-109">Members</span></span>

<span data-ttu-id="8cf8b-110">Die **CIM \_** -Klasse "-Zuweisung" weist die folgenden Typen von Membern auf:</span><span class="sxs-lookup"><span data-stu-id="8cf8b-110">The **CIM\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="8cf8b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cf8b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8cf8b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cf8b-112">Properties</span></span>

<span data-ttu-id="8cf8b-113">Die **CIM \_** -Klasse "-Zuweisung" weist die folgenden Eigenschaften auf.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-113">The **CIM\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8cf8b-114">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="8cf8b-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf8b-115">Datentyp: **CIM \_ Systemresource**</span><span class="sxs-lookup"><span data-stu-id="8cf8b-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="8cf8b-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cf8b-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cf8b-117">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="8cf8b-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8cf8b-118">Eine [**CIM- \_ System Ressource**](cim-systemresource.md) , die die Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-118">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the resource.</span></span>

</dd> <dt>

<span data-ttu-id="8cf8b-119">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="8cf8b-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cf8b-120">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="8cf8b-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="8cf8b-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cf8b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cf8b-122">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="8cf8b-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8cf8b-123">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät enthält, dem die Ressource zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device to which the resource is assigned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cf8b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cf8b-124">Remarks</span></span>

<span data-ttu-id="8cf8b-125">Die **CIM \_** -Klasse "-Zuweisung" ist von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-125">The **CIM\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="8cf8b-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-126">WMI does not implement this class.</span></span> <span data-ttu-id="8cf8b-127">Weitere Informationen zu Klassen, die von **CIM- \_ Zuweisung** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8cf8b-127">For more information about classes derived from **CIM\_AllocatedResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8cf8b-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8cf8b-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf8b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cf8b-130">Requirements</span></span>



| <span data-ttu-id="8cf8b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cf8b-131">Requirement</span></span> | <span data-ttu-id="8cf8b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="8cf8b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf8b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cf8b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf8b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8cf8b-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8cf8b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cf8b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf8b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cf8b-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8cf8b-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="8cf8b-137">Namespace</span></span><br/>                | <span data-ttu-id="8cf8b-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8cf8b-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8cf8b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8cf8b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8cf8b-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8cf8b-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8cf8b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8cf8b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cf8b-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cf8b-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cf8b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cf8b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf8b-144">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="8cf8b-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

