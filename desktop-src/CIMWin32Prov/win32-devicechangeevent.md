---
description: Die \_ WMI-Klasse "Win32 devicechangeevent abstract" stellt Geräte Änderungs Ereignisse dar, die sich aus dem Hinzufügen, entfernen oder Ändern von Geräten im Computersystem ergeben.
ms.assetid: 78155357-4231-4ded-980e-89feeb864ef2
ms.tgt_platform: multiple
title: Win32_DeviceChangeEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceChangeEvent
- Win32_DeviceChangeEvent.SECURITY_DESCRIPTOR
- Win32_DeviceChangeEvent.TIME_CREATED
- Win32_DeviceChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f97ab262d95b70a69b06e15202a78d5c1364f90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749032"
---
# <a name="win32_devicechangeevent-class"></a><span data-ttu-id="072a2-103">Win32 \_ devicechangeevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="072a2-103">Win32\_DeviceChangeEvent class</span></span>

<span data-ttu-id="072a2-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ devicechangeevent** abstract" stellt Geräte Änderungs Ereignisse dar, die sich aus dem Hinzufügen, entfernen oder Ändern von Geräten im Computersystem ergeben.</span><span class="sxs-lookup"><span data-stu-id="072a2-104">The **Win32\_DeviceChangeEvent** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents device change events that result from the addition, removal, or modification of devices on the computer system.</span></span> <span data-ttu-id="072a2-105">Dies umfasst Änderungen an der Hardwarekonfiguration (Andocken und Andocken), den Hardware Status oder neu zugeordnete Geräte (Zuordnung eines Netz Laufwerks).</span><span class="sxs-lookup"><span data-stu-id="072a2-105">This includes changes in the hardware configuration (docking and undocking), the hardware state, or newly mapped devices (mapping of a network drive).</span></span> <span data-ttu-id="072a2-106">Beispielsweise wurde ein Gerät geändert, wenn eine "WM \_ devicechange"-Meldung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="072a2-106">For example, a device has changed when a WM\_DEVICECHANGE message is sent.</span></span>

<span data-ttu-id="072a2-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="072a2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="072a2-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="072a2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="072a2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="072a2-109">Syntax</span></span>

``` syntax
[UUID("0DE6AAF8-49F1-4868-B3D4-61CB69BA4322"), AMENDMENT]
class Win32_DeviceChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="072a2-110">Member</span><span class="sxs-lookup"><span data-stu-id="072a2-110">Members</span></span>

<span data-ttu-id="072a2-111">Die **Win32 \_ devicechangeevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="072a2-111">The **Win32\_DeviceChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="072a2-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="072a2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="072a2-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="072a2-113">Properties</span></span>

<span data-ttu-id="072a2-114">Die **Win32 \_ devicechangeevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="072a2-114">The **Win32\_DeviceChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="072a2-115">**EventType**</span><span class="sxs-lookup"><span data-stu-id="072a2-115">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="072a2-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="072a2-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="072a2-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="072a2-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="072a2-118">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management Messages \| WM \_ devicechange \| wParam", "Win32APIDevice Management Messages \| WM \_ settingchange")</span><span class="sxs-lookup"><span data-stu-id="072a2-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="072a2-119">Der Typ der Ereignis Änderungs Benachrichtigung, die aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="072a2-119">Type of event change notification that has occurred.</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="072a2-120">**Konfiguration geändert** (1)</span><span class="sxs-lookup"><span data-stu-id="072a2-120">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="072a2-121">**Geräte Ankunft** (2)</span><span class="sxs-lookup"><span data-stu-id="072a2-121">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="072a2-122">**Entfernen von Geräten** (3)</span><span class="sxs-lookup"><span data-stu-id="072a2-122">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="072a2-123">**Andocken** (4)</span><span class="sxs-lookup"><span data-stu-id="072a2-123">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="072a2-124">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="072a2-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="072a2-125">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="072a2-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="072a2-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="072a2-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="072a2-127">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="072a2-127">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="072a2-128">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](/windows/desktop/WmiSdk/--event)geerbt.</span><span class="sxs-lookup"><span data-stu-id="072a2-128">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="072a2-129">Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="072a2-129">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="072a2-130">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="072a2-130">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="072a2-131">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="072a2-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="072a2-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="072a2-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="072a2-133">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="072a2-133">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="072a2-134">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="072a2-134">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="072a2-135">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="072a2-135">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="072a2-136">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](/windows/desktop/WmiSdk/--event)geerbt.</span><span class="sxs-lookup"><span data-stu-id="072a2-136">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="072a2-137">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="072a2-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="072a2-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="072a2-138">Remarks</span></span>

<span data-ttu-id="072a2-139">Das **Win32 \_ devicechangeevent** ist eine abstrakte Klasse, die von [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="072a2-139">The **Win32\_DeviceChangeEvent** is an abstract class derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="072a2-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="072a2-140">Requirements</span></span>



| <span data-ttu-id="072a2-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="072a2-141">Requirement</span></span> | <span data-ttu-id="072a2-142">Wert</span><span class="sxs-lookup"><span data-stu-id="072a2-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="072a2-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="072a2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="072a2-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="072a2-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="072a2-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="072a2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="072a2-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="072a2-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="072a2-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="072a2-147">Namespace</span></span><br/>                | <span data-ttu-id="072a2-148">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="072a2-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="072a2-149">MOF</span><span class="sxs-lookup"><span data-stu-id="072a2-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="072a2-150"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="072a2-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="072a2-151">DLL</span><span class="sxs-lookup"><span data-stu-id="072a2-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="072a2-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="072a2-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="072a2-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="072a2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="072a2-154">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="072a2-154">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

<span data-ttu-id="072a2-155">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="072a2-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

