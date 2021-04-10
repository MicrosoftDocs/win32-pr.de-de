---
description: Die CIM \_ InstalledSoftwareElement-Klasse ordnet ein Computersystem einem installierten Softwareelement zu.
ms.assetid: b9a570ed-b4e0-4f73-82e3-6d2bd1708e16
ms.tgt_platform: multiple
title: CIM_InstalledSoftwareElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledSoftwareElement
- CIM_InstalledSoftwareElement.Software
- CIM_InstalledSoftwareElement.System
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd082477b2e2ba194163784b74883872b1edb6a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126960"
---
# <a name="cim_installedsoftwareelement-class"></a><span data-ttu-id="da141-103">CIM \_ InstalledSoftwareElement-Klasse</span><span class="sxs-lookup"><span data-stu-id="da141-103">CIM\_InstalledSoftwareElement class</span></span>

<span data-ttu-id="da141-104">Die **CIM \_ InstalledSoftwareElement** -Klasse ordnet ein Computersystem einem installierten Softwareelement zu.</span><span class="sxs-lookup"><span data-stu-id="da141-104">The **CIM\_InstalledSoftwareElement** class associates a computer system with an installed software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da141-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="da141-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="da141-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="da141-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="da141-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="da141-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="da141-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="da141-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="da141-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="da141-109">Syntax</span></span>

``` syntax
[UUID("{A7B05028-DB2A-11d2-85FC-0000F8102E5F}"), Association, Abstract, AMENDMENT]
class CIM_InstalledSoftwareElement
{
  CIM_SoftwareElement REF Software;
  CIM_ComputerSystem  REF System;
};
```

## <a name="members"></a><span data-ttu-id="da141-110">Member</span><span class="sxs-lookup"><span data-stu-id="da141-110">Members</span></span>

<span data-ttu-id="da141-111">Die **CIM \_ InstalledSoftwareElement** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="da141-111">The **CIM\_InstalledSoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="da141-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da141-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da141-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da141-113">Properties</span></span>

<span data-ttu-id="da141-114">Die **CIM \_ InstalledSoftwareElement** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="da141-114">The **CIM\_InstalledSoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da141-115">**Software**</span><span class="sxs-lookup"><span data-stu-id="da141-115">**Software**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da141-116">Datentyp: **CIM \_ Softwareelement**</span><span class="sxs-lookup"><span data-stu-id="da141-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="da141-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da141-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da141-118">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)</span><span class="sxs-lookup"><span data-stu-id="da141-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="da141-119">Verweis auf das Softwareelement, das auf dem Computersystem installiert ist.</span><span class="sxs-lookup"><span data-stu-id="da141-119">Reference to the software element that is installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="da141-120">**System**</span><span class="sxs-lookup"><span data-stu-id="da141-120">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da141-121">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="da141-121">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="da141-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da141-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da141-123">Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)</span><span class="sxs-lookup"><span data-stu-id="da141-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="da141-124">Verweis auf das Computersystem, das ein bestimmtes Softwareelement gehostet.</span><span class="sxs-lookup"><span data-stu-id="da141-124">Reference to the computer system hosting a particular software element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da141-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da141-125">Remarks</span></span>

<span data-ttu-id="da141-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="da141-126">WMI does not implement this class.</span></span> <span data-ttu-id="da141-127">Informationen zu Klassen, die von **CIM \_ InstalledSoftwareElement** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="da141-127">For classes derived from **CIM\_InstalledSoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="da141-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="da141-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="da141-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="da141-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="da141-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da141-130">Requirements</span></span>



| <span data-ttu-id="da141-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da141-131">Requirement</span></span> | <span data-ttu-id="da141-132">Wert</span><span class="sxs-lookup"><span data-stu-id="da141-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da141-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da141-133">Minimum supported client</span></span><br/> | <span data-ttu-id="da141-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da141-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da141-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da141-135">Minimum supported server</span></span><br/> | <span data-ttu-id="da141-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da141-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da141-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="da141-137">Namespace</span></span><br/>                | <span data-ttu-id="da141-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="da141-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="da141-139">MOF</span><span class="sxs-lookup"><span data-stu-id="da141-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da141-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="da141-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="da141-141">DLL</span><span class="sxs-lookup"><span data-stu-id="da141-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da141-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da141-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

