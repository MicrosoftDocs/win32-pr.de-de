---
description: Die CIM \_ directorykontainsfile-Klasse stellt eine Zuordnung zwischen einem Verzeichnis und den Dateien dar, die in diesem Verzeichnis enthalten sind.
ms.assetid: e05ec86e-c3cf-4589-9815-83850e0c84ed
ms.tgt_platform: multiple
title: CIM_DirectoryContainsFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryContainsFile
- CIM_DirectoryContainsFile.PartComponent
- CIM_DirectoryContainsFile.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bd1913352d19a1ed5889413eed5e7fc4640ac53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861403"
---
# <a name="cim_directorycontainsfile-class"></a><span data-ttu-id="a16c7-103">CIM- \_ directorykontainsfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="a16c7-103">CIM\_DirectoryContainsFile class</span></span>

<span data-ttu-id="a16c7-104">Die **CIM \_ directorykontainsfile** -Klasse stellt eine Zuordnung zwischen einem Verzeichnis und den Dateien dar, die in diesem Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a16c7-104">The **CIM\_DirectoryContainsFile** class represents an association between a directory and files contained within that directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a16c7-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a16c7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a16c7-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a16c7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a16c7-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a16c7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a16c7-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a16c7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a16c7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a16c7-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{6F9D4740-8324-11d2-AAD9-006008C78BC7}"), AMENDMENT]
class CIM_DirectoryContainsFile : CIM_Component
{
  CIM_DataFile  REF PartComponent;
  CIM_Directory REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="a16c7-110">Member</span><span class="sxs-lookup"><span data-stu-id="a16c7-110">Members</span></span>

<span data-ttu-id="a16c7-111">Die CIM-Klasse " **\_ directorykontainsfile** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a16c7-111">The **CIM\_DirectoryContainsFile** class has these types of members:</span></span>

-   [<span data-ttu-id="a16c7-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a16c7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a16c7-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a16c7-113">Properties</span></span>

<span data-ttu-id="a16c7-114">Die **CIM \_ directorykontainsfile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a16c7-114">The **CIM\_DirectoryContainsFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a16c7-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a16c7-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16c7-116">Datentyp: **CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="a16c7-116">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="a16c7-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a16c7-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16c7-118">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="a16c7-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="a16c7-119">Ein [**CIM- \_ Verzeichnis**](cim-directory.md) , in dem das Verzeichnis beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="a16c7-119">A [**CIM\_Directory**](cim-directory.md) that describes the directory.</span></span>

</dd> <dt>

<span data-ttu-id="a16c7-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a16c7-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16c7-121">Datentyp: **CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="a16c7-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="a16c7-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a16c7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16c7-123">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="a16c7-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a16c7-124">Eine [**CIM- \_ Datendatei**](cim-datafile.md) , die die im Verzeichnis enthaltene LogicalFile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a16c7-124">A [**CIM\_DataFile**](cim-datafile.md) that describes the LogicalFile contained within the directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a16c7-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a16c7-125">Remarks</span></span>

<span data-ttu-id="a16c7-126">WMI implementiert die **CIM-Klasse \_ directorykontainsfile** , bei der es sich um eine dynamische Klasse handelt.</span><span class="sxs-lookup"><span data-stu-id="a16c7-126">WMI implements the **CIM\_DirectoryContainsFile** class, which is a dynamic class.</span></span>

<span data-ttu-id="a16c7-127">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a16c7-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a16c7-128">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a16c7-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a16c7-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a16c7-129">Requirements</span></span>



| <span data-ttu-id="a16c7-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a16c7-130">Requirement</span></span> | <span data-ttu-id="a16c7-131">Wert</span><span class="sxs-lookup"><span data-stu-id="a16c7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a16c7-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a16c7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a16c7-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a16c7-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a16c7-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a16c7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a16c7-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a16c7-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a16c7-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="a16c7-136">Namespace</span></span><br/>                | <span data-ttu-id="a16c7-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a16c7-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a16c7-138">MOF</span><span class="sxs-lookup"><span data-stu-id="a16c7-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a16c7-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a16c7-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a16c7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a16c7-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a16c7-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a16c7-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a16c7-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a16c7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a16c7-143">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="a16c7-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

