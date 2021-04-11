---
description: Die \_ WMI-Klasse der Win32-printersetting-Zuordnung bezieht einen Drucker und seine Konfigurationseinstellungen ein.
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Win32_PrinterSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90a77678e61b755550ebb1818c34ccdc3159a88c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214160"
---
# <a name="win32_printersetting-class"></a><span data-ttu-id="a5564-103">Win32- \_ Klasse "printersetting"</span><span class="sxs-lookup"><span data-stu-id="a5564-103">Win32\_PrinterSetting class</span></span>

<span data-ttu-id="a5564-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32- \_ printersetting** -Zuordnung bezieht einen Drucker und seine Konfigurationseinstellungen ein.</span><span class="sxs-lookup"><span data-stu-id="a5564-104">The **Win32\_PrinterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and its configuration settings.</span></span>

<span data-ttu-id="a5564-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a5564-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a5564-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a5564-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5564-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5564-107">Syntax</span></span>

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="a5564-108">Member</span><span class="sxs-lookup"><span data-stu-id="a5564-108">Members</span></span>

<span data-ttu-id="a5564-109">Die Win32-Klasse " **\_ printersetting** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a5564-109">The **Win32\_PrinterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="a5564-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5564-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5564-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5564-111">Properties</span></span>

<span data-ttu-id="a5564-112">Die Win32-Klasse " **\_ printersetting** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a5564-112">The **Win32\_PrinterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5564-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a5564-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5564-114">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="a5564-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="a5564-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5564-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5564-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="a5564-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="a5564-117">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das die Eigenschaften des logischen Geräts darstellt, auf das die Einstellungen angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a5564-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

<span data-ttu-id="a5564-118">Diese Eigenschaft wird von [**Win32- \_**](win32-devicesettings.md)Geräte-Debug-Elementen geerbt.</span><span class="sxs-lookup"><span data-stu-id="a5564-118">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5564-119">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="a5564-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5564-120">Datentyp: **CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="a5564-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="a5564-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a5564-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5564-122">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM- \_ Einstellung")</span><span class="sxs-lookup"><span data-stu-id="a5564-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="a5564-123">Eine [**CIM- \_ Einstellung**](cim-setting.md) , die Einstellungen darstellt, die auf das logische Gerät angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a5564-123">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

<span data-ttu-id="a5564-124">Diese Eigenschaft wird von [**Win32- \_**](win32-devicesettings.md)Geräte-Debug-Elementen geerbt.</span><span class="sxs-lookup"><span data-stu-id="a5564-124">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5564-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5564-125">Remarks</span></span>

<span data-ttu-id="a5564-126">Die Win32-Klasse " **\_ printersetting** " wird von [**Win32- \_ devicesettings**](win32-devicesettings.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a5564-126">The **Win32\_PrinterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5564-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5564-127">Requirements</span></span>



| <span data-ttu-id="a5564-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5564-128">Requirement</span></span> | <span data-ttu-id="a5564-129">Wert</span><span class="sxs-lookup"><span data-stu-id="a5564-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5564-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5564-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a5564-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5564-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="a5564-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5564-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a5564-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5564-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="a5564-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5564-134">Namespace</span></span><br/>                | <span data-ttu-id="a5564-135">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a5564-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="a5564-136">MOF</span><span class="sxs-lookup"><span data-stu-id="a5564-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5564-137"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a5564-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5564-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a5564-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5564-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5564-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="a5564-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5564-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5564-141">**Win32-Geräte-Manager \_**</span><span class="sxs-lookup"><span data-stu-id="a5564-141">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="a5564-142">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="a5564-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
