---
description: Die WM QUERYENDSESSION-Nachricht wird gesendet, wenn der Benutzer die Sitzung beendet oder wenn eine Anwendung eine der Funktionen zum Herunterfahren des \_ Systems aufruft.
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: WM_QUERYENDSESSION (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6807a861ffb0670013a1d1f5b98a2f202e5d7470a6c306b3ed29c42baad6e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664210"
---
# <a name="wm_queryendsession-message"></a>WM \_ QUERYENDSESSION-Meldung

Die **WM \_ QUERYENDSESSION-Nachricht** wird gesendet, wenn der Benutzer die Sitzung beendet oder wenn eine Anwendung eine der Funktionen zum Herunterfahren des Systems aufruft. Wenn eine Anwendung 0 (null) zurückgibt, wird die Sitzung nicht beendet. Das System beendet das Senden von **WM \_ QUERYENDSESSION-Nachrichten,** sobald eine Anwendung 0 (null) zurückgibt.

Nach der Verarbeitung dieser Nachricht sendet das System die [**WM \_ ENDSESSION-Nachricht**](wm-endsession.md) mit dem *wParam-Parameter,* der auf die Ergebnisse der **WM \_ QUERYENDSESSION-Nachricht festgelegt** ist.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*Hwnd* 
</dt> <dd>

Ein Handle für das Fenster.

</dd> <dt>

*uMsg* 
</dt> <dd>

Der **WM \_ QUERYENDSESSION-Bezeichner.**

</dd> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter kann einen oder mehrere der folgenden Werte sein. Wenn dieser Parameter 0 ist, wird das System heruntergefahren oder neu gestartet (es ist nicht möglich, zu bestimmen, welches Ereignis auftritt).



| Wert                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDSESSION \_ CLOSEAPP-0x00000001**</dt> <dt></dt> </dl> | Die Anwendung verwendet eine Datei, die ersetzt werden muss, das System wird serviced, oder die Systemressourcen sind erschöpft. Weitere Informationen finden Sie unter [Richtlinien für Anwendungen](../rstmgr/guidelines-for-applications.md).<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDSESSION \_ CRITICAL**</dt> <dt>0x40000000</dt> </dl> | Die Anwendung wird zum Herunterfahren gezwungen.<br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDSESSION \_ LOGOFF-0x80000000**</dt> <dt></dt> </dl>       | Der Benutzer wird abgemeldet. Weitere Informationen finden Sie unter [Logging Off](logging-off.md).<br/>                                                                                                                                   |



 

Beachten Sie, dass dieser Parameter eine Bitmaske ist. Um auf diesen Wert zu testen, verwenden Sie einen bitweisen Vorgang. nicht auf Gleichheit testen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Anwendungen sollten die Absichten des Benutzers achten und **TRUE zurückgeben.** Standardmäßig gibt die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) **TRUE für** diese Meldung zurück.

Wenn das Herunterfahren das System oder das Medium beschädigt, das bzw. das bzw. das gerade geschaltet wird, kann die Anwendung **FALSE zurückgeben.** Es ist jedoch eine bewährte Methode, die Aktionen des Benutzers zu achten.

## <a name="remarks"></a>Hinweise

Wenn eine Anwendung **TRUE für** diese Nachricht zurückgibt, empfängt sie die [**WM \_ ENDSESSION-Nachricht,**](wm-endsession.md) unabhängig davon, wie die anderen Anwendungen auf die **WM \_ QUERYENDSESSION-Nachricht** reagieren. Jede Anwendung sollte **SOFORT nach** dem Empfang dieser Nachricht TRUE oder **FALSE** zurückgeben und alle Bereinigungsvorgänge zurückverlangen, bis sie die **WM \_ ENDSESSION-Nachricht empfängt.**

Anwendungen können eine Benutzeroberfläche anzeigen, in der der Benutzer beim Herunterfahren zur Eingabe von Informationen aufgefordert wird. Dies wird jedoch nicht empfohlen. Nach fünf Sekunden zeigt das System Informationen zu den Anwendungen an, die das Herunterfahren verhindern, und ermöglicht es dem Benutzer, sie zu beenden. Beispielsweise zeigt Windows XP ein Dialogfeld an, während Windows Vista einen Vollbildbildschirm mit zusätzlichen Informationen zu den Anwendungen anzeigt, die das Herunterfahren blockieren. Wenn Ihre Anwendung das Herunterfahren des Systems blockieren oder verschieben muss, verwenden Sie die [**ShutdownBlockReasonCreate-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) Weitere Informationen finden Sie unter [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).

Konsolenanwendungen können die [**Funktion SetConsoleCtrlHandler verwenden,**](/windows/console/setconsolectrlhandler) um Benachrichtigungen zum Herunterfahren zu erhalten.

Dienstanwendungen können die [**RegisterServiceCtrlHandlerEx-Funktion**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) verwenden, um Benachrichtigungen zum Herunterfahren in einer Handlerroutine zu empfangen.

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Logging Off](logging-off.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[XP-Desktop-Apps \| UWP-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2003-Desktop-Apps \|\]<br/>                                              |
| Header<br/>                   | <dl> <dt>WinUser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Abmelden](logging-off.md)
</dt> <dt>

[Herunterfahren](shutting-down.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**WM \_ ENDSESSION**](wm-endsession.md)
</dt> </dl>

 

 
