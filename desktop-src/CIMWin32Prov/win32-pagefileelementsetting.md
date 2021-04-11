---
description: Die \_ WMI-Klasse der Win32 pagefileelementsetting-Zuordnung verknüpft die anfänglichen Einstellungen einer Auslagerungs Datei und den Zustand dieser Einstellungen während der normalen Verwendung.
ms.assetid: efc1f20d-166e-4e27-9767-f6ec0bbd6c14
ms.tgt_platform: multiple
title: Win32_PageFileElementSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileElementSetting
- Win32_PageFileElementSetting.Element
- Win32_PageFileElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfc1087225894cef2895cf41af5e5297769a4041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958539"
---
# <a name="win32_pagefileelementsetting-class"></a><span data-ttu-id="afca0-103">Win32 \_ pagefileelementsetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="afca0-103">Win32\_PageFileElementSetting class</span></span>

<span data-ttu-id="afca0-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32 \_ pagefileelementsetting** -Zuordnung verknüpft die anfänglichen Einstellungen einer Auslagerungs Datei und den Zustand dieser Einstellungen während der normalen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="afca0-104">The **Win32\_PageFileElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates the initial settings of a page file and the state of those settings during normal use.</span></span>

<span data-ttu-id="afca0-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="afca0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="afca0-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="afca0-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="afca0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="afca0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8E7F70E8-C856-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileElementSetting : CIM_ElementSetting
{
  Win32_PageFileUsage   REF Element;
  Win32_PageFileSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="afca0-108">Member</span><span class="sxs-lookup"><span data-stu-id="afca0-108">Members</span></span>

<span data-ttu-id="afca0-109">Die **Win32-Klasse \_ pagefileelementsetting** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="afca0-109">The **Win32\_PageFileElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="afca0-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="afca0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="afca0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="afca0-111">Properties</span></span>

<span data-ttu-id="afca0-112">Die **Win32-Klasse \_ pagefileelementsetting** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="afca0-112">The **Win32\_PageFileElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afca0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="afca0-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afca0-114">Datentyp: **Win32 \_ PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="afca0-114">Data type: **Win32\_PageFileUsage**</span></span>
</dt> <dt>

<span data-ttu-id="afca0-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="afca0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afca0-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileUsage")</span><span class="sxs-lookup"><span data-stu-id="afca0-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileUsage")</span></span>
</dt> </dl>

<span data-ttu-id="afca0-117">Verweis auf die-Instanz, die die Eigenschaften einer Auslagerungs Datei darstellt, während das Win32-System verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="afca0-117">Reference to the instance representing the properties of a page file while the Win32 system is in use.</span></span>

</dd> <dt>

<span data-ttu-id="afca0-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="afca0-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afca0-119">Datentyp: **Win32 \_ pagefilesetting**</span><span class="sxs-lookup"><span data-stu-id="afca0-119">Data type: **Win32\_PageFileSetting**</span></span>
</dt> <dt>

<span data-ttu-id="afca0-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="afca0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afca0-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ pagefilesetting")</span><span class="sxs-lookup"><span data-stu-id="afca0-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileSetting")</span></span>
</dt> </dl>

<span data-ttu-id="afca0-122">Verweis auf die-Instanz, die die anfänglichen Einstellungen einer Auslagerungs Datei darstellt, wenn das Win32-System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="afca0-122">Reference to the instance representing the initial settings of a page file when the Win32 system is starting up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afca0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afca0-123">Remarks</span></span>

<span data-ttu-id="afca0-124">Die **Win32-Klasse \_ pagefileelementsetting** wird von [**CIM \_ Element Setting**](cim-elementsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="afca0-124">The **Win32\_PageFileElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="afca0-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afca0-125">Requirements</span></span>



| <span data-ttu-id="afca0-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afca0-126">Requirement</span></span> | <span data-ttu-id="afca0-127">Wert</span><span class="sxs-lookup"><span data-stu-id="afca0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afca0-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afca0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="afca0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afca0-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="afca0-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afca0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="afca0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afca0-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="afca0-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="afca0-132">Namespace</span></span><br/>                | <span data-ttu-id="afca0-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="afca0-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="afca0-134">MOF</span><span class="sxs-lookup"><span data-stu-id="afca0-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afca0-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="afca0-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="afca0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="afca0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afca0-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afca0-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afca0-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afca0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afca0-139">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="afca0-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="afca0-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="afca0-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
