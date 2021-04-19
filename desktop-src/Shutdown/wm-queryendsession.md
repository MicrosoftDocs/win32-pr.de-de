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
# <a name="wm_queryendsession-message"></a>WM- \_ queryendsession-Nachricht

Die **WM- \_ queryendsession** -Nachricht wird gesendet, wenn der Benutzer die Sitzung beendet, oder wenn eine Anwendung eine der Funktionen zum Herunterfahren des Systems aufruft. Wenn eine Anwendung 0 (null) zurückgibt, wird die Sitzung nicht beendet. Das System beendet das Senden von **WM- \_ queryendsession** -Nachrichten, sobald eine Anwendung NULL zurückgibt.

Nach der Verarbeitung dieser Nachricht sendet das System die [**WM- \_ EndSession**](wm-endsession.md) -Nachricht mit dem *wParam* -Parameter, der auf die Ergebnisse der **WM-Abfrage " \_ queryendsession** " festgelegt ist.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Ein Handle für das Fenster.

</dd> <dt>

*Umschlag* 
</dt> <dd>

Der **WM- \_ queryendsession** -Bezeichner.

</dd> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen. Wenn dieser Parameter 0 ist, wird das System heruntergefahren oder neu gestartet (es ist nicht möglich, zu bestimmen, welches Ereignis auftritt).



| Wert                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**EndSession \_ CloseApp**</dt> <dt>0x00000001</dt> </dl> | Von der Anwendung wird eine Datei verwendet, die ersetzt werden muss, das System gewartet wird oder die Systemressourcen erschöpft sind. Weitere Informationen finden Sie unter [Richtlinien für Anwendungen](../rstmgr/guidelines-for-applications.md).<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**EndSession \_ Kritisch**</dt> <dt>0x40000000</dt> </dl> | Die Anwendung muss heruntergefahren werden.<br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**EndSession \_**</dt>Abmeldung <dt>0x80000000</dt> </dl>       | Der Benutzer meldet sich ab. Weitere Informationen finden Sie unter [Abmelden](logging-off.md).<br/>                                                                                                                                   |



 

Beachten Sie, dass dieser Parameter eine Bitmaske ist. Um diesen Wert zu testen, verwenden Sie einen bitweisen Vorgang. nicht auf Gleichheit testen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Anwendungen sollten die Absichten des Benutzers berücksichtigen und **true** zurückgeben. Standardmäßig gibt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion für diese Nachricht **true** zurück.

Wenn das Herunterfahren das System oder die Medien beschädigt, die verbrannt werden, kann die Anwendung **false** zurückgeben. Es wird jedoch empfohlen, die Aktionen des Benutzers zu berücksichtigen.

## <a name="remarks"></a>Bemerkungen

Wenn eine Anwendung für diese Nachricht **true** zurückgibt, empfängt Sie die [**WM- \_ endsitzungs**](wm-endsession.md) Nachricht, unabhängig davon, wie die anderen Anwendungen auf die **WM- \_ queryendsession** -Nachricht reagieren. Jede Anwendung sollte beim Empfang dieser Nachricht sofort **true** oder **false** zurückgeben und alle Bereinigungs Vorgänge verzögern, bis Sie die **WM- \_ EndSession** -Nachricht empfängt.

Anwendungen können eine Benutzeroberfläche anzeigen, in der der Benutzer zur Eingabe von Informationen aufgefordert wird. Dies wird jedoch nicht empfohlen. Nach fünf Sekunden zeigt das Systeminformationen zu den Anwendungen an, die das Herunterfahren verhindern, und ermöglicht es dem Benutzer, Sie zu beenden. Windows XP zeigt z. b. ein Dialogfeld an, während in Windows Vista ein voll Bildschirm mit zusätzlichen Informationen zu den Anwendungen angezeigt wird, die das Herunterfahren blockieren. Wenn die Anwendung das Herunterfahren des Systems blockieren oder verschieben muss, verwenden Sie die [**shutdownblockreasoncreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) -Funktion. Weitere Informationen finden Sie unter [Herunterfahren von Änderungen für Windows Vista](shutdown-changes-for-windows-vista.md).

Konsolen Anwendungen können die [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) -Funktion verwenden, um eine Benachrichtigung zum Herunterfahren zu empfangen.

Dienst Anwendungen können die [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) -Funktion verwenden, um Shutdown-Benachrichtigungen in einer Handlerroutine zu empfangen.

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Abmelden](logging-off.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[UWP-Apps für Windows XP-Desktop-Apps \|\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 \[ -Desktop-Apps \| UWP-apps\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Abmelden](logging-off.md)
</dt> <dt>

[Wird heruntergefahren](shutting-down.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[**Setprocessshutdownparameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**WM- \_ Endsitzung**](wm-endsession.md)
</dt> </dl>

 

 
