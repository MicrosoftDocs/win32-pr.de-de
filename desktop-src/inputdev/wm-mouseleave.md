---
title: WM_MOUSELEAVE Meldung (Winuser.h)
description: Wird an ein Fenster gesendet, wenn der Cursor den Clientbereich des Fensters verlässt, der in einem vorherigen Aufruf von TrackMouseEvent angegeben wurde.
ms.assetid: b23d24ff-531a-4b6d-8848-f82ac5568995
keywords:
- WM_MOUSELEAVE Meldung Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_MOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c115ed30da9651167d72bb8c3af604a8444bc0ddcec991df3f76f7a0edee4517
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451450"
---
# <a name="wm_mouseleave-message"></a>WM \_ MOUSELEAVE-Nachricht

Wird an ein Fenster gesendet, wenn der Cursor den Clientbereich des Fensters verlässt, der in einem vorherigen Aufruf von [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)angegeben wurde.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_MOUSELEAVE                   0x02A3
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Die gesamte von [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) angeforderte Nachverfolgung wird abgebrochen, wenn diese Nachricht generiert wird. Die Anwendung muss **TrackMouseEvent** aufrufen, wenn die Maus ihr Fenster erneut einblendt, wenn sie eine weitere Nachverfolgung des Mauszeigerverhaltens erfordert.

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

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**WM \_ NCMOUSELEAVE**](wm-ncmouseleave.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> </dl>

 

