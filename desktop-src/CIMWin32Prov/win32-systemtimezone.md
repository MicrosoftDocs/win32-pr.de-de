---
description: Die \_ WMI-Klasse "Win32 systemtimezone Association" bezieht sich auf ein Computersystem und eine Zeitzone.
ms.assetid: 53c74a61-c91d-4daa-933e-4cc7b9583d98
ms.tgt_platform: multiple
title: Win32_SystemTimeZone-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemTimeZone
- Win32_SystemTimeZone.Element
- Win32_SystemTimeZone.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ec294600fdc81f085bf29f5e664bcbec961417c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861156"
---
# <a name="win32_systemtimezone-class"></a><span data-ttu-id="1141e-103">Win32 \_ systemtimezone-Klasse</span><span class="sxs-lookup"><span data-stu-id="1141e-103">Win32\_SystemTimeZone class</span></span>

<span data-ttu-id="1141e-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemtimezone** Association" bezieht sich auf ein Computersystem und eine Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="1141e-104">The **Win32\_SystemTimeZone** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a time zone.</span></span>

<span data-ttu-id="1141e-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1141e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1141e-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="1141e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1141e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1141e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C504-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemTimeZone : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_TimeZone       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="1141e-108">Member</span><span class="sxs-lookup"><span data-stu-id="1141e-108">Members</span></span>

<span data-ttu-id="1141e-109">Die **Win32- \_ systemtimezone** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1141e-109">The **Win32\_SystemTimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="1141e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1141e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1141e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1141e-111">Properties</span></span>

<span data-ttu-id="1141e-112">Die **Win32- \_ systemtimezone** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1141e-112">The **Win32\_SystemTimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1141e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1141e-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1141e-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="1141e-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="1141e-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1141e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1141e-116">Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="1141e-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="1141e-117">Verweis auf die-Instanz, die das Computersystem darstellt, das die Zeitzone des Systems nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="1141e-117">Reference to the instance representing the computer system keeping track of the system time zone.</span></span>

</dd> <dt>

<span data-ttu-id="1141e-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="1141e-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1141e-119">Datentyp: **Win32- \_ Zeitzone**</span><span class="sxs-lookup"><span data-stu-id="1141e-119">Data type: **Win32\_TimeZone**</span></span>
</dt> <dt>

<span data-ttu-id="1141e-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1141e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1141e-121">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ TimeZone")</span><span class="sxs-lookup"><span data-stu-id="1141e-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_TimeZone")</span></span>
</dt> </dl>

<span data-ttu-id="1141e-122">Verweis auf die-Instanz, die die vom Computersystem nach verfolgten Zeit Zonen Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="1141e-122">Reference to the instance representing the time zone properties tracked by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1141e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1141e-123">Remarks</span></span>

<span data-ttu-id="1141e-124">Die **Win32- \_ systemtimezone** -Klasse wird von [**Win32 \_ systemsetting**](win32-systemsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1141e-124">The **Win32\_SystemTimeZone** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1141e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1141e-125">Requirements</span></span>



| <span data-ttu-id="1141e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1141e-126">Requirement</span></span> | <span data-ttu-id="1141e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1141e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1141e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1141e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1141e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1141e-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1141e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1141e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1141e-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1141e-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1141e-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="1141e-132">Namespace</span></span><br/>                | <span data-ttu-id="1141e-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1141e-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1141e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1141e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1141e-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1141e-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1141e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1141e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1141e-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1141e-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1141e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1141e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1141e-139">**Win32- \_ systemsetting**</span><span class="sxs-lookup"><span data-stu-id="1141e-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="1141e-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="1141e-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
