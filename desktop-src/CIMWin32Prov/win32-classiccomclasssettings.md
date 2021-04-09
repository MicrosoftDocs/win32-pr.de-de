---
description: Die Win32 \_ -WMI-Klasse classiccomclasssettings verknüpft eine Component Object Model (com)-Klasse und die Einstellungen, die zum Konfigurieren von Instanzen der com-Klasse verwendet werden.
ms.assetid: 50f253cc-b8ae-41ac-b01f-ea816f5ca3d4
ms.tgt_platform: multiple
title: Win32_ClassicCOMClassSettings-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSettings
- Win32_ClassicCOMClassSettings.Setting
- Win32_ClassicCOMClassSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9c190157742aeca7c1ba6008a784005d054ca6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860699"
---
# <a name="win32_classiccomclasssettings-class"></a><span data-ttu-id="1eb62-103">Win32 \_ classiccomclasssettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="1eb62-103">Win32\_ClassicCOMClassSettings class</span></span>

<span data-ttu-id="1eb62-104">Die Win32- [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **\_ classiccomclasssettings** verknüpft eine Component Object Model (com)-Klasse und die Einstellungen, die zum Konfigurieren von Instanzen der com-Klasse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1eb62-104">The **Win32\_ClassicCOMClassSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and the settings used to configure instances of the COM class.</span></span>

<span data-ttu-id="1eb62-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1eb62-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1eb62-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1eb62-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb62-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1eb62-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A564-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSettings : CIM_ElementSetting
{
  Win32_ClassicCOMClassSetting REF Setting;
  Win32_ClassicCOMClass        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="1eb62-108">Member</span><span class="sxs-lookup"><span data-stu-id="1eb62-108">Members</span></span>

<span data-ttu-id="1eb62-109">Die **Win32 \_ classiccomclasssettings** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1eb62-109">The **Win32\_ClassicCOMClassSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="1eb62-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1eb62-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1eb62-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1eb62-111">Properties</span></span>

<span data-ttu-id="1eb62-112">Die **Win32 \_ classiccomclasssettings** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1eb62-112">The **Win32\_ClassicCOMClassSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1eb62-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1eb62-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb62-114">Datentyp: **Win32 \_ classiccomclass**</span><span class="sxs-lookup"><span data-stu-id="1eb62-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="1eb62-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1eb62-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb62-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ classiccomclass")</span><span class="sxs-lookup"><span data-stu-id="1eb62-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="1eb62-117">Eine [**Win32 \_ classiccomclass**](win32-classiccomclass.md) , die die com-Klasse darstellt, in der die Einstellungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1eb62-117">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM class where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="1eb62-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="1eb62-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb62-119">Datentyp: **Win32 \_ classiccomclasssetting**</span><span class="sxs-lookup"><span data-stu-id="1eb62-119">Data type: **Win32\_ClassicCOMClassSetting**</span></span>
</dt> <dt>

<span data-ttu-id="1eb62-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1eb62-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb62-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ classiccomclasssetting")</span><span class="sxs-lookup"><span data-stu-id="1eb62-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClassSetting")</span></span>
</dt> </dl>

<span data-ttu-id="1eb62-122">Eine [**Win32 \_ classiccomclasssetting**](win32-classiccomclasssetting.md) , die Konfigurationseinstellungen darstellt, die der com-Klasse zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1eb62-122">A [**Win32\_ClassicCOMClassSetting**](win32-classiccomclasssetting.md) that represents configuration settings associated with the COM class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1eb62-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1eb62-123">Remarks</span></span>

<span data-ttu-id="1eb62-124">Die **Win32 \_ classiccomclasssettings** -Klasse wird von [**CIM \_ Element Setting**](cim-elementsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1eb62-124">The **Win32\_ClassicCOMClassSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb62-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1eb62-125">Requirements</span></span>



| <span data-ttu-id="1eb62-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1eb62-126">Requirement</span></span> | <span data-ttu-id="1eb62-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1eb62-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb62-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1eb62-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1eb62-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1eb62-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1eb62-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1eb62-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1eb62-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1eb62-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1eb62-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="1eb62-132">Namespace</span></span><br/>                | <span data-ttu-id="1eb62-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1eb62-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1eb62-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1eb62-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1eb62-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1eb62-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1eb62-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1eb62-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eb62-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1eb62-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eb62-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1eb62-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb62-139">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="1eb62-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="1eb62-140">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1eb62-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

