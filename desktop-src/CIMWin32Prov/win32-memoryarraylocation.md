---
description: Die \_ WMI-Klasse "Win32 memoryarraylocation Association" verknüpft ein Array Logischer Speicher und das Array physischer Speicher, auf dem es vorhanden ist.
ms.assetid: 455daeee-ad67-4599-84d6-fa3f4ac593aa
ms.tgt_platform: multiple
title: Win32_MemoryArrayLocation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArrayLocation
- Win32_MemoryArrayLocation.Dependent
- Win32_MemoryArrayLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62aae3bf672b12bdb947ff8ce6b76f919eaa11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524104"
---
# <a name="win32_memoryarraylocation-class"></a><span data-ttu-id="66264-103">Win32 \_ memoryarraylocation-Klasse</span><span class="sxs-lookup"><span data-stu-id="66264-103">Win32\_MemoryArrayLocation class</span></span>

<span data-ttu-id="66264-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ memoryarraylocation** Association" verknüpft ein Array Logischer Speicher und das Array physischer Speicher, auf dem es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="66264-104">The **Win32\_MemoryArrayLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical memory array and the physical memory array on which it exists.</span></span>

<span data-ttu-id="66264-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="66264-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="66264-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="66264-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="66264-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="66264-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF561-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryArrayLocation : CIM_Realizes
{
  Win32_MemoryArray         REF Dependent;
  Win32_PhysicalMemoryArray REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="66264-108">Member</span><span class="sxs-lookup"><span data-stu-id="66264-108">Members</span></span>

<span data-ttu-id="66264-109">Die **Win32 \_ memoryarraylocation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="66264-109">The **Win32\_MemoryArrayLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="66264-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66264-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66264-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66264-111">Properties</span></span>

<span data-ttu-id="66264-112">Die **Win32 \_ memoryarraylocation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="66264-112">The **Win32\_MemoryArrayLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66264-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="66264-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66264-114">Datentyp: **Win32 \_ physicalmemoryarray**</span><span class="sxs-lookup"><span data-stu-id="66264-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="66264-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="66264-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66264-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ physicalmemoryarray")</span><span class="sxs-lookup"><span data-stu-id="66264-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="66264-117">Ein [**Win32 \_ physicalmemoryarray**](win32-physicalmemoryarray.md) , das das Array des physischen Speichers beschreibt, das das logische Speicher Array implementiert.</span><span class="sxs-lookup"><span data-stu-id="66264-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that describes the physical memory array that implements the logical memory array.</span></span>

</dd> <dt>

<span data-ttu-id="66264-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="66264-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66264-119">Datentyp: **Win32 \_ memoryarray**</span><span class="sxs-lookup"><span data-stu-id="66264-119">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="66264-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="66264-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66264-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ memoryarray")</span><span class="sxs-lookup"><span data-stu-id="66264-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="66264-122">Ein [**Win32 \_ memoryarray**](win32-memoryarray.md) , das das vom physischen Speicher Array implementierte logische Speicher Array beschreibt.</span><span class="sxs-lookup"><span data-stu-id="66264-122">A [**Win32\_MemoryArray**](win32-memoryarray.md) that describes the logical memory array implemented by the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66264-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66264-123">Remarks</span></span>

<span data-ttu-id="66264-124">Die **Win32-Klasse \_ memoryarraylocation** ist von [**CIM \_**](cim-realizes.md)-ermittelungsort abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="66264-124">The **Win32\_MemoryArrayLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66264-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66264-125">Requirements</span></span>



| <span data-ttu-id="66264-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66264-126">Requirement</span></span> | <span data-ttu-id="66264-127">Wert</span><span class="sxs-lookup"><span data-stu-id="66264-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66264-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66264-128">Minimum supported client</span></span><br/> | <span data-ttu-id="66264-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66264-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66264-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66264-130">Minimum supported server</span></span><br/> | <span data-ttu-id="66264-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66264-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66264-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="66264-132">Namespace</span></span><br/>                | <span data-ttu-id="66264-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="66264-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="66264-134">MOF</span><span class="sxs-lookup"><span data-stu-id="66264-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66264-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="66264-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="66264-136">DLL</span><span class="sxs-lookup"><span data-stu-id="66264-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66264-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66264-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66264-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66264-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66264-139">**CIM \_ erkennt**</span><span class="sxs-lookup"><span data-stu-id="66264-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="66264-140">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="66264-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

