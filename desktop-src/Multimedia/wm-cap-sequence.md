---
title: WM_CAP_SEQUENCE-Nachricht (Vfw.h)
description: Die WM \_ CAP \_ SEQUENCE-Nachricht initiiert das Streamen von Video- und Audioaufnahmen in eine Datei. Sie können diese Nachricht explizit oder mithilfe des CapCaptureSequence-Makros senden.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- WM_CAP_SEQUENCE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023fd22d79fdfcd1df1f44b2862814ed809fd93c43ab9cd7122414ee1e27db39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800265"
---
# <a name="wm_cap_sequence-message"></a>WM \_ CAP \_ SEQUENCE-Meldung

Die **WM \_ CAP \_ SEQUENCE-Nachricht** initiiert das Streamen von Video- und Audioaufnahmen in eine Datei. Sie können diese Nachricht explizit oder mithilfe des [**CapCaptureSequence-Makros**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) senden.


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

Wenn ein Fehler auftritt und eine Fehlerrückruffunktion mithilfe der [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR-Meldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehlerrückruffunktion aufgerufen.

## <a name="remarks"></a>Hinweise

Wenn Sie die Parameter ändern möchten, die die Streamingerfassung steuern, verwenden Sie die [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP-Meldung,**](wm-cap-set-sequence-setup.md) bevor Sie die Erfassung starten.

Standardmäßig lässt das Erfassungsfenster nicht zu, dass andere Anwendungen während der Erfassung weiter ausgeführt werden. Um dies zu überschreiben, legen Sie entweder den **fYield-Member** der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) auf **TRUE** fest, oder installieren Sie eine Yield-Rückruffunktion.

Während der Streamingerfassung kann das Erfassungsfenster optional Benachrichtigungen über bestimmte Arten von Bedingungen an Ihre Anwendung senden. Verwenden Sie die folgenden Meldungen, um Rückrufverfahren für diese Benachrichtigungen zu installieren:

-   [**WM \_ CAP \_ SET \_ CALLBACK \_ ERROR**](wm-cap-set-callback-error.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ STATUS**](wm-cap-set-callback-status.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ YIELD**](wm-cap-set-callback-yield.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

 





