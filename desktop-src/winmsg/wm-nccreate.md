---
description: Wird vor der WM \_ CREATE-Nachricht gesendet, wenn ein Fenster zum ersten Mal erstellt wird.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: WM_NCCREATE Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa5638ef1b97365d202f2049fc79712d0ed3eec167825110f7c7967ce4605c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200056"
---
# <a name="wm_nccreate-message"></a>WM \_ NCCREATE-Nachricht

Wird vor der [**WM \_ CREATE-Nachricht**](wm-create.md) gesendet, wenn ein Fenster zum ersten Mal erstellt wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die [**CREATESTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-createstructa) die Informationen über das zu erstellende Fenster enthält. Die Elemente von **CREATESTRUCT** sind mit den Parametern der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) identisch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie **TRUE** zurückgeben, um die Erstellung des Fensters fortzusetzen. Wenn die Anwendung **FALSE** zurückgibt, gibt die [**CreateWindow-**](/windows/win32/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ein **NULL-Handle** zurück.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**WM \_ CREATE**](wm-create.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
