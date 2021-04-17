---
description: Die CIM \_ installedos Association-Klasse stellt eine Verknüpfung zwischen dem Computersystem und dem installierten Betriebssystem dar.
ms.assetid: 6db5b5a2-91b6-4540-83b8-bb9c86c7f94e
ms.tgt_platform: multiple
title: CIM_InstalledOS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledOS
- CIM_InstalledOS.PartComponent
- CIM_InstalledOS.GroupComponent
- CIM_InstalledOS.PrimaryOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53e01be6a87fa6e5ef91ad6e8a81dbbddff4a576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523763"
---
# <a name="cim_installedos-class"></a><span data-ttu-id="55e66-103">CIM \_ installedos-Klasse</span><span class="sxs-lookup"><span data-stu-id="55e66-103">CIM\_InstalledOS class</span></span>

<span data-ttu-id="55e66-104">Die **CIM \_ installedos** Association-Klasse stellt eine Verknüpfung zwischen dem Computersystem und dem installierten Betriebssystem dar.</span><span class="sxs-lookup"><span data-stu-id="55e66-104">The **CIM\_InstalledOS** association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="55e66-105">Ein Betriebssystem wird installiert, wenn es sich im Speicherbereich eines Computer Systems befindet (z. b. auf ein Laufwerk kopiert oder in den Arbeitsspeicher heruntergeladen wird).</span><span class="sxs-lookup"><span data-stu-id="55e66-105">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55e66-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="55e66-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="55e66-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="55e66-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="55e66-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="55e66-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="55e66-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="55e66-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="55e66-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="55e66-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C575-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_InstalledOS : CIM_SystemComponent
{
  CIM_OperatingSystem REF PartComponent;
  CIM_ComputerSystem  REF GroupComponent;
  boolean                 PrimaryOS;
};
```

## <a name="members"></a><span data-ttu-id="55e66-111">Member</span><span class="sxs-lookup"><span data-stu-id="55e66-111">Members</span></span>

<span data-ttu-id="55e66-112">Die **CIM \_ installedos** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="55e66-112">The **CIM\_InstalledOS** class has these types of members:</span></span>

-   [<span data-ttu-id="55e66-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55e66-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55e66-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55e66-114">Properties</span></span>

<span data-ttu-id="55e66-115">Die **CIM \_ installedos** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="55e66-115">The **CIM\_InstalledOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55e66-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="55e66-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55e66-117">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="55e66-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="55e66-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55e66-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55e66-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="55e66-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="55e66-120">Ein [**CIM- \_ Computersystem**](cim-computersystem.md) , das das Computersystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="55e66-120">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="55e66-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="55e66-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55e66-122">Datentyp: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="55e66-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="55e66-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55e66-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55e66-124">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("PartComponent"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="55e66-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="55e66-125">Ein [**CIM- \_ OperatingSystem**](cim-operatingsystem.md) , das das auf dem Computersystem installierte Betriebssystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="55e66-125">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="55e66-126">**Primaryos**</span><span class="sxs-lookup"><span data-stu-id="55e66-126">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55e66-127">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="55e66-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55e66-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55e66-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55e66-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Betriebs System \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="55e66-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="55e66-130">**True** gibt an, dass das installierte Betriebssystem das Standardbetriebssystem für das Computersystem ist.</span><span class="sxs-lookup"><span data-stu-id="55e66-130">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55e66-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55e66-131">Remarks</span></span>

<span data-ttu-id="55e66-132">Die **CIM \_ installedos** -Klasse wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="55e66-132">The **CIM\_InstalledOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="55e66-133">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="55e66-133">WMI does not implement this class.</span></span> <span data-ttu-id="55e66-134">Informationen zu Klassen, die von **CIM \_ installedos** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="55e66-134">For classes derived from **CIM\_InstalledOS**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="55e66-135">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="55e66-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="55e66-136">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="55e66-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="55e66-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55e66-137">Requirements</span></span>



| <span data-ttu-id="55e66-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55e66-138">Requirement</span></span> | <span data-ttu-id="55e66-139">Wert</span><span class="sxs-lookup"><span data-stu-id="55e66-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55e66-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55e66-140">Minimum supported client</span></span><br/> | <span data-ttu-id="55e66-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55e66-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55e66-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55e66-142">Minimum supported server</span></span><br/> | <span data-ttu-id="55e66-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55e66-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55e66-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="55e66-144">Namespace</span></span><br/>                | <span data-ttu-id="55e66-145">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="55e66-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55e66-146">MOF</span><span class="sxs-lookup"><span data-stu-id="55e66-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55e66-147"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="55e66-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55e66-148">DLL</span><span class="sxs-lookup"><span data-stu-id="55e66-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55e66-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55e66-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55e66-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55e66-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e66-151">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="55e66-151">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

