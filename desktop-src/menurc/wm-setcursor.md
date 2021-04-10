---
title: WM_SETCURSOR Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, wenn die Maus bewirkt, dass der Cursor innerhalb eines Fensters bewegt wird und die Maus Eingaben nicht aufgezeichnet werden.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e941919b447659e67fdcdd9e4e5f4ff2630f8bf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040696"
---
# <a name="wm_setcursor-message"></a>WM- \_ SetCursor-Nachricht

Wird an ein Fenster gesendet, wenn die Maus bewirkt, dass der Cursor innerhalb eines Fensters bewegt wird und die Maus Eingaben nicht aufgezeichnet werden.


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, das den Cursor enthält.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort von *LPARAM* gibt das Treffer Testergebnis für die Cursorposition an. Mögliche Werte finden Sie in den Rückgabe Werten für [WM_NCHITTEST](../inputdev/wm-nchittest.md) .

Das hochwertige Wort *LPARAM* gibt die Maus Fenster Meldung an, die dieses Ereignis ausgelöst hat, z. b. [WM_MOUSEMOVE](../inputdev/wm-mousemove.md). Wenn das Fenster in den Menü Modus wechselt, ist dieser Wert 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true** " zurückgeben, um die weitere Verarbeitung anzuhalten, oder " **false** ".

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) -Funktion übergibt die **WM- \_ SetCursor** -Nachricht vor der Verarbeitung an ein übergeordnetes Fenster. Wenn das übergeordnete Fenster **true** zurückgibt, wird die weitere Verarbeitung angehalten. Durch das übergeben der Nachricht an das übergeordnete Fenster eines Fensters erhält das übergeordnete Fenster Steuerelement über die Cursor Einstellung in einem untergeordneten Fenster. Die **defwindowproc** -Funktion verwendet diese Meldung auch, um den Cursor auf einen Pfeil festzulegen, wenn er sich nicht im Client Bereich befindet, oder an den registrierten Klassen Cursor, wenn er sich im Client Bereich befindet. Wenn das nieder wertige Wort des *LPARAM* -Parameters **HTError** und das hochwertige Wort *LPARAM* angibt, dass eine der Maustasten gedrückt ist, ruft **defwindowproc** die [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) -Funktion auf.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Licher**
</dt> <dt>

[Cursor](cursors.md)
</dt> </dl>

 

