---
description: Wird an eine Anwendung gesendet, wenn das IME-Fenster keinen Platz zum Erweitern des Bereichs für das Kompositionsfenster findet. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: WM_IME_COMPOSITIONFULL Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33051ac3e4e893eb803d4b13d7bfbf53751258b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218683"
---
# <a name="wm_ime_compositionfull-message"></a>"WM \_ IME \_ compositionfull"-Meldung

Wird an eine Anwendung gesendet, wenn das IME-Fenster keinen Platz zum Erweitern des Bereichs für das Kompositionsfenster findet. Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a>Parameter

Diese Nachricht weist keine Parameter auf.

<dl></dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Die Anwendung sollte mithilfe des Befehls [IMC \_ setcompositionwindow](imc-setcompositionwindow.md) angeben, wie das Fenster angezeigt werden soll.

Das IME-Fenster sendet diese Benachrichtigungs Meldung nicht in den IME, sondern von der [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion.

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
</dt> <dt>

[IMC \_ setcompositionwindow](imc-setcompositionwindow.md)
</dt> </dl>

 

 
