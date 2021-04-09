---
description: Die \_ WMI-Klasse für die Zuordnung der Win32-Zuordnungs Klasse ordnet ein logisches Gerät mit einer System Ressource in Beziehung. Diese Klasse wird verwendet, um zu ermitteln, welche Ressourcen, wie z. b. die unqs-oder DMA-Kanäle, von einem bestimmten Gerät verwendet werden.
ms.assetid: cfac1209-1405-4fee-847c-8a61504bfac1
ms.tgt_platform: multiple
title: Win32_AllocatedResource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AllocatedResource
- Win32_AllocatedResource.Dependent
- Win32_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 87a57e53a85e4433ae325fc2ed441211db75b79f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958547"
---
# <a name="win32_allocatedresource-class"></a><span data-ttu-id="405f2-104">Win32- \_ Klasse "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="405f2-104">Win32\_AllocatedResource class</span></span>

<span data-ttu-id="405f2-105">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für die **Zuordnung der Win32- \_ Zuordnungs Klasse ordnet** ein logisches Gerät mit einer System Ressource in Beziehung.</span><span class="sxs-lookup"><span data-stu-id="405f2-105">The **Win32\_AllocatedResource** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device to a system resource.</span></span> <span data-ttu-id="405f2-106">Diese Klasse wird verwendet, um zu ermitteln, welche Ressourcen, wie z. b. die unqs-oder DMA-Kanäle, von einem bestimmten Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="405f2-106">This class is used to discover which resources, such as IRQs or DMA channels, are in use by a specific device.</span></span>

<span data-ttu-id="405f2-107">Diese Klasse ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="405f2-107">This class is obsolete.</span></span> <span data-ttu-id="405f2-108">Anstelle dieser Klasse sollten Sie die Eigenschaften in der [**Win32- \_ pnpallocatedresource**](win32-pnpallocatedresource.md) -Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="405f2-108">In place of this class, you should use the properties in the [**Win32\_PNPAllocatedResource**](win32-pnpallocatedresource.md) class.</span></span>

<span data-ttu-id="405f2-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="405f2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="405f2-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="405f2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="405f2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="405f2-111">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C50D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="405f2-112">Member</span><span class="sxs-lookup"><span data-stu-id="405f2-112">Members</span></span>

<span data-ttu-id="405f2-113">Die **Win32 \_** -Klasse "-Klasse" weist die folgenden Typen von Membern auf:</span><span class="sxs-lookup"><span data-stu-id="405f2-113">The **Win32\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="405f2-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="405f2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="405f2-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="405f2-115">Properties</span></span>

<span data-ttu-id="405f2-116">Die **Win32 \_** -Klasse "-Klasse" weist diese Eigenschaften auf.</span><span class="sxs-lookup"><span data-stu-id="405f2-116">The **Win32\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="405f2-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="405f2-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="405f2-118">Datentyp: **CIM \_ Systemresource**</span><span class="sxs-lookup"><span data-stu-id="405f2-118">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="405f2-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="405f2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="405f2-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ Systemresource")</span><span class="sxs-lookup"><span data-stu-id="405f2-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="405f2-121">Eine [**CIM- \_ System Ressource**](cim-systemresource.md) , die die Eigenschaften einer für das logische Gerät verfügbaren System Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="405f2-121">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the properties of a system resource available to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="405f2-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="405f2-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="405f2-123">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="405f2-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="405f2-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="405f2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="405f2-125">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="405f2-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="405f2-126">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das die Eigenschaften des logischen Geräts darstellt, von dem die ihm zugewiesenen Systemressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="405f2-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is using the system resources assigned to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="405f2-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="405f2-127">Remarks</span></span>

<span data-ttu-id="405f2-128">Die **Win32 \_** -Klasse "-Klasse" ist von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="405f2-128">The **Win32\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="405f2-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="405f2-129">Requirements</span></span>



| <span data-ttu-id="405f2-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="405f2-130">Requirement</span></span> | <span data-ttu-id="405f2-131">Wert</span><span class="sxs-lookup"><span data-stu-id="405f2-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="405f2-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="405f2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="405f2-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="405f2-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="405f2-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="405f2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="405f2-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="405f2-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="405f2-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="405f2-136">Namespace</span></span><br/>                | <span data-ttu-id="405f2-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="405f2-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="405f2-138">MOF</span><span class="sxs-lookup"><span data-stu-id="405f2-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="405f2-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="405f2-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="405f2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="405f2-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="405f2-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="405f2-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="405f2-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="405f2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="405f2-143">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="405f2-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="405f2-144">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="405f2-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

