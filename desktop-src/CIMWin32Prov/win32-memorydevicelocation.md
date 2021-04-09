---
description: Die \_ WMI-Klasse "Win32 memorydevicelocation Association" verknüpft ein Speichergerät und den physischen Speicher, in dem es vorhanden ist.
ms.assetid: 6fef916e-44e2-4b9f-94b7-c7204259004a
ms.tgt_platform: multiple
title: Win32_MemoryDeviceLocation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceLocation
- Win32_MemoryDeviceLocation.Dependent
- Win32_MemoryDeviceLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5cf1ba93a2574810892443aefa43e1c7c501636c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958230"
---
# <a name="win32_memorydevicelocation-class"></a><span data-ttu-id="f25cb-103">Win32 \_ memorydeviceloationklasse</span><span class="sxs-lookup"><span data-stu-id="f25cb-103">Win32\_MemoryDeviceLocation class</span></span>

<span data-ttu-id="f25cb-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ memorydevicelocation** Association" verknüpft ein Speichergerät und den physischen Speicher, in dem es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f25cb-104">The **Win32\_MemoryDeviceLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the physical memory on which it exists.</span></span>

<span data-ttu-id="f25cb-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f25cb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f25cb-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f25cb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f25cb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f25cb-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDeviceLocation : CIM_Realizes
{
  Win32_MemoryDevice   REF Dependent;
  Win32_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f25cb-108">Member</span><span class="sxs-lookup"><span data-stu-id="f25cb-108">Members</span></span>

<span data-ttu-id="f25cb-109">Die **Win32-Klasse \_ memorydevicelokation** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f25cb-109">The **Win32\_MemoryDeviceLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="f25cb-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f25cb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f25cb-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f25cb-111">Properties</span></span>

<span data-ttu-id="f25cb-112">Die **Win32-Klasse \_ memorydevicelokation** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f25cb-112">The **Win32\_MemoryDeviceLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f25cb-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="f25cb-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f25cb-114">Datentyp: **Win32 \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="f25cb-114">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="f25cb-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f25cb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f25cb-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemory")</span><span class="sxs-lookup"><span data-stu-id="f25cb-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="f25cb-117">Ein [**Win32- \_ PhysicalMemory**](win32-physicalmemory.md) , der den physischen Speicher darstellt, der das Speichergerät enthält.</span><span class="sxs-lookup"><span data-stu-id="f25cb-117">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory containing the memory device.</span></span>

</dd> <dt>

<span data-ttu-id="f25cb-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="f25cb-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f25cb-119">Datentyp: **Win32 \_ memorydevice**</span><span class="sxs-lookup"><span data-stu-id="f25cb-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="f25cb-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f25cb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f25cb-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ memorydevice")</span><span class="sxs-lookup"><span data-stu-id="f25cb-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="f25cb-122">Ein **Win32 \_ memorydevicelokation** , das das im physischen Speicher vorhandene Speichergerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="f25cb-122">A **Win32\_MemoryDeviceLocation** that represents the memory device existing in the physical memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f25cb-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f25cb-123">Remarks</span></span>

<span data-ttu-id="f25cb-124">Die **Win32-Klasse \_ memorydeviceloationist** von [**CIM \_**](cim-realizes.md)-erkennen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f25cb-124">The **Win32\_MemoryDeviceLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f25cb-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f25cb-125">Requirements</span></span>



| <span data-ttu-id="f25cb-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f25cb-126">Requirement</span></span> | <span data-ttu-id="f25cb-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f25cb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f25cb-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f25cb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f25cb-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f25cb-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f25cb-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f25cb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f25cb-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f25cb-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f25cb-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f25cb-132">Namespace</span></span><br/>                | <span data-ttu-id="f25cb-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f25cb-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f25cb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f25cb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f25cb-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f25cb-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f25cb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f25cb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f25cb-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f25cb-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f25cb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f25cb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f25cb-139">**CIM \_ erkennt**</span><span class="sxs-lookup"><span data-stu-id="f25cb-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="f25cb-140">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="f25cb-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

