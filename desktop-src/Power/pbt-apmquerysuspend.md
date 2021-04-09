---
description: Fordert die Berechtigung zum Aussetzen des Computers an. Eine Anwendung, die die Erlaubnis erteilt, muss vor dem Beenden Vorbereitungen für den Standbymodus treffen.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: PBT_APMQUERYSUSPEND-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865072"
---
# <a name="pbt_apmquerysuspend-event"></a><span data-ttu-id="6ecca-104">PBT \_ apmquerysuspend-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6ecca-104">PBT\_APMQUERYSUSPEND event</span></span>

<span data-ttu-id="6ecca-105">\[PBT \_ apmquerysuspend ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6ecca-105">\[PBT\_APMQUERYSUSPEND is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6ecca-106">Die Unterstützung für dieses Ereignis wurde in Windows Vista entfernt.</span><span class="sxs-lookup"><span data-stu-id="6ecca-106">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="6ecca-107">Verwenden Sie stattdessen [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) .\]</span><span class="sxs-lookup"><span data-stu-id="6ecca-107">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="6ecca-108">Fordert die Berechtigung zum Aussetzen des Computers an.</span><span class="sxs-lookup"><span data-stu-id="6ecca-108">Requests permission to suspend the computer.</span></span> <span data-ttu-id="6ecca-109">Eine Anwendung, die die Erlaubnis erteilt, muss vor dem Beenden Vorbereitungen für den Standbymodus treffen.</span><span class="sxs-lookup"><span data-stu-id="6ecca-109">An application that grants permission should carry out preparations for the suspension before returning.</span></span>

