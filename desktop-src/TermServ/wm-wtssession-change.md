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
# <a name="wm_wtssession_change-message"></a>\_Wtssession- \_ Änderungs Meldung für WM

Benachrichtigt Anwendungen über Änderungen im Sitzungszustand.

Das Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle für das Fenster.

</dd> <dt>

 Meldung \[ in\]
</dt> <dd>

Gibt die Meldung an (**WM- \_ wtssession- \_ Änderung**).

</dd> <dt>

*wParam* \[ in\]
</dt> <dd>

Status Code, der die Ursache für das Senden der Benachrichtigung über Sitzungs Statusänderungen beschreibt. Dieser Parameter kann einen der folgenden Werte annehmen.

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ Konsolen \_ Verbindung** (0x1)


</dt> <dd>

Die von *LPARAM* identifizierte Sitzung wurde mit dem Konsolen Terminal oder der remotefx-Sitzung verbunden.

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ Konsolen \_ Trennung** (0x2)


</dt> <dd>

Die von *LPARAM* identifizierte Sitzung wurde von der Konsolen Terminal-oder remotefx-Sitzung getrennt.

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ Remote \_ Verbindung** (0x3)


</dt> <dd>

Die von *LPARAM* identifizierte Sitzung wurde mit dem Remote Terminal verbunden.

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ Remote \_ Trennung** (0x4)


</dt> <dd>

Die von *LPARAM* identifizierte Sitzung wurde vom Remote Terminal getrennt.

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ Sitzungs \_ Anmeldung** (0x5)


</dt> <dd>

Ein Benutzer hat sich bei der durch *LPARAM* identifizierten Sitzung angemeldet.

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ \_** Abmelde Sitzung (0x6)


</dt> <dd>

Ein Benutzer hat die von *LPARAM* identifizierte Sitzung abgemeldet.

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ Sitzungs \_ Sperre** (0x7)


</dt> <dd>

Die von *LPARAM* identifizierte Sitzung wurde gesperrt.

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ Aufheben \_ der Sitzung** (0x8)


</dt> <dd>

Die von *LPARAM* identifizierte Sitzung wurde entsperrt.

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ Sitzungs- \_ Remote \_ Steuerung** (0x9)


</dt> <dd>

Die von *LPARAM* identifizierte Sitzung hat den Status der Remote Kontrolle geändert. Um den Status zu ermitteln, müssen Sie [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) aufrufen und die Metrik " **SM \_ remotecontrol** " überprüfen.

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ Sitzung \_ Erstellen** (0xa)


</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ Sitzung \_ Beenden** (0xB)


</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> </dl> </dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Der Bezeichner der Sitzung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird nur an Anwendungen gesendet, die registriert wurden, um diese Nachricht durch Aufrufen von [**wzregistersessionnotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)zu empfangen.

Beispiele dafür, wie Anwendungen auf diese Nachricht reagieren können, sind das Freigeben oder erwerben von Konsolen spezifischen Ressourcen, das Festlegen der Art und Weise, wie ein Bildschirm gezeichnet werden soll, oder das Auslösen von Konsolen Animationseffekten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                           |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wwahrheits registersessionnotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

