---
title: WM_CAP_DLG_VIDEODISPLAY Meldung (VFW. h)
description: In der \_ Meldung "WM Cap \_ DLG \_ Videodisplay" wird ein Dialogfeld angezeigt, in dem der Benutzer die Videoausgabe festlegen oder anpassen kann.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- WM_CAP_DLG_VIDEODISPLAY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378d80923f9c0b7eda65fac83809e30626d53406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956436"
---
# <a name="wm_cap_dlg_videodisplay-message"></a>WM- \_ Cap- \_ DLG- \_ Videoanzeige Meldung

In der Meldung " **WM \_ Cap \_ DLG \_ Videodisplay** " wird ein Dialogfeld angezeigt, in dem der Benutzer die Videoausgabe festlegen oder anpassen kann. Dieses Dialogfeld enthält möglicherweise Steuerelemente, die den Farbton, den Kontrast und die Helligkeit des angezeigten Bilds sowie die Ausrichtung der Schlüsselfarbe beeinflussen. Sie können diese Nachricht explizit oder mithilfe des [**capdlgvideodisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) -Makros senden.


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die Steuerelemente in diesem Dialogfeld wirken sich nicht auf die digitalisierten Videodaten aus; Sie wirken sich nur auf die Ausgabe oder die erneute Anzeige des Videosignals aus.

Das Dialogfeld Video Anzeige ist für jeden Aufzeichnungs Treiber eindeutig. Einige Erfassungs Treiber unterstützen möglicherweise keine Video Anzeige (Dialogfeld). Anwendungen können bestimmen, ob der Erfassungs Treiber diese Nachricht unterstützt, indem Sie den **fhasdlgvideodisplay** -Member der [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) -Struktur überprüfen.

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

 

 





