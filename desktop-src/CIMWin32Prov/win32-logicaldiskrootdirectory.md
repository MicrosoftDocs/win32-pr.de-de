---
description: Die \_ WMI-Klasse "Win32 logicaldiskrootdirectory Association" verknüpft einen logischen Datenträger und seine Verzeichnisstruktur.
ms.assetid: 860cd28a-2a59-4ce3-be26-8fdc869c70d1
ms.tgt_platform: multiple
title: Win32_LogicalDiskRootDirectory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskRootDirectory
- Win32_LogicalDiskRootDirectory.GroupComponent
- Win32_LogicalDiskRootDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b015891a37c5cc92bbf102482f48306d537bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860628"
---
# <a name="win32_logicaldiskrootdirectory-class"></a><span data-ttu-id="74b3f-103">Win32 \_ logicaldiskrootdirectory-Klasse</span><span class="sxs-lookup"><span data-stu-id="74b3f-103">Win32\_LogicalDiskRootDirectory class</span></span>

<span data-ttu-id="74b3f-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ logicaldiskrootdirectory** Association" verknüpft einen logischen Datenträger und seine Verzeichnisstruktur.</span><span class="sxs-lookup"><span data-stu-id="74b3f-104">The **Win32\_LogicalDiskRootDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical disk and its directory structure.</span></span>

<span data-ttu-id="74b3f-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="74b3f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="74b3f-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="74b3f-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b3f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="74b3f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE468-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalDiskRootDirectory : CIM_Component
{
  Win32_LogicalDisk REF GroupComponent;
  Win32_Directory   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="74b3f-108">Member</span><span class="sxs-lookup"><span data-stu-id="74b3f-108">Members</span></span>

<span data-ttu-id="74b3f-109">Die **Win32 \_ logicaldiskrootdirectory** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="74b3f-109">The **Win32\_LogicalDiskRootDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="74b3f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74b3f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74b3f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74b3f-111">Properties</span></span>

<span data-ttu-id="74b3f-112">Die **Win32 \_ logicaldiskrootdirectory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="74b3f-112">The **Win32\_LogicalDiskRootDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74b3f-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="74b3f-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b3f-114">Datentyp: **Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="74b3f-114">Data type: **Win32\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="74b3f-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74b3f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74b3f-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalDisk")</span><span class="sxs-lookup"><span data-stu-id="74b3f-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalDisk")</span></span>
</dt> </dl>

<span data-ttu-id="74b3f-117">Verweis auf die-Instanz, die die Eigenschaften des logischen Datenträgers darstellt.</span><span class="sxs-lookup"><span data-stu-id="74b3f-117">Reference to the instance representing the properties of the logical disk.</span></span>

</dd> <dt>

<span data-ttu-id="74b3f-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="74b3f-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b3f-119">Datentyp: **Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="74b3f-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="74b3f-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74b3f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74b3f-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32- \_ Verzeichnis")</span><span class="sxs-lookup"><span data-stu-id="74b3f-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="74b3f-122">Verweis auf die-Instanz, die die Eigenschaften der Datei Verzeichnisstruktur darstellt.</span><span class="sxs-lookup"><span data-stu-id="74b3f-122">Reference to the instance representing the properties of the file directory structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74b3f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74b3f-123">Remarks</span></span>

<span data-ttu-id="74b3f-124">Die **Win32 \_ logicaldiskrootdirectory** -Klasse wird von der [**CIM- \_ Komponente**](cim-component.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="74b3f-124">The **Win32\_LogicalDiskRootDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74b3f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74b3f-125">Requirements</span></span>



| <span data-ttu-id="74b3f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74b3f-126">Requirement</span></span> | <span data-ttu-id="74b3f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="74b3f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74b3f-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74b3f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="74b3f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74b3f-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="74b3f-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74b3f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="74b3f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74b3f-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="74b3f-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="74b3f-132">Namespace</span></span><br/>                | <span data-ttu-id="74b3f-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="74b3f-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="74b3f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="74b3f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74b3f-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="74b3f-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="74b3f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="74b3f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74b3f-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74b3f-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74b3f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74b3f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b3f-139">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="74b3f-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="74b3f-140">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="74b3f-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

