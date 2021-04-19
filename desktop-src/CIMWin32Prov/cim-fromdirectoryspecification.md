---
description: Die CIM \_ fromdirector yspecification-Zuordnung identifiziert das Quellverzeichnis für die Datei Aktion.
ms.assetid: 031ff95f-aa68-4b05-92a6-97a5e0d8956f
ms.tgt_platform: multiple
title: CIM_FromDirectorySpecification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectorySpecification
- CIM_FromDirectorySpecification.FileName
- CIM_FromDirectorySpecification.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7690514b46d89bdf1aa926438456c49598034700
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346233"
---
# <a name="cim_fromdirectoryspecification-class"></a><span data-ttu-id="03b6b-103">CIM \_ fromdirectoryspecification-Klasse</span><span class="sxs-lookup"><span data-stu-id="03b6b-103">CIM\_FromDirectorySpecification class</span></span>

<span data-ttu-id="03b6b-104">Die **CIM \_ fromdirector yspecification** -Zuordnung identifiziert das Quellverzeichnis für die Datei Aktion.</span><span class="sxs-lookup"><span data-stu-id="03b6b-104">The **CIM\_FromDirectorySpecification** association identifies the source directory for the file action.</span></span> <span data-ttu-id="03b6b-105">Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Quellverzeichnis bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="03b6b-105">When this association is used, the assumption is that the source directory already exists.</span></span> <span data-ttu-id="03b6b-106">Diese Zuordnung darf nicht mit einer [**CIM \_ fromdirector yaction**](cim-fromdirectoryaction.md) -Zuordnung vorhanden sein. eine Datei Aktion kann nur ein einzelnes Quellverzeichnis umfassen.</span><span class="sxs-lookup"><span data-stu-id="03b6b-106">This association cannot exist with a [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association; a file action can only involve a single source directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03b6b-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="03b6b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="03b6b-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="03b6b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="03b6b-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="03b6b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="03b6b-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="03b6b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03b6b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="03b6b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{6715375E-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectorySpecification
{
  CIM_FileAction             REF FileName;
  CIM_DirectorySpecification REF SourceDirectory;
};
```

## <a name="members"></a><span data-ttu-id="03b6b-112">Member</span><span class="sxs-lookup"><span data-stu-id="03b6b-112">Members</span></span>

<span data-ttu-id="03b6b-113">Die **CIM \_ fromdirectoryspecification** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="03b6b-113">The **CIM\_FromDirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="03b6b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03b6b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03b6b-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03b6b-115">Properties</span></span>

<span data-ttu-id="03b6b-116">Die **CIM \_ fromdirectoryspecification** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="03b6b-116">The **CIM\_FromDirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03b6b-117">**FileName**</span><span class="sxs-lookup"><span data-stu-id="03b6b-117">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b6b-118">Datentyp: **CIM \_ fileaction**</span><span class="sxs-lookup"><span data-stu-id="03b6b-118">Data type: **CIM\_FileAction**</span></span>
</dt> <dt>

<span data-ttu-id="03b6b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03b6b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03b6b-120">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="03b6b-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="03b6b-121">Verweis auf den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="03b6b-121">Reference to the file name.</span></span>

</dd> <dt>

<span data-ttu-id="03b6b-122">**SourceDirectory**</span><span class="sxs-lookup"><span data-stu-id="03b6b-122">**SourceDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b6b-123">Datentyp: **CIM \_ directoriyspecification**</span><span class="sxs-lookup"><span data-stu-id="03b6b-123">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="03b6b-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03b6b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03b6b-125">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="03b6b-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="03b6b-126">Verweis auf das Quellverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="03b6b-126">Reference to the source directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03b6b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03b6b-127">Remarks</span></span>

<span data-ttu-id="03b6b-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="03b6b-128">WMI does not implement this class.</span></span>

<span data-ttu-id="03b6b-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="03b6b-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="03b6b-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="03b6b-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="03b6b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03b6b-131">Requirements</span></span>



| <span data-ttu-id="03b6b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03b6b-132">Requirement</span></span> | <span data-ttu-id="03b6b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="03b6b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03b6b-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03b6b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="03b6b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03b6b-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03b6b-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03b6b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="03b6b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03b6b-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03b6b-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="03b6b-138">Namespace</span></span><br/>                | <span data-ttu-id="03b6b-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="03b6b-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03b6b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="03b6b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03b6b-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="03b6b-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03b6b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="03b6b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03b6b-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03b6b-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

