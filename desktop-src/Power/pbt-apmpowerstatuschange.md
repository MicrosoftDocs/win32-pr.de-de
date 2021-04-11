---
description: Benachrichtigt Anwendungen über eine Änderung des Energiestatus des Computers, z. b. einen Wechsel von Akkuleistung zu a/C.
ms.assetid: dc56fee3-e0df-4f8e-8a41-92460279280a
title: PBT_APMPOWERSTATUSCHANGE-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ed67f7ba064d44614196da4190ce18a996bd5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216026"
---
# <a name="pbt_apmpowerstatuschange-event"></a><span data-ttu-id="6b23c-103">PBT \_ apmpowerstatuschange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6b23c-103">PBT\_APMPOWERSTATUSCHANGE event</span></span>

<span data-ttu-id="6b23c-104">Benachrichtigt Anwendungen über eine Änderung des Energiestatus des Computers, z. b. einen Wechsel von Akkuleistung zu a/C.</span><span class="sxs-lookup"><span data-stu-id="6b23c-104">Notifies applications of a change in the power status of the computer, such as a switch from battery power to A/C.</span></span> <span data-ttu-id="6b23c-105">Das System leitet dieses Ereignis auch dann weiter, wenn die verbleibende Akkuleistung unter einen vom Benutzer festgelegten Wert sinkt oder sich um einen angegebenen Prozentsatz ändert.</span><span class="sxs-lookup"><span data-stu-id="6b23c-105">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

<span data-ttu-id="6b23c-106">Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6b23c-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="6b23c-107">Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b23c-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMPOWERSTATUSCHANGE
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="6b23c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b23c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b23c-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6b23c-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6b23c-110">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="6b23c-110">A handle to window.</span></span>

<span data-ttu-id="6b23c-111"></dd> <dt>*Umschlag*</dt> </span><span class="sxs-lookup"><span data-stu-id="6b23c-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="6b23c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="6b23c-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="6b23c-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6b23c-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="6b23c-114"><dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="6b23c-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="6b23c-115">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="6b23c-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="6b23c-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="6b23c-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="6b23c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6b23c-117">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="6b23c-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6b23c-118">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="6b23c-119"><dt>**PBT \_ Apmpowerstatuschange**</dt> <dt>10 (0xa)</dt></span><span class="sxs-lookup"><span data-stu-id="6b23c-119"><dt>**PBT\_APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="6b23c-120">Ereignis Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="6b23c-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b23c-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b23c-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b23c-122">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="6b23c-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b23c-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b23c-123">Return value</span></span>

<span data-ttu-id="6b23c-124">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="6b23c-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b23c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b23c-125">Remarks</span></span>

<span data-ttu-id="6b23c-126">Eine Anwendung sollte dieses Ereignis verarbeiten, indem Sie die [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) -Funktion aufrufen, um den aktuellen Energiestatus des Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6b23c-126">An application should process this event by calling the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve the current power status of the computer.</span></span> <span data-ttu-id="6b23c-127">Insbesondere sollte die Anwendung die Elemente " **ACLineStatus**", " **BatteryFlag**", " **batterylifetime**" und " **batterylifeprozent** " der [**System \_ Energie \_ Status**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) -Struktur auf Änderungen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6b23c-127">In particular, the application should check the **ACLineStatus**, **BatteryFlag**, **BatteryLifeTime**, and **BatteryLifePercent** members of the [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) structure for any changes.</span></span> <span data-ttu-id="6b23c-128">Dieses Ereignis kann auftreten, wenn die Akku Lebensdauer weniger als 5 Minuten sinkt oder wenn der Prozentsatz der Akku Lebensdauer unter 10 Prozent sinkt oder wenn sich die Akku Lebensdauer um 3 Prozent ändert.</span><span class="sxs-lookup"><span data-stu-id="6b23c-128">This event can occur when battery life drops to less than 5 minutes, or when the percentage of battery life drops below 10 percent, or if the battery life changes by 3 percent.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b23c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b23c-129">Requirements</span></span>



| <span data-ttu-id="6b23c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b23c-130">Requirement</span></span> | <span data-ttu-id="6b23c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6b23c-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b23c-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b23c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6b23c-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b23c-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6b23c-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b23c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6b23c-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b23c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b23c-136">Header</span><span class="sxs-lookup"><span data-stu-id="6b23c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b23c-137"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="6b23c-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b23c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b23c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b23c-139">System Energie Status</span><span class="sxs-lookup"><span data-stu-id="6b23c-139">System Power Status</span></span>](system-power-status.md)
</dt> <dt>

[<span data-ttu-id="6b23c-140">Energie Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6b23c-140">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="6b23c-141">**GetSystemPowerStatus**</span><span class="sxs-lookup"><span data-stu-id="6b23c-141">**GetSystemPowerStatus**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus)
</dt> <dt>

[<span data-ttu-id="6b23c-142">**System \_ Energie \_ Status**</span><span class="sxs-lookup"><span data-stu-id="6b23c-142">**SYSTEM\_POWER\_STATUS**</span></span>](/windows/desktop/api/Winbase/ns-winbase-system_power_status)
</dt> <dt>

[<span data-ttu-id="6b23c-143">**WM- \_ powerbroadcast**</span><span class="sxs-lookup"><span data-stu-id="6b23c-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