<span data-ttu-id="6ecca-110">Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6ecca-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="6ecca-111">Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6ecca-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
```



## <a name="parameters"></a><span data-ttu-id="6ecca-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ecca-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ecca-113">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6ecca-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6ecca-114">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="6ecca-114">A handle to window.</span></span>

<span data-ttu-id="6ecca-115"></dd> <dt>*Umschlag*</dt> </span><span class="sxs-lookup"><span data-stu-id="6ecca-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="6ecca-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6ecca-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="6ecca-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6ecca-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="6ecca-118"><dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="6ecca-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="6ecca-119">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="6ecca-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="6ecca-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="6ecca-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="6ecca-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6ecca-121">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="6ecca-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6ecca-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <span data-ttu-id="6ecca-123"><dt>**PBT \_ Apmquerysuspend**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6ecca-123"><dt>**PBT\_APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6ecca-124">Ereignis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="6ecca-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6ecca-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ecca-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ecca-126">Die Aktionsflags.</span><span class="sxs-lookup"><span data-stu-id="6ecca-126">The action flags.</span></span> <span data-ttu-id="6ecca-127">Wenn Bit 0 1 ist, kann die Anwendung den Benutzer zur Eingabe von Anweisungen auffordern, wie die Unterbrechung vorbereitet werden soll. Andernfalls muss die Anwendung ohne Benutzerinteraktion vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="6ecca-127">If bit 0 is 1, the application can prompt the user for directions on how to prepare for the suspension; otherwise, the application must prepare without user interaction.</span></span> <span data-ttu-id="6ecca-128">Alle anderen Bitwerte sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="6ecca-128">All other bit values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ecca-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ecca-129">Return value</span></span>

<span data-ttu-id="6ecca-130">Gibt " **true** " zurück, um die Anforderung zum aussetzen zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="6ecca-130">Return **TRUE** to grant the request to suspend.</span></span> <span data-ttu-id="6ecca-131">Um die Anforderung zu verweigern, geben Sie **Broadcast \_ Query \_ Deny** zurück.</span><span class="sxs-lookup"><span data-stu-id="6ecca-131">To deny the request, return **BROADCAST\_QUERY\_DENY**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ecca-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ecca-132">Remarks</span></span>

<span data-ttu-id="6ecca-133">Eine Anwendung sollte dieses Ereignis so schnell wie möglich verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6ecca-133">An application should process this event as quickly as possible.</span></span> <span data-ttu-id="6ecca-134">Die Anwendung kann den Benutzer zur Eingabe von Anweisungen auffordern, wie die Unterbrechung vorbereitet werden soll, wenn Bit 0 im *Flags* -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6ecca-134">The application can prompt the user for directions on how to prepare for suspension only if bit 0 in the *Flags* parameter is set.</span></span> <span data-ttu-id="6ecca-135">Wenn diese Meldung jedoch ausgegeben wird, weil der Benutzer die Laptop-Lid schließt, ist es nicht möglich, den Benutzer zur Eingabe aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="6ecca-135">However, if this message is issued because the user is closing the laptop lid, it will not be possible to prompt the user.</span></span> <span data-ttu-id="6ecca-136">Anwendungen sollten beachten, dass der Benutzer ein bestimmtes Verhalten erwartet, wenn er die Laptop-Taste schließt oder den Netzschalter drückt und den Übergang zulässt.</span><span class="sxs-lookup"><span data-stu-id="6ecca-136">Applications should respect that the user expects a certain behavior when they close the laptop lid or press the power button and allow the transition to succeed.</span></span>

<span data-ttu-id="6ecca-137">Das System lässt zu, dass eine Anwendung ungefähr 20 Sekunden die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht entfernt, die das PBT \_ apmquerysuspend-Ereignis aus der Nachrichten Warteschlange der Anwendung sendet.</span><span class="sxs-lookup"><span data-stu-id="6ecca-137">The system allows approximately 20 seconds for an application to remove the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message that is sending the PBT\_APMQUERYSUSPEND event from the application's message queue.</span></span> <span data-ttu-id="6ecca-138">Wenn eine Anwendung die Nachricht nicht in weniger als 20 Sekunden aus der Warteschlange entfernt, geht das System davon aus, dass sich die Anwendung in einem nicht reagierenden Zustand befindet und dass die Anwendung der standbyanforderung zustimmt.</span><span class="sxs-lookup"><span data-stu-id="6ecca-138">If an application does not remove the message from its queue in less than 20 seconds, the system will assume that the application is in a non-responsive state, and that the application agrees to the sleep request.</span></span> <span data-ttu-id="6ecca-139">Anwendungen, die Ihre Nachrichten Warteschlangen nicht verarbeiten, werden möglicherweise unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="6ecca-139">Applications that do not process their message queues may have their operations interrupted.</span></span> <span data-ttu-id="6ecca-140">Nachdem die Nachricht aus der Nachrichten Warteschlange entfernt wurde, kann es so lange dauern, bis alle erforderlichen Vorgänge ausgeführt werden, bevor Sie in den Ruhezustand wechseln.</span><span class="sxs-lookup"><span data-stu-id="6ecca-140">After it removes the message from the message queue, an application can take as much time as needed to perform any required operations before entering the sleep state.</span></span> <span data-ttu-id="6ecca-141">Alle Vorgänge, die länger als 20 Sekunden dauern könnten, sollten zu diesem Zeitpunkt ausgeführt werden, da das System während der [PBT- \_ apmsuspend](pbt-apmsuspend.md) -Verarbeitung nur 20 Sekunden für den Abschluss von Vorgängen zulässt.</span><span class="sxs-lookup"><span data-stu-id="6ecca-141">Any operations that could take longer then 20 seconds should be performed at this time, since the system allows only 20 seconds for operations to complete during [PBT\_APMSUSPEND](pbt-apmsuspend.md) processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ecca-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ecca-142">Requirements</span></span>



| <span data-ttu-id="6ecca-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ecca-143">Requirement</span></span> | <span data-ttu-id="6ecca-144">Wert</span><span class="sxs-lookup"><span data-stu-id="6ecca-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ecca-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ecca-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6ecca-146">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ecca-146">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6ecca-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ecca-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6ecca-148">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ecca-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6ecca-149">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6ecca-149">End of client support</span></span><br/>    | <span data-ttu-id="6ecca-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6ecca-150">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="6ecca-151">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6ecca-151">End of server support</span></span><br/>    | <span data-ttu-id="6ecca-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ecca-152">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="6ecca-153">Header</span><span class="sxs-lookup"><span data-stu-id="6ecca-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ecca-154"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="6ecca-154"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ecca-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ecca-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ecca-156">System Aktivierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6ecca-156">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="6ecca-157">Energie Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6ecca-157">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="6ecca-158">PBT \_ apmsuspend</span><span class="sxs-lookup"><span data-stu-id="6ecca-158">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="6ecca-159">**WM- \_ powerbroadcast**</span><span class="sxs-lookup"><span data-stu-id="6ecca-159">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




