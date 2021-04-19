---
description: Die \_ WMI-Klasse "Win32 diskdrivedediskpartition" verknüpft ein Laufwerks und eine vorhandene Partition.
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Win32_DiskDriveToDiskPartition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDriveToDiskPartition
- Win32_DiskDriveToDiskPartition.Antecedent
- Win32_DiskDriveToDiskPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2bd5472bd4ad92ddde47f7d6a492916006a80cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343183"
---
# <a name="win32_diskdrivetodiskpartition-class"></a><span data-ttu-id="40848-103">Win32 \_ diskdrivedediskpartition-Klasse</span><span class="sxs-lookup"><span data-stu-id="40848-103">Win32\_DiskDriveToDiskPartition class</span></span>

<span data-ttu-id="40848-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ diskdrivedediskpartition** " verknüpft ein Laufwerks und eine vorhandene Partition.</span><span class="sxs-lookup"><span data-stu-id="40848-104">The **Win32\_DiskDriveToDiskPartition** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a disk drive and a partition existing on it.</span></span>

<span data-ttu-id="40848-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="40848-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="40848-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="40848-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="40848-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="40848-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDriveToDiskPartition : CIM_MediaPresent
{
  Win32_DiskDrive     REF Antecedent;
  Win32_DiskPartition REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="40848-108">Member</span><span class="sxs-lookup"><span data-stu-id="40848-108">Members</span></span>

<span data-ttu-id="40848-109">Die **Win32 \_ diskdrivetodiskpartition** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="40848-109">The **Win32\_DiskDriveToDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="40848-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40848-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40848-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40848-111">Properties</span></span>

<span data-ttu-id="40848-112">Die **Win32 \_ diskdrivedediskpartition** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="40848-112">The **Win32\_DiskDriveToDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40848-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="40848-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40848-114">Datentyp: **Win32 \_ diskdrive**</span><span class="sxs-lookup"><span data-stu-id="40848-114">Data type: **Win32\_DiskDrive**</span></span>
</dt> <dt>

<span data-ttu-id="40848-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40848-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40848-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ diskdrive")</span><span class="sxs-lookup"><span data-stu-id="40848-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskDrive")</span></span>
</dt> </dl>

<span data-ttu-id="40848-117">Verweis auf die-Instanz, die die Eigenschaften des Laufwerks darstellt, auf dem die Partition vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="40848-117">Reference to the instance representing the properties of the disk drive where the partition exists.</span></span>

</dd> <dt>

<span data-ttu-id="40848-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="40848-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40848-119">Datentyp: **Win32 \_ Diskpartition**</span><span class="sxs-lookup"><span data-stu-id="40848-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="40848-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40848-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40848-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Diskpartition")</span><span class="sxs-lookup"><span data-stu-id="40848-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="40848-122">Verweis auf die-Instanz, die die auf dem Laufwerk befindliche Datenträger Partition darstellt.</span><span class="sxs-lookup"><span data-stu-id="40848-122">Reference to the instance representing the disk partition residing on the disk drive.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40848-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40848-123">Remarks</span></span>

<span data-ttu-id="40848-124">Die **Win32-Klasse \_ diskdrivedediskpartition** ist von [**CIM \_ mediapresent**](cim-mediapresent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="40848-124">The **Win32\_DiskDriveToDiskPartition** class is derived from [**CIM\_MediaPresent**](cim-mediapresent.md).</span></span>

<span data-ttu-id="40848-125">Eine Erläuterung zur Verwendung dieser Klasse finden Sie unter [Verwenden von PowerShell zum Zuordnen von Laufwerken und Partitionen](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) und im Blog Artikel [wie kann ich logische Laufwerke und physische Datenträger korrelieren?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) .</span><span class="sxs-lookup"><span data-stu-id="40848-125">For a discussion on how to use this class, see the [Use PowerShell to Map Disk Drives and Partitions](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) and the [How Can I Correlate Logical Drives and Physical Disks?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) blog articles.</span></span>

## <a name="examples"></a><span data-ttu-id="40848-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40848-126">Examples</span></span>

<span data-ttu-id="40848-127">Das PowerShell-Beispiel [Verwenden von PowerShell zum Sammeln von Datenträgern/Partitionen/](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) einstellungspunktinformationen verwendet **Win32 \_ diskdrivedediskpartition** zum Zurückgeben von Informationen zu lokalen Datenträgern/Partitionen und einfügepunkten.</span><span class="sxs-lookup"><span data-stu-id="40848-127">The [Use Powershell to Gather Disk/Partition/Mount Point Information](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) PowerShell sample uses **Win32\_DiskDriveToDiskPartition** to return information about local disks/partitions and mount points.</span></span>

## <a name="requirements"></a><span data-ttu-id="40848-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40848-128">Requirements</span></span>



| <span data-ttu-id="40848-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40848-129">Requirement</span></span> | <span data-ttu-id="40848-130">Wert</span><span class="sxs-lookup"><span data-stu-id="40848-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40848-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40848-131">Minimum supported client</span></span><br/> | <span data-ttu-id="40848-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40848-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40848-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40848-133">Minimum supported server</span></span><br/> | <span data-ttu-id="40848-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40848-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40848-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="40848-135">Namespace</span></span><br/>                | <span data-ttu-id="40848-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="40848-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40848-137">MOF</span><span class="sxs-lookup"><span data-stu-id="40848-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40848-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="40848-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40848-139">DLL</span><span class="sxs-lookup"><span data-stu-id="40848-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40848-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40848-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40848-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40848-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40848-142">**CIM- \_ mediapresent**</span><span class="sxs-lookup"><span data-stu-id="40848-142">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

<span data-ttu-id="40848-143">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="40848-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="40848-144">WMI-Tasks: Datenträger und Dateisysteme</span><span class="sxs-lookup"><span data-stu-id="40848-144">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

