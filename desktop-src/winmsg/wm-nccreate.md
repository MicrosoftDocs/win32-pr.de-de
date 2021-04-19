---
description: Wird vor der WM Create-Meldung gesendet, \_ Wenn ein Fenster erstmalig erstellt wird.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: WM_NCCREATE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8757cbdeba49d54f6e5d842a5b40c7f7ae61cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362240"
---
# <a name="wm_nccreate-message"></a>WM- \_ nccreate-Meldung

Wird vor der [**WM \_ Create**](wm-create.md) -Meldung gesendet, wenn ein Fenster erstmalig erstellt wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

Ein Zeiger auf die [**foratestruct**](/windows/win32/api/winuser/ns-winuser-createstructa) -Struktur, die Informationen über das Fenster enthält, das erstellt wird. Die Member von " **kreatestruct** " sind identisch mit den Parametern der Funktion " [**foratewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true** " zurückgeben, um die Erstellung des Fensters fortzusetzen. Wenn die Anwendung **false** zurückgibt, gibt die Funktion " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " ein **null** -Handle zurück.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**WM \_ Erstellen**](wm-create.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
