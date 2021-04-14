---
title: WM_SETFOCUS Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, nachdem es den Tastaturfokus erhalten hat.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- Tastatur-und Maus Eingaben für WM_SETFOCUS Nachricht
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b304d7f7739ce551c1efc6a1d33a934c48dc8b4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478759"
---
# <a name="wm_setfocus-message"></a>WM- \_ SetFocus-Nachricht

Wird an ein Fenster gesendet, nachdem es den Tastaturfokus erhalten hat.


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, das den Tastaturfokus verloren hat. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Zum Anzeigen einer Einfügemarke sollte eine Anwendung die entsprechenden Caretzeichen aufrufen, wenn Sie die **WM \_ SetFocus** -Nachricht empfängt.

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

[**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**WM- \_ killfokus**](wm-killfocus.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

