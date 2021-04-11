---
description: Das Win32- \_ volumechangeevent stellt ein lokales Laufwerk Ereignis dar, das sich aus dem Hinzufügen eines Laufwerk Buchstabens oder eines eingebundenen Laufwerks auf dem Computersystem ergibt.
ms.assetid: 38595319-d7a1-4dcd-9ad8-a27cc484b699
ms.tgt_platform: multiple
title: Win32_VolumeChangeEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VolumeChangeEvent
- Win32_VolumeChangeEvent.SECURITY_DESCRIPTOR
- Win32_VolumeChangeEvent.TIME_CREATED
- Win32_VolumeChangeEvent.EventType
- Win32_VolumeChangeEvent.DriveName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7610cae8d0cc746774b99a101e3c6aaf1f8a64d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126074"
---
# <a name="win32_volumechangeevent-class"></a><span data-ttu-id="4fb7e-103">Win32 \_ volumechangeevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="4fb7e-103">Win32\_VolumeChangeEvent class</span></span>

<span data-ttu-id="4fb7e-104">Die **Win32 \_ volumechangeevent** [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt ein lokales Laufwerk Ereignis dar, das sich aus dem Hinzufügen eines Laufwerk Buchstabens oder eines eingebundenen Laufwerks auf dem Computersystem ergibt.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-104">The **Win32\_VolumeChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents a local drive event that results from the addition of a drive letter or mounted drive on the computer system.</span></span> <span data-ttu-id="4fb7e-105">Netzwerklaufwerke werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-105">Network drives are not currently supported.</span></span>

<span data-ttu-id="4fb7e-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4fb7e-107">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb7e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fb7e-108">Syntax</span></span>

``` syntax
[UUID("455CE053-2552-4051-A3E4-C4200DC31B7"), AMENDMENT]
class Win32_VolumeChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  string DriveName;
};
```

## <a name="members"></a><span data-ttu-id="4fb7e-109">Member</span><span class="sxs-lookup"><span data-stu-id="4fb7e-109">Members</span></span>

<span data-ttu-id="4fb7e-110">Die **Win32 \_ volumechangeevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4fb7e-110">The **Win32\_VolumeChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="4fb7e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4fb7e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4fb7e-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4fb7e-112">Properties</span></span>

<span data-ttu-id="4fb7e-113">Die **Win32 \_ volumechangeevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-113">The **Win32\_VolumeChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4fb7e-114">**DriveName**</span><span class="sxs-lookup"><span data-stu-id="4fb7e-114">**DriveName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb7e-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4fb7e-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb7e-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb7e-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb7e-117">Laufwerks Name (Buchstabe), der dem System hinzugefügt oder daraus entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-117">Drive name (letter) that has been added or removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4fb7e-118">**EventType**</span><span class="sxs-lookup"><span data-stu-id="4fb7e-118">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb7e-119">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4fb7e-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fb7e-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb7e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb7e-121">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages \| WM \_ devicechange \| wParam", "Win32APIDevice Management Messages \| WM \_ settingchange")</span><span class="sxs-lookup"><span data-stu-id="4fb7e-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="4fb7e-122">Der Typ der Ereignis Änderungs Benachrichtigung, die aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-122">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="4fb7e-123">Diese Eigenschaft wird von [**Win32 \_ devicechangeevent**](win32-devicechangeevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-123">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="4fb7e-124">**Konfiguration geändert** (1)</span><span class="sxs-lookup"><span data-stu-id="4fb7e-124">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="4fb7e-125">**Geräte Ankunft** (2)</span><span class="sxs-lookup"><span data-stu-id="4fb7e-125">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="4fb7e-126">**Entfernen von Geräten** (3)</span><span class="sxs-lookup"><span data-stu-id="4fb7e-126">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="4fb7e-127">**Andocken** (4)</span><span class="sxs-lookup"><span data-stu-id="4fb7e-127">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4fb7e-128">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4fb7e-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb7e-129">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="4fb7e-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4fb7e-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb7e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb7e-131">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="4fb7e-132">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](../wmisdk/--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-132">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="4fb7e-133">Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4fb7e-133">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fb7e-134">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="4fb7e-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb7e-135">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4fb7e-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4fb7e-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb7e-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb7e-137">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-137">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="4fb7e-138">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-138">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="4fb7e-139">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-139">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="4fb7e-140">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](../wmisdk/--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-140">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="4fb7e-141">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="4fb7e-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fb7e-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fb7e-142">Remarks</span></span>

<span data-ttu-id="4fb7e-143">Die **Win32 \_ volumechangeevent** -Klasse wird von [**Win32 \_ devicechangeevent**](win32-devicechangeevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4fb7e-143">The **Win32\_VolumeChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fb7e-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fb7e-144">Requirements</span></span>



| <span data-ttu-id="4fb7e-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fb7e-145">Requirement</span></span> | <span data-ttu-id="4fb7e-146">Wert</span><span class="sxs-lookup"><span data-stu-id="4fb7e-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb7e-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fb7e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="4fb7e-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4fb7e-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4fb7e-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fb7e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="4fb7e-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fb7e-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4fb7e-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="4fb7e-151">Namespace</span></span><br/>                | <span data-ttu-id="4fb7e-152">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4fb7e-152">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4fb7e-153">MOF</span><span class="sxs-lookup"><span data-stu-id="4fb7e-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fb7e-154"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4fb7e-154"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fb7e-155">DLL</span><span class="sxs-lookup"><span data-stu-id="4fb7e-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fb7e-156"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fb7e-156"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fb7e-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fb7e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb7e-158">**Win32 \_ devicechangeevent**</span><span class="sxs-lookup"><span data-stu-id="4fb7e-158">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="4fb7e-159">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="4fb7e-159">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
