---
description: Wird von IME an eine Anwendung gesendet, um die Anwendung über eine schlüsselfreigabe zu benachrichtigen und die Reihenfolge der Nachrichten zu erhalten. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: WM_IME_KEYUP Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0eb6c6701510a373573ff6d85d5b50a8541b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347775"
---
# <a name="wm_ime_keyup-message"></a>WM- \_ IME- \_ KeyUp-Meldung

Wird von IME an eine Anwendung gesendet, um die Anwendung über eine schlüsselfreigabe zu benachrichtigen und die Reihenfolge der Nachrichten zu erhalten. Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

*HWND* 
</dt> <dd>

Ein Handle für Fenster.

</dd> <dt>

*wParam* 
</dt> <dd>

Der virtuelle Schlüsselcode des Schlüssels.

</dd> <dt>

*lParam* 
</dt> <dd>

Wiederholungs Anzahl, Überprüfungs Code, erweitertes schlüsselflag, Kontext Code, Vorheriges schlüsselstatusflag und Übergangs Zustands Kennzeichen, wie unten gezeigt.



| bit   | Bedeutung                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | Wiederholungs Anzahl. Dieser Wert ist immer 1.                                       |
| 16-23 | Scannen Sie den Code.                                                                  |
| 24    | Erweiterter Schlüssel. Dieser Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0. |
| 25-28 | Nicht verwendet.                                                                   |
| 29    | Kontext Code. Dieser Wert ist immer 0.                                       |
| 30    | Vorheriger Schlüssel Zustand. Dieser Wert ist immer 1.                                 |
| 31    | Übergangsstatus. Dieser Wert ist immer 1.                                   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann diese Nachricht verarbeiten oder an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  -Funktion übergeben, um eine übereinstimmende [**WM- \_ KeyUp**](../inputdev/wm-keyup.md) -Nachricht zu generieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Meldungen](input-method-manager-messages.md)
</dt> </dl>

 

 
