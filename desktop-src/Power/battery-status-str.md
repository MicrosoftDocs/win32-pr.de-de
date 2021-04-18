---
description: Enthält den aktuellen Zustand des Akkus.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: BATTERY_STATUS-Struktur (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: d6e68f5cec0215687fe4fde66698ea1be0d62c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351678"
---
# <a name="battery_status-structure"></a><span data-ttu-id="67b87-103">Akku \_ Status Struktur</span><span class="sxs-lookup"><span data-stu-id="67b87-103">BATTERY\_STATUS structure</span></span>

<span data-ttu-id="67b87-104">Enthält den aktuellen Zustand des Akkus.</span><span class="sxs-lookup"><span data-stu-id="67b87-104">Contains the current state of the battery.</span></span> <span data-ttu-id="67b87-105">Diese Struktur wird vom Code der [**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md) Steuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="67b87-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="67b87-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="67b87-106">Syntax</span></span>


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a><span data-ttu-id="67b87-107">Member</span><span class="sxs-lookup"><span data-stu-id="67b87-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="67b87-108">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="67b87-108">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="67b87-109">Der Akku Zustand.</span><span class="sxs-lookup"><span data-stu-id="67b87-109">The battery state.</span></span> <span data-ttu-id="67b87-110">Dieser Member kann NULL, ein oder mehrere der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="67b87-110">This member can be zero, one, or more of the following values.</span></span>



| <span data-ttu-id="67b87-111">Wert</span><span class="sxs-lookup"><span data-stu-id="67b87-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="67b87-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="67b87-112">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="67b87-113"><dt>**Akku \_ Berechnen**</dt> von <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="67b87-113"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="67b87-114">Gibt an, dass der Akku zurzeit berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="67b87-114">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="67b87-115"><dt>**Akku \_ Kritisch**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="67b87-115"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="67b87-116">Gibt an, dass Akku Fehler bevorstehend ist.</span><span class="sxs-lookup"><span data-stu-id="67b87-116">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="67b87-117">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="67b87-117">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="67b87-118"><dt>**Akku \_**</dt>" <dt>0x00000002</dt> " wird entladen</span><span class="sxs-lookup"><span data-stu-id="67b87-118"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="67b87-119">Gibt an, dass der Akku gerade entladen wird.</span><span class="sxs-lookup"><span data-stu-id="67b87-119">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="67b87-120"><dt>**Akku \_ Netzteil \_ der \_ Zeile**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="67b87-120"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="67b87-121">Gibt an, dass das System auf die Stromversorgung zugreifen kann, sodass keine Akkus entladen werden.</span><span class="sxs-lookup"><span data-stu-id="67b87-121">Indicates that the system has access to AC power, so no batteries are being discharged.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="67b87-122">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="67b87-122">**Capacity**</span></span>
</dt> <dd>

<span data-ttu-id="67b87-123">Die aktuelle Akkukapazität in MWh (oder relativ).</span><span class="sxs-lookup"><span data-stu-id="67b87-123">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="67b87-124">Dieser Wert kann verwendet werden, um eine "Benzin Messgerät"-Anzeige zu generieren, indem Sie durch das **fullchargedcapacity** -Element der [**Akku \_ Informations**](battery-information-str.md) Struktur aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="67b87-124">This value can be used to generate a "gas gauge" display by dividing it by **FullChargedCapacity** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="67b87-125">Wenn die Kapazität nicht verfügbar ist, ist das Mitglied der \_ Kapazität für unbekannte Akku \_ Kapazität.</span><span class="sxs-lookup"><span data-stu-id="67b87-125">If the capacity is unavailable, this member is BATTERY\_UNKNOWN\_CAPACITY.</span></span>

</dd> <dt>

<span data-ttu-id="67b87-126">**Spannungs**</span><span class="sxs-lookup"><span data-stu-id="67b87-126">**Voltage**</span></span>
</dt> <dd>

<span data-ttu-id="67b87-127">Die aktuelle Akku Spannung in den Akku Terminals in Millivolt (MV).</span><span class="sxs-lookup"><span data-stu-id="67b87-127">The current battery voltage across the battery terminals, in millivolts (mv).</span></span> <span data-ttu-id="67b87-128">Wenn die Spannung nicht verfügbar ist, ist dieser Member eine Akku- \_ unbekannte \_ Spannung.</span><span class="sxs-lookup"><span data-stu-id="67b87-128">If the voltage is unavailable, this member is BATTERY\_UNKNOWN\_VOLTAGE.</span></span>

</dd> <dt>

<span data-ttu-id="67b87-129">**Rate**</span><span class="sxs-lookup"><span data-stu-id="67b87-129">**Rate**</span></span>
</dt> <dd>

<span data-ttu-id="67b87-130">Die aktuelle Rate der Akku Gebühren oder-Entladung.</span><span class="sxs-lookup"><span data-stu-id="67b87-130">The current rate of battery charge or discharge.</span></span> <span data-ttu-id="67b87-131">Dieser Wert wird in Milliwatt angegeben, es sei denn, die Akku rateninformationen sind relativ. in diesem Fall werden Sie in willkürlichen Einheiten pro Stunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="67b87-131">This value will be in milliwatts unless the battery rate information is relative, in which case it will be in arbitrary units per hour.</span></span> <span data-ttu-id="67b87-132">Um zu ermitteln, ob die Akku Informationen relativ sind, überprüfen Sie das Flag für die Akkukapazität in den Funktions Elementen der \_ \_ [**Akku \_ Informations**](battery-information-str.md) Struktur. </span><span class="sxs-lookup"><span data-stu-id="67b87-132">To determine if battery information is relative, examine the BATTERY\_CAPACITY\_RELATIVE flag in the **Capabilities** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="67b87-133">Ein positiver Wert ungleich 0 (null) gibt das berechnen an; ein negativer Satz weist auf das Entladen hin.</span><span class="sxs-lookup"><span data-stu-id="67b87-133">A nonzero, positive rate indicates charging; a negative rate indicates discharging.</span></span> <span data-ttu-id="67b87-134">Einige Akkus melden nur die Gebühren für die Entladung.</span><span class="sxs-lookup"><span data-stu-id="67b87-134">Some batteries report only discharging rates.</span></span> <span data-ttu-id="67b87-135">Wenn die Rate nicht verfügbar ist, ist dieser Mitglied der Akku- \_ Unknown- \_ Rate.</span><span class="sxs-lookup"><span data-stu-id="67b87-135">If the rate is unavailable, this member is BATTERY\_UNKNOWN\_RATE.</span></span> <span data-ttu-id="67b87-136">Wenn sich der Zustand des Akkus oder der Stromquelle ändert, kann die Rate verfügbar werden.</span><span class="sxs-lookup"><span data-stu-id="67b87-136">If the state of the battery or power source changes, the rate may become available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67b87-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67b87-137">Remarks</span></span>

<span data-ttu-id="67b87-138">Das \_ Flag "Akku kritisch" im **PowerState** -Member dieser Struktur weist auf eine Hardware-"Akku kritisch"-Bedingung hin.</span><span class="sxs-lookup"><span data-stu-id="67b87-138">The BATTERY\_CRITICAL flag in the **PowerState** member of this structure indicates a hardware "battery critical" condition.</span></span> <span data-ttu-id="67b87-139">Diese kritische Ebene wird vom Akku Hersteller festgelegt, nicht vom Benutzer im "kritischen Akku Alarm".</span><span class="sxs-lookup"><span data-stu-id="67b87-139">This critical level is set by the battery manufacturer, not by the user in the "critical battery alarm."</span></span> <span data-ttu-id="67b87-140">Im Allgemeinen bedeutet dies, dass das Akku System errechnet hat, dass der Akku vollständig erschöpft ist, und jede Stromversorgung überschreitet, was erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="67b87-140">It generally means that the battery system has calculated that the battery is totally drained, and any power being drawn is beyond what is expected.</span></span>

## <a name="requirements"></a><span data-ttu-id="67b87-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67b87-141">Requirements</span></span>



| <span data-ttu-id="67b87-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67b87-142">Requirement</span></span> | <span data-ttu-id="67b87-143">Wert</span><span class="sxs-lookup"><span data-stu-id="67b87-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67b87-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67b87-144">Minimum supported client</span></span><br/> | <span data-ttu-id="67b87-145">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67b87-145">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="67b87-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67b87-146">Minimum supported server</span></span><br/> | <span data-ttu-id="67b87-147">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67b87-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="67b87-148">Header</span><span class="sxs-lookup"><span data-stu-id="67b87-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="67b87-149"><dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="67b87-149"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67b87-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67b87-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67b87-151">**Akku \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="67b87-151">**BATTERY\_INFORMATION**</span></span>](battery-information-str.md)
</dt> <dt>

[<span data-ttu-id="67b87-152">**IOCTL \_ Akku \_ Query- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="67b87-152">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> </dl>

 

 




