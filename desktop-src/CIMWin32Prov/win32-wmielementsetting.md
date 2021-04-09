---
description: Die \_ WMI-Klasse für die Win32 wmielementsetting-Zuordnung verknüpft einen Dienst, der im Windows-System ausgeführt wird, und die verwendeten WMI-Einstellungen.
ms.assetid: 00e9f882-5f54-4042-a916-2f90ed9a37c0
ms.tgt_platform: multiple
title: Win32_WMIElementSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMIElementSetting
- Win32_WMIElementSetting.Element
- Win32_WMIElementSetting.Setting
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 41f79614fd0931759d502bbd61c7f4143e9e7dc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860687"
---
# <a name="win32_wmielementsetting-class"></a><span data-ttu-id="0882b-103">Win32 \_ wmielementsetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="0882b-103">Win32\_WMIElementSetting class</span></span>

<span data-ttu-id="0882b-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32 \_ wmielementsetting** -Zuordnung verknüpft einen Dienst, der im Windows-System ausgeführt wird, und die verwendeten WMI-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="0882b-104">The **Win32\_WMIElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a service running in the Windows system and the WMI settings it can use.</span></span>

<span data-ttu-id="0882b-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0882b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0882b-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="0882b-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0882b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0882b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("WBEMCORE"), UUID("{A83EF167-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMIElementSetting : CIM_ElementSetting
{
  Win32_Service    REF Element;
  Win32_WMISetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="0882b-108">Member</span><span class="sxs-lookup"><span data-stu-id="0882b-108">Members</span></span>

<span data-ttu-id="0882b-109">Die **Win32 \_ wmielementsetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0882b-109">The **Win32\_WMIElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="0882b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0882b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0882b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0882b-111">Properties</span></span>

<span data-ttu-id="0882b-112">Die **Win32 \_ wmielementsetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0882b-112">The **Win32\_WMIElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0882b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0882b-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0882b-114">Datentyp: **Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="0882b-114">Data type: **Win32\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="0882b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0882b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0882b-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32- \_ Dienst")</span><span class="sxs-lookup"><span data-stu-id="0882b-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Service")</span></span>
</dt> </dl>

<span data-ttu-id="0882b-117">Verweis auf die Instanz, die den Windows-Dienst mithilfe von WMI-Eigenschaften darstellt oder diese darstellt.</span><span class="sxs-lookup"><span data-stu-id="0882b-117">Reference to the instance representing the Windows service using or surfacing WMI properties.</span></span>

</dd> <dt>

<span data-ttu-id="0882b-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="0882b-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0882b-119">Datentyp: **Win32 \_ wmisetting**</span><span class="sxs-lookup"><span data-stu-id="0882b-119">Data type: **Win32\_WMISetting**</span></span>
</dt> <dt>

<span data-ttu-id="0882b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0882b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0882b-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ wmisetting")</span><span class="sxs-lookup"><span data-stu-id="0882b-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_WMISetting")</span></span>
</dt> </dl>

<span data-ttu-id="0882b-122">Verweis auf die-Instanz, die die für den Windows-Dienst verfügbaren WMI-Einstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="0882b-122">Reference to the instance representing the WMI settings available to the Windows service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0882b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0882b-123">Remarks</span></span>

<span data-ttu-id="0882b-124">Die **Win32- \_ wmielementsetting** -Klasse wird von [**CIM \_ Element Setting**](cim-elementsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0882b-124">The **Win32\_WMIElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0882b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0882b-125">Requirements</span></span>



| <span data-ttu-id="0882b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0882b-126">Requirement</span></span> | <span data-ttu-id="0882b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0882b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0882b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0882b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0882b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0882b-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0882b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0882b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0882b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0882b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0882b-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="0882b-132">Namespace</span></span><br/>                | <span data-ttu-id="0882b-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0882b-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0882b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0882b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0882b-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0882b-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0882b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0882b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0882b-137"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0882b-137"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0882b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0882b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0882b-139">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="0882b-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="0882b-140">WMI-Dienst Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="0882b-140">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
