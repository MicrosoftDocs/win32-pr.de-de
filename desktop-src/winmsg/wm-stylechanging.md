---
description: Wird an ein Fenster gesendet, wenn die SetWindowLong-Funktion im Begriff ist, mindestens einen Stil des Fensters zu ändern.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: WM_STYLECHANGING Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e587797404bb361a443a60750d4de5ea6a8924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865235"
---
# <a name="wm_stylechanging-message"></a>WM- \_ stylechanging-Meldung

Wird an ein Fenster gesendet, wenn die [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) -Funktion im Begriff ist, mindestens einen Stil des Fensters zu ändern.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob die Stile des Fensters oder erweiterte Fenster Stile geändert werden. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                            | Bedeutung                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_ ExStyle**</dt> <dt>-20</dt> </dl> | Die erweiterten Fenster Stile werden geändert.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_ Style**</dt> <dt>-16</dt> </dl>       | Die Fenster Stile werden geändert.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**stylestruct**](/windows/win32/api/winuser/ns-winuser-stylestruct) -Struktur, die die vorgeschlagenen neuen Stile für das Fenster enthält. Eine Anwendung kann die Stile untersuchen und ggf. ändern.

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

[**Stylestruct**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**WM- \_ StyleChanged**](wm-stylechanged.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
