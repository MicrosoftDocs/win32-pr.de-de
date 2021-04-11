---
description: Benachrichtigt Anwendungen, dass der Computer im Begriff ist, in einen angehaltenen Zustand zu wechseln.
ms.assetid: 61b177a0-4cff-4740-bed8-a46c06c43be8
title: PBT_APMSUSPEND-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6982e00565329c85e06765879b9b72b07fe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216025"
---
# <a name="pbt_apmsuspend-event"></a><span data-ttu-id="762b9-103">PBT \_ apmsuspend-Ereignis</span><span class="sxs-lookup"><span data-stu-id="762b9-103">PBT\_APMSUSPEND event</span></span>

<span data-ttu-id="762b9-104">Benachrichtigt Anwendungen, dass der Computer im Begriff ist, in einen angehaltenen Zustand zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="762b9-104">Notifies applications that the computer is about to enter a suspended state.</span></span> <span data-ttu-id="762b9-105">Dieses Ereignis wird in der Regel übertragen, wenn alle Anwendungen und installierbaren Treiber **true** für ein vorheriges [PBT \_ apmquerysuspend](pbt-apmquerysuspend.md) -Ereignis zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="762b9-105">This event is typically broadcast when all applications and installable drivers have returned **TRUE** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="762b9-106">Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="762b9-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="762b9-107">Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="762b9-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMSUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="762b9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="762b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="762b9-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="762b9-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="762b9-110">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="762b9-110">A handle to window.</span></span>

<span data-ttu-id="762b9-111"></dd> <dt>*Umschlag*</dt> </span><span class="sxs-lookup"><span data-stu-id="762b9-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="762b9-112">Wert</span><span class="sxs-lookup"><span data-stu-id="762b9-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="762b9-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="762b9-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="762b9-114"><dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="762b9-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="762b9-115">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="762b9-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="762b9-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="762b9-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="762b9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="762b9-117">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="762b9-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="762b9-118">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="762b9-119"><dt>**PBT \_ Apmsuspend**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="762b9-119"><dt>**PBT\_APMSUSPEND**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="762b9-120">Ereignis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="762b9-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="762b9-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="762b9-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="762b9-122">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="762b9-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="762b9-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="762b9-123">Return value</span></span>

<span data-ttu-id="762b9-124">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="762b9-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="762b9-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="762b9-125">Remarks</span></span>

<span data-ttu-id="762b9-126">Eine Anwendung sollte dieses Ereignis verarbeiten, indem alle Aufgaben abgeschlossen werden, die zum Speichern der Daten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="762b9-126">An application should process this event by completing all tasks necessary to save data.</span></span>

<span data-ttu-id="762b9-127">Das System lässt zu, dass eine Anwendung diese Benachrichtigung in ungefähr zwei Sekunden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="762b9-127">The system allows approximately two seconds for an application to handle this notification.</span></span> <span data-ttu-id="762b9-128">Wenn eine Anwendung nach Ablauf der Zeitzuweisung noch Vorgänge ausführt, kann das System die Anwendung unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="762b9-128">If an application is still performing operations after its time allotment has expired, the system may interrupt the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="762b9-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="762b9-129">Requirements</span></span>



| <span data-ttu-id="762b9-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="762b9-130">Requirement</span></span> | <span data-ttu-id="762b9-131">Wert</span><span class="sxs-lookup"><span data-stu-id="762b9-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="762b9-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="762b9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="762b9-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="762b9-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="762b9-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="762b9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="762b9-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="762b9-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="762b9-136">Header</span><span class="sxs-lookup"><span data-stu-id="762b9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="762b9-137"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="762b9-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="762b9-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="762b9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="762b9-139">System Energiespar Kriterien</span><span class="sxs-lookup"><span data-stu-id="762b9-139">System Sleep Criteria</span></span>](system-sleep-criteria.md)
</dt> <dt>

[<span data-ttu-id="762b9-140">System Aktivierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="762b9-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="762b9-141">Energie Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="762b9-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="762b9-142">PBT \_ apmquerysuspend</span><span class="sxs-lookup"><span data-stu-id="762b9-142">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="762b9-143">**SetSystemPowerState**</span><span class="sxs-lookup"><span data-stu-id="762b9-143">**SetSystemPowerState**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setsystempowerstate)
</dt> <dt>

[<span data-ttu-id="762b9-144">**WM- \_ powerbroadcast**</span><span class="sxs-lookup"><span data-stu-id="762b9-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




