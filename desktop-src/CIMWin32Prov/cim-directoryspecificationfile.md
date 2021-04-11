---
description: Die CIM- \_ directoryspecificationfile-Zuordnung stellt das Verzeichnis dar, das die Datei enthält, die durch Verweisen auf die CIM- \_ directoryspecification-Klasse angegeben wird.
ms.assetid: 57fe996e-6bd4-4070-9e99-460b2a36243f
ms.tgt_platform: multiple
title: CIM_DirectorySpecificationFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecificationFile
- CIM_DirectorySpecificationFile.DirectorySpecification
- CIM_DirectorySpecificationFile.FileSpecification
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1877d9864a76334c2b2e00fc7822adb09b91028b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127184"
---
# <a name="cim_directoryspecificationfile-class"></a><span data-ttu-id="02141-103">CIM- \_ directoryspecificationfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="02141-103">CIM\_DirectorySpecificationFile class</span></span>

<span data-ttu-id="02141-104">Die **CIM- \_ directoryspecificationfile-Zuordnung** stellt das Verzeichnis dar, das die Datei enthält, die durch Verweisen auf die CIM- [**\_ directoryspecification**](cim-directoryspecification.md) -Klasse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="02141-104">The **CIM\_DirectorySpecificationFile** association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02141-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="02141-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="02141-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="02141-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="02141-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="02141-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="02141-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="02141-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="02141-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="02141-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{BCD64CCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_DirectorySpecificationFile
{
  CIM_DirectorySpecification REF DirectorySpecification;
  CIM_FileSpecification      REF FileSpecification;
};
```

## <a name="members"></a><span data-ttu-id="02141-110">Member</span><span class="sxs-lookup"><span data-stu-id="02141-110">Members</span></span>

<span data-ttu-id="02141-111">Die **CIM- \_ directoryspecificationfile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="02141-111">The **CIM\_DirectorySpecificationFile** class has these types of members:</span></span>

-   [<span data-ttu-id="02141-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02141-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02141-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02141-113">Properties</span></span>

<span data-ttu-id="02141-114">Die **CIM- \_ directoryspecificationfile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02141-114">The **CIM\_DirectorySpecificationFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02141-115">**Directoriyspecification**</span><span class="sxs-lookup"><span data-stu-id="02141-115">**DirectorySpecification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02141-116">Datentyp: **CIM \_ directoriyspecification**</span><span class="sxs-lookup"><span data-stu-id="02141-116">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="02141-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02141-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02141-118">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="02141-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="02141-119">Verweis auf die Verzeichnis Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="02141-119">Reference to the directory specification.</span></span>

</dd> <dt>

<span data-ttu-id="02141-120">**File Specification**</span><span class="sxs-lookup"><span data-stu-id="02141-120">**FileSpecification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02141-121">Datentyp: **CIM \_ File Specification**</span><span class="sxs-lookup"><span data-stu-id="02141-121">Data type: **CIM\_FileSpecification**</span></span>
</dt> <dt>

<span data-ttu-id="02141-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02141-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02141-123">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="02141-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="02141-124">Verweis auf die Datei Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="02141-124">Reference to the file specification.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02141-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02141-125">Remarks</span></span>

<span data-ttu-id="02141-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="02141-126">WMI does not implement this class.</span></span>

<span data-ttu-id="02141-127">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="02141-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="02141-128">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="02141-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="02141-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02141-129">Requirements</span></span>



| <span data-ttu-id="02141-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02141-130">Requirement</span></span> | <span data-ttu-id="02141-131">Wert</span><span class="sxs-lookup"><span data-stu-id="02141-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02141-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02141-132">Minimum supported client</span></span><br/> | <span data-ttu-id="02141-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02141-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02141-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02141-134">Minimum supported server</span></span><br/> | <span data-ttu-id="02141-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02141-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02141-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="02141-136">Namespace</span></span><br/>                | <span data-ttu-id="02141-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="02141-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="02141-138">MOF</span><span class="sxs-lookup"><span data-stu-id="02141-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02141-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="02141-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="02141-140">DLL</span><span class="sxs-lookup"><span data-stu-id="02141-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02141-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02141-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

