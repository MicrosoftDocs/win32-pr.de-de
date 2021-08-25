---
title: WM_CAP_DLG_VIDEODISPLAY (Vfw.h)
description: In der MELDUNG WM CAP DLG VIDEODISPLAY wird ein Dialogfeld angezeigt, in dem der Benutzer \_ \_ die \_ Videoausgabe festlegen oder anpassen kann.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- WM_CAP_DLG_VIDEODISPLAY-Nachricht Windows Multimedia
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
ms.openlocfilehash: 16afffbf1d3450670b99d26303627771aa4bd3399a252cd16a68bc690012f541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803870"
---
# <a name="wm_cap_dlg_videodisplay-message"></a>WM \_ CAP \_ DLG \_ VIDEODISPLAY-Meldung

In **der MELDUNG WM CAP \_ \_ DLG \_ VIDEODISPLAY** wird ein Dialogfeld angezeigt, in dem der Benutzer die Videoausgabe festlegen oder anpassen kann. Dieses Dialogfeld kann Steuerelemente enthalten, die sich auf den Farbton, den Kontrast und die Helligkeit des angezeigten Bilds sowie die Ausrichtung der Schlüsselfarbe auswirken. Sie können diese Nachricht explizit oder mithilfe des [**Makros capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) senden.


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Die Steuerelemente in diesem Dialogfeld wirken sich nicht auf digitalisierte Videodaten aus. Sie wirken sich nur auf die Ausgabe oder erneute Anzeige des Videosignals aus.

Das Dialogfeld Videoanzeige ist für jeden Erfassungstreiber eindeutig. Einige Erfassungstreiber unterstützen möglicherweise kein Dialogfeld "Videoanzeige". Anwendungen können ermitteln, ob der Erfassungstreiber diese Meldung unterstützt, indem sie das **fHasDlgVideoDisplay-Member** der [**CAPDRIVERCAPS-Struktur**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) überprüfen.

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

 

 





