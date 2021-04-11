---
description: Die CIM \_ -Export Klasse stellt eine Zuordnung zwischen einem lokalen Dateisystem und den zugehörigen Verzeichnissen dar, die angeben, dass die angegebenen Verzeichnisse zum Einbinden verfügbar sind.
ms.assetid: 4c43ba5a-e003-4985-85b3-68ecf13a4bf5
ms.tgt_platform: multiple
title: CIM_Export-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Export
- CIM_Export.Directory
- CIM_Export.ExportedDirectoryName
- CIM_Export.LocalFS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 447601b61fb79cfa779ea0cab75962c835210c52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958410"
---
# <a name="cim_export-class"></a><span data-ttu-id="9d7b2-103">CIM- \_ Export Klasse</span><span class="sxs-lookup"><span data-stu-id="9d7b2-103">CIM\_Export class</span></span>

<span data-ttu-id="9d7b2-104">Die **CIM- \_ Export** Klasse stellt eine Zuordnung zwischen einem lokalen Dateisystem und den zugehörigen Verzeichnissen dar, die angeben, dass die angegebenen Verzeichnisse zum Einbinden verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9d7b2-104">The **CIM\_Export** class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="9d7b2-105">Beim Exportieren eines vollständigen Dateisystems sollte das Verzeichnis auf das oberste Verzeichnis des Dateisystems verweisen.</span><span class="sxs-lookup"><span data-stu-id="9d7b2-105">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d7b2-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9d7b2-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9d7b2-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9d7b2-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9d7b2-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="9d7b2-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9d7b2-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9d7b2-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d7b2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d7b2-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{75BCF4F8-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Export
{
  CIM_Directory       REF Directory;
  string                  ExportedDirectoryName;
  CIM_LocalFileSystem REF LocalFS;
};
```

## <a name="members"></a><span data-ttu-id="9d7b2-111">Member</span><span class="sxs-lookup"><span data-stu-id="9d7b2-111">Members</span></span>

<span data-ttu-id="9d7b2-112">Die **CIM- \_ Export** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9d7b2-112">The **CIM\_Export** class has these types of members:</span></span>

-   [<span data-ttu-id="9d7b2-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d7b2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d7b2-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d7b2-114">Properties</span></span>

<span data-ttu-id="9d7b2-115">Die **CIM- \_ Export** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9d7b2-115">The **CIM\_Export** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d7b2-116">**Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="9d7b2-116">**Directory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7b2-117">Datentyp: **CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="9d7b2-117">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="9d7b2-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d7b2-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d7b2-119">Verweis auf das Verzeichnis, das für die Network File System (NFS)-einreilegung exportiert wird</span><span class="sxs-lookup"><span data-stu-id="9d7b2-119">Reference to the directory exported for network file system (NFS) mount.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b2-120">**Exporteddirecteryname**</span><span class="sxs-lookup"><span data-stu-id="9d7b2-120">**ExportedDirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7b2-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d7b2-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d7b2-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d7b2-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d7b2-123">Der Name, unter dem das Verzeichnis exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="9d7b2-123">Name under which the directory is exported.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b2-124">**Localfs**</span><span class="sxs-lookup"><span data-stu-id="9d7b2-124">**LocalFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7b2-125">Datentyp: **CIM \_ LocalFile System**</span><span class="sxs-lookup"><span data-stu-id="9d7b2-125">Data type: **CIM\_LocalFileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="9d7b2-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d7b2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d7b2-127">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="9d7b2-127">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9d7b2-128">Verweis auf das lokale Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="9d7b2-128">Reference to the local file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d7b2-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d7b2-129">Remarks</span></span>

<span data-ttu-id="9d7b2-130">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9d7b2-130">WMI does not implement this class.</span></span>

<span data-ttu-id="9d7b2-131">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9d7b2-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9d7b2-132">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9d7b2-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d7b2-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d7b2-133">Requirements</span></span>



| <span data-ttu-id="9d7b2-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d7b2-134">Requirement</span></span> | <span data-ttu-id="9d7b2-135">Wert</span><span class="sxs-lookup"><span data-stu-id="9d7b2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d7b2-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d7b2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9d7b2-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d7b2-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d7b2-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d7b2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9d7b2-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d7b2-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d7b2-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d7b2-140">Namespace</span></span><br/>                | <span data-ttu-id="9d7b2-141">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9d7b2-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9d7b2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9d7b2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d7b2-143"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9d7b2-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d7b2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9d7b2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d7b2-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d7b2-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

