---
description: Benachrichtigt Anwendungen, dass ein Energie Verwaltungs Ereignis aufgetreten ist.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: WM_POWERBROADCAST Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f1b273462d8de27c19d715836d168ab8bf8c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529096"
---
# <a name="wm_powerbroadcast-message"></a><span data-ttu-id="56bdd-103">WM- \_ powerbroadcast-Meldung</span><span class="sxs-lookup"><span data-stu-id="56bdd-103">WM\_POWERBROADCAST message</span></span>

<span data-ttu-id="56bdd-104">Benachrichtigt Anwendungen, dass ein Energie Verwaltungs Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="56bdd-104">Notifies applications that a power-management event has occurred.</span></span>

<span data-ttu-id="56bdd-105">Ein Fenster empfängt diese Meldung über seine **WindowProc** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="56bdd-105">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="56bdd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56bdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56bdd-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="56bdd-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="56bdd-108">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="56bdd-108">A handle to window.</span></span>

<span data-ttu-id="56bdd-109"></dd> <dt>*Umschlag*</dt> </span><span class="sxs-lookup"><span data-stu-id="56bdd-109"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="56bdd-110">Wert</span><span class="sxs-lookup"><span data-stu-id="56bdd-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="56bdd-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="56bdd-111">Meaning</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="56bdd-112"><dt>\* \* \* \* WM \_ Powerbroadcast \* \*</dt> \* \* \* <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="56bdd-112"><dt>\*\*\*\*WM\_POWERBROADCAST\*\*\*\*</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="56bdd-113">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="56bdd-113">Message identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="56bdd-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56bdd-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56bdd-115">Das Energie Verwaltungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="56bdd-115">The power-management event.</span></span> <span data-ttu-id="56bdd-116">Dieser Parameter kann einem der folgenden Ereignis Bezeichner entsprechen.</span><span class="sxs-lookup"><span data-stu-id="56bdd-116">This parameter can be one of the following event identifiers.</span></span>



| <span data-ttu-id="56bdd-117">Ereignis</span><span class="sxs-lookup"><span data-stu-id="56bdd-117">Event</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="56bdd-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="56bdd-118">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="56bdd-119"><dt>**[PBT \_ Apmpowerstatuschange](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xa)</dt></span><span class="sxs-lookup"><span data-stu-id="56bdd-119"><dt>**[PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="56bdd-120">Der Energiestatus hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="56bdd-120">Power status has changed.</span></span><br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="56bdd-121"><dt>**[PBT \_ Apmresumeautomatic](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="56bdd-121"><dt>**[PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span></span> </dl>        | <span data-ttu-id="56bdd-122">Der Vorgang wird automatisch von einem Energiespar Zustand fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="56bdd-122">Operation is resuming automatically from a low-power state.</span></span> <span data-ttu-id="56bdd-123">Diese Meldung wird jedes Mal gesendet, wenn das System fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="56bdd-123">This message is sent every time the system resumes.</span></span><br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="56bdd-124"><dt>**[PBT \_ Apmresumesuspend](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="56bdd-124"><dt>**[PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span></span> </dl>                  | <span data-ttu-id="56bdd-125">Der Vorgang wird in einem Energiespar Zustand fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="56bdd-125">Operation is resuming from a low-power state.</span></span> <span data-ttu-id="56bdd-126">Diese Nachricht wird nach [PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md) gesendet, wenn die Fortsetzung durch Benutzereingaben ausgelöst wird, z. b. durch Drücken einer Taste.</span><span class="sxs-lookup"><span data-stu-id="56bdd-126">This message is sent after [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) if the resume is triggered by user input, such as pressing a key.</span></span><br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="56bdd-127"><dt>**[PBT \_ Apmsuspend](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="56bdd-127"><dt>**[PBT\_APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                          | <span data-ttu-id="56bdd-128">Der Vorgang wird vom System angehalten.</span><span class="sxs-lookup"><span data-stu-id="56bdd-128">System is suspending operation.</span></span><br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="56bdd-129"><dt>**[PBT \_ Powersettingchange](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="56bdd-129"><dt>**[PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span></span> </dl>   | <span data-ttu-id="56bdd-130">Ein Energie Einstellungs Änderungs Ereignis wurde empfangen.</span><span class="sxs-lookup"><span data-stu-id="56bdd-130">A power setting change event has been received.</span></span> <br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="56bdd-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56bdd-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56bdd-132">Die ereignisspezifischen Daten.</span><span class="sxs-lookup"><span data-stu-id="56bdd-132">The event-specific data.</span></span> <span data-ttu-id="56bdd-133">Bei den meisten Ereignissen ist dieser Parameter reserviert und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="56bdd-133">For most events, this parameter is reserved and not used.</span></span>

