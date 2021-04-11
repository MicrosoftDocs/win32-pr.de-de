---
description: Die \_ WMI-Klasse "Win32 systemoperatingsystem Association" bezieht sich auf ein Computersystem und dessen Betriebssystem.
ms.assetid: dc71f80b-6fbd-4bc8-8783-3922d8050518
ms.tgt_platform: multiple
title: Win32_SystemOperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemOperatingSystem
- Win32_SystemOperatingSystem.PrimaryOS
- Win32_SystemOperatingSystem.GroupComponent
- Win32_SystemOperatingSystem.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba3f8ac94ec882ee1df96da51d93d2c24fde9b3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127609"
---
# <a name="win32_systemoperatingsystem-class"></a><span data-ttu-id="7eeec-103">Win32 \_ systemoperatingsystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="7eeec-103">Win32\_SystemOperatingSystem class</span></span>

<span data-ttu-id="7eeec-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemoperatingsystem** Association" bezieht sich auf ein Computersystem und dessen Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="7eeec-104">The **Win32\_SystemOperatingSystem** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its operating system.</span></span>

<span data-ttu-id="7eeec-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7eeec-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7eeec-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="7eeec-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eeec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7eeec-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemOperatingSystem : CIM_InstalledOS
{
  boolean                   PrimaryOS;
  Win32_ComputerSystem  REF GroupComponent;
  Win32_OperatingSystem REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="7eeec-108">Member</span><span class="sxs-lookup"><span data-stu-id="7eeec-108">Members</span></span>

<span data-ttu-id="7eeec-109">Die **Win32 \_ systemoperatingsystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7eeec-109">The **Win32\_SystemOperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="7eeec-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7eeec-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7eeec-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7eeec-111">Properties</span></span>

<span data-ttu-id="7eeec-112">Die **Win32 \_ systemoperatingsystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7eeec-112">The **Win32\_SystemOperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7eeec-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="7eeec-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eeec-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="7eeec-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="7eeec-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eeec-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eeec-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="7eeec-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="7eeec-117">Ein [**Win32- \_ Computersystem**](win32-computersystemprocessor.md) , das die Eigenschaften des Computer Systems beschreibt, auf dem das Betriebssystem installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7eeec-117">A [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) that describes the properties of the computer system upon which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="7eeec-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7eeec-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eeec-119">Datentyp: **Win32- \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="7eeec-119">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="7eeec-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eeec-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eeec-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")</span><span class="sxs-lookup"><span data-stu-id="7eeec-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="7eeec-122">Ein [**Win32- \_ OperatingSystem**](win32-operatingsystem.md) , das die Eigenschaften des Betriebssystems beschreibt, das auf diesem Computersystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7eeec-122">A [**Win32\_OperatingSystem**](win32-operatingsystem.md) that describes properties of the operating system running on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="7eeec-123">**Primaryos**</span><span class="sxs-lookup"><span data-stu-id="7eeec-123">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eeec-124">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7eeec-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7eeec-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7eeec-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eeec-126">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Betriebs System \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="7eeec-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="7eeec-127">**True** gibt an, dass das installierte Betriebssystem das Standardbetriebssystem für das Computersystem ist.</span><span class="sxs-lookup"><span data-stu-id="7eeec-127">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

<span data-ttu-id="7eeec-128">Diese Eigenschaft wird von [**CIM \_ installedos**](cim-installedos.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7eeec-128">This property is inherited from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7eeec-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7eeec-129">Remarks</span></span>

<span data-ttu-id="7eeec-130">Die **Win32 \_ systemoperatingsystem** -Klasse wird von [**CIM \_ installedos**](cim-installedos.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7eeec-130">The **Win32\_SystemOperatingSystem** class is derived from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7eeec-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7eeec-131">Requirements</span></span>



| <span data-ttu-id="7eeec-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7eeec-132">Requirement</span></span> | <span data-ttu-id="7eeec-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7eeec-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7eeec-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7eeec-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7eeec-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7eeec-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7eeec-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7eeec-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7eeec-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7eeec-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7eeec-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="7eeec-138">Namespace</span></span><br/>                | <span data-ttu-id="7eeec-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7eeec-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7eeec-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7eeec-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7eeec-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7eeec-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7eeec-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7eeec-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eeec-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eeec-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eeec-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7eeec-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eeec-145">**CIM- \_ instanalledos**</span><span class="sxs-lookup"><span data-stu-id="7eeec-145">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dt>

[<span data-ttu-id="7eeec-146">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="7eeec-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
