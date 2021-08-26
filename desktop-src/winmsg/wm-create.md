---
description: Wird gesendet, wenn eine Anwendung die Erstellung eines Fensters durch Aufrufen der Funktion CreateWindowEx oder CreateWindow an fordert.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: WM_CREATE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ff80c3fe0c12aeaa8b968d2d609fb7d10765c0474ffc001b9b18385e38d149
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931280"
---
# <a name="wm_create-message"></a>WM \_ CREATE-Nachricht

Wird gesendet, wenn eine Anwendung die Erstellung eines Fensters durch Aufrufen der [**Funktion CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) oder [**CreateWindow an fordert.**](/windows/win32/api/winuser/nf-winuser-createwindowa) (Die Nachricht wird gesendet, bevor die Funktion zurückgegeben wird.) Die Fensterprozedur des neuen Fensters empfängt diese Meldung, nachdem das Fenster erstellt wurde, aber bevor das Fenster sichtbar wird.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Ein Zeiger auf eine [**CREATESTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-createstructa) die Informationen zum zu erstellenden Fenster enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Meldung verarbeitet, sollte sie 0 zurückgeben, um die Erstellung des Fensters fortsetzen zu können. Wenn die Anwendung –1 zurückgibt, wird das Fenster zerstört, und die [**CreateWindowEx-**](/windows/win32/api/winuser/nf-winuser-createwindowexa) oder [**CreateWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowa) gibt ein **NULL-Handle** zurück.

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

[**Createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**Createwindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**WM \_ NCCREATE**](wm-nccreate.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
