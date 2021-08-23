---
description: Wird an eine Anwendung gesendet, wenn das IME-Fenster keinen Platz findet, um den Bereich für das Kompositionsfenster zu erweitern. Ein Fenster empfängt diese Nachricht über seine WindowProc-Funktion.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: WM_IME_COMPOSITIONFULL (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954a5f91283ca5c4944c274d422508ef0b91b55b8acc34f790cf446f93a598ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811490"
---
# <a name="wm_ime_compositionfull-message"></a>WM \_ IME \_ COMPOSITIONFULL-Nachricht

Wird an eine Anwendung gesendet, wenn das IME-Fenster keinen Platz findet, um den Bereich für das Kompositionsfenster zu erweitern. Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a>Parameter

Diese Meldung enthält keine Parameter.

<dl></dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung hat keinen Rückgabewert.

## <a name="remarks"></a>Hinweise

Die Anwendung sollte den [Befehl IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) verwenden, um anzugeben, wie das Fenster angezeigt werden soll.

Das IME-Fenster sendet anstelle des IME diese Benachrichtigungsnachricht von der [**SendMessage-Funktion.**](/windows/win32/api/winuser/nf-winuser-sendmessage)

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
</dt> <dt>

[IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md)
</dt> </dl>

 

 
