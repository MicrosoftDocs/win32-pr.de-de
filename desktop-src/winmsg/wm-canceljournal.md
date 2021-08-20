---
description: Wird an eine Anwendung gesendet, wenn ein Benutzer die Journalaktivitäten der Anwendung abbricht. Die Nachricht wird mit einem NULL-Fensterhandle gesendet.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: WM_CANCELJOURNAL-Nachricht (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8672f86393275c46383c6eb27c7eb1884178b86635ea93bf758de16521e6d2c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849336"
---
# <a name="wm_canceljournal-message"></a>WM \_ CANCELJOURNAL-Nachricht

Wird an eine Anwendung gesendet, wenn ein Benutzer die Journalaktivitäten der Anwendung abbricht. Die Nachricht wird mit einem **NULL-Fensterhandle** gesendet.


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **void**

Diese Meldung gibt keinen Wert zurück. Sie soll innerhalb der Hauptschleife einer Anwendung oder einer GetMessage-Hookprozedur verarbeitet werden, nicht aus einer Fensterprozedur. [](/windows/win32/api/winuser/nf-winuser-getmessage)

## <a name="remarks"></a>Hinweise

Journalaufzeichnungs- und Wiedergabemodi sind Modi, die dem System unterliegen, mit denen eine Anwendung Benutzereingaben sequenziell aufzeichnen oder wiedergeben kann. Das System wechselt in diese Modi, wenn eine Anwendung eine [*JournalRecordProc-*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) oder [*JournalPlaybackProc-Hookprozedur*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) installiert. Wenn sich das System in einem dieser Journalingmodi befindet, müssen Anwendungen die Eingaben aus der Eingabewarteschlange lesen. Wenn eine Anwendung das Lesen von Eingaben beendet, während sich das System im Journalmodus befindet, werden andere Anwendungen gezwungen zu warten.

Um ein stabiles System sicherzustellen, das nicht von einer Anwendung nicht reagiert werden kann, bricht das System automatisch alle Journalaktivitäten ab, wenn ein Benutzer STRG+ESC oder STRG+ALT+ENTF drückt. Das System hebt dann alle Journalinghook-Hookprozesuren auf und sendet eine **WM \_ CANCELJOURNAL-Nachricht** mit einem **NULL-Fensterhandle** an die Anwendung, die den Journalinghook festgelegt hat.

Die **WM \_ CANCELJOURNAL-Nachricht** verfügt über ein **NULL-Fensterhandle,** daher kann sie nicht an eine Fensterprozedur gesendet werden. Es gibt zwei Möglichkeiten für eine Anwendung, eine **WM \_ CANCELJOURNAL-Nachricht** anzuzeigen: Wenn die Anwendung in einer eigenen Hauptschleife ausgeführt wird, muss sie die Nachricht zwischen ihrem Aufruf von [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) oder [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) und dem Aufruf von [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)abfangen. Wenn die Anwendung nicht in ihrer eigenen Hauptschleife ausgeführt wird, muss sie eine [*GetMsgProc-Hookprozedur*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) festlegen (durch einen Aufruf von [**SetWindowsHookEx,**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) der den **\_ WH GETMESSAGE-Hooktyp** angibt), die auf die Nachricht überwacht.

Wenn einer Anwendung eine **WM \_ CANCELJOURNAL-Nachricht** angezeigt wird, kann davon ausgegangen werden, dass zwei Dinge angenommen werden: Der Benutzer hat den Journaldatensatz oder den Wiedergabemodus absichtlich abgebrochen, und das System hat bereits alle Journaldatensatz- oder Wiedergabehookprozeduren aufgehoben.

Beachten Sie, dass die oben erwähnten Tastenkombinationen (STRG+ESC oder STRG+ALT+ENTF) dazu führen, dass das System das Journaling abbricht. Wenn eine Anwendung nicht reagiert, gibt sie dem Benutzer eine Möglichkeit zur Wiederherstellung. Der [**VK \_ CANCEL-Code**](../inputdev/virtual-key-codes.md) für virtuelle Schlüssel (in der Regel als Tastenkombination STRG+BREAK implementiert) ist das, worauf eine Anwendung im Journaldatensatzmodus als Signal achten sollte, dass der Benutzer die Journalaktivität abbrechen möchte. Der Unterschied besteht darin, dass das Überwachen von **VK \_ CANCEL** ein empfohlenes Verhalten für Journalanwendungen ist, während STRG+ESC oder STRG+ALT+ENTF dazu führen, dass das System die Journaling unabhängig vom Verhalten einer Journalanwendung abbricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))
</dt> <dt>

[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Hooks](hooks.md)
</dt> </dl>

 

 
