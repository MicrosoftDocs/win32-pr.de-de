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
# <a name="wm_endsession-message"></a>WM- \_ endsitzungs Nachricht

Die **WM- \_ endsitzungs** Nachricht wird an eine Anwendung gesendet, nachdem das System die Ergebnisse der [**WM \_ queryendsession**](wm-queryendsession.md) -Nachricht verarbeitet hat. Die **WM- \_ EndSession** -Nachricht informiert die Anwendung darüber, ob die Sitzung beendet wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
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

Der **WM- \_ endsitzungs** Bezeichner.

</dd> <dt>

*wParam* 
</dt> <dd>

Wenn die Sitzung beendet wird, ist dieser Parameter " **true**". die Sitzung kann jederzeit beendet werden, nachdem alle Anwendungen die Verarbeitung dieser Nachricht durchgeführt haben. Andernfalls ist Sie **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen. Wenn dieser Parameter 0 ist, wird das System heruntergefahren oder neu gestartet (es ist nicht möglich, zu bestimmen, welches Ereignis auftritt).



| Wert                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**EndSession \_ CloseApp**</dt> <dt>0x1</dt> </dl>        | Wenn *wParam* den Wert **true** hat, muss die Anwendung heruntergefahren werden. Alle Daten sollten automatisch gespeichert werden, ohne den Benutzer aufzufordern (Weitere Informationen finden Sie unter "Hinweise"). Der Neustart-Manager sendet diese Meldung, wenn die Anwendung eine Datei verwendet, die ersetzt werden muss, wenn Sie das System bedienen muss oder wenn die Systemressourcen erschöpft sind. Die Anwendung wird neu gestartet, wenn Sie sich für den Neustart mithilfe der [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) -Funktion registriert hat. Weitere Informationen finden Sie unter [Richtlinien für Anwendungen](../rstmgr/guidelines-for-applications.md). <br/> Wenn *wParam* den Wert **false** hat, sollte die Anwendung nicht heruntergefahren werden.<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**EndSession \_ Kritisch**</dt> <dt>0x40000000</dt> </dl> | Die Anwendung muss heruntergefahren werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**EndSession \_**</dt>Abmeldung <dt>0x80000000</dt> </dl>       | Der Benutzer meldet sich ab. Weitere Informationen finden Sie unter [Abmelden](logging-off.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Beachten Sie, dass dieser Parameter eine Bitmaske ist. Um diesen Wert zu testen, verwenden Sie einen bitweisen Vorgang. nicht auf Gleichheit testen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Anwendungen mit nicht gespeicherten Daten könnten die Daten an einem temporären Speicherort speichern und beim nächsten Start der Anwendung wiederherstellen. Es wird empfohlen, dass Anwendungen Ihre Daten und ihren Status häufig speichern. Beispielsweise werden Daten Zwischenspeicher Vorgängen, die vom Benutzer initiiert wurden, automatisch gespeichert, um die beim Herunterfahren zu speichernde Datenmenge zu verringern.

Die Anwendung muss die Funktion [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) oder [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) nicht anrufen, wenn die Sitzung beendet wird.

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

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**Setprocessshutdownparameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**WM- \_ queryendsession**](wm-queryendsession.md)
</dt> </dl>

 

 
