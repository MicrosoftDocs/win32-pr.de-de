---
description: Die \_ WMI-Klasse "Win32 Systembios Association" bezieht sich auf ein Computersystem (einschließlich Daten wie Starteigenschaften, Zeitzonen, Start Konfigurationen oder Administrator Kennwörter) und ein System-BIOS (Dienste, Sprachen und System Verwaltungs Eigenschaften).
ms.assetid: 92747b1b-ef28-40ab-868a-6755aee8c723
ms.tgt_platform: multiple
title: Win32_SystemBIOS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBIOS
- Win32_SystemBIOS.PartComponent
- Win32_SystemBIOS.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc8ec1f3526e2faefe0e63c9dea357accd025c13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861575"
---
# <a name="win32_systembios-class"></a><span data-ttu-id="9764e-103">Win32- \_ Systembios-Klasse</span><span class="sxs-lookup"><span data-stu-id="9764e-103">Win32\_SystemBIOS class</span></span>

<span data-ttu-id="9764e-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ Systembios** Association" bezieht sich auf ein Computersystem (einschließlich Daten wie Starteigenschaften, Zeitzonen, Start Konfigurationen oder Administrator Kennwörter) und ein System-BIOS (Dienste, Sprachen und System Verwaltungs Eigenschaften).</span><span class="sxs-lookup"><span data-stu-id="9764e-104">The **Win32\_SystemBIOS** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system (including data such as startup properties, time zones, boot configurations, or administrative passwords), and a system BIOS (services, languages, and system management properties).</span></span>

<span data-ttu-id="9764e-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9764e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9764e-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9764e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9764e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9764e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBIOS : CIM_SystemComponent
{
  Win32_BIOS           REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="9764e-108">Member</span><span class="sxs-lookup"><span data-stu-id="9764e-108">Members</span></span>

<span data-ttu-id="9764e-109">Die **Win32- \_ Systembios** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9764e-109">The **Win32\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="9764e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9764e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9764e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9764e-111">Properties</span></span>

<span data-ttu-id="9764e-112">Die **Win32- \_ Systembios** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9764e-112">The **Win32\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9764e-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9764e-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9764e-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="9764e-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="9764e-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9764e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9764e-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="9764e-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="9764e-117">Das [**Win32- \_ Computersystem**](win32-computersystemprocessor.md) , das das BIOS der Zuordnung enthält.</span><span class="sxs-lookup"><span data-stu-id="9764e-117">The [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) containing the BIOS of the association.</span></span>

</dd> <dt>

<span data-ttu-id="9764e-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9764e-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9764e-119">Datentyp: **Win32- \_ BIOS**</span><span class="sxs-lookup"><span data-stu-id="9764e-119">Data type: **Win32\_BIOS**</span></span>
</dt> <dt>

<span data-ttu-id="9764e-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9764e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9764e-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ BIOS")</span><span class="sxs-lookup"><span data-stu-id="9764e-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BIOS")</span></span>
</dt> </dl>

<span data-ttu-id="9764e-122">Ein [**Win32- \_ BIOS**](win32-bios.md) , das im Computersystem dieser Zuordnung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9764e-122">A [**Win32\_BIOS**](win32-bios.md) contained in the computer system of this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9764e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9764e-123">Remarks</span></span>

<span data-ttu-id="9764e-124">Die **Win32- \_ Systembios** -Klasse wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9764e-124">The **Win32\_SystemBIOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9764e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9764e-125">Requirements</span></span>



| <span data-ttu-id="9764e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9764e-126">Requirement</span></span> | <span data-ttu-id="9764e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9764e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9764e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9764e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9764e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9764e-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9764e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9764e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9764e-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9764e-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9764e-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="9764e-132">Namespace</span></span><br/>                | <span data-ttu-id="9764e-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9764e-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9764e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9764e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9764e-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9764e-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9764e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9764e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9764e-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9764e-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9764e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9764e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9764e-139">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="9764e-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="9764e-140">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="9764e-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
