---
description: Wird vom IME an eine Anwendung gesendet, um die Anwendung über eine Schlüsselfreigabe zu benachrichtigen und die Nachrichten reihenfolge zu behalten. Ein Fenster empfängt diese Nachricht über seine WindowProc-Funktion.
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: WM_IME_KEYUP (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65d80876643cc27136223c112c1e045bc797adbd0bf160adda1c3cea894767e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102070"
---
# <a name="wm_ime_keyup-message"></a>WM \_ IME \_ KEYUP-Meldung

Wird vom IME an eine Anwendung gesendet, um die Anwendung über eine Schlüsselfreigabe zu benachrichtigen und die Nachrichten reihenfolge zu behalten. Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_KEYUP,    
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Ein Handle für ein Fenster.

</dd> <dt>

*wParam* 
</dt> <dd>

Virtueller Schlüsselcode des Schlüssels.

</dd> <dt>

*lParam* 
</dt> <dd>

Wiederholungsanzahl, Scancode, erweitertes Schlüsselflag, Kontextcode, vorheriges Schlüsselzustandsflag und Übergangszustandsflag, wie unten dargestellt.



| bit   | Bedeutung                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | Wiederholungsanzahl. Dieser Wert ist immer 1.                                       |
| 16-23 | Scancode.                                                                  |
| 24    | Erweiterter Schlüssel. Dieser Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0. |
| 25-28 | Wird nicht verwendet.                                                                   |
| 29    | Kontextcode. Dieser Wert ist immer 0.                                       |
| 30    | Vorheriger Schlüsselzustand. Dieser Wert ist immer 1.                                 |
| 31    | Übergangsstatus. Dieser Wert ist immer 1.                                   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Eine Anwendung kann diese Nachricht verarbeiten oder an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  übergeben, um eine entsprechende [**WM \_ KEYUP-Nachricht zu**](../inputdev/wm-keyup.md) generieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethode-Manager](input-method-manager.md)
</dt> <dt>

[Meldungen des Eingabemethode-Managers](input-method-manager-messages.md)
</dt> </dl>

 

 
