---
description: Wird an eine Anwendung gesendet, wenn ein Benutzer die journalingaktivitäten der Anwendung abbricht. Die Nachricht wird mit einem NULL-Fenster Handle gepostet.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: WM_CANCELJOURNAL Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5676472d12c8cef2a03e508eca6bb742596a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350341"
---
# <a name="wm_canceljournal-message"></a>WM \_ canceljournal-Nachricht

Wird an eine Anwendung gesendet, wenn ein Benutzer die journalingaktivitäten der Anwendung abbricht. Die Nachricht wird mit einem **null** -Fenster Handle gepostet.


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

Diese Meldung gibt keinen Wert zurück. Sie soll aus einer-Hauptschleife einer Anwendung oder einer [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Hook-Prozedur, nicht aus einer Fenster Prozedur verarbeitet werden.

## <a name="remarks"></a>Bemerkungen

Journal Daten Satz-und Wiedergabe Modi sind Modi, die auf dem System angewendet werden, mit denen eine Anwendung die Benutzereingaben sequenziell aufzeichnen oder wiedergeben können. Das System gibt diese Modi ein, wenn eine Anwendung eine [*journalrecordproc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) -oder [*journalplaybackproc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) -Hook-Prozedur installiert. Wenn sich das System in einem dieser Journalmodi befindet, müssen Anwendungen das Lesen von Eingaben aus der Eingabe Warteschlange durchführen. Wenn eine Anwendung das Lesen von Eingaben beendet, während sich das System in einem journalingmodus befindet, wird die Wartezeit für andere Anwendungen erzwungen.

Um ein robustes System zu gewährleisten, das nicht von einer Anwendung als nicht reaktionsfähig festgestellt werden kann, bricht das System automatisch alle journalaktivitäten ab, wenn ein Benutzer STRG + ESC oder STRG + ALT + ENTF drückt. Das System entbindet dann alle Journalen Hook-Prozeduren und sendet eine **WM \_ canceljournal** -Nachricht mit einem **null** -Fenster Handle an die Anwendung, die den Journal Hook festgelegt hat.

Die **WM \_ canceljournal** -Nachricht weist ein Fenster Handle mit dem Wert **null** auf und kann daher nicht an eine Fenster Prozedur weitergeleitet werden. Es gibt zwei Möglichkeiten für eine Anwendung, eine **WM \_ canceljournal** -Nachricht anzuzeigen: Wenn die Anwendung in einer eigenen Hauptschleife ausgeführt wird, muss Sie die Nachricht zwischen dem Aufrufen von [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) oder der [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) -Nachricht und dem Aufrufen von [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)abfangen. Wenn die Anwendung nicht in einer eigenen Hauptschleife ausgeführt wird, muss Sie eine [*getmsgproc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) -Hook-Prozedur festlegen (durch Aufrufen von [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) , die den Typ " **WH \_ GetMessage** Hook" angibt), der die Nachricht überwacht.

Wenn eine Anwendung eine **WM- \_ canceljournal** -Nachricht sieht, kann Sie zwei Dinge annehmen: der Benutzer hat den Journal Daten Satz oder den Wiedergabemodus absichtlich abgebrochen, und das System hat bereits alle Journal Datensätze oder Wiedergabe-Hook-Prozeduren nicht eingebunden.

Beachten Sie, dass die oben erwähnten Tastenkombinationen (STRG + ESC oder STRG + ALT + ENTF) bewirken, dass das System Journal Vorgang abgebrochen wird. Wenn eine Anwendung nicht mehr reagiert, können Sie dem Benutzer eine Möglichkeit zur Wiederherstellung zur Verfügung stehen. Der Code der virtuellen Taste für den [**VK \_**](../inputdev/virtual-key-codes.md) -Abbruch (in der Regel als STRG + UNTBR-Tastenkombination implementiert) ist das, was eine Anwendung, die sich im Journal Daten Satz Modus befindet, als Signal ansehen soll, dass der Benutzer die Journal Aktivität abbrechen möchte. Der Unterschied besteht darin, dass das Überwachen von **VK \_ Cancel** ein empfohlenes Verhalten für das journalisieren von Anwendungen ist, während STRG + ESC oder STRG + ALT + ENTF bewirkt, dass das System das Journal Vorgang unabhängig vom Verhalten einer Journalen Anwendung abbricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[*Journalplaybackproc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[*Journalrecordproc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))
</dt> <dt>

[*Getmsgproc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Licher**
</dt> <dt>

[Hooks](hooks.md)
</dt> </dl>

 

 
