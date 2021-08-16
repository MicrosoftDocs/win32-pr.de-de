---
title: WM_CAP_DLG_VIDEOFORMAT Meldung (Vfw.h)
description: Die MELDUNG WM \_ CAP \_ DLG \_ VIDEOFORMAT zeigt ein Dialogfeld an, in dem der Benutzer das Videoformat auswählen kann.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- WM_CAP_DLG_VIDEOFORMAT nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaa58e99c6a07db9109a0b1a6dae25de8abd46fef2631eb539961de16455ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135399"
---
# <a name="wm_cap_dlg_videoformat-message"></a>WM \_ CAP \_ DLG \_ VIDEOFORMAT-Nachricht

Die **MELDUNG WM CAP \_ \_ DLG \_ VIDEOFORMAT** zeigt ein Dialogfeld an, in dem der Benutzer das Videoformat auswählen kann. Das Dialogfeld Videoformat kann verwendet werden, um Bilddimensionen, Bittiefe und Hardwarekomprimierungsoptionen auszuwählen. Sie können diese Nachricht explizit oder mithilfe des [**Makros capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) senden.


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Nachdem diese Meldung zurückgegeben wurde, müssen Anwendungen möglicherweise die [**CAPSTATUS-Struktur**](/windows/win32/api/vfw/ns-vfw-capstatus) aktualisieren, da der Benutzer möglicherweise die Bilddimensionen geändert hat.

Das Dialogfeld Videoformat ist für jeden Aufzeichnungstreiber eindeutig. Einige Erfassungstreiber unterstützen möglicherweise kein Dialogfeld Videoformat. Anwendungen können ermitteln, ob der Erfassungstreiber diese Meldung unterstützt, indem sie den **Member fHasDlgVideoFormat** von [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)überprüfen.

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

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

 





