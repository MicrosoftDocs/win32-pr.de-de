---
title: WM_CAP_SEQUENCE_NOFILE Meldung (VFW. h)
description: Die "WM \_ Cap \_ Sequence NoFile"- \_ Meldung initiiert die Streaming-Video Erfassung, ohne Daten in eine Datei zu schreiben. Sie können diese Nachricht explizit oder mithilfe des capcapturesequencenofile-Makros senden.
ms.assetid: 60cbcb62-3bfa-4182-a049-1e3cb2ede423
keywords:
- WM_CAP_SEQUENCE_NOFILE-Nachricht (Multimedia)
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
ms.openlocfilehash: e0a08f470989b8000e9757c1cb81924b875b5303
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103027"
---
# <a name="wm_cap_sequence_nofile-message"></a>WM- \_ Abdeckungs \_ Sequenz- \_ NoFile-Nachricht

Die " **WM \_ Cap \_ Sequence \_ NoFile** "-Meldung initiiert die Streaming-Video Erfassung, ohne Daten in eine Datei zu schreiben. Sie können diese Nachricht explizit oder mithilfe des [**capcapturesequencenofile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) -Makros senden.


```C++
WM_CAP_SEQUENCE_NOFILE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Meldung ist hilfreich in Verbindung mit Videostream-oder Waveform-Audiodatenstrom-Rückruf Funktionen, mit denen Ihre Anwendung die Video-und Audiodaten direkt verwenden kann.

Wenn Sie die Parameter, die die streamingerfassung steuern, ändern möchten, verwenden Sie vor dem Start der Erfassung die [**\_ \_ Set \_ Sequence- \_ Setup**](wm-cap-set-sequence-setup.md) Nachricht.

Standardmäßig lässt das Erfassungsfenster nicht zu, dass andere Anwendungen während der Erfassung weiter ausgeführt werden. Um dies zu überschreiben, legen Sie entweder den **fyield** -Member der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) auf **true** fest, oder installieren Sie eine Yield-Rückruffunktion.

Während der streamingerfassung kann das Erfassungsfenster optional Benachrichtigungen für bestimmte Arten von Bedingungen an Ihre Anwendung ausgeben. Verwenden Sie zum Installieren von Rückruf Prozeduren für diese Benachrichtigungen die folgenden Meldungen:

-   [**Rückruf Fehler bei WM-Abdeckung \_ \_ festgelegt \_ \_**](wm-cap-set-callback-error.md)
-   [**Rückruf Status der WM- \_ Obergrenze \_ festlegen \_ \_**](wm-cap-set-callback-status.md)
-   [**\_ \_ \_ Rückruf \_ Rendite für WM-Cap-Satz**](wm-cap-set-callback-yield.md)
-   [**WM- \_ Abdeckungs \_ Satz \_ Rückruf \_ Videostream**](wm-cap-set-callback-videostream.md)
-   [**WM- \_ Cap- \_ Satz \_ Rückruf \_ WaveStream**](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> <dt>

[Video Erfassungs Meldungen](video-capture-messages.md)
</dt> </dl>

 

 





