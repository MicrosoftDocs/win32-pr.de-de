---
title: WM_WTSSESSION_CHANGE Meldung (Winuser. h)
description: Benachrichtigt Anwendungen über Änderungen im Sitzungszustand.
ms.assetid: 758a130c-b75a-40fd-8530-3766aa86c5ba
ms.tgt_platform: multiple
keywords:
- WM_WTSSESSION_CHANGE Meldung Remotedesktopdienste
topic_type:
- apiref
api_name:
- WM_WTSSESSION_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f1dc421aa160824a194588711e84f961ea4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740169"
---
# <a name="wm_wtssession_change-message"></a><span data-ttu-id="5bd86-104">\_Wtssession- \_ Änderungs Meldung für WM</span><span class="sxs-lookup"><span data-stu-id="5bd86-104">WM\_WTSSESSION\_CHANGE message</span></span>

<span data-ttu-id="5bd86-105">Benachrichtigt Anwendungen über Änderungen im Sitzungszustand.</span><span class="sxs-lookup"><span data-stu-id="5bd86-105">Notifies applications of changes in session state.</span></span>

<span data-ttu-id="5bd86-106">Das Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5bd86-106">The window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a><span data-ttu-id="5bd86-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bd86-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bd86-108">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bd86-108">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd86-109">Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="5bd86-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="5bd86-110"> Meldung \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bd86-110">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd86-111">Gibt die Meldung an (**WM- \_ wtssession- \_ Änderung**).</span><span class="sxs-lookup"><span data-stu-id="5bd86-111">Specifies the message (**WM\_WTSSESSION\_CHANGE**).</span></span>

</dd> <dt>

<span data-ttu-id="5bd86-112">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bd86-112">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd86-113">Status Code, der die Ursache für das Senden der Benachrichtigung über Sitzungs Statusänderungen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5bd86-113">Status code describing the reason the session state change notification was sent.</span></span> <span data-ttu-id="5bd86-114">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="5bd86-114">This parameter can be one of the following values.</span></span>

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span data-ttu-id="5bd86-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ Konsolen \_ Verbindung** (0x1)</span><span class="sxs-lookup"><span data-stu-id="5bd86-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS\_CONSOLE\_CONNECT** (0x1)</span></span>


</dt> <dd>

<span data-ttu-id="5bd86-116">Die von *LPARAM* identifizierte Sitzung wurde mit dem Konsolen Terminal oder der remotefx-Sitzung verbunden.</span><span class="sxs-lookup"><span data-stu-id="5bd86-116">The session identified by *lParam* was connected to the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span data-ttu-id="5bd86-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ Konsolen \_ Trennung** (0x2)</span><span class="sxs-lookup"><span data-stu-id="5bd86-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS\_CONSOLE\_DISCONNECT** (0x2)</span></span>


</dt> <dd>

<span data-ttu-id="5bd86-118">Die von *LPARAM* identifizierte Sitzung wurde von der Konsolen Terminal-oder remotefx-Sitzung getrennt.</span><span class="sxs-lookup"><span data-stu-id="5bd86-118">The session identified by *lParam* was disconnected from the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span data-ttu-id="5bd86-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ Remote \_ Verbindung** (0x3)</span><span class="sxs-lookup"><span data-stu-id="5bd86-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS\_REMOTE\_CONNECT** (0x3)</span></span>


</dt> <dd>

<span data-ttu-id="5bd86-120">Die von *LPARAM* identifizierte Sitzung wurde mit dem Remote Terminal verbunden.</span><span class="sxs-lookup"><span data-stu-id="5bd86-120">The session identified by *lParam* was connected to the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span data-ttu-id="5bd86-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ Remote \_ Trennung** (0x4)</span><span class="sxs-lookup"><span data-stu-id="5bd86-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS\_REMOTE\_DISCONNECT** (0x4)</span></span>


</dt> <dd>

<span data-ttu-id="5bd86-122">Die von *LPARAM* identifizierte Sitzung wurde vom Remote Terminal getrennt.</span><span class="sxs-lookup"><span data-stu-id="5bd86-122">The session identified by *lParam* was disconnected from the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span data-ttu-id="5bd86-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ Sitzungs \_ Anmeldung** (0x5)</span><span class="sxs-lookup"><span data-stu-id="5bd86-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS\_SESSION\_LOGON** (0x5)</span></span>


</dt> <dd>

<span data-ttu-id="5bd86-124">Ein Benutzer hat sich bei der durch *LPARAM* identifizierten Sitzung angemeldet.</span><span class="sxs-lookup"><span data-stu-id="5bd86-124">A user has logged on to the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span data-ttu-id="5bd86-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ \_** Abmelde Sitzung (0x6)</span><span class="sxs-lookup"><span data-stu-id="5bd86-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS\_SESSION\_LOGOFF** (0x6)</span></span>


