---
description: Wird unmittelbar vor dem Generieren der Kompositions Zeichenfolge als Ergebnis eines Tastatur Schlags gesendet. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: WM_IME_STARTCOMPOSITION Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bd9a93b4c6c2e8dba6658c84b5f431dd9a54e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862647"
---
# <a name="wm_ime_startcomposition-message"></a>WM \_ IME \_ StartComposition-Nachricht

Wird unmittelbar vor dem Generieren der Kompositions Zeichenfolge als Ergebnis eines Tastatur Schlags gesendet. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
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

Diese Meldung ist eine Benachrichtigung an ein IME-Fenster, um das Kompositionsfenster zu öffnen. Eine Anwendung sollte diese Nachricht verarbeiten, wenn Sie selbst Kompositions Zeichen anzeigt.

Wenn eine Anwendung ein IME-Fenster erstellt hat, sollte diese Meldung an dieses Fenster übergeben werden. Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion verarbeitet die Nachricht, indem Sie Sie an das IME-Standardfenster übergibt.

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

 

 
