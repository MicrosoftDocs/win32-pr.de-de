---
title: WM_CAP_SET_SCALE (Vfw.h)
description: Die WM \_ CAP \_ SET \_ SCALE-Meldung aktiviert oder deaktiviert die Skalierung der Vorschauvideobilder.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- WM_CAP_SET_SCALE von Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3293be6917917581957df0f5dae9456274f1d2cc3eeffff5ea971c3596209a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369394"
---
# <a name="wm_cap_set_scale-message"></a>WM \_ CAP \_ SET \_ SCALE-Meldung

Die **WM CAP SET \_ \_ \_ SCALE-Meldung** aktiviert oder deaktiviert die Skalierung der Vorschauvideobilder. Wenn die Skalierung aktiviert ist, wird der erfasste Videoframe auf die Dimensionen des Erfassungsfensters gestreckt. Sie können diese Nachricht explizit oder mithilfe des [**Makros capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) senden.


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Vorschauskalierungsflag. Geben **Sie TRUE** für diesen Parameter an, um Vorschauframes auf die Größe des Erfassungsfensters zu strecken, oder **FALSE,** um sie in ihrer natürlichen Größe anzuzeigen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Das Skalieren von Vorschaubildern steuert die sofortige Darstellung erfasster Frames im Erfassungsfenster. Dies hat keine Auswirkungen auf die Größe der in der Datei gespeicherten Frames.

Die Skalierung hat keine Auswirkungen, wenn überlagernd verwendet wird, um Videos im Framepuffer anzuzeigen.

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

 

 





