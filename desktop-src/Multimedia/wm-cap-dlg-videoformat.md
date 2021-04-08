---
title: WM_CAP_DLG_VIDEOFORMAT Meldung (VFW. h)
description: Die Meldung "WM \_ Cap \_ DLG \_ Videoformat" zeigt ein Dialogfeld an, in dem der Benutzer das Videoformat auswählen kann.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- WM_CAP_DLG_VIDEOFORMAT-Nachricht (Multimedia)
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
ms.openlocfilehash: 8d244c4c141845d4ede66804918514e091872e89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949753"
---
# <a name="wm_cap_dlg_videoformat-message"></a>WM \_ Cap \_ DLG- \_ Videoformat Meldung

Die Meldung " **WM \_ Cap \_ DLG \_ Videoformat** " zeigt ein Dialogfeld an, in dem der Benutzer das Videoformat auswählen kann. Das Dialogfeld Video Format kann verwendet werden, um Bild Dimensionen, Bittiefe und Hardware Komprimierungs Optionen auszuwählen. Sie können diese Nachricht explizit oder mithilfe des [**capdlgvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) -Makros senden.


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Nachdem diese Nachricht zurückgegeben wurde, müssen Anwendungen möglicherweise die [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur aktualisieren, da der Benutzer möglicherweise die Bild Dimensionen geändert hat.

Das Dialogfeld Video Format ist für jeden Aufzeichnungs Treiber eindeutig. Einige Aufzeichnungs Treiber unterstützen möglicherweise kein Video Format-Dialogfeld. Anwendungen können ermitteln, ob der Erfassungs Treiber diese Nachricht unterstützt, indem Sie den Member **fhasdlgvideoformat** von [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)überprüfen.

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

 

 





