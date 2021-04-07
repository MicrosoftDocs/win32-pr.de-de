---
description: Die CIM-Verzeichnis Verbindungs Zuordnung \_ identifiziert das Zielverzeichnis für die Datei Aktion.
ms.assetid: f4dcd99c-4da8-447d-b6f7-7e3da63ca9c4
ms.tgt_platform: multiple
title: CIM_ToDirectoryAction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectoryAction
- CIM_ToDirectoryAction.DestinationDirectory
- CIM_ToDirectoryAction.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10ed2f7c2e2b46e63e2cc02cc8e6ce09ab2688e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749049"
---
# <a name="cim_todirectoryaction-class"></a><span data-ttu-id="d48fb-103">CIM- \_ Klasse "dedirectoryaction"</span><span class="sxs-lookup"><span data-stu-id="d48fb-103">CIM\_ToDirectoryAction class</span></span>

<span data-ttu-id="d48fb-104">Die **CIM \_** -Verzeichnis Verbindungs Zuordnung identifiziert das Zielverzeichnis für die Datei Aktion.</span><span class="sxs-lookup"><span data-stu-id="d48fb-104">The **CIM\_ToDirectoryAction** association identifies the target directory for the file action.</span></span> <span data-ttu-id="d48fb-105">Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Zielverzeichnis durch eine vorherige Aktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d48fb-105">When this association is used, it is assumed that the target directory was created by a previous action.</span></span> <span data-ttu-id="d48fb-106">Diese Zuordnung darf nicht mit einer [**CIM- \_ Verzeichnis Verbindungs Spezifikation vorhanden sein**](cim-todirectoryspecification.md) , da eine Datei Aktion nur ein einzelnes Zielverzeichnis umfassen kann.</span><span class="sxs-lookup"><span data-stu-id="d48fb-106">This association cannot exist with a [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d48fb-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d48fb-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d48fb-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d48fb-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d48fb-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d48fb-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d48fb-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d48fb-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d48fb-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d48fb-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{B58D172E-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectoryAction
{
  CIM_DirectoryAction REF DestinationDirectory;
  CIM_CopyFileAction  REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="d48fb-112">Member</span><span class="sxs-lookup"><span data-stu-id="d48fb-112">Members</span></span>

<span data-ttu-id="d48fb-113">Die **CIM \_ todirectoryaction** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d48fb-113">The **CIM\_ToDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="d48fb-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d48fb-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d48fb-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d48fb-115">Properties</span></span>

<span data-ttu-id="d48fb-116">Die CIM-Klasse " **\_ dedirectoryaction** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d48fb-116">The **CIM\_ToDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d48fb-117">**DestinationDirectory**</span><span class="sxs-lookup"><span data-stu-id="d48fb-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48fb-118">Datentyp: **CIM \_ directoriyaction**</span><span class="sxs-lookup"><span data-stu-id="d48fb-118">Data type: **CIM\_DirectoryAction**</span></span>
</dt> <dt>

<span data-ttu-id="d48fb-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d48fb-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48fb-120">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="d48fb-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="d48fb-121">Verweis auf das Zielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d48fb-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="d48fb-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="d48fb-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d48fb-123">Datentyp: **CIM \_ copyfileaction**</span><span class="sxs-lookup"><span data-stu-id="d48fb-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="d48fb-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d48fb-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d48fb-125">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="d48fb-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="d48fb-126">Verweis auf den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="d48fb-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d48fb-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d48fb-127">Remarks</span></span>

<span data-ttu-id="d48fb-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d48fb-128">WMI does not implement this class.</span></span>

<span data-ttu-id="d48fb-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d48fb-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d48fb-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d48fb-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d48fb-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d48fb-131">Requirements</span></span>



| <span data-ttu-id="d48fb-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d48fb-132">Requirement</span></span> | <span data-ttu-id="d48fb-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d48fb-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d48fb-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d48fb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d48fb-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d48fb-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d48fb-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d48fb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d48fb-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d48fb-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d48fb-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="d48fb-138">Namespace</span></span><br/>                | <span data-ttu-id="d48fb-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d48fb-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d48fb-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d48fb-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d48fb-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d48fb-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d48fb-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d48fb-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d48fb-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d48fb-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

