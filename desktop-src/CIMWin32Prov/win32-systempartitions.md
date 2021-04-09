---
description: Die \_ WMI-Klasse Win32 systempartitions Association verknüpft ein Computersystem und eine Datenträger Partition auf diesem System.
ms.assetid: e8f02cd0-9446-4258-b476-5dc6c72c80d4
ms.tgt_platform: multiple
title: Win32_SystemPartitions-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemPartitions
- Win32_SystemPartitions.GroupComponent
- Win32_SystemPartitions.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deae8129772e5d854f05b5b953ec66a12bd5bcaf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861163"
---
# <a name="win32_systempartitions-class"></a><span data-ttu-id="4576c-103">Win32 \_ systempartitions-Klasse</span><span class="sxs-lookup"><span data-stu-id="4576c-103">Win32\_SystemPartitions class</span></span>

<span data-ttu-id="4576c-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ systempartitions** Association verknüpft ein Computersystem und eine Datenträger Partition auf diesem System.</span><span class="sxs-lookup"><span data-stu-id="4576c-104">The **Win32\_SystemPartitions** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a disk partition on that system.</span></span>

<span data-ttu-id="4576c-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4576c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4576c-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4576c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4576c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4576c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemPartitions : Win32_SystemDevices
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_DiskPartition  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="4576c-108">Member</span><span class="sxs-lookup"><span data-stu-id="4576c-108">Members</span></span>

<span data-ttu-id="4576c-109">Die **Win32 \_ systempartitions** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4576c-109">The **Win32\_SystemPartitions** class has these types of members:</span></span>

-   [<span data-ttu-id="4576c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4576c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4576c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4576c-111">Properties</span></span>

<span data-ttu-id="4576c-112">Die **Win32 \_ systempartitions** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4576c-112">The **Win32\_SystemPartitions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4576c-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4576c-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4576c-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="4576c-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4576c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4576c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4576c-116">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="4576c-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="4576c-117">Verweis auf die-Instanz, die die Eigenschaften des Computer Systems darstellt, in dem sich die Datenträger Partition befindet.</span><span class="sxs-lookup"><span data-stu-id="4576c-117">Reference to the instance representing the properties of the computer system where the disk partition is located.</span></span>

</dd> <dt>

<span data-ttu-id="4576c-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4576c-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4576c-119">Datentyp: **Win32 \_ Diskpartition**</span><span class="sxs-lookup"><span data-stu-id="4576c-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="4576c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4576c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4576c-121">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Diskpartition")</span><span class="sxs-lookup"><span data-stu-id="4576c-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="4576c-122">Verweis auf die-Instanz, die die Eigenschaften einer Datenträger Partition darstellt, die auf dem Computersystem vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4576c-122">Reference to the instance representing the properties of a disk partition that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4576c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4576c-123">Remarks</span></span>

<span data-ttu-id="4576c-124">Die **Win32 \_ systempartitions** -Klasse wird von [**Win32 \_ systemdevices**](win32-systemdevices.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4576c-124">The **Win32\_SystemPartitions** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4576c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4576c-125">Requirements</span></span>



| <span data-ttu-id="4576c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4576c-126">Requirement</span></span> | <span data-ttu-id="4576c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="4576c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4576c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4576c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4576c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4576c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4576c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4576c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4576c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4576c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4576c-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="4576c-132">Namespace</span></span><br/>                | <span data-ttu-id="4576c-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4576c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4576c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="4576c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4576c-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4576c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4576c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4576c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4576c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4576c-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4576c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4576c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4576c-139">**Win32- \_ Systemgeräte**</span><span class="sxs-lookup"><span data-stu-id="4576c-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

[<span data-ttu-id="4576c-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="4576c-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
