---
description: Wird an eine Anwendung gesendet, wenn die IME die Komposition beendet. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: WM_IME_ENDCOMPOSITION Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9e19bcf1834d4f9e721efb2a2be53ca20268c7be42109975a7dea52e75d214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560400"
---
# <a name="wm_ime_endcomposition-message"></a>WM \_ IME \_ ENDCOMPOSITION-Nachricht

Wird an eine Anwendung gesendet, wenn die IME die Komposition beendet. Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
  WPARAM wParam,      
  LPARAM lParam             
);
```



## <a name="parameters"></a>Parameter

Diese Nachricht enthält keine Parameter.

<dl></dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Hinweise

Eine Anwendung sollte diese Meldung verarbeiten, wenn sie Kompositionszeichen selbst anzeigt.

Wenn die Anwendung ein IME-Fenster erstellt hat, sollte sie diese Meldung an dieses Fenster übergeben. Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  verarbeitet diese Nachricht, indem sie sie an das STANDARD-IME-Fenster übergibt.

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

 

 
