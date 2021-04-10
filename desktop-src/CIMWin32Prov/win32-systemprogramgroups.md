---
description: Die \_ WMI-Klasse "Win32 systemprogramgroups Association" bezieht sich auf ein Computersystem und eine logische Programmgruppe.
ms.assetid: cbf810c8-a967-4d60-889c-e47c43b039ea
ms.tgt_platform: multiple
title: Win32_SystemProgramGroups-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProgramGroups
- Win32_SystemProgramGroups.Element
- Win32_SystemProgramGroups.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1a8ca556c24295e2c4b04ab851610ef35ec9b715
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127596"
---
# <a name="win32_systemprogramgroups-class"></a><span data-ttu-id="5ecd4-103">Win32 \_ System Program Groups-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ecd4-103">Win32\_SystemProgramGroups class</span></span>

<span data-ttu-id="5ecd4-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemprogramgroups** Association" bezieht sich auf ein Computersystem und eine logische Programmgruppe.</span><span class="sxs-lookup"><span data-stu-id="5ecd4-104">The **Win32\_SystemProgramGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical program group.</span></span>

<span data-ttu-id="5ecd4-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5ecd4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5ecd4-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="5ecd4-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ecd4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ecd4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C505-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProgramGroups : Win32_SystemSetting
{
  Win32_ComputerSystem      REF Element;
  Win32_LogicalProgramGroup REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="5ecd4-108">Member</span><span class="sxs-lookup"><span data-stu-id="5ecd4-108">Members</span></span>

<span data-ttu-id="5ecd4-109">Die **Win32-Klasse \_ System Program Groups** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5ecd4-109">The **Win32\_SystemProgramGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="5ecd4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ecd4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ecd4-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ecd4-111">Properties</span></span>

<span data-ttu-id="5ecd4-112">Die **Win32-Klasse \_ System Program Groups** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5ecd4-112">The **Win32\_SystemProgramGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ecd4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5ecd4-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecd4-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="5ecd4-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="5ecd4-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5ecd4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecd4-116">Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="5ecd4-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="5ecd4-117">Verweis auf die-Instanz, die das Computersystem darstellt, das die logische Programmgruppe enthält.</span><span class="sxs-lookup"><span data-stu-id="5ecd4-117">Reference to the instance representing the computer system containing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="5ecd4-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="5ecd4-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecd4-119">Datentyp: **Win32 \_ logicalprogramgroup**</span><span class="sxs-lookup"><span data-stu-id="5ecd4-119">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="5ecd4-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5ecd4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ecd4-121">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ logicalprogramgroup")</span><span class="sxs-lookup"><span data-stu-id="5ecd4-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="5ecd4-122">Verweis auf die-Instanz, die die logische Programmgruppe auf dem Computersystem darstellt.</span><span class="sxs-lookup"><span data-stu-id="5ecd4-122">Reference to the instance representing the logical program group on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ecd4-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ecd4-123">Remarks</span></span>

<span data-ttu-id="5ecd4-124">Die **Win32-Klasse \_ System Program Groups** wird von [**Win32 \_ systemsetting**](win32-systemsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5ecd4-124">The **Win32\_SystemProgramGroups** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ecd4-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ecd4-125">Requirements</span></span>



| <span data-ttu-id="5ecd4-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ecd4-126">Requirement</span></span> | <span data-ttu-id="5ecd4-127">Wert</span><span class="sxs-lookup"><span data-stu-id="5ecd4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ecd4-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ecd4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5ecd4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ecd4-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ecd4-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ecd4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5ecd4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ecd4-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ecd4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ecd4-132">Namespace</span></span><br/>                | <span data-ttu-id="5ecd4-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5ecd4-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ecd4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5ecd4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ecd4-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5ecd4-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ecd4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5ecd4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ecd4-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ecd4-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ecd4-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ecd4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ecd4-139">**Win32- \_ systemsetting**</span><span class="sxs-lookup"><span data-stu-id="5ecd4-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="5ecd4-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="5ecd4-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
