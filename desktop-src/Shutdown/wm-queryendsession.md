---
description: Die WM- \_ queryendsession-Nachricht wird gesendet, wenn der Benutzer die Sitzung beendet, oder wenn eine Anwendung eine der Funktionen zum Herunterfahren des Systems aufruft.
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: WM_QUERYENDSESSION Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2e2f82388b229523f371c680d6ccc7c4b1e27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362969"
---
# <a name="wm_queryendsession-message"></a><span data-ttu-id="0b738-103">WM- \_ queryendsession-Nachricht</span><span class="sxs-lookup"><span data-stu-id="0b738-103">WM\_QUERYENDSESSION message</span></span>

<span data-ttu-id="0b738-104">Die **WM- \_ queryendsession** -Nachricht wird gesendet, wenn der Benutzer die Sitzung beendet, oder wenn eine Anwendung eine der Funktionen zum Herunterfahren des Systems aufruft.</span><span class="sxs-lookup"><span data-stu-id="0b738-104">The **WM\_QUERYENDSESSION** message is sent when the user chooses to end the session or when an application calls one of the system shutdown functions.</span></span> <span data-ttu-id="0b738-105">Wenn eine Anwendung 0 (null) zurückgibt, wird die Sitzung nicht beendet.</span><span class="sxs-lookup"><span data-stu-id="0b738-105">If any application returns zero, the session is not ended.</span></span> <span data-ttu-id="0b738-106">Das System beendet das Senden von **WM- \_ queryendsession** -Nachrichten, sobald eine Anwendung NULL zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0b738-106">The system stops sending **WM\_QUERYENDSESSION** messages as soon as one application returns zero.</span></span>

<span data-ttu-id="0b738-107">Nach der Verarbeitung dieser Nachricht sendet das System die [**WM- \_ EndSession**](wm-endsession.md) -Nachricht mit dem *wParam* -Parameter, der auf die Ergebnisse der **WM-Abfrage " \_ queryendsession** " festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0b738-107">After processing this message, the system sends the [**WM\_ENDSESSION**](wm-endsession.md) message with the *wParam* parameter set to the results of the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="0b738-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0b738-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="0b738-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b738-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b738-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="0b738-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0b738-111">Ein Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="0b738-111">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="0b738-112">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="0b738-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="0b738-113">Der **WM- \_ queryendsession** -Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="0b738-113">The **WM\_QUERYENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0b738-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b738-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b738-115">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="0b738-115">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="0b738-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b738-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b738-117">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0b738-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="0b738-118">Wenn dieser Parameter 0 ist, wird das System heruntergefahren oder neu gestartet (es ist nicht möglich, zu bestimmen, welches Ereignis auftritt).</span><span class="sxs-lookup"><span data-stu-id="0b738-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="0b738-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0b738-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="0b738-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0b738-120">Meaning</span></span>                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="0b738-121"><dt>**EndSession \_ CloseApp**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0b738-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="0b738-122">Von der Anwendung wird eine Datei verwendet, die ersetzt werden muss, das System gewartet wird oder die Systemressourcen erschöpft sind.</span><span class="sxs-lookup"><span data-stu-id="0b738-122">The application is using a file that must be replaced, the system is being serviced, or system resources are exhausted.</span></span> <span data-ttu-id="0b738-123">Weitere Informationen finden Sie unter [Richtlinien für Anwendungen](../rstmgr/guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="0b738-123">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="0b738-124"><dt>**EndSession \_ Kritisch**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="0b738-124"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="0b738-125">Die Anwendung muss heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="0b738-125">The application is forced to shut down.</span></span><br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="0b738-126"><dt>**EndSession \_**</dt>Abmeldung <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="0b738-126"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="0b738-127">Der Benutzer meldet sich ab.</span><span class="sxs-lookup"><span data-stu-id="0b738-127">The user is logging off.</span></span> <span data-ttu-id="0b738-128">Weitere Informationen finden Sie unter [Abmelden](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="0b738-128">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                   |



 

<span data-ttu-id="0b738-129">Beachten Sie, dass dieser Parameter eine Bitmaske ist.</span><span class="sxs-lookup"><span data-stu-id="0b738-129">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="0b738-130">Um diesen Wert zu testen, verwenden Sie einen bitweisen Vorgang. nicht auf Gleichheit testen.</span><span class="sxs-lookup"><span data-stu-id="0b738-130">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b738-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b738-131">Return value</span></span>

<span data-ttu-id="0b738-132">Anwendungen sollten die Absichten des Benutzers berücksichtigen und **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0b738-132">Applications should respect the user's intentions and return **TRUE**.</span></span> <span data-ttu-id="0b738-133">Standardmäßig gibt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion für diese Nachricht **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="0b738-133">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE** for this message.</span></span>

<span data-ttu-id="0b738-134">Wenn das Herunterfahren das System oder die Medien beschädigt, die verbrannt werden, kann die Anwendung **false** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0b738-134">If shutting down would corrupt the system or media that is being burned, the application can return **FALSE**.</span></span> <span data-ttu-id="0b738-135">Es wird jedoch empfohlen, die Aktionen des Benutzers zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="0b738-135">However, it is good practice to respect the user's actions.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b738-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b738-136">Remarks</span></span>

