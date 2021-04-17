---
description: Die \_ WMI-Klasse "Win32 systemsystemdriver Association" bezieht sich auf ein Computersystem und einen System Treiber, der auf diesem Computersystem ausgeführt wird.
ms.assetid: 82638c29-6769-4410-90bc-b408b27adad4
ms.tgt_platform: multiple
title: Win32_SystemSystemDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSystemDriver
- Win32_SystemSystemDriver.GroupComponent
- Win32_SystemSystemDriver.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b193d173fa0592a44ba437543659dec456e432ea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524232"
---
# <a name="win32_systemsystemdriver-class"></a><span data-ttu-id="f2e88-103">Win32 \_ systemsystemdriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="f2e88-103">Win32\_SystemSystemDriver class</span></span>

<span data-ttu-id="f2e88-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemsystemdriver** Association" bezieht sich auf ein Computersystem und einen System Treiber, der auf diesem Computersystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2e88-104">The **Win32\_SystemSystemDriver** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a system driver running on that computer system.</span></span>

<span data-ttu-id="f2e88-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f2e88-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f2e88-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="f2e88-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e88-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2e88-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSystemDriver : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_SystemDriver   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="f2e88-108">Member</span><span class="sxs-lookup"><span data-stu-id="f2e88-108">Members</span></span>

<span data-ttu-id="f2e88-109">Die **Win32 \_ systemsystemdriver** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f2e88-109">The **Win32\_SystemSystemDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="f2e88-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2e88-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2e88-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2e88-111">Properties</span></span>

<span data-ttu-id="f2e88-112">Die **Win32 \_ systemsystemdriver** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f2e88-112">The **Win32\_SystemSystemDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2e88-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f2e88-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2e88-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="f2e88-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="f2e88-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2e88-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2e88-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="f2e88-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="f2e88-117">Verweis auf die-Instanz, die die Eigenschaften des Computer Systems darstellt, auf dem der Treiber ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2e88-117">Reference to the instance representing the properties of the computer system upon which the driver is running.</span></span>

</dd> <dt>

<span data-ttu-id="f2e88-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f2e88-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2e88-119">Datentyp: **Win32 \_ System Driver**</span><span class="sxs-lookup"><span data-stu-id="f2e88-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="f2e88-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2e88-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2e88-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ System Driver")</span><span class="sxs-lookup"><span data-stu-id="f2e88-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="f2e88-122">Verweis auf die-Instanz, die den System Treiber darstellt, der auf dem Computersystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2e88-122">Reference to the instance representing the system driver running on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2e88-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2e88-123">Remarks</span></span>

<span data-ttu-id="f2e88-124">Die **Win32 \_ systemsystemdriver** -Klasse wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f2e88-124">The **Win32\_SystemSystemDriver** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e88-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2e88-125">Requirements</span></span>



| <span data-ttu-id="f2e88-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2e88-126">Requirement</span></span> | <span data-ttu-id="f2e88-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f2e88-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e88-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2e88-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e88-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2e88-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2e88-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2e88-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e88-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2e88-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2e88-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2e88-132">Namespace</span></span><br/>                | <span data-ttu-id="f2e88-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f2e88-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f2e88-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f2e88-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2e88-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f2e88-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2e88-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f2e88-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2e88-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2e88-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e88-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2e88-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e88-139">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="f2e88-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="f2e88-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="f2e88-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
