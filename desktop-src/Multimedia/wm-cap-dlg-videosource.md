---
title: WM_CAP_DLG_VIDEOSOURCE (Vfw.h)
description: In der MELDUNG WM \_ CAP DLG VIDEOSOURCE wird ein Dialogfeld angezeigt, in dem der Benutzer \_ \_ die Videoquelle steuern kann.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- WM_CAP_DLG_VIDEOSOURCE-Nachricht Windows Multimedia
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
ms.openlocfilehash: 7a1f05d7e3dc421759229adffa4ecc4b78affc26f1b4244887b017614c2ab4d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803880"
---
# <a name="wm_cap_dlg_videosource-message"></a>WM \_ CAP \_ DLG \_ VIDEOSOURCE-Meldung

In **der MELDUNG WM CAP \_ \_ DLG \_ VIDEOSOURCE** wird ein Dialogfeld angezeigt, in dem der Benutzer die Videoquelle steuern kann. Das Dialogfeld Videoquelle enthält möglicherweise Steuerelemente, die Eingabequellen auswählen. Ändern von Farbton, Kontrast und Helligkeit des Bilds; und ändern die Videoqualität, bevor die Bilder in den Framepuffer digitalisiert werden. Sie können diese Nachricht explizit oder mithilfe des [**Makros capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) senden.


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Das Dialogfeld Videoquelle ist für jeden Erfassungstreiber eindeutig. Einige Erfassungstreiber unterstützen möglicherweise kein Dialogfeld Videoquelle. Anwendungen können ermitteln, ob der Erfassungstreiber diese Meldung unterstützt, indem sie das **fHasDlgVideoSource-Member** der [**CAPDRIVERCAPS-Struktur**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) überprüfen.

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

 

 





