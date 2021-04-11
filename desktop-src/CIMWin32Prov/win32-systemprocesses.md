---
description: Die \_ WMI-Klasse Win32 systemprocesses Association bezieht sich auf ein Computersystem und einen Prozess, der auf diesem System ausgeführt wird.
ms.assetid: 0d8c3ec6-265e-4486-8e94-f5acd2845cf5
ms.tgt_platform: multiple
title: Win32_SystemProcesses-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProcesses
- Win32_SystemProcesses.GroupComponent
- Win32_SystemProcesses.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b963aea5d9c651e27dc4380200e40dd3dcb9a77
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041439"
---
# <a name="win32_systemprocesses-class"></a><span data-ttu-id="21619-103">Win32 \_ systemprocesses-Klasse</span><span class="sxs-lookup"><span data-stu-id="21619-103">Win32\_SystemProcesses class</span></span>

<span data-ttu-id="21619-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ systemprocesses** Association bezieht sich auf ein Computersystem und einen Prozess, der auf diesem System ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21619-104">The **Win32\_SystemProcesses** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a process running on that system.</span></span>

<span data-ttu-id="21619-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="21619-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="21619-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="21619-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="21619-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="21619-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProcesses : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Process        REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="21619-108">Member</span><span class="sxs-lookup"><span data-stu-id="21619-108">Members</span></span>

<span data-ttu-id="21619-109">Die **Win32 \_ systemprocesses** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="21619-109">The **Win32\_SystemProcesses** class has these types of members:</span></span>

-   [<span data-ttu-id="21619-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21619-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21619-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21619-111">Properties</span></span>

<span data-ttu-id="21619-112">Die **Win32 \_ systemprocesses** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="21619-112">The **Win32\_SystemProcesses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21619-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="21619-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21619-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="21619-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="21619-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21619-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21619-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="21619-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="21619-117">Verweis auf die-Instanz, die das Computersystem darstellt, auf dem der Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21619-117">Reference to the instance representing the computer system upon which the process is running.</span></span>

</dd> <dt>

<span data-ttu-id="21619-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="21619-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21619-119">Datentyp: **Win32- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="21619-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="21619-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21619-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21619-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32- \_ Prozess")</span><span class="sxs-lookup"><span data-stu-id="21619-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Process")</span></span>
</dt> </dl>

<span data-ttu-id="21619-122">Verweis auf die-Instanz, die den auf dem Computersystem laufenden Prozess darstellt.</span><span class="sxs-lookup"><span data-stu-id="21619-122">Reference to the instance representing the process running on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21619-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21619-123">Remarks</span></span>

<span data-ttu-id="21619-124">Die **Win32 \_ systemprocesses** -Klasse wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="21619-124">The **Win32\_SystemProcesses** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21619-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21619-125">Requirements</span></span>



| <span data-ttu-id="21619-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21619-126">Requirement</span></span> | <span data-ttu-id="21619-127">Wert</span><span class="sxs-lookup"><span data-stu-id="21619-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21619-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21619-128">Minimum supported client</span></span><br/> | <span data-ttu-id="21619-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21619-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21619-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21619-130">Minimum supported server</span></span><br/> | <span data-ttu-id="21619-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21619-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21619-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="21619-132">Namespace</span></span><br/>                | <span data-ttu-id="21619-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="21619-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="21619-134">MOF</span><span class="sxs-lookup"><span data-stu-id="21619-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21619-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="21619-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="21619-136">DLL</span><span class="sxs-lookup"><span data-stu-id="21619-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21619-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21619-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21619-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21619-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21619-139">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="21619-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="21619-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="21619-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
