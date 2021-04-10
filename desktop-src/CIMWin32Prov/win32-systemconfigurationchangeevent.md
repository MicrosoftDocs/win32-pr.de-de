---
description: Das Win32 \_ systemconfigurationchangeevent-&\# 8194; WMI-Klasse gibt an, dass die Geräteliste im System aktualisiert wurde (ein Gerät wurde hinzugefügt oder entfernt, oder die Konfiguration wurde geändert).
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Win32_SystemConfigurationChangeEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0bc479d3415906a6536c6df1d163056e94e2af76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127444"
---
# <a name="win32_systemconfigurationchangeevent-class"></a><span data-ttu-id="ac81c-103">Win32 \_ systemconfigurationchangeevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="ac81c-103">Win32\_SystemConfigurationChangeEvent class</span></span>

<span data-ttu-id="ac81c-104">Die **Win32 \_ systemconfigurationchangeevent** [WMI-Klasse](../wmisdk/retrieving-a-class.md) gibt an, dass die Geräteliste im System aktualisiert wurde (ein Gerät wurde hinzugefügt oder entfernt, oder die Konfiguration wurde geändert).</span><span class="sxs-lookup"><span data-stu-id="ac81c-104">The **Win32\_SystemConfigurationChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) indicates that the device list on the system has been refreshed (a device has been added or removed, or the configuration changed).</span></span> <span data-ttu-id="ac81c-105">Ein Ereignis wird ausgelöst, und eine Instanz dieser Klasse wird erstellt, wenn die Meldung "devmgrerfrischendes on<*Computername*>" gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="ac81c-105">An event is fired and an instance of this is class created when the "DevMgrRefreshOn<*ComputerName*>" message is sent.</span></span> <span data-ttu-id="ac81c-106">Die genaue Änderung der Geräteliste ist nicht in der Nachricht enthalten. Daher ist eine Geräte Aktualisierung erforderlich, um die aktuellen Systemeinstellungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ac81c-106">The exact change to the device list is not contained in the message, so a device refresh is required to obtain the current system settings.</span></span> <span data-ttu-id="ac81c-107">Es folgen Beispiele für Änderungen an der Konfiguration, die sich auf die Einstellungen von "Iran", com-Ports und BIOS</span><span class="sxs-lookup"><span data-stu-id="ac81c-107">Examples of configuration changes affected are IRQ settings, COM ports, and BIOS versions.</span></span>

<span data-ttu-id="ac81c-108">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac81c-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ac81c-109">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="ac81c-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac81c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac81c-110">Syntax</span></span>

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="ac81c-111">Member</span><span class="sxs-lookup"><span data-stu-id="ac81c-111">Members</span></span>

<span data-ttu-id="ac81c-112">Die **Win32 \_ systemconfigurationchangeevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ac81c-112">The **Win32\_SystemConfigurationChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ac81c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac81c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac81c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac81c-114">Properties</span></span>

<span data-ttu-id="ac81c-115">Die **Win32 \_ systemconfigurationchangeevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac81c-115">The **Win32\_SystemConfigurationChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac81c-116">**EventType**</span><span class="sxs-lookup"><span data-stu-id="ac81c-116">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac81c-117">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac81c-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac81c-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac81c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac81c-119">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages \| WM \_ devicechange \| wParam", "Win32APIDevice Management Messages \| WM \_ settingchange")</span><span class="sxs-lookup"><span data-stu-id="ac81c-119">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="ac81c-120">Der Typ der Ereignis Änderungs Benachrichtigung, die aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ac81c-120">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="ac81c-121">Diese Eigenschaft wird von [**Win32 \_ devicechangeevent**](win32-devicechangeevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ac81c-121">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="ac81c-122">**Konfiguration geändert** (1)</span><span class="sxs-lookup"><span data-stu-id="ac81c-122">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="ac81c-123">**Geräte Ankunft** (2)</span><span class="sxs-lookup"><span data-stu-id="ac81c-123">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="ac81c-124">**Entfernen von Geräten** (3)</span><span class="sxs-lookup"><span data-stu-id="ac81c-124">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="ac81c-125">**Andocken** (4)</span><span class="sxs-lookup"><span data-stu-id="ac81c-125">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac81c-126">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac81c-126">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac81c-127">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="ac81c-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ac81c-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac81c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac81c-129">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="ac81c-129">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="ac81c-130">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](../wmisdk/--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ac81c-130">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="ac81c-131">Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ac81c-131">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac81c-132">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="ac81c-132">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac81c-133">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ac81c-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ac81c-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac81c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac81c-135">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ac81c-135">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="ac81c-136">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="ac81c-136">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="ac81c-137">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="ac81c-137">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="ac81c-138">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](../wmisdk/--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ac81c-138">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="ac81c-139">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ac81c-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac81c-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac81c-140">Remarks</span></span>

<span data-ttu-id="ac81c-141">Die **Win32 \_ systemconfigurationchangeevent** -Klasse wird von [**Win32 \_ devicechangeevent**](win32-devicechangeevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ac81c-141">The **Win32\_SystemConfigurationChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac81c-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac81c-142">Requirements</span></span>



| <span data-ttu-id="ac81c-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac81c-143">Requirement</span></span> | <span data-ttu-id="ac81c-144">Wert</span><span class="sxs-lookup"><span data-stu-id="ac81c-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac81c-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac81c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ac81c-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac81c-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ac81c-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac81c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ac81c-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac81c-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ac81c-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac81c-149">Namespace</span></span><br/>                | <span data-ttu-id="ac81c-150">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ac81c-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ac81c-151">MOF</span><span class="sxs-lookup"><span data-stu-id="ac81c-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac81c-152"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ac81c-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac81c-153">DLL</span><span class="sxs-lookup"><span data-stu-id="ac81c-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac81c-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac81c-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac81c-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac81c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac81c-156">**Win32 \_ devicechangeevent**</span><span class="sxs-lookup"><span data-stu-id="ac81c-156">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="ac81c-157">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="ac81c-157">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
