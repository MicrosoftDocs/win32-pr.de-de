---
description: Die WM- \_ endsitzungs Nachricht wird an eine Anwendung gesendet, nachdem das System die Ergebnisse der WM \_ queryendsession-Nachricht verarbeitet hat. Die WM- \_ EndSession-Nachricht informiert die Anwendung darüber, ob die Sitzung beendet wird.
ms.assetid: 9bf04f24-da1e-4680-a47b-28e9c500635e
title: WM_ENDSESSION Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa62f356d881182dd6e6fd9e0558332bcc1b3fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348246"
---
# <a name="wm_endsession-message"></a><span data-ttu-id="bdc71-104">WM- \_ endsitzungs Nachricht</span><span class="sxs-lookup"><span data-stu-id="bdc71-104">WM\_ENDSESSION message</span></span>

<span data-ttu-id="bdc71-105">Die **WM- \_ endsitzungs** Nachricht wird an eine Anwendung gesendet, nachdem das System die Ergebnisse der [**WM \_ queryendsession**](wm-queryendsession.md) -Nachricht verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="bdc71-105">The **WM\_ENDSESSION** message is sent to an application after the system processes the results of the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message.</span></span> <span data-ttu-id="bdc71-106">Die **WM- \_ EndSession** -Nachricht informiert die Anwendung darüber, ob die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdc71-106">The **WM\_ENDSESSION** message informs the application whether the session is ending.</span></span>

<span data-ttu-id="bdc71-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bdc71-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="bdc71-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdc71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdc71-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="bdc71-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc71-110">Ein Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="bdc71-110">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="bdc71-111">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="bdc71-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc71-112">Der **WM- \_ endsitzungs** Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="bdc71-112">The **WM\_ENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bdc71-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdc71-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc71-114">Wenn die Sitzung beendet wird, ist dieser Parameter " **true**". die Sitzung kann jederzeit beendet werden, nachdem alle Anwendungen die Verarbeitung dieser Nachricht durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="bdc71-114">If the session is being ended, this parameter is **TRUE**; the session can end any time after all applications have returned from processing this message.</span></span> <span data-ttu-id="bdc71-115">Andernfalls ist Sie **false**.</span><span class="sxs-lookup"><span data-stu-id="bdc71-115">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bdc71-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdc71-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc71-117">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bdc71-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="bdc71-118">Wenn dieser Parameter 0 ist, wird das System heruntergefahren oder neu gestartet (es ist nicht möglich, zu bestimmen, welches Ereignis auftritt).</span><span class="sxs-lookup"><span data-stu-id="bdc71-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="bdc71-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bdc71-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="bdc71-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bdc71-120">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="bdc71-121"><dt>**EndSession \_ CloseApp**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="bdc71-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x1</dt></span></span> </dl>        | <span data-ttu-id="bdc71-122">Wenn *wParam* den Wert **true** hat, muss die Anwendung heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="bdc71-122">If *wParam* is **TRUE**, the application must shut down.</span></span> <span data-ttu-id="bdc71-123">Alle Daten sollten automatisch gespeichert werden, ohne den Benutzer aufzufordern (Weitere Informationen finden Sie unter "Hinweise").</span><span class="sxs-lookup"><span data-stu-id="bdc71-123">Any data should be saved automatically without prompting the user (for more information, see Remarks).</span></span> <span data-ttu-id="bdc71-124">Der Neustart-Manager sendet diese Meldung, wenn die Anwendung eine Datei verwendet, die ersetzt werden muss, wenn Sie das System bedienen muss oder wenn die Systemressourcen erschöpft sind.</span><span class="sxs-lookup"><span data-stu-id="bdc71-124">The Restart Manager sends this message when the application is using a file that needs to be replaced, when it must service the system, or when system resources are exhausted.</span></span> <span data-ttu-id="bdc71-125">Die Anwendung wird neu gestartet, wenn Sie sich für den Neustart mithilfe der [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) -Funktion registriert hat.</span><span class="sxs-lookup"><span data-stu-id="bdc71-125">The application will be restarted if it has registered for restart using the [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) function.</span></span> <span data-ttu-id="bdc71-126">Weitere Informationen finden Sie unter [Richtlinien für Anwendungen](../rstmgr/guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="bdc71-126">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span> <br/> <span data-ttu-id="bdc71-127">Wenn *wParam* den Wert **false** hat, sollte die Anwendung nicht heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="bdc71-127">If *wParam* is **FALSE**, the application should not shut down.</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="bdc71-128"><dt>**EndSession \_ Kritisch**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="bdc71-128"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="bdc71-129">Die Anwendung muss heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="bdc71-129">The application is forced to shut down.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="bdc71-130"><dt>**EndSession \_**</dt>Abmeldung <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="bdc71-130"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="bdc71-131">Der Benutzer meldet sich ab.</span><span class="sxs-lookup"><span data-stu-id="bdc71-131">The user is logging off.</span></span> <span data-ttu-id="bdc71-132">Weitere Informationen finden Sie unter [Abmelden](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="bdc71-132">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="bdc71-133">Beachten Sie, dass dieser Parameter eine Bitmaske ist.</span><span class="sxs-lookup"><span data-stu-id="bdc71-133">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="bdc71-134">Um diesen Wert zu testen, verwenden Sie einen bitweisen Vorgang. nicht auf Gleichheit testen.</span><span class="sxs-lookup"><span data-stu-id="bdc71-134">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdc71-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdc71-135">Return value</span></span>

