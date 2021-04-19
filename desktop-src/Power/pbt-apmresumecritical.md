---
description: Benachrichtigt Anwendungen, dass das System den Vorgang fortgesetzt hat.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: PBT_APMRESUMECRITICAL-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4a76e163f2e61e723f4df6572254e8ef89b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353457"
---
# <a name="pbt_apmresumecritical-event"></a><span data-ttu-id="c7b07-103">PBT \_ apmresumecritical-Ereignis</span><span class="sxs-lookup"><span data-stu-id="c7b07-103">PBT\_APMRESUMECRITICAL event</span></span>

<span data-ttu-id="c7b07-104">\[PBT \_ apmresumecritical ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c7b07-104">\[PBT\_APMRESUMECRITICAL is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c7b07-105">Die Unterstützung für dieses Ereignis wurde in Windows Vista entfernt.</span><span class="sxs-lookup"><span data-stu-id="c7b07-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="c7b07-106">Verwenden Sie stattdessen [PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md) .\]</span><span class="sxs-lookup"><span data-stu-id="c7b07-106">Use [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) instead.\]</span></span>

<span data-ttu-id="c7b07-107">Benachrichtigt Anwendungen, dass das System den Vorgang fortgesetzt hat.</span><span class="sxs-lookup"><span data-stu-id="c7b07-107">Notifies applications that the system has resumed operation.</span></span> <span data-ttu-id="c7b07-108">Dieses Ereignis kann darauf hinweisen, dass einige oder alle Anwendungen kein [PBT \_ apmsuspend](pbt-apmsuspend.md) -Ereignis empfangen haben.</span><span class="sxs-lookup"><span data-stu-id="c7b07-108">This event can indicate that some or all applications did not receive a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event.</span></span> <span data-ttu-id="c7b07-109">Beispielsweise kann dieses Ereignis nach einer kritischen Unterbrechung gesendet werden, die durch einen fehlerhaften Akku verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="c7b07-109">For example, this event can be broadcast after a critical suspension caused by a failing battery.</span></span>

<span data-ttu-id="c7b07-110">Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c7b07-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="c7b07-111">Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c7b07-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="c7b07-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7b07-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7b07-113">*HWND*</span><span class="sxs-lookup"><span data-stu-id="c7b07-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c7b07-114">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="c7b07-114">A handle to window.</span></span>

<span data-ttu-id="c7b07-115"></dd> <dt>*Umschlag*</dt> </span><span class="sxs-lookup"><span data-stu-id="c7b07-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="c7b07-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c7b07-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="c7b07-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c7b07-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="c7b07-118"><dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="c7b07-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="c7b07-119">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="c7b07-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="c7b07-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="c7b07-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="c7b07-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c7b07-121">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="c7b07-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c7b07-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <span data-ttu-id="c7b07-123"><dt>**PBT \_ Apmresumecritical**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="c7b07-123"><dt>**PBT\_APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="c7b07-124">Ereignis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c7b07-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c7b07-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7b07-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7b07-126">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="c7b07-126">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7b07-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7b07-127">Return value</span></span>

<span data-ttu-id="c7b07-128">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="c7b07-128">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7b07-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7b07-129">Remarks</span></span>

<span data-ttu-id="c7b07-130">Da eine Notabschaltung ohne vorherige Benachrichtigung aufgetreten ist, sind zuvor verfügbare Ressourcen und Daten möglicherweise nicht vorhanden, wenn die Anwendung dieses Ereignis empfängt.</span><span class="sxs-lookup"><span data-stu-id="c7b07-130">Because a critical suspension occurs without prior notification, resources and data previously available may not be present when the application receives this event.</span></span> <span data-ttu-id="c7b07-131">Die Anwendung sollte versuchen, ihren Status im Rahmen ihrer Möglichkeiten optimal wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c7b07-131">The application should attempt to restore its state to the best of its ability.</span></span> <span data-ttu-id="c7b07-132">Während einer kritischen Unterbrechung behält das System den Status des DRAM und der lokalen Festplatten bei, behält aber möglicherweise keine Netzwerkverbindungen bei.</span><span class="sxs-lookup"><span data-stu-id="c7b07-132">While in a critical suspension, the system maintains the state of the DRAM and local hard disks, but may not maintain net connections.</span></span> <span data-ttu-id="c7b07-133">Eine Anwendung muss möglicherweise in Bezug auf Dateien, die im Netzwerk geöffnet waren, vor kritischer Unterbrechung Maßnahmen ergreifen.</span><span class="sxs-lookup"><span data-stu-id="c7b07-133">An application may need to take action with respect to files that were open on the network before critical suspension.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7b07-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7b07-134">Requirements</span></span>



| <span data-ttu-id="c7b07-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7b07-135">Requirement</span></span> | <span data-ttu-id="c7b07-136">Wert</span><span class="sxs-lookup"><span data-stu-id="c7b07-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b07-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7b07-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c7b07-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7b07-138">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c7b07-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7b07-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c7b07-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7b07-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7b07-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c7b07-141">End of client support</span></span><br/>    | <span data-ttu-id="c7b07-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7b07-142">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="c7b07-143">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c7b07-143">End of server support</span></span><br/>    | <span data-ttu-id="c7b07-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c7b07-144">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="c7b07-145">Header</span><span class="sxs-lookup"><span data-stu-id="c7b07-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7b07-146"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c7b07-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7b07-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7b07-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7b07-148">System Aktivierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="c7b07-148">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="c7b07-149">Energie Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="c7b07-149">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="c7b07-150">**WM- \_ powerbroadcast**</span><span class="sxs-lookup"><span data-stu-id="c7b07-150">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




