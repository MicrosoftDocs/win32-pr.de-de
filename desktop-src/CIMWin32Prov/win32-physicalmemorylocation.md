---
description: Die \_ WMI-Klasse für die Win32 physicalmemorylocation-Zuordnung verknüpft ein Array von physischem Arbeitsspeicher und dessen physischem Arbeitsspeicher.
ms.assetid: 40252428-77ca-4dfb-8048-c05096a114d8
ms.tgt_platform: multiple
title: Win32_PhysicalMemoryLocation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryLocation
- Win32_PhysicalMemoryLocation.LocationWithinContainer
- Win32_PhysicalMemoryLocation.PartComponent
- Win32_PhysicalMemoryLocation.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daa6d47b13cb5caa74a10f28ab5fcd6e66e1524f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958607"
---
# <a name="win32_physicalmemorylocation-class"></a><span data-ttu-id="a08de-103">Win32 \_ physicalmemorylocation-Klasse</span><span class="sxs-lookup"><span data-stu-id="a08de-103">Win32\_PhysicalMemoryLocation class</span></span>

<span data-ttu-id="a08de-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32 \_ physicalmemorylocation** -Zuordnung verknüpft ein Array von physischem Arbeitsspeicher und dessen physischem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a08de-104">The **Win32\_PhysicalMemoryLocation** association [WMI class](../wmisdk/retrieving-a-class.md) relates an array of physical memory and its physical memory.</span></span>

<span data-ttu-id="a08de-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a08de-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a08de-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a08de-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a08de-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a08de-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF562-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_PhysicalMemoryLocation : CIM_PackagedComponent
{
  string                        LocationWithinContainer;
  Win32_PhysicalMemory      REF PartComponent;
  Win32_PhysicalMemoryArray REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="a08de-108">Member</span><span class="sxs-lookup"><span data-stu-id="a08de-108">Members</span></span>

<span data-ttu-id="a08de-109">Die **Win32 \_ physicalmemorylocation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a08de-109">The **Win32\_PhysicalMemoryLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="a08de-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a08de-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a08de-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a08de-111">Properties</span></span>

<span data-ttu-id="a08de-112">Die **Win32 \_ physicalmemorylocation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a08de-112">The **Win32\_PhysicalMemoryLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a08de-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a08de-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a08de-114">Datentyp: **Win32 \_ physicalmemoryarray**</span><span class="sxs-lookup"><span data-stu-id="a08de-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="a08de-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a08de-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a08de-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ physicalmemoryarray")</span><span class="sxs-lookup"><span data-stu-id="a08de-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="a08de-117">Ein [**Win32 \_ physicalmemoryarray**](win32-physicalmemoryarray.md) , das das physische Speicher Array darstellt, das den physischen Speicher enthält.</span><span class="sxs-lookup"><span data-stu-id="a08de-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that represents the physical memory array that contains the physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="a08de-118">**Locationwithincontainer**</span><span class="sxs-lookup"><span data-stu-id="a08de-118">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a08de-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a08de-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a08de-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a08de-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a08de-121">Eine frei Form Zeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt.</span><span class="sxs-lookup"><span data-stu-id="a08de-121">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="a08de-122">Informationen in Bezug auf die stationären Elemente im Container (z. b. "Second Drive Bay from the Top"), Winkel, Höhen und andere Daten können in dieser Eigenschaft aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a08de-122">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="a08de-123">Diese Zeichenfolge kann anstelle der Instanziierung des [**CIM- \_ Speicherort**](cim-location.md) Objekts ergänzt oder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a08de-123">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="a08de-124">Diese Eigenschaft wird vom [**CIM- \_ Container**](cim-container.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a08de-124">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="a08de-125">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a08de-125">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a08de-126">Datentyp: **Win32 \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="a08de-126">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="a08de-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a08de-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a08de-128">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemory")</span><span class="sxs-lookup"><span data-stu-id="a08de-128">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="a08de-129">Ein [**Win32- \_ PhysicalMemory**](win32-physicalmemory.md) , der den physischen Speicher darstellt, der im physischen Speicher Array enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a08de-129">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory contained in the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a08de-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a08de-130">Remarks</span></span>

<span data-ttu-id="a08de-131">Die **Win32 \_ physicalmemorylocation** -Klasse wird von [**CIM \_ packagedcomponent**](cim-packagedcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a08de-131">The **Win32\_PhysicalMemoryLocation** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a08de-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a08de-132">Requirements</span></span>



| <span data-ttu-id="a08de-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a08de-133">Requirement</span></span> | <span data-ttu-id="a08de-134">Wert</span><span class="sxs-lookup"><span data-stu-id="a08de-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a08de-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a08de-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a08de-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a08de-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a08de-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a08de-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a08de-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a08de-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a08de-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="a08de-139">Namespace</span></span><br/>                | <span data-ttu-id="a08de-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a08de-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a08de-141">MOF</span><span class="sxs-lookup"><span data-stu-id="a08de-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a08de-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a08de-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a08de-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a08de-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a08de-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a08de-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a08de-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a08de-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08de-146">**CIM \_ packagedcomponent**</span><span class="sxs-lookup"><span data-stu-id="a08de-146">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dt>

[<span data-ttu-id="a08de-147">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="a08de-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
