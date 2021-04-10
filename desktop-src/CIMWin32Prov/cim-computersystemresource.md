---
description: Die CIM \_ computersystemresource-Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren Systemressourcen dar.
ms.assetid: 365a3cc2-89f9-4fbd-aa70-a89608fc3c1f
ms.tgt_platform: multiple
title: CIM_ComputerSystemResource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemResource
- CIM_ComputerSystemResource.PartComponent
- CIM_ComputerSystemResource.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 170e92b6c31ce038f1bccc4003248b8ae86d5f79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041463"
---
# <a name="cim_computersystemresource-class"></a><span data-ttu-id="69c53-103">CIM \_ computersystemresource-Klasse</span><span class="sxs-lookup"><span data-stu-id="69c53-103">CIM\_ComputerSystemResource class</span></span>

<span data-ttu-id="69c53-104">Die **CIM \_ computersystemresource** -Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren Systemressourcen dar.</span><span class="sxs-lookup"><span data-stu-id="69c53-104">The **CIM\_ComputerSystemResource** class represents an association between a computer system and its available system resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69c53-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="69c53-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="69c53-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="69c53-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="69c53-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="69c53-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="69c53-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="69c53-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="69c53-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="69c53-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340A-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemResource : CIM_SystemComponent
{
  CIM_SystemResource REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="69c53-110">Member</span><span class="sxs-lookup"><span data-stu-id="69c53-110">Members</span></span>

<span data-ttu-id="69c53-111">Die **CIM \_ computersystemresource** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="69c53-111">The **CIM\_ComputerSystemResource** class has these types of members:</span></span>

-   [<span data-ttu-id="69c53-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69c53-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69c53-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69c53-113">Properties</span></span>

<span data-ttu-id="69c53-114">Die **CIM \_ computersystemresource** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="69c53-114">The **CIM\_ComputerSystemResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="69c53-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="69c53-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69c53-116">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="69c53-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="69c53-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69c53-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69c53-118">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="69c53-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="69c53-119">Ein [**CIM- \_ Computersystem**](cim-computersystem.md) , das das Computersystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="69c53-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="69c53-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="69c53-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69c53-121">Datentyp: **CIM \_ Systemresource**</span><span class="sxs-lookup"><span data-stu-id="69c53-121">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="69c53-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69c53-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69c53-123">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="69c53-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="69c53-124">Eine [**CIM \_**](cim-systemresource.md) -System Ressource, die eine System Ressource des Computer Systems beschreibt.</span><span class="sxs-lookup"><span data-stu-id="69c53-124">A [**CIM\_SystemResource**](cim-systemresource.md) that describes a system resource of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69c53-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69c53-125">Remarks</span></span>

<span data-ttu-id="69c53-126">Die **CIM \_ computersystemresource** -Klasse wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="69c53-126">The **CIM\_ComputerSystemResource** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="69c53-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="69c53-127">WMI does not implement this class.</span></span> <span data-ttu-id="69c53-128">Weitere Informationen zu Klassen, die von **CIM \_ computersystemresource** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="69c53-128">For more information about classes derived from **CIM\_ComputerSystemResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="69c53-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="69c53-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="69c53-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="69c53-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="69c53-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69c53-131">Requirements</span></span>



| <span data-ttu-id="69c53-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69c53-132">Requirement</span></span> | <span data-ttu-id="69c53-133">Wert</span><span class="sxs-lookup"><span data-stu-id="69c53-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69c53-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69c53-134">Minimum supported client</span></span><br/> | <span data-ttu-id="69c53-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69c53-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="69c53-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69c53-136">Minimum supported server</span></span><br/> | <span data-ttu-id="69c53-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69c53-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="69c53-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="69c53-138">Namespace</span></span><br/>                | <span data-ttu-id="69c53-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="69c53-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="69c53-140">MOF</span><span class="sxs-lookup"><span data-stu-id="69c53-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69c53-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="69c53-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="69c53-142">DLL</span><span class="sxs-lookup"><span data-stu-id="69c53-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69c53-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69c53-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69c53-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69c53-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c53-145">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="69c53-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