<span data-ttu-id="bdc71-136">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bdc71-136">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdc71-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdc71-137">Remarks</span></span>

<span data-ttu-id="bdc71-138">Anwendungen mit nicht gespeicherten Daten könnten die Daten an einem temporären Speicherort speichern und beim nächsten Start der Anwendung wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="bdc71-138">Applications that have unsaved data could save the data to a temporary location and restore it the next time the application starts.</span></span> <span data-ttu-id="bdc71-139">Es wird empfohlen, dass Anwendungen Ihre Daten und ihren Status häufig speichern. Beispielsweise werden Daten Zwischenspeicher Vorgängen, die vom Benutzer initiiert wurden, automatisch gespeichert, um die beim Herunterfahren zu speichernde Datenmenge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="bdc71-139">It is recommended that applications save their data and state frequently; for example, automatically save data between save operations initiated by the user to reduce the amount of data to be saved at shutdown.</span></span>

<span data-ttu-id="bdc71-140">Die Anwendung muss die Funktion [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) oder [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) nicht anrufen, wenn die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdc71-140">The application need not call the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) or [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function when the session is ending.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc71-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdc71-141">Requirements</span></span>



| <span data-ttu-id="bdc71-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdc71-142">Requirement</span></span> | <span data-ttu-id="bdc71-143">Wert</span><span class="sxs-lookup"><span data-stu-id="bdc71-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc71-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdc71-144">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc71-145">\[UWP-Apps für Windows XP-Desktop-Apps \|\]</span><span class="sxs-lookup"><span data-stu-id="bdc71-145">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="bdc71-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdc71-146">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc71-147">Windows Server 2003 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bdc71-147">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="bdc71-148">Header</span><span class="sxs-lookup"><span data-stu-id="bdc71-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdc71-149"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bdc71-149"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc71-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdc71-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc71-151">Abmelden</span><span class="sxs-lookup"><span data-stu-id="bdc71-151">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="bdc71-152">Wird heruntergefahren</span><span class="sxs-lookup"><span data-stu-id="bdc71-152">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="bdc71-153">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="bdc71-153">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="bdc71-154">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="bdc71-154">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="bdc71-155">**Setprocessshutdownparameters**</span><span class="sxs-lookup"><span data-stu-id="bdc71-155">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="bdc71-156">**WM- \_ queryendsession**</span><span class="sxs-lookup"><span data-stu-id="bdc71-156">**WM\_QUERYENDSESSION**</span></span>](wm-queryendsession.md)
</dt> </dl>

 

 
