---
title: WM_CAP_STOP (Vfw.h)
description: Die WM \_ CAP \_ STOP-Meldung beendet den Erfassungsvorgang. Sie können diese Nachricht explizit oder mithilfe des Makros capCaptureStop senden.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- WM_CAP_STOP von Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bceac7a821a42227a388de6ebc2b9ea548156ec80d1e5baba7f1e1ad708002d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369329"
---
# <a name="wm_cap_stop-message"></a>WM \_ CAP \_ STOP-Meldung

Die **WM \_ CAP \_ STOP-Meldung** beendet den Erfassungsvorgang. Sie können diese Nachricht explizit oder mithilfe des [**Makros capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) senden.

Bei der Schrittframeerfassung werden die Bilddaten, die vor dem Senden dieser Nachricht gesammelt wurden, in der Erfassungsdatei beibehalten. Eine äquivalente Dauer von Audiodaten wird auch in der Erfassungsdatei beibehalten, wenn die Audioaufnahme aktiviert wurde.


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Der Erfassungsvorgang muss ergeben, damit diese Meldung verwendet werden kann. Verwenden Sie die [**WM \_ CAP \_ ABORT-Meldung,**](wm-cap-abort.md) um den aktuellen Erfassungsvorgang zu verabbruchen.

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

 

 





