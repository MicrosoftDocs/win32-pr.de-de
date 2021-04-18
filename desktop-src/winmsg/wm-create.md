---
description: Wird gesendet, wenn eine Anwendung anfordert, dass ein Fenster durch Aufrufen der CreateWindowEx-oder CreateWindow-Funktion erstellt wird.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: WM_CREATE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37437adbb4df714d7604af59a2abdd11ac9d00a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347483"
---
# <a name="wm_create-message"></a>WM- \_ Nachricht erstellen

Wird gesendet, wenn eine Anwendung anfordert, dass ein Fenster durch Aufrufen der [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) -oder [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) -Funktion erstellt wird. (Die Nachricht wird gesendet, bevor die Funktion zurückgegeben wird.) Die Fenster Prozedur des neuen Fensters empfängt diese Meldung, nachdem das Fenster erstellt wurde, aber bevor das Fenster sichtbar wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**kreatestruct**](/windows/win32/api/winuser/ns-winuser-createstructa) -Struktur, die Informationen über das Fenster enthält, das erstellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben, um die Erstellung des Fensters fortzusetzen. Wenn die Anwendung "– 1" zurückgibt, wird das Fenster zerstört, und die Funktion " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " oder " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " gibt ein **null** -Handle zurück.

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

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**WM- \_ nccreate**](wm-nccreate.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
