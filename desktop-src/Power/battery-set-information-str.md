---
description: Enthält Akku Informationen, die festgelegt werden sollen.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: BATTERY_SET_INFORMATION-Struktur (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 0b23489bc5a7608e2e8afb297bb4be7ba35cecb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131673"
---
# <a name="battery_set_information-structure"></a><span data-ttu-id="40186-103">Struktur der Batterie \_ Satz \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="40186-103">BATTERY\_SET\_INFORMATION structure</span></span>

<span data-ttu-id="40186-104">Enthält Akku Informationen, die festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="40186-104">Contains battery information to be set.</span></span> <span data-ttu-id="40186-105">Diese Struktur wird zusammen mit dem [**ioctl-Code für die \_ Akku \_ Satz \_ Informationen**](ioctl-battery-set-information.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="40186-105">This structure is used with the [**IOCTL\_BATTERY\_SET\_INFORMATION**](ioctl-battery-set-information.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="40186-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="40186-106">Syntax</span></span>


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="40186-107">Member</span><span class="sxs-lookup"><span data-stu-id="40186-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="40186-108">**Batterytag**</span><span class="sxs-lookup"><span data-stu-id="40186-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="40186-109">Das aktuelle Akku Kennzeichen für den Akku.</span><span class="sxs-lookup"><span data-stu-id="40186-109">The current battery tag for the battery.</span></span> <span data-ttu-id="40186-110">Informationen zu einem Akku, der mit dem Tag übereinstimmt, können nur zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="40186-110">Information for a battery matching the tag can only be returned.</span></span> <span data-ttu-id="40186-111">Wenn dieser Wert nicht mit dem aktuellen Tag des Akkus identisch ist, wird die ioctl-Anforderung mit der Fehler \_ Datei "nicht gefunden" abgeschlossen, was dem Aufrufer anzeigt, \_ \_ dass der Akku, für den er ein Tag besitzt, nicht mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="40186-111">Whenever this value does not match the battery's current tag, the IOCTL request will be completed with ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag for no longer exists.</span></span> <span data-ttu-id="40186-112">Der Aufrufer kann den [**IOCTL- \_ Akku- \_ abfragetagvorgang \_**](ioctl-battery-query-tag.md) verwenden, um das Tag des neu installierten Akkus zu ermitteln, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="40186-112">The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if one exists.</span></span> <span data-ttu-id="40186-113">(Weitere Informationen finden Sie unter [Akku-Tags](battery-information.md) .)</span><span class="sxs-lookup"><span data-stu-id="40186-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

<span data-ttu-id="40186-114">Wenn eine Abfrage Informationsanforderung erfolgt, wird dieser Wert überprüft.</span><span class="sxs-lookup"><span data-stu-id="40186-114">When a query information request is made, this value is verified.</span></span> <span data-ttu-id="40186-115">Wenn die Anforderung ausgeführt wird, während sich dieser Wert ändert, wird die Anforderung mit dem Status "Fehler \_ Datei nicht gefunden" abgebrochen \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="40186-115">In addition, if the request is in progress while this value changes, the request is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="40186-116">**Informationlevel**</span><span class="sxs-lookup"><span data-stu-id="40186-116">**InformationLevel**</span></span>
</dt> <dd>

<span data-ttu-id="40186-117">Die Akku Informationen, die festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="40186-117">The battery information to be set.</span></span> <span data-ttu-id="40186-118">Der Typ der Daten im **Puffer** Element hängt vom Wert dieses Members ab.</span><span class="sxs-lookup"><span data-stu-id="40186-118">The type of data in the **Buffer** member depends on the value of this member.</span></span> <span data-ttu-id="40186-119">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="40186-119">This member can be one of the following values.</span></span>



| <span data-ttu-id="40186-120">Wert</span><span class="sxs-lookup"><span data-stu-id="40186-120">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="40186-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="40186-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <span data-ttu-id="40186-122"><dt>**Akkuladung**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="40186-122"><dt>**BatteryCharge**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="40186-123">Informiert das Akku Gerät, dass der Benutzer zu diesem Zeitpunkt die Abrechnung durch den Akku angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="40186-123">Informs the battery device that the user has requested that the battery should be charging at this time.</span></span> <span data-ttu-id="40186-124">Beispielsweise kann die Anwendung mit einem intelligenten Akku/Ladegerät/Selektor jeweils eine Akkukapazität berechnen.</span><span class="sxs-lookup"><span data-stu-id="40186-124">For example, with a smart battery/charger/selector, the application could charge one battery at a time.</span></span> <span data-ttu-id="40186-125">Der **puffermember** dieser Struktur wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="40186-125">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <span data-ttu-id="40186-126"><dt>**Batterycriticalbias**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="40186-126"><dt>**BatteryCriticalBias**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="40186-127">Legt die kritische Bias-Anpassung des Akkus fest.</span><span class="sxs-lookup"><span data-stu-id="40186-127">Sets the battery's critical bias adjustment.</span></span> <span data-ttu-id="40186-128">Beachten Sie, dass dieser Wert normalerweise von Software geändert wird und in den Schnittstellen nur als Wartungs Feature vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="40186-128">Note it is not envisioned that this value would normally be changed by software, and is present in the interfaces only as a maintenance feature.</span></span> <span data-ttu-id="40186-129">Nicht alle Akkus können eine solche Einstellung beibehalten, und die Akku Informationen sollten gelesen werden, um zu bestätigen, dass der Akku die Einstellung akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="40186-129">Not all batteries can maintain such a setting, and the battery information should be read to confirm that the battery accepted the setting.</span></span><br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <span data-ttu-id="40186-130"><dt>**Akku Entladung**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="40186-130"><dt>**BatteryDischarge**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="40186-131">Informiert das Akku Gerät, dass der Benutzer zu diesem Zeitpunkt die Entladung des Akkus angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="40186-131">Informs the battery device that the user has requested that the battery be discharging at this time.</span></span> <span data-ttu-id="40186-132">Dies könnte beispielsweise verwendet werden, um anzugeben, welche Akkukapazität der Benutzer zurzeit für das System benötigt.</span><span class="sxs-lookup"><span data-stu-id="40186-132">For example, this could be used to indicate which battery the user currently wants to power the system.</span></span> <span data-ttu-id="40186-133">Der **puffermember** dieser Struktur wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="40186-133">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                          |



 

</dd> <dt>

<span data-ttu-id="40186-134">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="40186-134">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="40186-135">Die Akku Informationen, die festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="40186-135">The battery information to be set.</span></span> <span data-ttu-id="40186-136">Die Daten hängen vom Wert von **informationlevel** ab.</span><span class="sxs-lookup"><span data-stu-id="40186-136">The data depends on the value of **InformationLevel**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40186-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40186-137">Remarks</span></span>

<span data-ttu-id="40186-138">Die Struktur der **Batterie \_ Satz \_ Informationen** ist eine Struktur mit variabler Länge, und Sie müssen einen Puffer der passenden Größe zuordnen, damit die Informationen in die Struktur eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="40186-138">The **BATTERY\_SET\_INFORMATION** structure is a variable-length structure, and you must allocate a buffer of suitable size for the information to be included in the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="40186-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40186-139">Requirements</span></span>



| <span data-ttu-id="40186-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40186-140">Requirement</span></span> | <span data-ttu-id="40186-141">Wert</span><span class="sxs-lookup"><span data-stu-id="40186-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40186-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40186-142">Minimum supported client</span></span><br/> | <span data-ttu-id="40186-143">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40186-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="40186-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40186-144">Minimum supported server</span></span><br/> | <span data-ttu-id="40186-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40186-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="40186-146">Header</span><span class="sxs-lookup"><span data-stu-id="40186-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="40186-147"><dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="40186-147"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40186-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40186-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40186-149">**IOCTL- \_ Akku \_ Satz \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="40186-149">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

 




