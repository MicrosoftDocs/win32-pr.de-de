---
description: Benachrichtigt Anwendungen, dass ein Energieverwaltungsereignis aufgetreten ist.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: WM_POWERBROADCAST-Nachricht (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b205a146b731bdf8cf9adc1563621232c24c10b4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396505"
---
# <a name="wm_powerbroadcast-message"></a><span data-ttu-id="bae6b-103">WM \_ POWERBROADCAST-Nachricht</span><span class="sxs-lookup"><span data-stu-id="bae6b-103">WM\_POWERBROADCAST message</span></span>

<span data-ttu-id="bae6b-104">Benachrichtigt Anwendungen, dass ein Energieverwaltungsereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="bae6b-104">Notifies applications that a power-management event has occurred.</span></span>

<span data-ttu-id="bae6b-105">Ein Fenster empfängt diese Meldung über seine **WindowProc-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="bae6b-105">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="bae6b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bae6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bae6b-107">*Hwnd*</span><span class="sxs-lookup"><span data-stu-id="bae6b-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bae6b-108">Ein Handle für fenster.</span><span class="sxs-lookup"><span data-stu-id="bae6b-108">A handle to window.</span></span>

</dd> <dt>
  
<span data-ttu-id="bae6b-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="bae6b-109">*uMsg*</span></span>
</dt> <dd> 

| <span data-ttu-id="bae6b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="bae6b-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="bae6b-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bae6b-111">Meaning</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="bae6b-112"><dt>–WM \_ POWERBROADCAST\*\*</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="bae6b-112"><dt>\*\*\*\*WM\_POWERBROADCAST\*\*\*\*</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="bae6b-113">Nachrichtenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="bae6b-113">Message identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bae6b-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bae6b-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bae6b-115">Das Energieverwaltungsereignis.</span><span class="sxs-lookup"><span data-stu-id="bae6b-115">The power-management event.</span></span> <span data-ttu-id="bae6b-116">Dieser Parameter kann einer der folgenden Ereignisbezeichner sein.</span><span class="sxs-lookup"><span data-stu-id="bae6b-116">This parameter can be one of the following event identifiers.</span></span>



| <span data-ttu-id="bae6b-117">Ereignis</span><span class="sxs-lookup"><span data-stu-id="bae6b-117">Event</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="bae6b-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bae6b-118">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="bae6b-119"><dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="bae6b-119"><dt>**[PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="bae6b-120">Der Energiestatus wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="bae6b-120">Power status has changed.</span></span><br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="bae6b-121"><dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="bae6b-121"><dt>**[PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span></span> </dl>        | <span data-ttu-id="bae6b-122">Der Vorgang wird automatisch von einem Energiesparzustand aus fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="bae6b-122">Operation is resuming automatically from a low-power state.</span></span> <span data-ttu-id="bae6b-123">Diese Meldung wird jedes Mal gesendet, wenn das System fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="bae6b-123">This message is sent every time the system resumes.</span></span><br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="bae6b-124"><dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="bae6b-124"><dt>**[PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span></span> </dl>                  | <span data-ttu-id="bae6b-125">Der Vorgang wird von einem Energiesparzustand aus fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="bae6b-125">Operation is resuming from a low-power state.</span></span> <span data-ttu-id="bae6b-126">Diese Meldung wird nach [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) gesendet, wenn der Fortsetzen durch Benutzereingabe ausgelöst wird, z. B. durch Drücken einer Taste.</span><span class="sxs-lookup"><span data-stu-id="bae6b-126">This message is sent after [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) if the resume is triggered by user input, such as pressing a key.</span></span><br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="bae6b-127"><dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="bae6b-127"><dt>**[PBT\_APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                          | <span data-ttu-id="bae6b-128">Das System hält den Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="bae6b-128">System is suspending operation.</span></span><br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="bae6b-129"><dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="bae6b-129"><dt>**[PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span></span> </dl>   | <span data-ttu-id="bae6b-130">Ein Energieeinstellungsänderungsereignis wurde empfangen.</span><span class="sxs-lookup"><span data-stu-id="bae6b-130">A power setting change event has been received.</span></span> <br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="bae6b-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bae6b-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bae6b-132">Die ereignisspezifischen Daten.</span><span class="sxs-lookup"><span data-stu-id="bae6b-132">The event-specific data.</span></span> <span data-ttu-id="bae6b-133">Für die meisten Ereignisse ist dieser Parameter reserviert und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bae6b-133">For most events, this parameter is reserved and not used.</span></span>

<span data-ttu-id="bae6b-134">Wenn der *wParam-Parameter* [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)ist, ist der *lParam-Parameter* ein Zeiger auf eine [**POWERBROADCAST \_ SETTING-Struktur.**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)</span><span class="sxs-lookup"><span data-stu-id="bae6b-134">If the *wParam* parameter is [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md), the *lParam* parameter is a pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bae6b-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bae6b-135">Return value</span></span>

<span data-ttu-id="bae6b-136">Eine Anwendung sollte **TRUE** zurückgeben, wenn sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="bae6b-136">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="bae6b-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bae6b-137">Remarks</span></span>

<span data-ttu-id="bae6b-138">Das System sendet immer dann eine [PBT-APMRESUMEAUTOMATIC-Nachricht, \_ ](pbt-apmresumeautomatic.md) wenn das System fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="bae6b-138">The system always sends a [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) message whenever the system resumes.</span></span> <span data-ttu-id="bae6b-139">Wenn das System als Reaktion auf Benutzereingaben wie das Drücken einer Taste fortgesetzt wird, sendet das System nach dem Senden von PBT APMRESUMEAUTOMATIC auch eine **PBT-APMRESUMESUSPEND-Nachricht. \_** \_</span><span class="sxs-lookup"><span data-stu-id="bae6b-139">If the system resumes in response to user input such as pressing a key, the system also sends a **PBT\_APMRESUMESUSPEND** message after sending PBT\_APMRESUMEAUTOMATIC.</span></span>

<span data-ttu-id="bae6b-140">**WM \_ POWERBROADCAST-Nachrichten** unterscheiden nicht zwischen verschiedenen Zuständen mit geringer Leistung.</span><span class="sxs-lookup"><span data-stu-id="bae6b-140">**WM\_POWERBROADCAST** messages do not distinguish between different low-power states.</span></span> <span data-ttu-id="bae6b-141">Eine Anwendung kann nur feststellen, dass das System in einen Energiesparzustand übergeht oder wieder aufgenommen wurde. der spezifische Energiezustand kann nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="bae6b-141">An application can determine only that the system is entering or has resumed from a low-power state; it cannot determine the specific power state.</span></span> <span data-ttu-id="bae6b-142">Das System zeichnet Details zu Energiezustandsübergängen im Windows-Systemereignisprotokoll auf.</span><span class="sxs-lookup"><span data-stu-id="bae6b-142">The system records details about power state transitions in the Windows System event log.</span></span>

<span data-ttu-id="bae6b-143">Um zu verhindern, dass das System in Windows Vista in einen Energiesparzustand übergehen kann, muss eine Anwendung [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) aufrufen, um das System darüber zu informieren, dass es verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bae6b-143">To prevent the system from transitioning to a low-power state in Windows Vista, an application must call [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) to inform the system that it is in use.</span></span>

<span data-ttu-id="bae6b-144">Die folgenden Meldungen werden auf keinem der im Abschnitt Anforderungen angegebenen Betriebssysteme unterstützt:</span><span class="sxs-lookup"><span data-stu-id="bae6b-144">The following messages are not supported on any of the operating systems specified in the Requirements section:</span></span>

- <span data-ttu-id="bae6b-145">PBT_APMQUERYSTANDBY</span><span class="sxs-lookup"><span data-stu-id="bae6b-145">PBT_APMQUERYSTANDBY</span></span>  
- <span data-ttu-id="bae6b-146">PBT_APMQUERYSTANDBYFAILED</span><span class="sxs-lookup"><span data-stu-id="bae6b-146">PBT_APMQUERYSTANDBYFAILED</span></span>  
- <span data-ttu-id="bae6b-147">PBT_APMSTANDBY</span><span class="sxs-lookup"><span data-stu-id="bae6b-147">PBT_APMSTANDBY</span></span>  
- <span data-ttu-id="bae6b-148">PBT_APMRESUMESTANDBY</span><span class="sxs-lookup"><span data-stu-id="bae6b-148">PBT_APMRESUMESTANDBY</span></span>  

## <a name="requirements"></a><span data-ttu-id="bae6b-149">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bae6b-149">Requirements</span></span>



| <span data-ttu-id="bae6b-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bae6b-150">Requirement</span></span> | <span data-ttu-id="bae6b-151">Wert</span><span class="sxs-lookup"><span data-stu-id="bae6b-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bae6b-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bae6b-152">Minimum supported client</span></span><br/> | <span data-ttu-id="bae6b-153">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bae6b-153">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bae6b-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bae6b-154">Minimum supported server</span></span><br/> | <span data-ttu-id="bae6b-155">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bae6b-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bae6b-156">Header</span><span class="sxs-lookup"><span data-stu-id="bae6b-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="bae6b-157"><dt>WinUser.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bae6b-157"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bae6b-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bae6b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae6b-159">WM \_ POWERBROADCAST Messages</span><span class="sxs-lookup"><span data-stu-id="bae6b-159">WM\_POWERBROADCAST Messages</span></span>](wm-powerbroadcast-messages.md)
</dt> <dt>

[<span data-ttu-id="bae6b-160">Energieverwaltungsmeldungen</span><span class="sxs-lookup"><span data-stu-id="bae6b-160">Power Management Messages</span></span>](power-management-messages.md)
</dt> </dl>

 

 




