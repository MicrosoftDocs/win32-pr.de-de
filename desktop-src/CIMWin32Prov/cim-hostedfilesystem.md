---
description: Die CIM \_ hostedfile System-Zuordnung stellt eine Verknüpfung zwischen dem Computersystem und dem Dateisystem dar, das auf dem Computersystem gehostet wird.
ms.assetid: 1027fc6b-588b-4da8-8b3f-0c4c3328534a
ms.tgt_platform: multiple
title: CIM_HostedFileSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedFileSystem
- CIM_HostedFileSystem.PartComponent
- CIM_HostedFileSystem.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eef90ea3f1ed743ec5bee0eefa5afebc8c340077
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126965"
---
# <a name="cim_hostedfilesystem-class"></a><span data-ttu-id="2942d-103">CIM-Klasse für das \_ Klassensystem</span><span class="sxs-lookup"><span data-stu-id="2942d-103">CIM\_HostedFileSystem class</span></span>

<span data-ttu-id="2942d-104">Die **CIM \_ hostedfile** System-Zuordnung stellt eine Verknüpfung zwischen dem Computersystem und dem Dateisystem dar, das auf dem Computersystem gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="2942d-104">The **CIM\_HostedFileSystem** association represents a link between the computer system and the file system hosted on the computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2942d-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2942d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2942d-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2942d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2942d-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2942d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2942d-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2942d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2942d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2942d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC898-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_HostedFileSystem : CIM_SystemComponent
{
  CIM_FileSystem     REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="2942d-110">Member</span><span class="sxs-lookup"><span data-stu-id="2942d-110">Members</span></span>

<span data-ttu-id="2942d-111">Die CIM-Klasse " **\_ hustedfile System** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2942d-111">The **CIM\_HostedFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="2942d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2942d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2942d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2942d-113">Properties</span></span>

<span data-ttu-id="2942d-114">Die CIM-Klasse " **\_ hustedfile System** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2942d-114">The **CIM\_HostedFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2942d-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2942d-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2942d-116">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="2942d-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="2942d-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2942d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2942d-118">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="2942d-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2942d-119">Ein [**CIM- \_ Computersystem**](cim-computersystem.md) , das das Computersystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2942d-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="2942d-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2942d-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2942d-121">Datentyp: **CIM \_ File System**</span><span class="sxs-lookup"><span data-stu-id="2942d-121">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="2942d-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2942d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2942d-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("PartComponent"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2942d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2942d-124">Ein [**CIM- \_ Datei**](cim-filesystem.md) System, das das Dateisystem im Besitz des Computer Systems beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2942d-124">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system owned by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2942d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2942d-125">Remarks</span></span>

<span data-ttu-id="2942d-126">Die CIM-Klasse " **\_ hustedfile System** " wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2942d-126">The **CIM\_HostedFileSystem** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="2942d-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2942d-127">WMI does not implement this class.</span></span>

<span data-ttu-id="2942d-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2942d-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2942d-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2942d-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2942d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2942d-130">Requirements</span></span>



| <span data-ttu-id="2942d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2942d-131">Requirement</span></span> | <span data-ttu-id="2942d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2942d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2942d-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2942d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2942d-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2942d-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2942d-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2942d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2942d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2942d-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2942d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="2942d-137">Namespace</span></span><br/>                | <span data-ttu-id="2942d-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2942d-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2942d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2942d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2942d-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2942d-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2942d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2942d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2942d-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2942d-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2942d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2942d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2942d-144">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="2942d-144">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

