---
description: Die \_ WMI-Klasse "Win32 systembootconfiguration Association" bezieht sich auf ein Computersystem und dessen Startkonfiguration.
ms.assetid: 1c6bce81-84d9-4949-92da-6111b4ecc939
ms.tgt_platform: multiple
title: Win32_SystemBootConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBootConfiguration
- Win32_SystemBootConfiguration.Element
- Win32_SystemBootConfiguration.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 863e4103f7e87681e25ccf53679bfe006ed3ff75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861167"
---
# <a name="win32_systembootconfiguration-class"></a><span data-ttu-id="b4add-103">Win32 \_ systembootconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="b4add-103">Win32\_SystemBootConfiguration class</span></span>

<span data-ttu-id="b4add-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systembootconfiguration** Association" bezieht sich auf ein Computersystem und dessen Startkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="b4add-104">The **Win32\_SystemBootConfiguration** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its boot configuration.</span></span>

<span data-ttu-id="b4add-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b4add-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b4add-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="b4add-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4add-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4add-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C507-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBootConfiguration : Win32_SystemSetting
{
  Win32_ComputerSystem    REF Element;
  Win32_BootConfiguration REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="b4add-108">Member</span><span class="sxs-lookup"><span data-stu-id="b4add-108">Members</span></span>

<span data-ttu-id="b4add-109">Die **Win32 \_ systembootconfiguration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b4add-109">The **Win32\_SystemBootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="b4add-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4add-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4add-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4add-111">Properties</span></span>

<span data-ttu-id="b4add-112">Die **Win32 \_ systembootconfiguration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b4add-112">The **Win32\_SystemBootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4add-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b4add-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4add-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="b4add-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b4add-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4add-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4add-116">Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="b4add-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="b4add-117">Verweis auf die Instanz, die das Computersystem mithilfe der Startkonfiguration darstellt.</span><span class="sxs-lookup"><span data-stu-id="b4add-117">Reference to the instance representing the computer system using the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b4add-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="b4add-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4add-119">Datentyp: **Win32- \_ bootconfiguration**</span><span class="sxs-lookup"><span data-stu-id="b4add-119">Data type: **Win32\_BootConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="b4add-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4add-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4add-121">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ bootconfiguration")</span><span class="sxs-lookup"><span data-stu-id="b4add-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BootConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="b4add-122">Verweis auf die-Instanz, die die Startkonfiguration für das Computersystem darstellt.</span><span class="sxs-lookup"><span data-stu-id="b4add-122">Reference to the instance representing the boot configuration for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4add-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4add-123">Remarks</span></span>

<span data-ttu-id="b4add-124">Die **Win32 \_ systembootconfiguration** -Klasse wird von [**Win32 \_ systemsetting**](win32-systemsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b4add-124">The **Win32\_SystemBootConfiguration** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4add-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4add-125">Requirements</span></span>



| <span data-ttu-id="b4add-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4add-126">Requirement</span></span> | <span data-ttu-id="b4add-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b4add-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4add-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4add-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b4add-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4add-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4add-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4add-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b4add-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4add-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4add-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4add-132">Namespace</span></span><br/>                | <span data-ttu-id="b4add-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b4add-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b4add-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b4add-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4add-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b4add-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4add-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b4add-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4add-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4add-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4add-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4add-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4add-139">**Win32- \_ systemsetting**</span><span class="sxs-lookup"><span data-stu-id="b4add-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="b4add-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="b4add-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
