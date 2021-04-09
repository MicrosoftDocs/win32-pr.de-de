---
description: Die \_ WMI-Klasse Win32 systemdevices Association verknüpft ein Computersystem und ein logisches Gerät, das auf diesem System installiert ist.
ms.assetid: 84dfcb75-3b44-4b27-8eee-779be522eb1f
ms.tgt_platform: multiple
title: Win32_SystemDevices-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDevices
- Win32_SystemDevices.GroupComponent
- Win32_SystemDevices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2b28c11e10318e3bca562baf93bc20df9b756cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861572"
---
# <a name="win32_systemdevices-class"></a><span data-ttu-id="82f83-103">Win32 \_ systemdevices-Klasse</span><span class="sxs-lookup"><span data-stu-id="82f83-103">Win32\_SystemDevices class</span></span>

<span data-ttu-id="82f83-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ systemdevices** Association verknüpft ein Computersystem und ein logisches Gerät, das auf diesem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="82f83-104">The **Win32\_SystemDevices** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical device installed on that system.</span></span>

<span data-ttu-id="82f83-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="82f83-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="82f83-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="82f83-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="82f83-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="82f83-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDevices : CIM_SystemDevice
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_LogicalDevice    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="82f83-108">Member</span><span class="sxs-lookup"><span data-stu-id="82f83-108">Members</span></span>

<span data-ttu-id="82f83-109">Die **Win32 \_ systemdevices** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="82f83-109">The **Win32\_SystemDevices** class has these types of members:</span></span>

-   [<span data-ttu-id="82f83-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82f83-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82f83-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82f83-111">Properties</span></span>

<span data-ttu-id="82f83-112">Die **Win32 \_ systemdevices** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="82f83-112">The **Win32\_SystemDevices** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82f83-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="82f83-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f83-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="82f83-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="82f83-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f83-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82f83-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="82f83-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="82f83-117">Verweis auf die-Instanz, die die Eigenschaften des Computer Systems darstellt, auf dem das logische Gerät vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="82f83-117">Reference to the instance representing the properties of the computer system where the logical device exists.</span></span>

</dd> <dt>

<span data-ttu-id="82f83-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="82f83-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f83-119">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="82f83-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="82f83-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f83-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82f83-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="82f83-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="82f83-122">Verweis auf die-Instanz, die die Eigenschaften eines logischen Geräts darstellt, das auf dem Computersystem vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="82f83-122">Reference to the instance representing the properties of a logical device that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82f83-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82f83-123">Remarks</span></span>

<span data-ttu-id="82f83-124">Die **Win32 \_ systemdevices** -Klasse wird von [**CIM \_ SystemDevice**](cim-systemdevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="82f83-124">The **Win32\_SystemDevices** class is derived from [**CIM\_SystemDevice**](cim-systemdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82f83-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82f83-125">Requirements</span></span>



| <span data-ttu-id="82f83-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82f83-126">Requirement</span></span> | <span data-ttu-id="82f83-127">Wert</span><span class="sxs-lookup"><span data-stu-id="82f83-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82f83-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82f83-128">Minimum supported client</span></span><br/> | <span data-ttu-id="82f83-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82f83-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82f83-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82f83-130">Minimum supported server</span></span><br/> | <span data-ttu-id="82f83-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82f83-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82f83-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="82f83-132">Namespace</span></span><br/>                | <span data-ttu-id="82f83-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="82f83-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="82f83-134">MOF</span><span class="sxs-lookup"><span data-stu-id="82f83-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82f83-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="82f83-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="82f83-136">DLL</span><span class="sxs-lookup"><span data-stu-id="82f83-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82f83-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82f83-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82f83-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82f83-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f83-139">**CIM- \_ System Gerät**</span><span class="sxs-lookup"><span data-stu-id="82f83-139">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="82f83-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="82f83-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
