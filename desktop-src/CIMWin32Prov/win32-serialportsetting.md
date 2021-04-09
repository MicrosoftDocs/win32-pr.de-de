---
description: Die \_ WMI-Klasse Win32 serialportsetting Association verknüpft einen seriellen Anschluss und seine Konfigurationseinstellungen.
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Win32_SerialPortSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958199"
---
# <a name="win32_serialportsetting-class"></a><span data-ttu-id="439a5-103">Win32 \_ serialportsetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="439a5-103">Win32\_SerialPortSetting class</span></span>

<span data-ttu-id="439a5-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ serialportsetting** Association verknüpft einen seriellen Anschluss und seine Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="439a5-104">The **Win32\_SerialPortSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a serial port and its configuration settings.</span></span>

<span data-ttu-id="439a5-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="439a5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="439a5-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="439a5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="439a5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="439a5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="439a5-108">Member</span><span class="sxs-lookup"><span data-stu-id="439a5-108">Members</span></span>

<span data-ttu-id="439a5-109">Die **Win32 \_ serialportsetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="439a5-109">The **Win32\_SerialPortSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="439a5-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="439a5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="439a5-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="439a5-111">Properties</span></span>

<span data-ttu-id="439a5-112">Die **Win32 \_ serialportsetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="439a5-112">The **Win32\_SerialPortSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="439a5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="439a5-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="439a5-114">Datentyp: **Win32- \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="439a5-114">Data type: **Win32\_SerialPort**</span></span>
</dt> <dt>

<span data-ttu-id="439a5-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="439a5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="439a5-116">Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")</span><span class="sxs-lookup"><span data-stu-id="439a5-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPort")</span></span>
</dt> </dl>

<span data-ttu-id="439a5-117">Ein [**Win32- \_ SerialPort**](win32-serialport.md) , der die Eigenschaften eines seriellen Anschlusses auf dem Computersystem enthält.</span><span class="sxs-lookup"><span data-stu-id="439a5-117">A [**Win32\_SerialPort**](win32-serialport.md) that contains the properties of a serial port on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="439a5-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="439a5-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="439a5-119">Datentyp: **Win32 \_ serialportconfiguration**</span><span class="sxs-lookup"><span data-stu-id="439a5-119">Data type: **Win32\_SerialPortConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="439a5-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="439a5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="439a5-121">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ serialportconfiguration")</span><span class="sxs-lookup"><span data-stu-id="439a5-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPortConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="439a5-122">Eine [**Win32- \_ serialportconfiguration**](win32-serialportconfiguration.md) , die die Konfigurationseinstellung für den seriellen Anschluss enthält.</span><span class="sxs-lookup"><span data-stu-id="439a5-122">A [**Win32\_SerialPortConfiguration**](win32-serialportconfiguration.md) that contains the configuration setting for the serial port.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="439a5-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="439a5-123">Remarks</span></span>

<span data-ttu-id="439a5-124">Die Win32-Klasse " **\_ serialportsetting** " wird von [**Win32- \_ devicesettings**](win32-devicesettings.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="439a5-124">The **Win32\_SerialPortSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="439a5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="439a5-125">Requirements</span></span>



| <span data-ttu-id="439a5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="439a5-126">Requirement</span></span> | <span data-ttu-id="439a5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="439a5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="439a5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="439a5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="439a5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="439a5-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="439a5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="439a5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="439a5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="439a5-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="439a5-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="439a5-132">Namespace</span></span><br/>                | <span data-ttu-id="439a5-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="439a5-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="439a5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="439a5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="439a5-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="439a5-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="439a5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="439a5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="439a5-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="439a5-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="439a5-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="439a5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="439a5-139">**Win32-Geräte-Manager \_**</span><span class="sxs-lookup"><span data-stu-id="439a5-139">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="439a5-140">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="439a5-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
