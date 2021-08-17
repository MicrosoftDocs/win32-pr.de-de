---
title: WM_CAP_ABORT (Vfw.h)
description: Die WM \_ CAP \_ ABORT-Meldung beendet den Erfassungsvorgang.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- WM_CAP_ABORT von Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904edb47c371ee13ed3492fd9257e3933bf2f001010d7dd2b0177a7729500813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800656"
---
# <a name="wm_cap_abort-message"></a>WM \_ CAP \_ ABORT-Meldung

Die **WM \_ CAP \_ ABORT-Meldung** beendet den Erfassungsvorgang. Im Fall der Schritterfassung werden die bilddaten, die bis zum Zeitpunkt der **WM \_ CAP \_ ABORT-Nachricht** gesammelt wurden, in der Erfassungsdatei beibehalten, audio wird jedoch nicht erfasst. Sie können diese Nachricht explizit oder mithilfe des [**Makros capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) senden.


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Der Erfassungsvorgang muss ergeben, damit diese Meldung verwendet werden kann.

Verwenden Sie die [**WM \_ CAP \_ STOP-Nachricht,**](wm-cap-stop.md) um die Schritterfassung an der aktuellen Position anzuhalten und dann Audio zu erfassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Videoaufnahmenachrichten](video-capture-messages.md)
</dt> </dl>

 

 





