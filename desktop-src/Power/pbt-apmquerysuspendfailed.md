---
description: Benachrichtigt Anwendungen, dass die Berechtigung zum Aussetzen des Computers verweigert wurde.
ms.assetid: 0f68628f-9d38-45ca-9487-95bf62075e00
title: PBT_APMQUERYSUSPENDFAILED-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1544cd5ed94ae0228c739e2ddb576b0bd77146eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358889"
---
# <a name="pbt_apmquerysuspendfailed-event"></a><span data-ttu-id="6ab52-103">PBT \_ apmquerysuspendfailed-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6ab52-103">PBT\_APMQUERYSUSPENDFAILED event</span></span>

<span data-ttu-id="6ab52-104">\[PBT \_ apmquerysuspendfailed ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6ab52-104">\[PBT\_APMQUERYSUSPENDFAILED is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6ab52-105">Die Unterstützung für dieses Ereignis wurde in Windows Vista entfernt.</span><span class="sxs-lookup"><span data-stu-id="6ab52-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="6ab52-106">Verwenden Sie stattdessen [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) .\]</span><span class="sxs-lookup"><span data-stu-id="6ab52-106">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="6ab52-107">Benachrichtigt Anwendungen, dass die Berechtigung zum Aussetzen des Computers verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="6ab52-107">Notifies applications that permission to suspend the computer was denied.</span></span> <span data-ttu-id="6ab52-108">Dieses Ereignis wird gesendet, wenn eine Anwendung oder ein Treiber eine Broadcast Abfrage zurückgegeben hat, die einem vorherigen [PBT \_ apmquerysuspend](pbt-apmquerysuspend.md) -Ereignis **\_ \_ verweigert** wurde.</span><span class="sxs-lookup"><span data-stu-id="6ab52-108">This event is broadcast if any application or driver returned **BROADCAST\_QUERY\_DENY** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="6ab52-109">Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6ab52-109">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="6ab52-110">Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6ab52-110">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPENDFAILED
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="6ab52-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ab52-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ab52-112">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6ab52-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6ab52-113">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="6ab52-113">A handle to window.</span></span>

<span data-ttu-id="6ab52-114"></dd> <dt>*Umschlag*</dt> </span><span class="sxs-lookup"><span data-stu-id="6ab52-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="6ab52-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6ab52-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="6ab52-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6ab52-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="6ab52-117"><dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="6ab52-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="6ab52-118">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="6ab52-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="6ab52-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="6ab52-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="6ab52-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6ab52-120">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="6ab52-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6ab52-121">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPENDFAILED"></span><span id="pbt_apmquerysuspendfailed"></span><dl> <span data-ttu-id="6ab52-122"><dt>**PBT \_ Apmquerysuspendfailed**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="6ab52-122"><dt>**PBT\_APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="6ab52-123">Ereignis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="6ab52-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6ab52-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ab52-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ab52-125">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="6ab52-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ab52-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ab52-126">Return value</span></span>

<span data-ttu-id="6ab52-127">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="6ab52-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ab52-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ab52-128">Remarks</span></span>

<span data-ttu-id="6ab52-129">Anwendungen reagieren in der Regel auf dieses Ereignis, indem Sie den normalen Betrieb fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="6ab52-129">Applications typically respond to this event by resuming normal operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab52-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ab52-130">Requirements</span></span>



| <span data-ttu-id="6ab52-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ab52-131">Requirement</span></span> | <span data-ttu-id="6ab52-132">Wert</span><span class="sxs-lookup"><span data-stu-id="6ab52-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab52-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ab52-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6ab52-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ab52-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6ab52-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ab52-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6ab52-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ab52-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6ab52-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6ab52-137">End of client support</span></span><br/>    | <span data-ttu-id="6ab52-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6ab52-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="6ab52-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6ab52-139">End of server support</span></span><br/>    | <span data-ttu-id="6ab52-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ab52-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="6ab52-141">Header</span><span class="sxs-lookup"><span data-stu-id="6ab52-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ab52-142"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="6ab52-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ab52-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ab52-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ab52-144">Energieverwaltung</span><span class="sxs-lookup"><span data-stu-id="6ab52-144">Power Management</span></span>](power-management-portal.md)
</dt> <dt>

[<span data-ttu-id="6ab52-145">Energie Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6ab52-145">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="6ab52-146">PBT \_ apmquerysuspend</span><span class="sxs-lookup"><span data-stu-id="6ab52-146">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="6ab52-147">**WM- \_ powerbroadcast**</span><span class="sxs-lookup"><span data-stu-id="6ab52-147">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