</dt> <dd>

<span data-ttu-id="5bd86-126">Ein Benutzer hat die von *LPARAM* identifizierte Sitzung abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="5bd86-126">A user has logged off the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span data-ttu-id="5bd86-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ Sitzungs \_ Sperre** (0x7)</span><span class="sxs-lookup"><span data-stu-id="5bd86-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS\_SESSION\_LOCK** (0x7)</span></span>


</dt> <dd>

<span data-ttu-id="5bd86-128">Die von *LPARAM* identifizierte Sitzung wurde gesperrt.</span><span class="sxs-lookup"><span data-stu-id="5bd86-128">The session identified by *lParam* has been locked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span data-ttu-id="5bd86-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ Aufheben \_ der Sitzung** (0x8)</span><span class="sxs-lookup"><span data-stu-id="5bd86-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS\_SESSION\_UNLOCK** (0x8)</span></span>


</dt> <dd>

<span data-ttu-id="5bd86-130">Die von *LPARAM* identifizierte Sitzung wurde entsperrt.</span><span class="sxs-lookup"><span data-stu-id="5bd86-130">The session identified by *lParam* has been unlocked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span data-ttu-id="5bd86-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ Sitzungs- \_ Remote \_ Steuerung** (0x9)</span><span class="sxs-lookup"><span data-stu-id="5bd86-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS\_SESSION\_REMOTE\_CONTROL** (0x9)</span></span>


</dt> <dd>

<span data-ttu-id="5bd86-132">Die von *LPARAM* identifizierte Sitzung hat den Status der Remote Kontrolle geändert.</span><span class="sxs-lookup"><span data-stu-id="5bd86-132">The session identified by *lParam* has changed its remote controlled status.</span></span> <span data-ttu-id="5bd86-133">Um den Status zu ermitteln, müssen Sie [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) aufrufen und die Metrik " **SM \_ remotecontrol** " überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5bd86-133">To determine the status, call [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) and check the **SM\_REMOTECONTROL** metric.</span></span>

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span data-ttu-id="5bd86-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ Sitzung \_ Erstellen** (0xa)</span><span class="sxs-lookup"><span data-stu-id="5bd86-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS\_SESSION\_CREATE** (0xA)</span></span>


</dt> <dd>

<span data-ttu-id="5bd86-135">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5bd86-135">Reserved for future use.</span></span>

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span data-ttu-id="5bd86-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ Sitzung \_ Beenden** (0xB)</span><span class="sxs-lookup"><span data-stu-id="5bd86-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS\_SESSION\_TERMINATE** (0xB)</span></span>


</dt> <dd>

<span data-ttu-id="5bd86-137">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5bd86-137">Reserved for future use.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5bd86-138">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bd86-138">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd86-139">Der Bezeichner der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="5bd86-139">The identifier of the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bd86-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5bd86-140">Return value</span></span>

<span data-ttu-id="5bd86-141">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5bd86-141">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bd86-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bd86-142">Remarks</span></span>

<span data-ttu-id="5bd86-143">Diese Meldung wird nur an Anwendungen gesendet, die registriert wurden, um diese Nachricht durch Aufrufen von [**wzregistersessionnotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="5bd86-143">This message is sent only to applications that have registered to receive this message by calling [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).</span></span>

<span data-ttu-id="5bd86-144">Beispiele dafür, wie Anwendungen auf diese Nachricht reagieren können, sind das Freigeben oder erwerben von Konsolen spezifischen Ressourcen, das Festlegen der Art und Weise, wie ein Bildschirm gezeichnet werden soll, oder das Auslösen von Konsolen Animationseffekten.</span><span class="sxs-lookup"><span data-stu-id="5bd86-144">Examples of how applications can respond to this message include releasing or acquiring console-specific resources, determining how a screen is to be painted, or triggering console animation effects.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bd86-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bd86-145">Requirements</span></span>



| <span data-ttu-id="5bd86-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bd86-146">Requirement</span></span> | <span data-ttu-id="5bd86-147">Wert</span><span class="sxs-lookup"><span data-stu-id="5bd86-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd86-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5bd86-148">Minimum supported client</span></span><br/> | <span data-ttu-id="5bd86-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5bd86-149">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="5bd86-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5bd86-150">Minimum supported server</span></span><br/> | <span data-ttu-id="5bd86-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5bd86-151">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="5bd86-152">Header</span><span class="sxs-lookup"><span data-stu-id="5bd86-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bd86-153"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5bd86-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bd86-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bd86-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd86-155">**Wwahrheits registersessionnotification**</span><span class="sxs-lookup"><span data-stu-id="5bd86-155">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[<span data-ttu-id="5bd86-156">**WTSUnRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="5bd86-156">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

