---
description: Die CIM \_ -FileStorage-Zuordnung verknüpft das Dateisystem und die logischen Dateien, die über das Dateisystem adressiert werden.
ms.assetid: 1d0b698b-4c57-4a1c-8b00-0a6079be8dcc
ms.tgt_platform: multiple
title: CIM_FileStorage-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileStorage
- CIM_FileStorage.PartComponent
- CIM_FileStorage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3630bdf3250ce93765809df17e9318d3cd44f393
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342766"
---
# <a name="cim_filestorage-class"></a><span data-ttu-id="66e47-103">CIM- \_ FileStorage-Klasse</span><span class="sxs-lookup"><span data-stu-id="66e47-103">CIM\_FileStorage class</span></span>

<span data-ttu-id="66e47-104">Die **CIM- \_ FileStorage** -Zuordnung verknüpft das Dateisystem und die logischen Dateien, die über das Dateisystem adressiert werden.</span><span class="sxs-lookup"><span data-stu-id="66e47-104">The **CIM\_FileStorage** association links the file system and the logical files addressed through the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66e47-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="66e47-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="66e47-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="66e47-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="66e47-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="66e47-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="66e47-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="66e47-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="66e47-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="66e47-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4A626026-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FileStorage : CIM_Component
{
  CIM_LogicalFile REF PartComponent;
  CIM_FileSystem  REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="66e47-110">Member</span><span class="sxs-lookup"><span data-stu-id="66e47-110">Members</span></span>

<span data-ttu-id="66e47-111">Die **CIM- \_ FileStorage** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="66e47-111">The **CIM\_FileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="66e47-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66e47-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66e47-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66e47-113">Properties</span></span>

<span data-ttu-id="66e47-114">Die **CIM- \_ FileStorage** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="66e47-114">The **CIM\_FileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66e47-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="66e47-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e47-116">Datentyp: **CIM \_ File System**</span><span class="sxs-lookup"><span data-stu-id="66e47-116">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="66e47-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="66e47-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66e47-118">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="66e47-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="66e47-119">Ein [**CIM- \_ Datei**](cim-filesystem.md) System, das das Dateisystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="66e47-119">A [**CIM\_FileSystem**](cim-filesystem.md) describing the file system.</span></span>

</dd> <dt>

<span data-ttu-id="66e47-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="66e47-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66e47-121">Datentyp: **CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="66e47-121">Data type: **CIM\_LogicalFile**</span></span>
</dt> <dt>

<span data-ttu-id="66e47-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="66e47-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66e47-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("PartComponent"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="66e47-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="66e47-124">Eine [**CIM \_ LogicalFile**](cim-logicalfile.md) , die die logische Datei beschreibt, die im Kontext des Dateisystems gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="66e47-124">A [**CIM\_LogicalFile**](cim-logicalfile.md) describing the logical file stored in the context of the file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66e47-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66e47-125">Remarks</span></span>

<span data-ttu-id="66e47-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="66e47-126">WMI does not implement this class.</span></span>

<span data-ttu-id="66e47-127">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="66e47-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="66e47-128">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="66e47-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="66e47-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66e47-129">Requirements</span></span>



| <span data-ttu-id="66e47-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66e47-130">Requirement</span></span> | <span data-ttu-id="66e47-131">Wert</span><span class="sxs-lookup"><span data-stu-id="66e47-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66e47-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66e47-132">Minimum supported client</span></span><br/> | <span data-ttu-id="66e47-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66e47-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66e47-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66e47-134">Minimum supported server</span></span><br/> | <span data-ttu-id="66e47-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66e47-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66e47-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="66e47-136">Namespace</span></span><br/>                | <span data-ttu-id="66e47-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="66e47-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="66e47-138">MOF</span><span class="sxs-lookup"><span data-stu-id="66e47-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66e47-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="66e47-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="66e47-140">DLL</span><span class="sxs-lookup"><span data-stu-id="66e47-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66e47-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66e47-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e47-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66e47-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e47-143">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="66e47-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

