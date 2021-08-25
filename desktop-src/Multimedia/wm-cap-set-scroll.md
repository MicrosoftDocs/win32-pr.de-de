---
title: WM_CAP_SET_SCROLL-Nachricht (Vfw.h)
description: Die WM \_ CAP \_ SET \_ SCROLL-Meldung definiert den Teil des Videoframes, der im Erfassungsfenster angezeigt werden soll.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- WM_CAP_SET_SCROLL nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 352d65c2ad8e80622f7ff50cca0a8f7d6e523d53ae002a2325327a634b97c931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134984"
---
# <a name="wm_cap_set_scroll-message"></a>WM \_ CAP \_ SET \_ SCROLL-Meldung

Die **WM CAP SET \_ \_ \_ SCROLL-Meldung** definiert den Teil des Videoframes, der im Erfassungsfenster angezeigt werden soll. Diese Meldung legt die obere linke Ecke des Clientbereichs des Erfassungsfensters auf die Koordinaten eines angegebenen Pixels innerhalb des Videoframes fest. Sie können diese Nachricht explizit oder mithilfe des [**Makros capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) senden.


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*Bvg*
</dt> <dd>

Adresse, die die gewünschte Bildlaufposition enthalten soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Die Bildlaufposition wirkt sich sowohl im Vorschau- als auch im Überlagerungsmodus auf das Bild aus.

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

 

 





