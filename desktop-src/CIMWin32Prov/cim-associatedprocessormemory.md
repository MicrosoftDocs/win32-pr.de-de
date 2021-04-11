---
description: Die CIM \_ associatedprocessormemory-Klasse ordnet den Prozessor-und Systemspeicher oder den Cache eines Prozessors zu.
ms.assetid: a4c28a0a-e4cc-4db2-bd77-b7b5023eace6
ms.tgt_platform: multiple
title: CIM_AssociatedProcessorMemory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedProcessorMemory
- CIM_AssociatedProcessorMemory.Antecedent
- CIM_AssociatedProcessorMemory.Dependent
- CIM_AssociatedProcessorMemory.BusSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f35cdca92cb15e1c6fff215ff1363844e0d47012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958483"
---
# <a name="cim_associatedprocessormemory-class"></a><span data-ttu-id="c91d1-103">CIM \_ associatedprocessormemory-Klasse</span><span class="sxs-lookup"><span data-stu-id="c91d1-103">CIM\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="c91d1-104">Die **CIM \_ associatedprocessormemory** -Klasse ordnet den Prozessor-und Systemspeicher oder den Cache eines Prozessors zu.</span><span class="sxs-lookup"><span data-stu-id="c91d1-104">The **CIM\_AssociatedProcessorMemory** class associates the processor and system memory, or a processor's cache.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c91d1-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c91d1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c91d1-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c91d1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c91d1-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c91d1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c91d1-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c91d1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c91d1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c91d1-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB1-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedProcessorMemory : CIM_AssociatedMemory
{
  CIM_Memory    REF Antecedent;
  CIM_Processor REF Dependent;
  uint32            BusSpeed;
};
```

## <a name="members"></a><span data-ttu-id="c91d1-110">Member</span><span class="sxs-lookup"><span data-stu-id="c91d1-110">Members</span></span>

<span data-ttu-id="c91d1-111">Die **CIM \_ associatedprocessormemory** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c91d1-111">The **CIM\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="c91d1-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c91d1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c91d1-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c91d1-113">Properties</span></span>

<span data-ttu-id="c91d1-114">Die **CIM \_ associatedprocessormemory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c91d1-114">The **CIM\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c91d1-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="c91d1-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c91d1-116">Datentyp: **CIM- \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="c91d1-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="c91d1-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c91d1-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c91d1-118">Ein [**CIM- \_ Speicher**](cim-memory.md) , der den Arbeitsspeicher beschreibt, der auf einem Gerät installiert oder diesem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c91d1-118">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

<span data-ttu-id="c91d1-119">Diese Eigenschaft wird von [**CIM \_ associatedmemory**](cim-associatedmemory.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c91d1-119">This property is inherited from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c91d1-120">**Busgeschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="c91d1-120">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c91d1-121">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c91d1-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c91d1-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c91d1-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c91d1-123">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Megahertz")</span><span class="sxs-lookup"><span data-stu-id="c91d1-123">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="c91d1-124">Geschwindigkeit des Busses in Megahertz (MHz) zwischen Prozessor und Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c91d1-124">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

</dd> <dt>

<span data-ttu-id="c91d1-125">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="c91d1-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c91d1-126">Datentyp: **CIM- \_ Prozessor**</span><span class="sxs-lookup"><span data-stu-id="c91d1-126">Data type: **CIM\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="c91d1-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c91d1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c91d1-128">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="c91d1-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c91d1-129">Ein [**CIM- \_ Prozessor**](cim-processor.md) , der den Prozessor beschreibt, der auf den Arbeitsspeicher zugreift oder den Cache verwendet.</span><span class="sxs-lookup"><span data-stu-id="c91d1-129">A [**CIM\_Processor**](cim-processor.md) describing the processor that accesses the memory or uses the cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c91d1-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c91d1-130">Remarks</span></span>

<span data-ttu-id="c91d1-131">Die **CIM \_ associatedprocessormemory** -Klasse wird von [**CIM \_ associatedmemory**](cim-associatedmemory.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c91d1-131">The **CIM\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

<span data-ttu-id="c91d1-132">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c91d1-132">WMI does not implement this class.</span></span> <span data-ttu-id="c91d1-133">Weitere Informationen zu Klassen, die von **CIM \_ associatedprocessormemory** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c91d1-133">For more information about classes derived from **CIM\_AssociatedProcessorMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c91d1-134">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c91d1-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c91d1-135">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c91d1-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c91d1-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c91d1-136">Requirements</span></span>



| <span data-ttu-id="c91d1-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c91d1-137">Requirement</span></span> | <span data-ttu-id="c91d1-138">Wert</span><span class="sxs-lookup"><span data-stu-id="c91d1-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c91d1-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c91d1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c91d1-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c91d1-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c91d1-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c91d1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c91d1-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c91d1-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c91d1-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="c91d1-143">Namespace</span></span><br/>                | <span data-ttu-id="c91d1-144">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c91d1-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c91d1-145">MOF</span><span class="sxs-lookup"><span data-stu-id="c91d1-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c91d1-146"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c91d1-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c91d1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c91d1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c91d1-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c91d1-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c91d1-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c91d1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c91d1-150">**CIM \_ associatedmemory**</span><span class="sxs-lookup"><span data-stu-id="c91d1-150">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> </dl>

 

