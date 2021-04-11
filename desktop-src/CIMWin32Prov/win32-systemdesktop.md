---
description: Die \_ WMI-Klasse der Win32 Systemdesktop Association bezieht sich auf ein Computersystem und dessen Desktop Konfiguration.
ms.assetid: 2b024660-d707-4463-8207-73df74bfa7d6
ms.tgt_platform: multiple
title: Win32_SystemDesktop-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDesktop
- Win32_SystemDesktop.Element
- Win32_SystemDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e14cab58a445fd645b9d59c1aea713bf6c40ac0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958572"
---
# <a name="win32_systemdesktop-class"></a><span data-ttu-id="5dd61-103">Win32 \_ Systemdesktop-Klasse</span><span class="sxs-lookup"><span data-stu-id="5dd61-103">Win32\_SystemDesktop class</span></span>

<span data-ttu-id="5dd61-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32 \_ Systemdesktop** Association bezieht sich auf ein Computersystem und dessen Desktop Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5dd61-104">The **Win32\_SystemDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its desktop configuration.</span></span>

<span data-ttu-id="5dd61-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5dd61-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5dd61-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="5dd61-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd61-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dd61-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C506-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDesktop : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_Desktop        REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="5dd61-108">Member</span><span class="sxs-lookup"><span data-stu-id="5dd61-108">Members</span></span>

<span data-ttu-id="5dd61-109">Die **Win32- \_ Systemdesktop-** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5dd61-109">The **Win32\_SystemDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="5dd61-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5dd61-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5dd61-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5dd61-111">Properties</span></span>

<span data-ttu-id="5dd61-112">Die **Win32 \_ Systemdesktop-** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5dd61-112">The **Win32\_SystemDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5dd61-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5dd61-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dd61-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="5dd61-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="5dd61-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5dd61-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dd61-116">Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="5dd61-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="5dd61-117">Verweis auf die-Instanz, die das Computersystem darstellt, auf dem die Desktop Konfiguration vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5dd61-117">Reference to the instance representing the computer system where the desktop configuration exists.</span></span>

</dd> <dt>

<span data-ttu-id="5dd61-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="5dd61-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dd61-119">Datentyp: **Win32 \_ -Desktop**</span><span class="sxs-lookup"><span data-stu-id="5dd61-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="5dd61-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5dd61-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dd61-121">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Desktop")</span><span class="sxs-lookup"><span data-stu-id="5dd61-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="5dd61-122">Verweis auf die-Instanz, die die auf dem Computersystem vorhandene Konfiguration darstellt.</span><span class="sxs-lookup"><span data-stu-id="5dd61-122">Reference to the instance representing the configuration existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dd61-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5dd61-123">Remarks</span></span>

<span data-ttu-id="5dd61-124">Die **Win32- \_ Systemdesktop-** Klasse wird von [**Win32 \_ systemsetting**](win32-systemsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5dd61-124">The **Win32\_SystemDesktop** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5dd61-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5dd61-125">Requirements</span></span>



| <span data-ttu-id="5dd61-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5dd61-126">Requirement</span></span> | <span data-ttu-id="5dd61-127">Wert</span><span class="sxs-lookup"><span data-stu-id="5dd61-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd61-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5dd61-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5dd61-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5dd61-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5dd61-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5dd61-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5dd61-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dd61-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5dd61-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="5dd61-132">Namespace</span></span><br/>                | <span data-ttu-id="5dd61-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5dd61-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5dd61-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5dd61-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5dd61-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5dd61-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5dd61-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5dd61-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dd61-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dd61-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dd61-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dd61-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd61-139">**Win32- \_ systemsetting**</span><span class="sxs-lookup"><span data-stu-id="5dd61-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="5dd61-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="5dd61-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
