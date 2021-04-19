---
description: Benachrichtigt Anwendungen, dass das System den Vorgang fortgesetzt hat, nachdem es angehalten wurde.
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: PBT_APMRESUMESUSPEND-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363466"
---
# <a name="pbt_apmresumesuspend-event"></a><span data-ttu-id="1b270-103">PBT \_ apmresumesuspend-Ereignis</span><span class="sxs-lookup"><span data-stu-id="1b270-103">PBT\_APMRESUMESUSPEND event</span></span>

<span data-ttu-id="1b270-104">Benachrichtigt Anwendungen, dass das System den Vorgang fortgesetzt hat, nachdem es angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="1b270-104">Notifies applications that the system has resumed operation after being suspended.</span></span>

<span data-ttu-id="1b270-105">Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1b270-105">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="1b270-106">Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1b270-106">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="1b270-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b270-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b270-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="1b270-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1b270-109">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="1b270-109">A handle to window.</span></span>

<span data-ttu-id="1b270-110"></dd> <dt>*Umschlag*</dt> </span><span class="sxs-lookup"><span data-stu-id="1b270-110"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="1b270-111">Wert</span><span class="sxs-lookup"><span data-stu-id="1b270-111">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="1b270-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1b270-112">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="1b270-113"><dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="1b270-113"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="1b270-114">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="1b270-114">Message identifier.</span></span><br/> |



 

<span data-ttu-id="1b270-115"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="1b270-115"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="1b270-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1b270-116">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="1b270-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1b270-117">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="1b270-118"><dt>**PBT \_ Apmresumesuspend**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="1b270-118"><dt>**PBT\_APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt></span></span> </dl> | <span data-ttu-id="1b270-119">Ereignis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1b270-119">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1b270-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b270-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b270-121">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="1b270-121">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b270-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b270-122">Return value</span></span>

<span data-ttu-id="1b270-123">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="1b270-123">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b270-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b270-124">Remarks</span></span>

<span data-ttu-id="1b270-125">Eine Anwendung kann dieses Ereignis nur empfangen, wenn Sie das [PBT \_ apmsuspend](pbt-apmsuspend.md) -Ereignis empfangen hat, bevor der Computer angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="1b270-125">An application can receive this event only if it received the [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended.</span></span> <span data-ttu-id="1b270-126">Andernfalls empfängt die Anwendung ein [PBT \_ apmresumecritical](pbt-apmresumecritical.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1b270-126">Otherwise, the application will receive a [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event.</span></span>

<span data-ttu-id="1b270-127">Wenn das System aufgrund der Benutzeraktivität reaktiviert wird (z. b. durch Drücken der Schaltfläche "einschalten") oder wenn das System eine Benutzerinteraktion in der physischen Konsole (z. b. Maus-oder Tastatureingabe) erkennt, nachdem das unbeaufsichtigte Einschalten erfolgt ist, überträgt das System zunächst das [PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md) -Ereignis und überträgt es dann übermittelt \_</span><span class="sxs-lookup"><span data-stu-id="1b270-127">If the system wakes due to user activity (such as pressing the power button) or if the system detects user interaction at the physical console (such as mouse or keyboard input) after waking unattended, the system first broadcasts the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event, then it broadcasts the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="1b270-128">Außerdem schaltet das System die Anzeige ein.</span><span class="sxs-lookup"><span data-stu-id="1b270-128">In addition, the system turns on the display.</span></span> <span data-ttu-id="1b270-129">Die Anwendung sollte die Dateien erneut öffnen, die Sie geschlossen haben, als das System in den Standbymodus gewechselt und die Benutzereingaben vorbereitet</span><span class="sxs-lookup"><span data-stu-id="1b270-129">Your application should reopen files that it closed when the system entered sleep and prepare for user input.</span></span>

<span data-ttu-id="1b270-130">Wenn das System aufgrund eines externen Aktivierungs Signals (Remote Wake) aktiviert wird, überträgt das System nur das [PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1b270-130">If the system wakes due to an external wake signal (remote wake), the system broadcasts only the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event.</span></span> <span data-ttu-id="1b270-131">Das PBT \_ apmresumesuspend-Ereignis wird nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="1b270-131">The PBT\_APMRESUMESUSPEND event is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b270-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b270-132">Requirements</span></span>



| <span data-ttu-id="1b270-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b270-133">Requirement</span></span> | <span data-ttu-id="1b270-134">Wert</span><span class="sxs-lookup"><span data-stu-id="1b270-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b270-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b270-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1b270-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b270-136">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1b270-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b270-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1b270-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b270-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1b270-139">Header</span><span class="sxs-lookup"><span data-stu-id="1b270-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b270-140"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1b270-140"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b270-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b270-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b270-142">System Aktivierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="1b270-142">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="1b270-143">Energie Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="1b270-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="1b270-144">PBT \_ apmsuspend</span><span class="sxs-lookup"><span data-stu-id="1b270-144">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="1b270-145">PBT \_ apmresumecritical</span><span class="sxs-lookup"><span data-stu-id="1b270-145">PBT\_APMRESUMECRITICAL</span></span>](pbt-apmresumecritical.md)
</dt> <dt>

[<span data-ttu-id="1b270-146">**WM- \_ powerbroadcast**</span><span class="sxs-lookup"><span data-stu-id="1b270-146">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




