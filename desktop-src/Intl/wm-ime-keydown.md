---
description: Wird vom IME an eine Anwendung gesendet, um die Anwendung über einen Tastendruck zu benachrichtigen und die Nachrichtenreihenfolge beizubehalten. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: WM_IME_KEYDOWN Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beed8bb074e1bae300d52c52867cc8d1f26b84bb8abf358ad2858df7356a0a0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535310"
---
# <a name="wm_ime_keydown-message"></a>WM \_ IME \_ KEYDOWN-Nachricht

Wird vom IME an eine Anwendung gesendet, um die Anwendung über einen Tastendruck zu benachrichtigen und die Nachrichtenreihenfolge beizubehalten. Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
  WPARAM wParam, 
  LPARAM lParam      
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Ein Handle für fenster.

</dd> <dt>

*wParam* 
</dt> <dd>

Virtueller Schlüsselcode des Schlüssels.

</dd> <dt>

*lParam* 
</dt> <dd>

Wiederholungsanzahl, Scancode, erweitertes Schlüsselflag, Kontextcode, vorheriges Schlüsselzustandsflag und Übergangszustandsflag, wie in der folgenden Tabelle dargestellt.



| bit   | Bedeutung                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | Wiederholungsanzahl.                                                               |
| 16-23 | Code überprüfen.                                                                  |
| 24    | Erweiterter Schlüssel. Dieser Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0. |
| 25-28 | Wird nicht verwendet.                                                                   |
| 29    | Kontextcode. Dieser Wert ist immer 0.                                       |
| 30    | Vorheriger Schlüsselstatus. Dieser Wert ist 1, wenn der Schlüssel ausgeschaltet ist, oder 0, wenn er hoch ist.    |
| 31    | Übergangsstatus. Dieser Wert ist immer 0.                                   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Eine Anwendung kann diese Nachricht verarbeiten oder an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  übergeben, um eine entsprechende [**WM \_ KEYDOWN-Nachricht**](../inputdev/wm-keydown.md) zu generieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Nachrichten](input-method-manager-messages.md)
</dt> </dl>

 

 
