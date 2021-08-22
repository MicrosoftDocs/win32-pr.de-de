---
description: Wird an ein Fenster gesendet, nachdem die SetWindowLong-Funktion einen oder mehrere Stile des Fensters geändert hat.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: WM_STYLECHANGED Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc84d3df087cb8667367830998675903a83f633eba4797e64125269d0c937c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705940"
---
# <a name="wm_stylechanged-message"></a>WM \_ STYLECHANGED-Nachricht

Wird an ein Fenster gesendet, nachdem die [**SetWindowLong-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) einen oder mehrere Stile des Fensters geändert hat.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob sich die Stile des Fensters oder der erweiterten Fensterstile geändert haben. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                                                            | Bedeutung                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_ EXSTYLE**</dt> <dt>-20</dt> </dl> | Die erweiterten Fensterstile wurden geändert.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_ STYLE**</dt> <dt>-16</dt> </dl>       | Die Fensterstile wurden geändert.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**STYLESTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-stylestruct) die die neuen Stile für das Fenster enthält. Eine Anwendung kann die Stile untersuchen, aber nicht ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

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

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**WM \_ STYLECHANGING**](wm-stylechanging.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
