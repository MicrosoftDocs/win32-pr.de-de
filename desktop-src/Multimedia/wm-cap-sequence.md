---
title: WM_CAP_SEQUENCE Meldung (VFW. h)
description: Die WM \_ \_ -Cap-Sequenz Nachricht initiiert Streaming-Video und Audioerfassung in eine Datei. Sie können diese Nachricht explizit oder mithilfe des capcapturesequence-Makros senden.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- WM_CAP_SEQUENCE-Nachricht (Multimedia)
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
ms.openlocfilehash: e2ef945510d0d71f1aa0e0cb5827288a613f5991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956611"
---
# <a name="wm_cap_sequence-message"></a>WM- \_ Abdeckungs \_ Sequenz Nachricht

Die **WM- \_ Cap- \_ Sequenz** Nachricht initiiert Streaming-Video und Audioerfassung in eine Datei. Sie können diese Nachricht explizit oder mithilfe des [**capcapturesequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) -Makros senden.


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.

## <a name="remarks"></a>Bemerkungen

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

 

 





