---
description: Die CIM- \_ Verzeichnisdienst Spezifikation identifiziert das Zielverzeichnis für die Datei Aktion.
ms.assetid: ab31101f-1948-4b3d-baef-0d61d5898b21
ms.tgt_platform: multiple
title: CIM_ToDirectorySpecification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectorySpecification
- CIM_ToDirectorySpecification.DestinationDirectory
- CIM_ToDirectorySpecification.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0728f605e02195a6bf2bd4beb0ca67fe8744e12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127769"
---
# <a name="cim_todirectoryspecification-class"></a><span data-ttu-id="e522b-103">CIM- \_ Klasse für directoryspecification</span><span class="sxs-lookup"><span data-stu-id="e522b-103">CIM\_ToDirectorySpecification class</span></span>

<span data-ttu-id="e522b-104">Die **CIM \_** -Verzeichnisdienst Spezifikation identifiziert das Zielverzeichnis für die Datei Aktion.</span><span class="sxs-lookup"><span data-stu-id="e522b-104">The **CIM\_ToDirectorySpecification** association identifies the target directory for the file action.</span></span> <span data-ttu-id="e522b-105">Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Zielverzeichnis bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e522b-105">When this association is used, it is assumed that the target directory already existed.</span></span> <span data-ttu-id="e522b-106">Diese Zuordnung darf nicht mit einer [**CIM-" \_ dedirector yaction**](cim-todirectoryaction.md) "-Zuordnung vorhanden sein, da eine Datei Aktion nur ein einzelnes Zielverzeichnis umfassen kann.</span><span class="sxs-lookup"><span data-stu-id="e522b-106">This association cannot exist with a [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e522b-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e522b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e522b-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e522b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e522b-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e522b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e522b-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e522b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e522b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e522b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{C3E25A3C-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectorySpecification
{
  CIM_DirectorySpecification REF DestinationDirectory;
  CIM_CopyFileAction         REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="e522b-112">Member</span><span class="sxs-lookup"><span data-stu-id="e522b-112">Members</span></span>

<span data-ttu-id="e522b-113">Die **CIM \_ todirectoryspecification** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e522b-113">The **CIM\_ToDirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="e522b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e522b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e522b-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e522b-115">Properties</span></span>

<span data-ttu-id="e522b-116">Die CIM-Klasse " **\_ dedirectoryspecification** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e522b-116">The **CIM\_ToDirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e522b-117">**DestinationDirectory**</span><span class="sxs-lookup"><span data-stu-id="e522b-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e522b-118">Datentyp: **CIM \_ directoriyspecification**</span><span class="sxs-lookup"><span data-stu-id="e522b-118">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="e522b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e522b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e522b-120">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="e522b-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="e522b-121">Verweis auf das Zielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e522b-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="e522b-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="e522b-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e522b-123">Datentyp: **CIM \_ copyfileaction**</span><span class="sxs-lookup"><span data-stu-id="e522b-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="e522b-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e522b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e522b-125">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="e522b-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="e522b-126">Verweis auf den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="e522b-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e522b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e522b-127">Remarks</span></span>

<span data-ttu-id="e522b-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="e522b-128">WMI does not implement this class.</span></span>

<span data-ttu-id="e522b-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e522b-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e522b-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e522b-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e522b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e522b-131">Requirements</span></span>



| <span data-ttu-id="e522b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e522b-132">Requirement</span></span> | <span data-ttu-id="e522b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e522b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e522b-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e522b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e522b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e522b-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e522b-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e522b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e522b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e522b-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e522b-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="e522b-138">Namespace</span></span><br/>                | <span data-ttu-id="e522b-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e522b-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e522b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e522b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e522b-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e522b-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e522b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e522b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e522b-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e522b-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

