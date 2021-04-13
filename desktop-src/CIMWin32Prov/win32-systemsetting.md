---
description: Die \_ WMI-Klasse der WMI-Klasse für die WMI-Klasse "Win32 systemsetting" verknüpft ein Computersystem und eine allgemeine Einstellung
ms.assetid: 796ee263-2526-43f8-bd3d-23442b6bd4ca
ms.tgt_platform: multiple
title: Win32_SystemSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSetting
- Win32_SystemSetting.Element
- Win32_SystemSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e29b752d769cd347ce1cfdb729bf8c0c3959a4f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483894"
---
# <a name="win32_systemsetting-class"></a><span data-ttu-id="8a9c4-103">Win32 \_ systemsetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="8a9c4-103">Win32\_SystemSetting class</span></span>

<span data-ttu-id="8a9c4-104">Die [WMI-Klasse der WMI-Klasse für die WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemsetting** " verknüpft ein Computersystem und eine allgemeine Einstellung</span><span class="sxs-lookup"><span data-stu-id="8a9c4-104">The **Win32\_SystemSetting** abstract association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a general setting on that system.</span></span>

<span data-ttu-id="8a9c4-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8a9c4-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a9c4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a9c4-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C501-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSetting : CIM_ElementSetting
{
  Win32_ComputerSystem REF Element;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="8a9c4-108">Member</span><span class="sxs-lookup"><span data-stu-id="8a9c4-108">Members</span></span>

<span data-ttu-id="8a9c4-109">Die **Win32- \_ systemsetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8a9c4-109">The **Win32\_SystemSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8a9c4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8a9c4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8a9c4-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8a9c4-111">Properties</span></span>

<span data-ttu-id="8a9c4-112">Die **Win32- \_ systemsetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-112">The **Win32\_SystemSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a9c4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8a9c4-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a9c4-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="8a9c4-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="8a9c4-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8a9c4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a9c4-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="8a9c4-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="8a9c4-117">Verweis auf die-Instanz, die die Eigenschaften eines Computer Systems darstellt, auf dem diese Einstellung angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-117">Reference to the instance representing the properties of a computer system where this setting can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="8a9c4-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="8a9c4-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a9c4-119">Datentyp: **CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="8a9c4-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="8a9c4-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8a9c4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a9c4-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM- \_ Einstellung")</span><span class="sxs-lookup"><span data-stu-id="8a9c4-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="8a9c4-122">Verweis auf die-Instanz, die die Eigenschaften der Einstellung darstellt, die auf das Computersystem angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-122">Reference to the instance representing the properties of the setting that can be applied to the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a9c4-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a9c4-123">Remarks</span></span>

<span data-ttu-id="8a9c4-124">Die **Win32- \_ systemsetting** -Klasse wird von [**CIM \_ Element Setting**](cim-elementsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-124">The **Win32\_SystemSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a9c4-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a9c4-125">Requirements</span></span>



| <span data-ttu-id="8a9c4-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a9c4-126">Requirement</span></span> | <span data-ttu-id="8a9c4-127">Wert</span><span class="sxs-lookup"><span data-stu-id="8a9c4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a9c4-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a9c4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8a9c4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a9c4-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a9c4-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a9c4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8a9c4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a9c4-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a9c4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a9c4-132">Namespace</span></span><br/>                | <span data-ttu-id="8a9c4-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8a9c4-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8a9c4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8a9c4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a9c4-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8a9c4-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a9c4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8a9c4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a9c4-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a9c4-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a9c4-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a9c4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a9c4-139">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="8a9c4-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="8a9c4-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="8a9c4-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
