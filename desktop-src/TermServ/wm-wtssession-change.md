---
title: WM_WTSSESSION_CHANGE (Winuser.h)
description: Benachrichtigt Anwendungen über Änderungen im Sitzungszustand.
ms.assetid: 758a130c-b75a-40fd-8530-3766aa86c5ba
ms.tgt_platform: multiple
keywords:
- WM_WTSSESSION_CHANGE-Remotedesktopdienste
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
ms.openlocfilehash: f29bef7eb7778602a256f80cb04e47eae905a245783906c3388b576aecedee18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419840"
---
# <a name="wm_wtssession_change-message"></a>WM \_ WTSSESSION \_ CHANGE-Meldung

Benachrichtigt Anwendungen über Änderungen im Sitzungszustand.

Das Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*hWnd* \[ In\]
</dt> <dd>

Handle zum Fenster.

</dd> <dt>

*Msg* \[ In\]
</dt> <dd>

Gibt die Meldung an (**WM \_ WTSSESSION \_ CHANGE**).

</dd> <dt>

*wParam* \[ In\]
</dt> <dd>

Statuscode, der den Grund für das Senden der Sitzungszustandsänderungsbenachrichtigung beschreibt. Dieser Parameter kann einen der folgenden Werte annehmen.

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ CONSOLE \_ CONNECT** (0X1)


</dt> <dd>

Die von *lParam identifizierte* Sitzung wurde mit dem Konsolenterminal oder der RemoteFX verbunden.

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ CONSOLE \_ DISCONNECT** (0X2)


</dt> <dd>

Die von *lParam identifizierte* Sitzung wurde vom Konsolenterminal oder der RemoteFX getrennt.

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ REMOTE \_ CONNECT** (0x3)


</dt> <dd>

Die von *lParam identifizierte Sitzung* wurde mit dem Remoteterminal verbunden.

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ REMOTE \_ DISCONNECT** (0x4)


</dt> <dd>

Die von *lParam identifizierte* Sitzung wurde vom Remoteterminal getrennt.

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ \_SITZUNGSANMELDUNG** (0x5)


</dt> <dd>

Ein Benutzer hat sich bei der durch *lParam* identifizierten Sitzung angemeldet.

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ \_SITZUNGSANMELDUNG** (0x6)


</dt> <dd>

Ein Benutzer hat die durch *lParam identifizierte Sitzung abgemelgt.*

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ \_SITZUNGSSPERRE** (0x7)


</dt> <dd>

Die von *lParam identifizierte* Sitzung wurde gesperrt.

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ \_SITZUNGSENTSPERRUNG** (0x8)


</dt> <dd>

Die von *lParam identifizierte* Sitzung wurde entsperrt.

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ \_ \_ SITZUNGS-REMOTESTEUERUNG** (0x9)


</dt> <dd>

Die von *lParam identifizierte* Sitzung hat ihren remote gesteuerten Status geändert. Um den Status zu ermitteln, rufen [**Sie GetSystemMetrics auf,**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) und überprüfen Sie die **Metrik SM \_ REMOTECONTROL.**

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ SESSION \_ CREATE** (0xA)


</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ SESSION \_ TERMINATE** (0xB)


</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> </dl> </dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Der Bezeichner der Sitzung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Diese Nachricht wird nur an Anwendungen gesendet, die sich durch Aufrufen von [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)für den Empfang dieser Nachricht registriert haben.

Beispiele dafür, wie Anwendungen auf diese Meldung reagieren können, sind das Freigeben oder Abrufen konsolenspezifischer Ressourcen, das Bestimmen der Art des Zeichnens eines Bildschirms oder das Auslösen von Konsolenanimationseffekten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                           |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

