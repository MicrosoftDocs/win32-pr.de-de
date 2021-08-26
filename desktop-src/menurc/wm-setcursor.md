---
title: WM_SETCURSOR Meldung (Winuser.h)
description: Wird an ein Fenster gesendet, wenn die Maus bewirkt, dass der Cursor innerhalb eines Fensters bewegt wird und die Mauseingabe nicht erfasst wird.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR Meldung Menüs und andere Ressourcen
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
ms.openlocfilehash: 19dccc4fab0d24dd233133e97b3ddcc71f615d9abb27a4684821099b6ad15802
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846870"
---
# <a name="wm_setcursor-message"></a>WM \_ SETCURSOR-Nachricht

Wird an ein Fenster gesendet, wenn die Maus bewirkt, dass der Cursor innerhalb eines Fensters bewegt wird und die Mauseingabe nicht erfasst wird.


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

Das Wort *lParam* mit niedriger Reihenfolge gibt das Treffertestergebnis für die Cursorposition an. Mögliche Werte finden Sie in den Rückgabewerten für [WM_NCHITTEST.](../inputdev/wm-nchittest.md)

Das Wort *lParam* in hoher Reihenfolge gibt die Mausfenstermeldung an, die dieses Ereignis ausgelöst hat, z. [B. WM_MOUSEMOVE](../inputdev/wm-mousemove.md). Wenn das Fenster in den Menümodus wechselt, ist dieser Wert 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie **TRUE** zurückgeben, um die weitere Verarbeitung anzuhalten, oder **FALSE,** um fortzufahren.

## <a name="remarks"></a>Hinweise

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) übergibt die **WM \_ SETCURSOR-Nachricht** vor der Verarbeitung an ein übergeordnetes Fenster. Wenn das übergeordnete Fenster **TRUE** zurückgibt, wird die weitere Verarbeitung angehalten. Wenn die Nachricht an das übergeordnete Fenster eines Fensters übergeben wird, kann das übergeordnete Fenster die Einstellung des Cursors in einem untergeordneten Fenster steuern. Die **DefWindowProc-Funktion** verwendet diese Meldung auch, um den Cursor auf einen Pfeil festzulegen, wenn er sich nicht im Clientbereich befindet, oder auf den registrierten Klassencursor, wenn er sich im Clientbereich befindet. Wenn das Wort in niedriger Reihenfolge des *lParam-Parameters* **HTERROR** ist und das Wort *lParam* in hoher Reihenfolge angibt, dass eine der Maustasten gedrückt wird, ruft **DefWindowProc** die [**MessageBeep-Funktion**](/windows/desktop/api/winuser/nf-winuser-messagebeep) auf.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Cursor](cursors.md)
</dt> </dl>

 

