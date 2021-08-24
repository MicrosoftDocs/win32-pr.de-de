---
description: Wird gesendet, wenn ein Fenster zerstört wird. Sie wird an die Fensterprozedur des Fensters gesendet, das zerstört wird, nachdem das Fenster vom Bildschirm entfernt wurde.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: WM_DESTROY Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7acff03f01e9bf0c8021f8324411f646341a29a5b3b6dc1f9b3493ec89010c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587450"
---
# <a name="wm_destroy-message"></a>WM \_ DESTROY-Nachricht

Wird gesendet, wenn ein Fenster zerstört wird. Sie wird an die Fensterprozedur des Fensters gesendet, das zerstört wird, nachdem das Fenster vom Bildschirm entfernt wurde.

Diese Meldung wird zuerst an das Fenster gesendet, das zerstört wird, und dann an die untergeordneten Fenster (falls vorhanden), da sie zerstört werden. Während der Verarbeitung der Nachricht kann davon ausgegangen werden, dass alle untergeordneten Fenster noch vorhanden sind.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Wenn das zu zerstörende Fenster Teil der Kette des Zwischenablage-Viewers ist (durch Aufrufen der [**SetClipboardViewer-Funktion**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) festgelegt), muss sich das Fenster aus der Kette entfernen, indem die [**ChangeClipboardChain-Funktion**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) verarbeitet wird, bevor es von der **WM \_ DESTROY-Nachricht** zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**WM \_ CLOSE**](wm-close.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
