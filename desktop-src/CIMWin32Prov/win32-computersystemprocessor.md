---
description: Die \_ WMI-Klasse "Win32 computersystemprocessor Association" bezieht sich auf ein Computersystem und einen Prozessor, der auf dem System ausgeführt wird.
ms.assetid: e630ebea-19bf-43c7-a8a0-7acfda3a752b
ms.tgt_platform: multiple
title: Win32_ComputerSystemProcessor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProcessor
- Win32_ComputerSystemProcessor.PartComponent
- Win32_ComputerSystemProcessor.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f836d8f5e9053029763c38d2c4f2116987b08fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126271"
---
# <a name="win32_computersystemprocessor-class"></a><span data-ttu-id="5d65b-103">Win32 \_ computersystemprocessor-Klasse</span><span class="sxs-lookup"><span data-stu-id="5d65b-103">Win32\_ComputerSystemProcessor class</span></span>

<span data-ttu-id="5d65b-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ computersystemprocessor** Association" bezieht sich auf ein Computersystem und einen Prozessor, der auf dem System ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d65b-104">The **Win32\_ComputerSystemProcessor** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a computer system and a processor running on that system.</span></span>

<span data-ttu-id="5d65b-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5d65b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5d65b-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5d65b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d65b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d65b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{719A6839-C124-11d2-85E8-0000F8102E5F}"), AMENDMENT]
class Win32_ComputerSystemProcessor : Win32_SystemDevices
{
  Win32_Processor      REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="5d65b-108">Member</span><span class="sxs-lookup"><span data-stu-id="5d65b-108">Members</span></span>

<span data-ttu-id="5d65b-109">Die **Win32 \_ computersystemprocessor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5d65b-109">The **Win32\_ComputerSystemProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="5d65b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d65b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d65b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d65b-111">Properties</span></span>

<span data-ttu-id="5d65b-112">Die **Win32 \_ computersystemprocessor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5d65b-112">The **Win32\_ComputerSystemProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d65b-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="5d65b-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d65b-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="5d65b-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="5d65b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5d65b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d65b-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="5d65b-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="5d65b-117">Ein **Win32- \_ Computersystem** , das die Eigenschaften des Computer Systems beschreibt, auf dem der Prozessor ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d65b-117">A **Win32\_ComputerSystem** that describes the properties of the computer system on which the processor is running.</span></span>

</dd> <dt>

<span data-ttu-id="5d65b-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="5d65b-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d65b-119">Datentyp: **Win32- \_ Prozessor**</span><span class="sxs-lookup"><span data-stu-id="5d65b-119">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="5d65b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5d65b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d65b-121">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Processor")</span><span class="sxs-lookup"><span data-stu-id="5d65b-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="5d65b-122">Ein [**Win32- \_ Prozessor**](win32-processor.md) , der die Eigenschaften eines Prozessors beschreibt, auf dem das Computersystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d65b-122">A [**Win32\_Processor**](win32-processor.md) that describes the properties of a processor which is running the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d65b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d65b-123">Remarks</span></span>

<span data-ttu-id="5d65b-124">Die **Win32 \_ computersystemprocessor** -Klasse wird von [**Win32 \_ systemdevices**](win32-systemdevices.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5d65b-124">The **Win32\_ComputerSystemProcessor** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d65b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d65b-125">Requirements</span></span>



| <span data-ttu-id="5d65b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d65b-126">Requirement</span></span> | <span data-ttu-id="5d65b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="5d65b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d65b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d65b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5d65b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d65b-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d65b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d65b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5d65b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d65b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d65b-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d65b-132">Namespace</span></span><br/>                | <span data-ttu-id="5d65b-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5d65b-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d65b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5d65b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d65b-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5d65b-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d65b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5d65b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d65b-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d65b-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d65b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d65b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d65b-139">**Win32- \_ Systemgeräte**</span><span class="sxs-lookup"><span data-stu-id="5d65b-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

<span data-ttu-id="5d65b-140">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5d65b-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

