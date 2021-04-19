---
description: Benachrichtigt Anwendungen, dass der Akku Strom niedrig ist.
ms.assetid: ef24b8cf-d801-4452-a03c-3f2bdbdd7e5d
title: PBT_APMBATTERYLOW-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64884f9bb01e37883e1be61b2de88862e8b119fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358890"
---
# <a name="pbt_apmbatterylow-event"></a><span data-ttu-id="09800-103">PBT \_ apmbatterylow-Ereignis</span><span class="sxs-lookup"><span data-stu-id="09800-103">PBT\_APMBATTERYLOW event</span></span>

<span data-ttu-id="09800-104">\[PBT \_ apmbatterylow ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="09800-104">\[PBT\_APMBATTERYLOW is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="09800-105">Die Unterstützung für dieses Ereignis wurde in Windows Vista entfernt.</span><span class="sxs-lookup"><span data-stu-id="09800-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="09800-106">Verwenden Sie stattdessen [PBT \_ apmpowerstatuschange](pbt-apmpowerstatuschange.md) .\]</span><span class="sxs-lookup"><span data-stu-id="09800-106">Use [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) instead.\]</span></span>

<span data-ttu-id="09800-107">Benachrichtigt Anwendungen, dass der Akku Strom niedrig ist.</span><span class="sxs-lookup"><span data-stu-id="09800-107">Notifies applications that the battery power is low.</span></span>

<span data-ttu-id="09800-108">Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="09800-108">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="09800-109">Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="09800-109">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMBATTERYLOW
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="09800-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="09800-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09800-111">*HWND*</span><span class="sxs-lookup"><span data-stu-id="09800-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="09800-112">Ein Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="09800-112">A handle to the window.</span></span>

<span data-ttu-id="09800-113"></dd> <dt>*Umschlag*</dt> </span><span class="sxs-lookup"><span data-stu-id="09800-113"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="09800-114">Wert</span><span class="sxs-lookup"><span data-stu-id="09800-114">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="09800-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="09800-115">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="09800-116"><dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="09800-116"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="09800-117">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="09800-117">Message identifier.</span></span><br/> |



 

<span data-ttu-id="09800-118"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="09800-118"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="09800-119">Wert</span><span class="sxs-lookup"><span data-stu-id="09800-119">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="09800-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="09800-120">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMBATTERYLOW"></span><span id="pbt_apmbatterylow"></span><dl> <span data-ttu-id="09800-121"><dt>**PBT \_ Apmbatterylow**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="09800-121"><dt>**PBT\_APMBATTERYLOW**</dt> <dt>9 (0x9)</dt></span></span> </dl> | <span data-ttu-id="09800-122">Ereignis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="09800-122">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="09800-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09800-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09800-124">Reserviert, muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="09800-124">Reserved, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09800-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09800-125">Return value</span></span>

<span data-ttu-id="09800-126">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="09800-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09800-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09800-127">Remarks</span></span>

<span data-ttu-id="09800-128">Dieses Ereignis wird gesendet, wenn das APM-BIOS eines Systems eine apm-Akku Benachrichtigung mit geringer Leistung signalisiert.</span><span class="sxs-lookup"><span data-stu-id="09800-128">This event is broadcast when a system's APM BIOS signals an APM battery low notification.</span></span> <span data-ttu-id="09800-129">Da einige APM-BIOS-Implementierungen keine Benachrichtigungen bereitstellen, wenn Akkus niedrig sind, wird dieses Ereignis möglicherweise nie auf einigen Computern übertragen.</span><span class="sxs-lookup"><span data-stu-id="09800-129">Because some APM BIOS implementations do not provide notifications when batteries are low, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="09800-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09800-130">Requirements</span></span>



| <span data-ttu-id="09800-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09800-131">Requirement</span></span> | <span data-ttu-id="09800-132">Wert</span><span class="sxs-lookup"><span data-stu-id="09800-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09800-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09800-133">Minimum supported client</span></span><br/> | <span data-ttu-id="09800-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09800-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="09800-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09800-135">Minimum supported server</span></span><br/> | <span data-ttu-id="09800-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09800-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="09800-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="09800-137">End of client support</span></span><br/>    | <span data-ttu-id="09800-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="09800-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="09800-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="09800-139">End of server support</span></span><br/>    | <span data-ttu-id="09800-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09800-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="09800-141">Header</span><span class="sxs-lookup"><span data-stu-id="09800-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="09800-142"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="09800-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09800-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09800-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09800-144">Energie Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="09800-144">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="09800-145">**WM- \_ powerbroadcast**</span><span class="sxs-lookup"><span data-stu-id="09800-145">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




