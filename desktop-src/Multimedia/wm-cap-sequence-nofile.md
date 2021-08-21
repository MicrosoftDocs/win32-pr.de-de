---
title: WM_CAP_SEQUENCE_NOFILE (Vfw.h)
description: Die WM \_ CAP \_ SEQUENCE \_ NOFILE-Nachricht initiiert die Streamingvideoerfassung, ohne Daten in eine Datei zu schreiben. Sie können diese Nachricht explizit oder mithilfe des Makros capCaptureSequenceNoFile senden.
ms.assetid: 60cbcb62-3bfa-4182-a049-1e3cb2ede423
keywords:
- WM_CAP_SEQUENCE_NOFILE von Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE_NOFILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d9344b53a52caa2e536483a339439a6d942ff1fea0313767d0e1be520c09b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940728"
---
# <a name="wm_cap_sequence_nofile-message"></a>WM \_ CAP \_ SEQUENCE \_ NOFILE-Meldung

Die **WM CAP SEQUENCE \_ \_ \_ NOFILE-Nachricht** initiiert die Streamingvideoerfassung, ohne Daten in eine Datei zu schreiben. Sie können diese Nachricht explizit oder mithilfe des [**Makros capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) senden.


```C++
WM_CAP_SEQUENCE_NOFILE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Diese Nachricht ist in Verbindung mit Rückruffunktionen für Videostreams oder Waveform-Audiostreams nützlich, mit denen Ihre Anwendung die Video- und Audiodaten direkt verwenden kann.

Wenn Sie die Parameter ändern möchten, die die Streamingerfassung steuern, verwenden Sie die [**MELDUNG WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP,**](wm-cap-set-sequence-setup.md) bevor Sie die Erfassung starten.

Standardmäßig lässt das Erfassungsfenster nicht zu, dass andere Anwendungen während der Erfassung weiter ausgeführt werden. Um dies zu überschreiben, legen Sie entweder den **fYield-Member** der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) auf **TRUE** fest, oder installieren Sie eine Yield-Rückruffunktion.

Während der Streamingerfassung kann das Erfassungsfenster optional Benachrichtigungen zu bestimmten Bedingungen an Ihre Anwendung senden. Verwenden Sie die folgenden Meldungen, um Rückrufverfahren für diese Benachrichtigungen zu installieren:

-   [**WM \_ CAP SET CALLBACK ERROR (WM-CAP \_ \_ SET-RÜCKRUFFEHLER) \_**](wm-cap-set-callback-error.md)
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

[Videoaufnahmenachrichten](video-capture-messages.md)
</dt> </dl>

 

 





