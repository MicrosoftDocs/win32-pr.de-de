---
description: Die \_ WMI-Klasse "Win32 devicebus Association" verknüpft einen Systembus und ein logisches Gerät mithilfe des Busses. Diese Klasse wird verwendet, um zu ermitteln, welche Geräte sich auf welchem Bus befinden.
ms.assetid: 2d7d83a5-c058-40c0-aab3-7700f4067a16
ms.tgt_platform: multiple
title: Win32_DeviceBus-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceBus
- Win32_DeviceBus.Dependent
- Win32_DeviceBus.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2dde01ee6b3f3be026dbc19f8c4b8e2c238f4ff2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127721"
---
# <a name="win32_devicebus-class"></a><span data-ttu-id="46bb8-104">Win32 \_ devicebus-Klasse</span><span class="sxs-lookup"><span data-stu-id="46bb8-104">Win32\_DeviceBus class</span></span>

<span data-ttu-id="46bb8-105">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ devicebus** Association" verknüpft einen Systembus und ein logisches Gerät mithilfe des Busses.</span><span class="sxs-lookup"><span data-stu-id="46bb8-105">The **Win32\_DeviceBus** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a system bus and a logical device using the bus.</span></span> <span data-ttu-id="46bb8-106">Diese Klasse wird verwendet, um zu ermitteln, welche Geräte sich auf welchem Bus befinden.</span><span class="sxs-lookup"><span data-stu-id="46bb8-106">This class is used to discover which devices are on which bus.</span></span>

<span data-ttu-id="46bb8-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="46bb8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="46bb8-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="46bb8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="46bb8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="46bb8-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceBus : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  Win32_Bus         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="46bb8-110">Member</span><span class="sxs-lookup"><span data-stu-id="46bb8-110">Members</span></span>

<span data-ttu-id="46bb8-111">Die **Win32 \_ devicebus** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="46bb8-111">The **Win32\_DeviceBus** class has these types of members:</span></span>

-   [<span data-ttu-id="46bb8-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46bb8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46bb8-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46bb8-113">Properties</span></span>

<span data-ttu-id="46bb8-114">Die **Win32 \_ devicebus** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="46bb8-114">The **Win32\_DeviceBus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46bb8-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="46bb8-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46bb8-116">Datentyp: **Win32- \_ Bus**</span><span class="sxs-lookup"><span data-stu-id="46bb8-116">Data type: **Win32\_Bus**</span></span>
</dt> <dt>

<span data-ttu-id="46bb8-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46bb8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46bb8-118">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Bus")</span><span class="sxs-lookup"><span data-stu-id="46bb8-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Bus")</span></span>
</dt> </dl>

<span data-ttu-id="46bb8-119">Ein [**Win32- \_ Bus**](win32-bus.md) , der die Eigenschaften des Systembus beschreibt, die vom logischen Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46bb8-119">A [**Win32\_Bus**](win32-bus.md) that describes the properties of the system bus that is used by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="46bb8-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="46bb8-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46bb8-121">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="46bb8-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="46bb8-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46bb8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46bb8-123">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="46bb8-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="46bb8-124">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das die Eigenschaften des logischen Geräts beschreibt, von dem der Systembus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46bb8-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the properties of the logical device that is using the system bus.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46bb8-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46bb8-125">Remarks</span></span>

<span data-ttu-id="46bb8-126">Die **Win32 \_ devicebus** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="46bb8-126">The **Win32\_DeviceBus** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46bb8-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46bb8-127">Requirements</span></span>



| <span data-ttu-id="46bb8-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46bb8-128">Requirement</span></span> | <span data-ttu-id="46bb8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="46bb8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46bb8-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46bb8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="46bb8-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46bb8-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46bb8-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46bb8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="46bb8-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46bb8-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46bb8-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="46bb8-134">Namespace</span></span><br/>                | <span data-ttu-id="46bb8-135">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="46bb8-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="46bb8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="46bb8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46bb8-137"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="46bb8-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="46bb8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="46bb8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46bb8-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46bb8-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46bb8-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46bb8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46bb8-141">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="46bb8-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="46bb8-142">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="46bb8-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

