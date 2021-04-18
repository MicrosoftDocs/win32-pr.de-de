---
description: Die Win32 \_ -Klasse "devicesettings abstract, Association WMI" verknüpft ein logisches Gerät und eine Einstellung, die darauf angewendet werden kann.
ms.assetid: 4f6c4c26-8da9-4e2c-8b8c-cec658ac08d4
ms.tgt_platform: multiple
title: Win32_DeviceSettings-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceSettings
- Win32_DeviceSettings.Setting
- Win32_DeviceSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1cd9cae29cfa608c9f3c0c36ebfe3ca7f903c809
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214247"
---
# <a name="win32_devicesettings-class"></a><span data-ttu-id="a2e74-103">Win32- \_ Klasse "devicesettings"</span><span class="sxs-lookup"><span data-stu-id="a2e74-103">Win32\_DeviceSettings class</span></span>

<span data-ttu-id="a2e74-104">Die Win32-Klasse " **\_ devicesettings** abstract, Association [WMI](/windows/desktop/WmiSdk/retrieving-a-class) " verknüpft ein logisches Gerät und eine Einstellung, die darauf angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2e74-104">The **Win32\_DeviceSettings** abstract, association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device and a setting that can be applied to it.</span></span>

<span data-ttu-id="a2e74-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a2e74-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a2e74-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a2e74-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2e74-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2e74-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4FD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceSettings : CIM_ElementSetting
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="a2e74-108">Member</span><span class="sxs-lookup"><span data-stu-id="a2e74-108">Members</span></span>

<span data-ttu-id="a2e74-109">Die Win32-Klasse " **\_ devicesettings** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a2e74-109">The **Win32\_DeviceSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="a2e74-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2e74-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2e74-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2e74-111">Properties</span></span>

<span data-ttu-id="a2e74-112">Die **Win32-Klasse \_ devicesettings** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a2e74-112">The **Win32\_DeviceSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2e74-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a2e74-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2e74-114">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="a2e74-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="a2e74-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2e74-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2e74-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="a2e74-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="a2e74-117">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das die Eigenschaften des logischen Geräts darstellt, auf das die Einstellungen angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a2e74-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="a2e74-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="a2e74-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2e74-119">Datentyp: **CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="a2e74-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="a2e74-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2e74-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2e74-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM- \_ Einstellung")</span><span class="sxs-lookup"><span data-stu-id="a2e74-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="a2e74-122">Eine [**CIM- \_ Einstellung**](cim-setting.md) , die Einstellungen darstellt, die auf das logische Gerät angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a2e74-122">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2e74-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2e74-123">Remarks</span></span>

<span data-ttu-id="a2e74-124">Die **Win32-Klasse \_ devicesettings** wird von [**CIM \_ Element Setting**](cim-elementsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a2e74-124">The **Win32\_DeviceSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2e74-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2e74-125">Requirements</span></span>



| <span data-ttu-id="a2e74-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2e74-126">Requirement</span></span> | <span data-ttu-id="a2e74-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a2e74-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2e74-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2e74-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a2e74-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2e74-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2e74-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2e74-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a2e74-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2e74-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2e74-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2e74-132">Namespace</span></span><br/>                | <span data-ttu-id="a2e74-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a2e74-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2e74-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a2e74-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2e74-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a2e74-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2e74-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a2e74-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2e74-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2e74-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2e74-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2e74-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2e74-139">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="a2e74-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="a2e74-140">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="a2e74-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

