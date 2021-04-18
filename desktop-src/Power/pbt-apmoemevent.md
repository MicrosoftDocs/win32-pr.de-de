---
description: Benachrichtigt Anwendungen, dass das APM-BIOS ein APM-OEM-Ereignis signalisiert hat.
ms.assetid: 3251ac00-41f1-44e9-a579-fa31e7c7d2ff
title: PBT_APMOEMEVENT-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a99b99bdaf69b1a53a24ad33cd898fd1c806694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347360"
---
# <a name="pbt_apmoemevent-event"></a><span data-ttu-id="b9dbd-103">PBT \_ apmuemevent-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b9dbd-103">PBT\_APMOEMEVENT event</span></span>

<span data-ttu-id="b9dbd-104">\[PBT \_ apmuemevent ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b9dbd-104">\[PBT\_APMOEMEVENT is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b9dbd-105">Die Unterstützung für dieses Ereignis wurde in Windows Vista entfernt.\]</span><span class="sxs-lookup"><span data-stu-id="b9dbd-105">Support for this event was removed in Windows Vista.\]</span></span>

<span data-ttu-id="b9dbd-106">Benachrichtigt Anwendungen, dass das APM-BIOS ein APM-OEM-Ereignis signalisiert hat.</span><span class="sxs-lookup"><span data-stu-id="b9dbd-106">Notifies applications that the APM BIOS has signaled an APM OEM event.</span></span>

<span data-ttu-id="b9dbd-107">Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b9dbd-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="b9dbd-108">Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9dbd-108">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMOEMEVENT
            LPARAM lParam); // OEM event code
```



## <a name="parameters"></a><span data-ttu-id="b9dbd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9dbd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9dbd-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="b9dbd-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b9dbd-111">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="b9dbd-111">A handle to window.</span></span>

<span data-ttu-id="b9dbd-112"></dd> <dt>*Umschlag*</dt> </span><span class="sxs-lookup"><span data-stu-id="b9dbd-112"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="b9dbd-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b9dbd-113">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="b9dbd-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b9dbd-114">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="b9dbd-115"><dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="b9dbd-115"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="b9dbd-116">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="b9dbd-116">Message identifier.</span></span><br/> |



 

<span data-ttu-id="b9dbd-117"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="b9dbd-117"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="b9dbd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b9dbd-118">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="b9dbd-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b9dbd-119">Meaning</span></span>                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMOEMEVENT"></span><span id="pbt_apmoemevent"></span><dl> <span data-ttu-id="b9dbd-120"><dt>**PBT \_ Apmuemevent**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="b9dbd-120"><dt>**PBT\_APMOEMEVENT**</dt> <dt>11 (0xB)</dt></span></span> </dl> | <span data-ttu-id="b9dbd-121">Ereignis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b9dbd-121">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b9dbd-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9dbd-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9dbd-123">Der von OEM definierte Ereignis Code, der vom APM-BIOS des Systems signalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b9dbd-123">The OEM-defined event code that was signaled by the system's APM BIOS.</span></span> <span data-ttu-id="b9dbd-124">OEM-Ereignis Codes liegen im Bereich von 0200h-02ffh.</span><span class="sxs-lookup"><span data-stu-id="b9dbd-124">OEM event codes are in the range 0200h - 02FFh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9dbd-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9dbd-125">Return value</span></span>

<span data-ttu-id="b9dbd-126">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="b9dbd-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9dbd-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9dbd-127">Remarks</span></span>

<span data-ttu-id="b9dbd-128">Da nicht alle APM-BIOS-Implementierungen OEM-Ereignis Benachrichtigungen bereitstellen, wird dieses Ereignis möglicherweise nie auf einigen Computern übertragen.</span><span class="sxs-lookup"><span data-stu-id="b9dbd-128">Because not all APM BIOS implementations provide OEM event notifications, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9dbd-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9dbd-129">Requirements</span></span>



| <span data-ttu-id="b9dbd-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9dbd-130">Requirement</span></span> | <span data-ttu-id="b9dbd-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b9dbd-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9dbd-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9dbd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b9dbd-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9dbd-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b9dbd-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9dbd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b9dbd-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9dbd-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b9dbd-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b9dbd-136">End of client support</span></span><br/>    | <span data-ttu-id="b9dbd-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b9dbd-137">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="b9dbd-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b9dbd-138">End of server support</span></span><br/>    | <span data-ttu-id="b9dbd-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b9dbd-139">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="b9dbd-140">Header</span><span class="sxs-lookup"><span data-stu-id="b9dbd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9dbd-141"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b9dbd-141"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9dbd-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9dbd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9dbd-143">Energie Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="b9dbd-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="b9dbd-144">**WM- \_ powerbroadcast**</span><span class="sxs-lookup"><span data-stu-id="b9dbd-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




