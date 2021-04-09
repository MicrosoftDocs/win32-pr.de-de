---
description: Die \_ WMI-Klasse für die Win32-pnpallocatedresource-Zuordnung stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar.
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Win32_PnPAllocatedResource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353009016c8d4d54cdc92fb8f0ed062567dded6f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861711"
---
# <a name="win32_pnpallocatedresource-class"></a><span data-ttu-id="132b6-103">Win32- \_ pnpallocatedresource-Klasse</span><span class="sxs-lookup"><span data-stu-id="132b6-103">Win32\_PnPAllocatedResource class</span></span>

<span data-ttu-id="132b6-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32- \_ pnpallocatedresource** -Zuordnung stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar.</span><span class="sxs-lookup"><span data-stu-id="132b6-104">The **Win32\_PnPAllocatedResource** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between logical devices and system resources.</span></span> <span data-ttu-id="132b6-105">Diese Klasse wird verwendet, um die Ressourcen zu ermitteln, die von einem bestimmten Gerät verwendet werden, z. b. eine Interruptanforderung (UNQ) oder einen DMA-Kanal (Direct Memory Access).</span><span class="sxs-lookup"><span data-stu-id="132b6-105">This class is used to discover the resources that are in-use by a specific device, such as an Interrupt ReQuest (IRQ) or a Direct Memory Access (DMA) channel.</span></span>

<span data-ttu-id="132b6-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="132b6-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="132b6-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="132b6-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="132b6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="132b6-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="132b6-109">Member</span><span class="sxs-lookup"><span data-stu-id="132b6-109">Members</span></span>

<span data-ttu-id="132b6-110">Die **Win32- \_ pnpallocatedresource** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="132b6-110">The **Win32\_PnPAllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="132b6-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="132b6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="132b6-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="132b6-112">Properties</span></span>

<span data-ttu-id="132b6-113">Die **Win32- \_ pnpallocatedresource** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="132b6-113">The **Win32\_PnPAllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="132b6-114">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="132b6-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="132b6-115">Datentyp: **CIM \_ Systemresource**</span><span class="sxs-lookup"><span data-stu-id="132b6-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="132b6-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="132b6-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="132b6-117">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Vorgänger"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ Systemresource")</span><span class="sxs-lookup"><span data-stu-id="132b6-117">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="132b6-118">Verweis auf die [**CIM- \_ systemressourceninstanz**](cim-systemresource.md) , die die Eigenschaften einer für das logische Gerät verfügbaren System Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="132b6-118">Reference to the [**CIM\_SystemResource**](cim-systemresource.md) instance that represents the properties of a system resource available to the logical device.</span></span> <span data-ttu-id="132b6-119">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="132b6-119">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="132b6-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="132b6-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="132b6-121">Datentyp: **Win32 \_ pnptity**</span><span class="sxs-lookup"><span data-stu-id="132b6-121">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="132b6-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="132b6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="132b6-123">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="132b6-123">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="132b6-124">Verweis auf die [**Win32 \_ pnptity**](win32-pnpentity.md) -Instanz, die die Eigenschaften des logischen Geräts mit den zugewiesenen Systemressourcen darstellt.</span><span class="sxs-lookup"><span data-stu-id="132b6-124">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance that represents the properties of the logical device using the system resources assigned to it.</span></span> <span data-ttu-id="132b6-125">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="132b6-125">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="132b6-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="132b6-126">Remarks</span></span>

<span data-ttu-id="132b6-127">Die **Win32- \_ pnpallocatedresource** -Klasse wird von CIM "" [**\_ zugeordnet**](cim-allocatedresource.md).</span><span class="sxs-lookup"><span data-stu-id="132b6-127">The **Win32\_PnPAllocatedResource** class is derived from [**CIM\_AllocatedResource**](cim-allocatedresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="132b6-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="132b6-128">Requirements</span></span>



| <span data-ttu-id="132b6-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="132b6-129">Requirement</span></span> | <span data-ttu-id="132b6-130">Wert</span><span class="sxs-lookup"><span data-stu-id="132b6-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="132b6-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="132b6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="132b6-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="132b6-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="132b6-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="132b6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="132b6-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="132b6-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="132b6-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="132b6-135">Namespace</span></span><br/>                | <span data-ttu-id="132b6-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="132b6-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="132b6-137">MOF</span><span class="sxs-lookup"><span data-stu-id="132b6-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="132b6-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="132b6-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="132b6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="132b6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="132b6-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="132b6-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="132b6-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="132b6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="132b6-142">**CIM- \_ Verteilungs Quelle**</span><span class="sxs-lookup"><span data-stu-id="132b6-142">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dt>

[<span data-ttu-id="132b6-143">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="132b6-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
