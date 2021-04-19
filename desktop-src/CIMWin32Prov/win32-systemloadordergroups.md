---
description: Die \_ WMI-Klasse "Win32 systemloadordergroups Association" bezieht sich auf ein Computersystem und eine Gruppe der Lade Reihenfolge.
ms.assetid: fb637300-0f70-465a-a72b-f0ab3f246790
ms.tgt_platform: multiple
title: Win32_SystemLoadOrderGroups-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemLoadOrderGroups
- Win32_SystemLoadOrderGroups.GroupComponent
- Win32_SystemLoadOrderGroups.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 510acfbde2f562493a454abe80a4f7788377e556
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342781"
---
# <a name="win32_systemloadordergroups-class"></a><span data-ttu-id="87bc4-103">Win32 \_ systemloadordergroups-Klasse</span><span class="sxs-lookup"><span data-stu-id="87bc4-103">Win32\_SystemLoadOrderGroups class</span></span>

<span data-ttu-id="87bc4-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemloadordergroups** Association" bezieht sich auf ein Computersystem und eine Gruppe der Lade Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="87bc4-104">The **Win32\_SystemLoadOrderGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a load order group.</span></span>

<span data-ttu-id="87bc4-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="87bc4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="87bc4-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="87bc4-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="87bc4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="87bc4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C503-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemLoadOrderGroups : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_LoadOrderGroup REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="87bc4-108">Member</span><span class="sxs-lookup"><span data-stu-id="87bc4-108">Members</span></span>

<span data-ttu-id="87bc4-109">Die Win32-Klasse " **\_ systemloadordergroups** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="87bc4-109">The **Win32\_SystemLoadOrderGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="87bc4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87bc4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87bc4-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87bc4-111">Properties</span></span>

<span data-ttu-id="87bc4-112">Die **Win32 \_ systemloadordergroups** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="87bc4-112">The **Win32\_SystemLoadOrderGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87bc4-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="87bc4-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87bc4-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="87bc4-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="87bc4-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="87bc4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87bc4-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="87bc4-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="87bc4-117">Verweis auf die-Instanz, die das Computersystem darstellt, auf dem die Lade Auftrags Gruppe vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="87bc4-117">Reference to the instance representing the computer system where the load order group exists.</span></span>

</dd> <dt>

<span data-ttu-id="87bc4-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="87bc4-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87bc4-119">Datentyp: **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="87bc4-119">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="87bc4-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="87bc4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87bc4-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LoadOrderGroup")</span><span class="sxs-lookup"><span data-stu-id="87bc4-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="87bc4-122">Verweis auf die-Instanz, die die auf dem Computersystem vorhandene Gruppe der Lade Reihenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="87bc4-122">Reference to the instance representing the load order group existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87bc4-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87bc4-123">Remarks</span></span>

<span data-ttu-id="87bc4-124">Die **Win32 \_ systemloadordergroups** -Klasse wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="87bc4-124">The **Win32\_SystemLoadOrderGroups** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87bc4-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87bc4-125">Requirements</span></span>



| <span data-ttu-id="87bc4-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87bc4-126">Requirement</span></span> | <span data-ttu-id="87bc4-127">Wert</span><span class="sxs-lookup"><span data-stu-id="87bc4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87bc4-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87bc4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="87bc4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87bc4-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87bc4-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87bc4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="87bc4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87bc4-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87bc4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="87bc4-132">Namespace</span></span><br/>                | <span data-ttu-id="87bc4-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="87bc4-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="87bc4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="87bc4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87bc4-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="87bc4-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="87bc4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="87bc4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87bc4-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87bc4-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87bc4-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87bc4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87bc4-139">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="87bc4-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="87bc4-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="87bc4-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
