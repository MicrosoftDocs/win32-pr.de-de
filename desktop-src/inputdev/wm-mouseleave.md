---
title: WM_MOUSELEAVE Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, wenn der Cursor den Client Bereich des Fensters verlässt, das in einem vorherigen Befehl von trackmouserevent angegeben wurde.
ms.assetid: b23d24ff-531a-4b6d-8848-f82ac5568995
keywords:
- Tastatur-und Maus Eingaben für WM_MOUSELEAVE Nachricht
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
ms.openlocfilehash: 7dc96022e94df7f518b21b1c9a46895fc9204b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476143"
---
# <a name="wm_mouseleave-message"></a>WM- \_ MouseLeave-Nachricht

Wird an ein Fenster gesendet, wenn der Cursor den Client Bereich des Fensters verlässt, das in einem vorherigen Befehl von [**trackmouserevent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)angegeben wurde.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_MOUSELEAVE                   0x02A3
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Wenn diese Meldung generiert wird, wird die gesamte von [**trackmouserevent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) angeforderte Überwachung abgebrochen. Die Anwendung muss **TrackMouseEvent** aufrufen, wenn der Mauszeiger wieder in das Fenster wechselt, wenn Sie das Verhalten der Mausbewegung weiter verfolgen muss.

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

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**WM- \_ ncmouseleave**](wm-ncmouseleave.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> </dl>

 

