---
description: Enthält Informationen zu den Bedingungen, unter denen der Akku Status abgerufen werden soll.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: BATTERY_WAIT_STATUS-Struktur (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 08d1e3b85d22122426f1e4648f47a808468bfb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351677"
---
# <a name="battery_wait_status-structure"></a><span data-ttu-id="594bb-103">\_ \_ Status Struktur der Akku Wartezeit</span><span class="sxs-lookup"><span data-stu-id="594bb-103">BATTERY\_WAIT\_STATUS structure</span></span>

<span data-ttu-id="594bb-104">Enthält Informationen zu den Bedingungen, unter denen der Akku Status abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="594bb-104">Contains information about the conditions under which the battery status is to be retrieved.</span></span> <span data-ttu-id="594bb-105">Diese Struktur wird vom Code der [**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md) Steuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="594bb-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="594bb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="594bb-106">Syntax</span></span>


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a><span data-ttu-id="594bb-107">Member</span><span class="sxs-lookup"><span data-stu-id="594bb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="594bb-108">**Batterytag**</span><span class="sxs-lookup"><span data-stu-id="594bb-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="594bb-109">Das aktuelle Akku Kennzeichen für den Akku.</span><span class="sxs-lookup"><span data-stu-id="594bb-109">The current battery tag for the battery.</span></span> <span data-ttu-id="594bb-110">Es können nur Informationen zu einem Akku zurückgegeben werden, der mit dem Tag übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="594bb-110">Only information for a battery matching the tag can be returned.</span></span> <span data-ttu-id="594bb-111">Wenn dieser Wert nicht mit dem aktuellen Tag des Akkus identisch ist, misslingt der [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Vorgang mit dem Fehlercode "Fehler \_ Datei \_ nicht \_ gefunden", was dem Aufrufer anzeigt, dass der Akku, für den er ein Tag besitzt, nicht mehr installiert ist. der Aufrufer kann den [**IOCTL- \_ Akku \_ abfragetagvorgang \_**](ioctl-battery-query-tag.md) verwenden, um ggf</span><span class="sxs-lookup"><span data-stu-id="594bb-111">Whenever this value does not match the battery's current tag, the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) operation will fail with an error code of ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag is no longer installed The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if any.</span></span> <span data-ttu-id="594bb-112">Außerdem wird der Vorgang abgebrochen, wenn die Anforderung beim Entfernen des Akkus oder das Tag geändert wird, und der Status der Fehler \_ Datei wurde \_ nicht \_ gefunden.</span><span class="sxs-lookup"><span data-stu-id="594bb-112">In addition, if the request is in progress when the battery is removed, or the tag changes, the operation is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="594bb-113">(Weitere Informationen finden Sie unter [Akku-Tags](battery-information.md) .)</span><span class="sxs-lookup"><span data-stu-id="594bb-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

</dd> <dt>

<span data-ttu-id="594bb-114">**Timeout**</span><span class="sxs-lookup"><span data-stu-id="594bb-114">**Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="594bb-115">Die Anzahl der Millisekunden, die die Anforderung auf die von den Elementen " **PowerState**", " **lowcapacity**" und " **highcapacity** " angegebene Bedingung wartet, bevor Sie abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="594bb-115">The number of milliseconds the request will wait for the condition specified by the **PowerState**, **LowCapacity**, and **HighCapacity** members before completing.</span></span> <span data-ttu-id="594bb-116">Der Wert-1 gibt an, dass die Anforderung unbegrenzt wartet, bis die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="594bb-116">A value of -1 indicates that the request will wait indefinitely for the conditions to be satisfied.</span></span> <span data-ttu-id="594bb-117">Der Wert 0 (null) gibt an, dass die angeforderten Akku Informationen unabhängig von den anderen Bedingungen sofort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="594bb-117">A value of zero indicates that the requested battery information is to be returned immediately, regardless of the other conditions.</span></span> <span data-ttu-id="594bb-118">Jeder andere Wert gibt an, dass die Anforderung auf die Zeitspanne warten soll, oder bis eine der anderen Bedingungen erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="594bb-118">Any other value indicates that the request should wait that length of time, or until any one of the other conditions is satisfied.</span></span>

<span data-ttu-id="594bb-119">Wenn sich der Computer im Energiesparmodus befindet, wird die Uhr weiterhin ausgeführt, aber die Anzahl der Ausschöpfung wird den Computer nicht verbleiben.</span><span class="sxs-lookup"><span data-stu-id="594bb-119">If the computer has entered sleep mode, the clock will continue to run, but exhausting the count will not wake the computer up.</span></span> <span data-ttu-id="594bb-120">Wenn die Anzahl erschöpft ist, wenn der Computer aktiviert ist, und andere Bedingungen erfüllt sind, wird der-Rückruf sofort beim Erwachen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="594bb-120">If the count is exhausted when the computer is awoken, and other conditions are satisfied, the call will return immediately on awakening.</span></span>

</dd> <dt>

<span data-ttu-id="594bb-121">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="594bb-121">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="594bb-122">NULL, mindestens eine der folgenden Status Bits, die den Zustand des Akkus angeben.</span><span class="sxs-lookup"><span data-stu-id="594bb-122">Zero, one, or more of the following status bits, which indicate the state of the battery.</span></span> <span data-ttu-id="594bb-123">Es ist identisch mit dem **PowerState** -Member der [**Akku \_ Status**](battery-status-str.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="594bb-123">It is identical to the **PowerState** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>



| <span data-ttu-id="594bb-124">Wert</span><span class="sxs-lookup"><span data-stu-id="594bb-124">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="594bb-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="594bb-125">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="594bb-126"><dt>**Akku \_ Berechnen**</dt> von <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="594bb-126"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="594bb-127">Gibt an, dass der Akku zurzeit berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="594bb-127">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="594bb-128"><dt>**Akku \_ Kritisch**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="594bb-128"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="594bb-129">Gibt an, dass Akku Fehler bevorstehend ist.</span><span class="sxs-lookup"><span data-stu-id="594bb-129">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="594bb-130">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="594bb-130">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="594bb-131"><dt>**Akku \_**</dt>" <dt>0x00000002</dt> " wird entladen</span><span class="sxs-lookup"><span data-stu-id="594bb-131"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="594bb-132">Gibt an, dass der Akku gerade entladen wird.</span><span class="sxs-lookup"><span data-stu-id="594bb-132">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="594bb-133"><dt>**Akku \_ Netzteil \_ der \_ Zeile**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="594bb-133"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="594bb-134">Gibt an, dass der Akku Zugang zur Stromversorgung hat.</span><span class="sxs-lookup"><span data-stu-id="594bb-134">Indicates that the battery has access to AC power.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="594bb-135">**Lowcapacity**</span><span class="sxs-lookup"><span data-stu-id="594bb-135">**LowCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="594bb-136">Die aktuelle Akkukapazität in MWh (oder relativ).</span><span class="sxs-lookup"><span data-stu-id="594bb-136">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="594bb-137">Dieser Wert ist identisch mit dem **Capacity** -Member der [**Akku \_ Status**](battery-status-str.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="594bb-137">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="594bb-138">**Highcapacity**</span><span class="sxs-lookup"><span data-stu-id="594bb-138">**HighCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="594bb-139">Die aktuelle Akkukapazität in MWh (oder relativ).</span><span class="sxs-lookup"><span data-stu-id="594bb-139">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="594bb-140">Dieser Wert ist identisch mit dem **Capacity** -Member der [**Akku \_ Status**](battery-status-str.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="594bb-140">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="594bb-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="594bb-141">Remarks</span></span>

<span data-ttu-id="594bb-142">Die Anforderungen für Akku Informationen werden bis zu einem der folgenden Punkte verschoben:</span><span class="sxs-lookup"><span data-stu-id="594bb-142">Requests for battery information are postponed until one of the following occurs:</span></span>

-   <span data-ttu-id="594bb-143">Das Timeout läuft ab (vorausgesetzt, **Timeout** ist nicht-1).</span><span class="sxs-lookup"><span data-stu-id="594bb-143">The time-out expires (assuming **Timeout** is not -1).</span></span>
-   <span data-ttu-id="594bb-144">Der aktuelle Status des Akkus stimmt nicht mit dem **PowerState**-Wert.</span><span class="sxs-lookup"><span data-stu-id="594bb-144">The battery's current status does not match **PowerState**.</span></span>
-   <span data-ttu-id="594bb-145">Die Kapazität des Akkus liegt unter **lowcapacity**.</span><span class="sxs-lookup"><span data-stu-id="594bb-145">The battery's capacity is below **LowCapacity**.</span></span>
-   <span data-ttu-id="594bb-146">Die Kapazität des Akkus liegt über der **highcapacity**.</span><span class="sxs-lookup"><span data-stu-id="594bb-146">The battery's capacity is above **HighCapacity**.</span></span>
-   <span data-ttu-id="594bb-147">Das Akku-Tag ändert sich.</span><span class="sxs-lookup"><span data-stu-id="594bb-147">The battery tag changes.</span></span>

<span data-ttu-id="594bb-148">Wenn eine dieser Bedingungen erfüllt ist, werden die Daten gesammelt und der Vorgang zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="594bb-148">When any one of these conditions is satisfied, the data is collected and the operation returns.</span></span> <span data-ttu-id="594bb-149">Dadurch können Anwendungen typische dynamische Akku Informationen überwachen, ohne das Gerät abzufragen.</span><span class="sxs-lookup"><span data-stu-id="594bb-149">This allows applications to monitor typical dynamic battery information without polling the device.</span></span>

<span data-ttu-id="594bb-150">Bevor Sie eine der beiden Kapazitäts Bedingungen verwenden, stellen Sie sicher, dass der Akku diese unterstützt, indem Sie den Code der [**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md) Steuerung mit einem Timeout von 0 (null) verwenden.</span><span class="sxs-lookup"><span data-stu-id="594bb-150">Before using either of the two Capacity conditions, make sure the battery supports them by using the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code with a time-out of zero.</span></span> <span data-ttu-id="594bb-151">Überprüfen Sie die Ergebnisse, um zu bestimmen, ob das **Kapazitäts** Mitglied unterstützt wird \_ \_</span><span class="sxs-lookup"><span data-stu-id="594bb-151">Examine the results to determine if the **Capacity** member is supported (that is, not BATTERY\_UNKNOWN\_CAPACITY).</span></span>

## <a name="requirements"></a><span data-ttu-id="594bb-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="594bb-152">Requirements</span></span>



| <span data-ttu-id="594bb-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="594bb-153">Requirement</span></span> | <span data-ttu-id="594bb-154">Wert</span><span class="sxs-lookup"><span data-stu-id="594bb-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="594bb-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="594bb-155">Minimum supported client</span></span><br/> | <span data-ttu-id="594bb-156">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="594bb-156">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="594bb-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="594bb-157">Minimum supported server</span></span><br/> | <span data-ttu-id="594bb-158">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="594bb-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="594bb-159">Header</span><span class="sxs-lookup"><span data-stu-id="594bb-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="594bb-160"><dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="594bb-160"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="594bb-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="594bb-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="594bb-162">**Akku \_ Status**</span><span class="sxs-lookup"><span data-stu-id="594bb-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="594bb-163">**IOCTL \_ Akku \_ Query- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="594bb-163">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="594bb-164">**IOCTL \_ Akku \_ - \_ abfragetag**</span><span class="sxs-lookup"><span data-stu-id="594bb-164">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

