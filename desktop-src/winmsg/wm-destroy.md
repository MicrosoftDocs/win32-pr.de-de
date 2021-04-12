---
description: Wird gesendet, wenn ein Fenster zerstört wird. Sie wird an die Fenster Prozedur des Fensters gesendet, das zerstört wird, nachdem das Fenster aus dem Bildschirm entfernt wurde.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: WM_DESTROY Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db195c22c38759146fb76e98edf4ca7f605a1c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216960"
---
# <a name="wm_destroy-message"></a>WM-Lösch \_ Meldung

Wird gesendet, wenn ein Fenster zerstört wird. Sie wird an die Fenster Prozedur des Fensters gesendet, das zerstört wird, nachdem das Fenster aus dem Bildschirm entfernt wurde.

Diese Meldung wird zuerst an das Fenster gesendet, das zerstört wird, und dann an die untergeordneten Fenster (sofern vorhanden), wenn Sie zerstört werden. Bei der Verarbeitung der Nachricht kann davon ausgegangen werden, dass alle untergeordneten Fenster noch vorhanden sind.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_DESTROY                      0x0002
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

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Wenn das Fenster, das zerstört wird, Teil der Zwischenablage-Viewer-Kette ist (durch Aufrufen der [**setclipboardviewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) -Funktion festgelegt), muss sich das Fenster selbst aus der Kette entfernen, indem die [**changeclipboardchain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) -Funktion verarbeitet wird, bevor die WM-Lösch Nachricht zurückgegeben wird. **\_**

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

[**Changeclipboardchain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**Setclipboardviewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**WM \_ Schließen**](wm-close.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
