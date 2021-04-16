---
description: Wird an ein Fenster gesendet, nachdem die Funktion SetWindowLong mindestens einen Stil des Fensters geändert hat.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: WM_STYLECHANGED Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5429db06dea95dbbc003e432a2b619c5cf8d056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529834"
---
# <a name="wm_stylechanged-message"></a>Meldung "WM- \_ StyleChanged"

Wird an ein Fenster gesendet, nachdem die Funktion [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) mindestens einen Stil des Fensters geändert hat.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob die Stile des Fensters oder erweiterte Fenster Stile geändert wurden. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                            | Bedeutung                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_ ExStyle**</dt> <dt>-20</dt> </dl> | Die erweiterten Fenster Stile wurden geändert.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_ Style**</dt> <dt>-16</dt> </dl>       | Die Fenster Stile wurden geändert.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**stylestruct**](/windows/win32/api/winuser/ns-winuser-stylestruct) -Struktur, die die neuen Stile für das Fenster enthält. Eine Anwendung kann die Stile untersuchen, aber nicht ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

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

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[**Stylestruct**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**WM- \_ stylechanging**](wm-stylechanging.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
