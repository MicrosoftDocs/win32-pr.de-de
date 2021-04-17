---
title: WM_CAP_DLG_VIDEOSOURCE Meldung (VFW. h)
description: Die Meldung "WM \_ Cap \_ DLG \_ videosource" zeigt ein Dialogfeld an, in dem der Benutzer die Videoquelle steuern kann.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- WM_CAP_DLG_VIDEOSOURCE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e8ae7e3d619964a547fbe0db4517fd1e7d277f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476221"
---
# <a name="wm_cap_dlg_videosource-message"></a>WM- \_ Cap- \_ DLG- \_ videosource-Nachricht

Die Meldung " **WM \_ Cap \_ DLG \_ videosource** " zeigt ein Dialogfeld an, in dem der Benutzer die Videoquelle steuern kann. Das Dialogfeld Video Quelle enthält möglicherweise Steuerelemente, die Eingabe Quellen auswählen. Ändern Sie den Farbton, den Kontrast und die Helligkeit des Bilds. und ändern Sie die Videoqualität, bevor Sie die Bilder im Frame Puffer digitalisieren. Sie können diese Nachricht explizit oder mithilfe des [**capdlgvideosource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) -Makros senden.


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Das Dialogfeld Video Quelle ist für jeden Aufzeichnungs Treiber eindeutig. Einige Aufzeichnungs Treiber unterstützen möglicherweise kein Dialogfeld "Video Quelle". Anwendungen können bestimmen, ob der Erfassungs Treiber diese Nachricht unterstützt, indem Sie den **fhasdlgvideosource** -Member der [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) -Struktur überprüfen.

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

 

 





