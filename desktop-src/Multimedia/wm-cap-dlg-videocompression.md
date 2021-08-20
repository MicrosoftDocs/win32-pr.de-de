---
title: WM_CAP_DLG_VIDEOCOMPRESSION Nachricht (Vfw.h)
description: Die \_ WM CAP \_ DLG \_ VIDEOCOMPRESSION-Meldung zeigt ein Dialogfeld an, in dem der Benutzer eine Während des Erfassungsprozesses zu verwendende Komprimierung auswählen kann.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- WM_CAP_DLG_VIDEOCOMPRESSION nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816aeb26455ba375b4446edc275ec4fbaa318b67b1fea64bd6049760f45d8235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135443"
---
# <a name="wm_cap_dlg_videocompression-message"></a>WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION-Meldung

Die **WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION-Meldung** zeigt ein Dialogfeld an, in dem der Benutzer eine Während des Erfassungsprozesses zu verwendende Komprimierung auswählen kann. Die Liste der verfügbaren Zuschauer kann je nach dem Videoformat variieren, das im Dialogfeld Videoformat des Aufzeichnungstreibers ausgewählt ist. Sie können diese Nachricht explizit oder mithilfe des [**Makros capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) senden.


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Meldung mit Erfassungstreibern, die Frames nur im BI \_ RGB-Format bereitstellen. Diese Meldung ist besonders nützlich beim Schritterfassungsvorgang, um Erfassung und Komprimierung in einem einzigen Vorgang zu kombinieren. Das Komprimieren von Frames mit einer Softwareeinbindung im Rahmen eines Echtzeiterfassungsvorgangs ist wahrscheinlich zu zeitaufwändig für die Ausführung.

Die Komprimierung wirkt sich nicht auf die Frames aus, die in die Zwischenablage kopiert werden.

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

 

 





