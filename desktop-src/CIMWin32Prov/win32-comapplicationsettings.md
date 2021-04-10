---
description: Die \_ WMI-Klasse "Win32 comapplicationsettings" verknüpft eine DCOM-Anwendung und Ihre Konfigurationseinstellungen.
ms.assetid: b08eaff1-b42a-42f3-abf7-3664b6195acd
ms.tgt_platform: multiple
title: Win32_COMApplicationSettings-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationSettings
- Win32_COMApplicationSettings.Setting
- Win32_COMApplicationSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f2fd5953d770d541e704b7dc7fe8580e98b3066
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214053"
---
# <a name="win32_comapplicationsettings-class"></a><span data-ttu-id="3fd5c-103">Win32 \_ comapplicationsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="3fd5c-103">Win32\_COMApplicationSettings class</span></span>

<span data-ttu-id="3fd5c-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ comapplicationsettings** " verknüpft eine DCOM-Anwendung und Ihre Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="3fd5c-104">The **Win32\_COMApplicationSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a DCOM application and its configuration settings.</span></span>

<span data-ttu-id="3fd5c-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="3fd5c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3fd5c-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3fd5c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd5c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fd5c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A563-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationSettings : CIM_ElementSetting
{
  Win32_DCOMApplicationSetting REF Setting;
  Win32_DCOMApplication        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="3fd5c-108">Member</span><span class="sxs-lookup"><span data-stu-id="3fd5c-108">Members</span></span>

<span data-ttu-id="3fd5c-109">Die **Win32 \_ comapplicationsettings** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3fd5c-109">The **Win32\_COMApplicationSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="3fd5c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3fd5c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3fd5c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3fd5c-111">Properties</span></span>

<span data-ttu-id="3fd5c-112">Die **Win32 \_ comapplicationsettings** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3fd5c-112">The **Win32\_COMApplicationSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3fd5c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3fd5c-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fd5c-114">Datentyp: **Win32 \_ dcomapplication**</span><span class="sxs-lookup"><span data-stu-id="3fd5c-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="3fd5c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3fd5c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fd5c-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ dcomapplication")</span><span class="sxs-lookup"><span data-stu-id="3fd5c-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="3fd5c-117">Eine [**Win32 \_ dcomapplication**](win32-dcomapplication.md) , die die DCOM-Anwendung darstellt, in der die Einstellungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="3fd5c-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents the DCOM application where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="3fd5c-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="3fd5c-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fd5c-119">Datentyp: **Win32 \_ dcomapplicationsetting**</span><span class="sxs-lookup"><span data-stu-id="3fd5c-119">Data type: **Win32\_DCOMApplicationSetting**</span></span>
</dt> <dt>

<span data-ttu-id="3fd5c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3fd5c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fd5c-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ dcomapplicationsetting")</span><span class="sxs-lookup"><span data-stu-id="3fd5c-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplicationSetting")</span></span>
</dt> </dl>

<span data-ttu-id="3fd5c-122">Ein [**Win32 \_ dcomapplicationsetting**](win32-dcomapplicationsetting.md) , das die der DCOM-Anwendung zugeordneten Konfigurationseinstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="3fd5c-122">A [**Win32\_DCOMApplicationSetting**](win32-dcomapplicationsetting.md) that represents the configuration settings associated with the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fd5c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fd5c-123">Remarks</span></span>

<span data-ttu-id="3fd5c-124">Die **Win32 \_ comapplicationsettings** -Klasse wird von [**CIM \_ Element Setting**](cim-elementsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3fd5c-124">The **Win32\_COMApplicationSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd5c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fd5c-125">Requirements</span></span>



| <span data-ttu-id="3fd5c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fd5c-126">Requirement</span></span> | <span data-ttu-id="3fd5c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3fd5c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd5c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3fd5c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd5c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3fd5c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3fd5c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3fd5c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd5c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fd5c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3fd5c-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3fd5c-132">Namespace</span></span><br/>                | <span data-ttu-id="3fd5c-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3fd5c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3fd5c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3fd5c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fd5c-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3fd5c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fd5c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3fd5c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fd5c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fd5c-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd5c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fd5c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd5c-139">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="3fd5c-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="3fd5c-140">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3fd5c-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

