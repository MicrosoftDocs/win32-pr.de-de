---
title: WM_NCMOUSELEAVE (Winuser.h)
description: Wird in einem Fenster veröffentlicht, wenn der Cursor den Nicht-Clientbereich des Fensters verlässt, das in einem vorherigen Aufruf von TrackMouseEvent angegeben wurde.
ms.assetid: b3ada6db-93ce-45d7-b408-d08692328aeb
keywords:
- WM_NCMOUSELEAVE der Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_NCMOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141c4f1f2483e1cbd725a70454b1df1be12c46ec1970c052938181fb511ed248
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778450"
---
# <a name="wm_ncmouseleave-message"></a>WM \_ NCMOUSELEAVE-Meldung

Wird in einem Fenster veröffentlicht, wenn der Cursor den Nicht-Clientbereich des Fensters verlässt, das in einem vorherigen Aufruf von [**TrackMouseEvent angegeben wurde.**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCMOUSELEAVE                 0x02A2
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

Alle von [**TrackMouseEvent angeforderten Nachverfolgungen**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) werden abgebrochen, wenn diese Nachricht generiert wird. Die Anwendung muss **TrackMouseEvent aufrufen,** wenn die Maus ihr Fenster erneut einlädt, wenn eine weitere Nachverfolgung des Mauszeigerzeigerverhaltens erforderlich ist.

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

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ MOUSELEAVE**](wm-mouseleave.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> </dl>

 

