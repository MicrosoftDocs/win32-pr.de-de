---
description: Die \_ WMI-Klasse der Win32 associatedprocessormemory-Zuordnung bezieht einen Prozessor und den zugehörigen Cache Speicher.
ms.assetid: 23da2a9d-772e-4258-9489-07d47801b2d8
ms.tgt_platform: multiple
title: Win32_AssociatedProcessorMemory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AssociatedProcessorMemory
- Win32_AssociatedProcessorMemory.BusSpeed
- Win32_AssociatedProcessorMemory.Dependent
- Win32_AssociatedProcessorMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3737dca869c539d1414c4399f35fb8f107697b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958546"
---
# <a name="win32_associatedprocessormemory-class"></a><span data-ttu-id="d95bd-103">Win32 \_ associatedprocessormemory-Klasse</span><span class="sxs-lookup"><span data-stu-id="d95bd-103">Win32\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="d95bd-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) der **Win32 \_ associatedprocessormemory** -Zuordnung bezieht einen Prozessor und den zugehörigen Cache Speicher.</span><span class="sxs-lookup"><span data-stu-id="d95bd-104">The **Win32\_AssociatedProcessorMemory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a processor and its cache memory.</span></span>

<span data-ttu-id="d95bd-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d95bd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d95bd-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d95bd-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d95bd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d95bd-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{074737F0-ACBC-11d2-ABF6-00805F538618}"), AMENDMENT]
class Win32_AssociatedProcessorMemory : CIM_AssociatedProcessorMemory
{
  uint32                BusSpeed;
  Win32_Processor   REF Dependent;
  Win32_CacheMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d95bd-108">Member</span><span class="sxs-lookup"><span data-stu-id="d95bd-108">Members</span></span>

<span data-ttu-id="d95bd-109">Die **Win32 \_ associatedprocessormemory** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d95bd-109">The **Win32\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="d95bd-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d95bd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d95bd-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d95bd-111">Properties</span></span>

<span data-ttu-id="d95bd-112">Die **Win32 \_ associatedprocessormemory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d95bd-112">The **Win32\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d95bd-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="d95bd-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d95bd-114">Datentyp: **Win32 \_ CacheMemory**</span><span class="sxs-lookup"><span data-stu-id="d95bd-114">Data type: **Win32\_CacheMemory**</span></span>
</dt> <dt>

<span data-ttu-id="d95bd-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d95bd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d95bd-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ CacheMemory")</span><span class="sxs-lookup"><span data-stu-id="d95bd-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_CacheMemory")</span></span>
</dt> </dl>

<span data-ttu-id="d95bd-117">Ein [**Win32- \_ CacheMemory**](win32-cachememory.md) , der den für den Prozessor verfügbaren Cache Speicher beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d95bd-117">A [**Win32\_CacheMemory**](win32-cachememory.md) that describes the cache memory available to the processor.</span></span>

</dd> <dt>

<span data-ttu-id="d95bd-118">**Busgeschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="d95bd-118">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d95bd-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d95bd-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d95bd-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d95bd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d95bd-121">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Megahertz")</span><span class="sxs-lookup"><span data-stu-id="d95bd-121">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="d95bd-122">Geschwindigkeit des Busses in Megahertz (MHz) zwischen Prozessor und Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d95bd-122">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

<span data-ttu-id="d95bd-123">Diese Eigenschaft wird von [**CIM \_ associatedprocessormemory**](cim-associatedprocessormemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d95bd-123">This property is inherited from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d95bd-124">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="d95bd-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d95bd-125">Datentyp: **Win32- \_ Prozessor**</span><span class="sxs-lookup"><span data-stu-id="d95bd-125">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="d95bd-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d95bd-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d95bd-127">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Processor")</span><span class="sxs-lookup"><span data-stu-id="d95bd-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="d95bd-128">Ein [**Win32- \_ Prozessor**](win32-processor.md) , der den Prozessor beschreibt, von dem der Cache Speicher verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d95bd-128">A [**Win32\_Processor**](win32-processor.md) that describes the processor that is using the cache memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d95bd-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d95bd-129">Remarks</span></span>

<span data-ttu-id="d95bd-130">Die **Win32 \_ associatedprocessormemory** -Klasse wird von [**CIM \_ associatedprocessormemory**](cim-associatedprocessormemory.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d95bd-130">The **Win32\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d95bd-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d95bd-131">Requirements</span></span>



| <span data-ttu-id="d95bd-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d95bd-132">Requirement</span></span> | <span data-ttu-id="d95bd-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d95bd-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d95bd-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d95bd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d95bd-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d95bd-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d95bd-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d95bd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d95bd-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d95bd-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d95bd-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="d95bd-138">Namespace</span></span><br/>                | <span data-ttu-id="d95bd-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d95bd-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d95bd-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d95bd-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d95bd-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d95bd-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d95bd-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d95bd-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d95bd-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d95bd-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d95bd-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d95bd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d95bd-145">**CIM \_ associatedprocessormemory**</span><span class="sxs-lookup"><span data-stu-id="d95bd-145">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dt>

[<span data-ttu-id="d95bd-146">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="d95bd-146">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

