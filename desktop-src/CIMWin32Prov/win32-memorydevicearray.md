---
description: Die \_ WMI-Klasse der Win32 memorydevicearray-Zuordnung verknüpft ein Speichergerät und das Speicher Array, in dem es sich befindet.
ms.assetid: 39ea6333-2352-488b-99e4-97594bea7dcd
ms.tgt_platform: multiple
title: Win32_MemoryDeviceArray-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceArray
- Win32_MemoryDeviceArray.GroupComponent
- Win32_MemoryDeviceArray.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e527f77183c3bdc09d464f6fed4808e45adefa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860696"
---
# <a name="win32_memorydevicearray-class"></a><span data-ttu-id="92b7c-103">Win32 \_ memorydevicearray-Klasse</span><span class="sxs-lookup"><span data-stu-id="92b7c-103">Win32\_MemoryDeviceArray class</span></span>

<span data-ttu-id="92b7c-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) der **Win32 \_ memorydevicearray** -Zuordnung verknüpft ein Speichergerät und das Speicher Array, in dem es sich befindet.</span><span class="sxs-lookup"><span data-stu-id="92b7c-104">The **Win32\_MemoryDeviceArray** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the memory array in which it resides.</span></span>

<span data-ttu-id="92b7c-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92b7c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="92b7c-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="92b7c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b7c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="92b7c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF563-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryDeviceArray : CIM_Component
{
  Win32_MemoryArray  REF GroupComponent;
  Win32_MemoryDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="92b7c-108">Member</span><span class="sxs-lookup"><span data-stu-id="92b7c-108">Members</span></span>

<span data-ttu-id="92b7c-109">Die **Win32 \_ memorydevicearray** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="92b7c-109">The **Win32\_MemoryDeviceArray** class has these types of members:</span></span>

-   [<span data-ttu-id="92b7c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92b7c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92b7c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92b7c-111">Properties</span></span>

<span data-ttu-id="92b7c-112">Die **Win32 \_ memorydevicearray** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92b7c-112">The **Win32\_MemoryDeviceArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92b7c-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="92b7c-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92b7c-114">Datentyp: **Win32 \_ memoryarray**</span><span class="sxs-lookup"><span data-stu-id="92b7c-114">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="92b7c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92b7c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92b7c-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ memoryarray")</span><span class="sxs-lookup"><span data-stu-id="92b7c-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="92b7c-117">Ein [**Win32 \_ memoryarray**](win32-memoryarray.md) , das den Speicher Array Teil der Win32- \_ memorydevicearray-Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="92b7c-117">A [**Win32\_MemoryArray**](win32-memoryarray.md) that represents the memory array part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> <dt>

<span data-ttu-id="92b7c-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="92b7c-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92b7c-119">Datentyp: **Win32 \_ memorydevice**</span><span class="sxs-lookup"><span data-stu-id="92b7c-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="92b7c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92b7c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92b7c-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ memorydevice")</span><span class="sxs-lookup"><span data-stu-id="92b7c-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="92b7c-122">Ein [**Win32- \_ memorydevice**](win32-memorydevice.md) , das einen Teil des Speichergeräts der Win32- \_ memorydevicearray-Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="92b7c-122">A [**Win32\_MemoryDevice**](win32-memorydevice.md) that represents a memory device part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92b7c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92b7c-123">Remarks</span></span>

<span data-ttu-id="92b7c-124">Die **Win32-Klasse \_ memorydevicearray** wird von der [**CIM- \_ Komponente**](cim-component.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="92b7c-124">The **Win32\_MemoryDeviceArray** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="92b7c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92b7c-125">Requirements</span></span>



| <span data-ttu-id="92b7c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92b7c-126">Requirement</span></span> | <span data-ttu-id="92b7c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="92b7c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92b7c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92b7c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="92b7c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92b7c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92b7c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92b7c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="92b7c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92b7c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92b7c-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="92b7c-132">Namespace</span></span><br/>                | <span data-ttu-id="92b7c-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="92b7c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="92b7c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="92b7c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92b7c-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="92b7c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="92b7c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="92b7c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92b7c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92b7c-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92b7c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92b7c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b7c-139">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="92b7c-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="92b7c-140">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="92b7c-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