<span data-ttu-id="0b738-137">Wenn eine Anwendung für diese Nachricht **true** zurückgibt, empfängt Sie die [**WM- \_ endsitzungs**](wm-endsession.md) Nachricht, unabhängig davon, wie die anderen Anwendungen auf die **WM- \_ queryendsession** -Nachricht reagieren.</span><span class="sxs-lookup"><span data-stu-id="0b738-137">When an application returns **TRUE** for this message, it receives the [**WM\_ENDSESSION**](wm-endsession.md) message, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span> <span data-ttu-id="0b738-138">Jede Anwendung sollte beim Empfang dieser Nachricht sofort **true** oder **false** zurückgeben und alle Bereinigungs Vorgänge verzögern, bis Sie die **WM- \_ EndSession** -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="0b738-138">Each application should return **TRUE** or **FALSE** immediately upon receiving this message, and defer any cleanup operations until it receives the **WM\_ENDSESSION** message.</span></span>

<span data-ttu-id="0b738-139">Anwendungen können eine Benutzeroberfläche anzeigen, in der der Benutzer zur Eingabe von Informationen aufgefordert wird. Dies wird jedoch nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="0b738-139">Applications can display a user interface prompting the user for information at shutdown, however it is not recommended.</span></span> <span data-ttu-id="0b738-140">Nach fünf Sekunden zeigt das Systeminformationen zu den Anwendungen an, die das Herunterfahren verhindern, und ermöglicht es dem Benutzer, Sie zu beenden.</span><span class="sxs-lookup"><span data-stu-id="0b738-140">After five seconds, the system displays information about the applications that are preventing shutdown and allows the user to terminate them.</span></span> <span data-ttu-id="0b738-141">Windows XP zeigt z. b. ein Dialogfeld an, während in Windows Vista ein voll Bildschirm mit zusätzlichen Informationen zu den Anwendungen angezeigt wird, die das Herunterfahren blockieren.</span><span class="sxs-lookup"><span data-stu-id="0b738-141">For example, Windows XP displays a dialog box, while Windows Vista displays a full screen with additional information about the applications blocking shutdown.</span></span> <span data-ttu-id="0b738-142">Wenn die Anwendung das Herunterfahren des Systems blockieren oder verschieben muss, verwenden Sie die [**shutdownblockreasoncreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0b738-142">If your application must block or postpone system shutdown, use the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span> <span data-ttu-id="0b738-143">Weitere Informationen finden Sie unter [Herunterfahren von Änderungen für Windows Vista](shutdown-changes-for-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="0b738-143">For more information, see [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).</span></span>

<span data-ttu-id="0b738-144">Konsolen Anwendungen können die [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) -Funktion verwenden, um eine Benachrichtigung zum Herunterfahren zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="0b738-144">Console applications can use the [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) function to receive shutdown notification.</span></span>

<span data-ttu-id="0b738-145">Dienst Anwendungen können die [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) -Funktion verwenden, um Shutdown-Benachrichtigungen in einer Handlerroutine zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="0b738-145">Service applications can use the [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function to receive shutdown notifications in a handler routine.</span></span>

## <a name="examples"></a><span data-ttu-id="0b738-146">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b738-146">Examples</span></span>

<span data-ttu-id="0b738-147">Ein Beispiel finden Sie unter [Abmelden](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="0b738-147">For an example, see [Logging Off](logging-off.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b738-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b738-148">Requirements</span></span>



| <span data-ttu-id="0b738-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b738-149">Requirement</span></span> | <span data-ttu-id="0b738-150">Wert</span><span class="sxs-lookup"><span data-stu-id="0b738-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b738-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b738-151">Minimum supported client</span></span><br/> | <span data-ttu-id="0b738-152">\[UWP-Apps für Windows XP-Desktop-Apps \|\]</span><span class="sxs-lookup"><span data-stu-id="0b738-152">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="0b738-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b738-153">Minimum supported server</span></span><br/> | <span data-ttu-id="0b738-154">Windows Server 2003 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0b738-154">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="0b738-155">Header</span><span class="sxs-lookup"><span data-stu-id="0b738-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b738-156"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0b738-156"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b738-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b738-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b738-158">Abmelden</span><span class="sxs-lookup"><span data-stu-id="0b738-158">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="0b738-159">Wird heruntergefahren</span><span class="sxs-lookup"><span data-stu-id="0b738-159">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="0b738-160">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="0b738-160">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="0b738-161">**Exitwindows**</span><span class="sxs-lookup"><span data-stu-id="0b738-161">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[<span data-ttu-id="0b738-162">**Setprocessshutdownparameters**</span><span class="sxs-lookup"><span data-stu-id="0b738-162">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="0b738-163">**WM- \_ Endsitzung**</span><span class="sxs-lookup"><span data-stu-id="0b738-163">**WM\_ENDSESSION**</span></span>](wm-endsession.md)
</dt> </dl>

 

 
