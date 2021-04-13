---
description: Wird an eine Anwendung gesendet, wenn das IME die Komposition beendet. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: WM_IME_ENDCOMPOSITION Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ca9d1560810b22ae0d36010d2371e75b83a81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343629"
---
# <a name="wm_ime_endcomposition-message"></a>WM- \_ IME- \_ endkompositions Nachricht

Wird an eine Anwendung gesendet, wenn das IME die Komposition beendet. Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
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

Eine Anwendung sollte diese Nachricht verarbeiten, wenn Sie selbst Kompositions Zeichen anzeigt.

Wenn die Anwendung ein IME-Fenster erstellt hat, sollte diese Meldung an dieses Fenster übergeben werden. Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  -Funktion verarbeitet diese Nachricht, indem Sie Sie an das IME-Standardfenster übergibt.

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

 

 
