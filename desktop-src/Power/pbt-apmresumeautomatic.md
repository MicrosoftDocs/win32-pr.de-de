---
description: Benachrichtigt Anwendungen, dass das System aus dem Standbymodus oder Ruhezustand wieder aufgenommen wird. Dieses Ereignis wird jedes Mal übermittelt, wenn das System fortgesetzt wird, und gibt nicht an, ob ein Benutzer vorhanden ist.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: PBT_APMRESUMEAUTOMATIC-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a481dee356c85b3831fcace0c1ff127b0b276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865071"
---
# <a name="pbt_apmresumeautomatic-event"></a><span data-ttu-id="57071-104">PBT \_ apmresumeautomatic-Ereignis</span><span class="sxs-lookup"><span data-stu-id="57071-104">PBT\_APMRESUMEAUTOMATIC event</span></span>

<span data-ttu-id="57071-105">Benachrichtigt Anwendungen, dass das System aus dem Standbymodus oder Ruhezustand wieder aufgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="57071-105">Notifies applications that the system is resuming from sleep or hibernation.</span></span> <span data-ttu-id="57071-106">Dieses Ereignis wird jedes Mal übermittelt, wenn das System fortgesetzt wird, und gibt nicht an, ob ein Benutzer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="57071-106">This event is delivered every time the system resumes and does not indicate whether a user is present.</span></span>

<span data-ttu-id="57071-107">Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="57071-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="57071-108">Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="57071-108">The *wParam* and *lParam* parameters are set as described following.</span></span>

> [!Note]  
> <span data-ttu-id="57071-109">Wenn das System in Windows 10, Version 1507, oder höher, nur wieder aus dem Standbymodus wechselt, um sofort in den Ruhezustand zu wechseln, wird dieses Ereignis nicht übermittelt.</span><span class="sxs-lookup"><span data-stu-id="57071-109">In Windows 10, version 1507 systems or later, if the system is resuming from sleep only to immediately enter hibernation, this event is not delivered.</span></span> <span data-ttu-id="57071-110">In diesem Fall wird keine [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="57071-110">A [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message is not sent in this case.</span></span>

 


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMEAUTOMATIC
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="57071-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="57071-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57071-112">*HWND*</span><span class="sxs-lookup"><span data-stu-id="57071-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="57071-113">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="57071-113">A handle to window.</span></span>

<span data-ttu-id="57071-114"></dd> <dt>*Umschlag*</dt> </span><span class="sxs-lookup"><span data-stu-id="57071-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="57071-115">Wert</span><span class="sxs-lookup"><span data-stu-id="57071-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="57071-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="57071-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="57071-117"><dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="57071-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="57071-118">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="57071-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="57071-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="57071-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="57071-120">Wert</span><span class="sxs-lookup"><span data-stu-id="57071-120">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="57071-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="57071-121">Meaning</span></span>                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="57071-122"><dt>**PBT \_ Apmresumeautomatic**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="57071-122"><dt>**PBT\_APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="57071-123">Ereignis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="57071-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="57071-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57071-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57071-125">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="57071-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57071-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57071-126">Return value</span></span>

<span data-ttu-id="57071-127">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="57071-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57071-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57071-128">Remarks</span></span>

<span data-ttu-id="57071-129">Wenn das System nach der Übertragung von PBT \_ apmresumeautomatic eine Benutzeraktivität erkennt, sendet es ein [PBT \_ apmresumesuspend](pbt-apmresumesuspend.md) -Ereignis, um Anwendungen mitzuteilen, dass die vollständige Interaktion mit dem Benutzer fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="57071-129">If the system detects any user activity after broadcasting PBT\_APMRESUMEAUTOMATIC, it will broadcast a [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) event to let applications know they can resume full interaction with the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="57071-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57071-130">Requirements</span></span>



| <span data-ttu-id="57071-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57071-131">Requirement</span></span> | <span data-ttu-id="57071-132">Wert</span><span class="sxs-lookup"><span data-stu-id="57071-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57071-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57071-133">Minimum supported client</span></span><br/> | <span data-ttu-id="57071-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57071-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="57071-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57071-135">Minimum supported server</span></span><br/> | <span data-ttu-id="57071-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57071-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57071-137">Header</span><span class="sxs-lookup"><span data-stu-id="57071-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="57071-138"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="57071-138"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57071-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57071-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57071-140">System Aktivierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="57071-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="57071-141">Energie Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="57071-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="57071-142">PBT \_ apmresumesuspend</span><span class="sxs-lookup"><span data-stu-id="57071-142">PBT\_APMRESUMESUSPEND</span></span>](pbt-apmresumesuspend.md)
</dt> <dt>

[<span data-ttu-id="57071-143">**WM- \_ powerbroadcast**</span><span class="sxs-lookup"><span data-stu-id="57071-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