<span data-ttu-id="56bdd-134">Wenn der *wParam* -Parameter [PBT \_ powersettingchange](pbt-powersettingchange.md)ist, ist der *LPARAM* -Parameter ein Zeiger auf eine [**powerbroadcast- \_ Einstellungs**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) Struktur.</span><span class="sxs-lookup"><span data-stu-id="56bdd-134">If the *wParam* parameter is [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md), the *lParam* parameter is a pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56bdd-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56bdd-135">Return value</span></span>

<span data-ttu-id="56bdd-136">Eine Anwendung sollte **true** zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="56bdd-136">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="56bdd-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56bdd-137">Remarks</span></span>

<span data-ttu-id="56bdd-138">Das System sendet immer dann eine [PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md) -Meldung, wenn das System fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="56bdd-138">The system always sends a [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) message whenever the system resumes.</span></span> <span data-ttu-id="56bdd-139">Wenn das System als Reaktion auf Benutzereingaben (z. b. Drücken einer Taste) fortgesetzt wird, sendet das System nach dem Senden von PBT apmresumeautomatic auch eine **PBT \_ apmresumesuspend** -Nachricht \_ .</span><span class="sxs-lookup"><span data-stu-id="56bdd-139">If the system resumes in response to user input such as pressing a key, the system also sends a **PBT\_APMRESUMESUSPEND** message after sending PBT\_APMRESUMEAUTOMATIC.</span></span>

<span data-ttu-id="56bdd-140">**WM \_ Powerbroadcast** -Nachrichten unterscheiden sich nicht zwischen unterschiedlichen Zuständen mit niedrigem Energiezustand.</span><span class="sxs-lookup"><span data-stu-id="56bdd-140">**WM\_POWERBROADCAST** messages do not distinguish between different low-power states.</span></span> <span data-ttu-id="56bdd-141">Eine Anwendung kann nur bestimmen, ob das System in den Energiesparmodus wechselt oder ihn wieder aufgenommen hat. der jeweilige Energiezustand kann nicht ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="56bdd-141">An application can determine only that the system is entering or has resumed from a low-power state; it cannot determine the specific power state.</span></span> <span data-ttu-id="56bdd-142">Das System zeichnet Details zu Energie Zustands Übergängen im Windows-System Ereignisprotokoll auf.</span><span class="sxs-lookup"><span data-stu-id="56bdd-142">The system records details about power state transitions in the Windows System event log.</span></span>

<span data-ttu-id="56bdd-143">Um zu verhindern, dass das System in Windows Vista in einen Energiespar Zustand übergeht, muss eine Anwendung [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) aufrufen, um das System zu informieren, dass es verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56bdd-143">To prevent the system from transitioning to a low-power state in Windows Vista, an application must call [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) to inform the system that it is in use.</span></span>

<span data-ttu-id="56bdd-144">Die folgenden Meldungen werden von keinem der im Abschnitt "Anforderungen" angegebenen Betriebssysteme unterstützt:</span><span class="sxs-lookup"><span data-stu-id="56bdd-144">The following messages are not supported on any of the operating systems specified in the Requirements section:</span></span>

- <span data-ttu-id="56bdd-145">PBT_APMQUERYSTANDBY</span><span class="sxs-lookup"><span data-stu-id="56bdd-145">PBT_APMQUERYSTANDBY</span></span>  
- <span data-ttu-id="56bdd-146">PBT_APMQUERYSTANDBYFAILED</span><span class="sxs-lookup"><span data-stu-id="56bdd-146">PBT_APMQUERYSTANDBYFAILED</span></span>  
- <span data-ttu-id="56bdd-147">PBT_APMSTANDBY</span><span class="sxs-lookup"><span data-stu-id="56bdd-147">PBT_APMSTANDBY</span></span>  
- <span data-ttu-id="56bdd-148">PBT_APMRESUMESTANDBY</span><span class="sxs-lookup"><span data-stu-id="56bdd-148">PBT_APMRESUMESTANDBY</span></span>  

## <a name="requirements"></a><span data-ttu-id="56bdd-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56bdd-149">Requirements</span></span>



| <span data-ttu-id="56bdd-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56bdd-150">Requirement</span></span> | <span data-ttu-id="56bdd-151">Wert</span><span class="sxs-lookup"><span data-stu-id="56bdd-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56bdd-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56bdd-152">Minimum supported client</span></span><br/> | <span data-ttu-id="56bdd-153">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56bdd-153">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="56bdd-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56bdd-154">Minimum supported server</span></span><br/> | <span data-ttu-id="56bdd-155">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56bdd-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="56bdd-156">Header</span><span class="sxs-lookup"><span data-stu-id="56bdd-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="56bdd-157"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="56bdd-157"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56bdd-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56bdd-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56bdd-159">WM- \_ powerbroadcast-Meldungen</span><span class="sxs-lookup"><span data-stu-id="56bdd-159">WM\_POWERBROADCAST Messages</span></span>](wm-powerbroadcast-messages.md)
</dt> <dt>

[<span data-ttu-id="56bdd-160">Energie Verwaltungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="56bdd-160">Power Management Messages</span></span>](power-management-messages.md)
</dt> </dl>

 

 




