---
title: WM_CAP_SET_SCROLL Meldung (VFW. h)
description: Die "WM Cap"- \_ \_ \_ scrollnachricht definiert den Teil des Video Frames, der im Erfassungsfenster angezeigt werden soll.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- WM_CAP_SET_SCROLL-Nachricht (Multimedia)
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
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479053"
---
# <a name="wm_cap_set_scroll-message"></a>Bild \_ Lauf \_ \_ Meldung zur WM-Abdeckung

Die " **WM Cap"- \_ \_ \_ scrollnachricht** definiert den Teil des Video Frames, der im Erfassungsfenster angezeigt werden soll. Mit dieser Meldung wird die linke obere Ecke des Client Bereichs des Aufzeichnungs Fensters auf die Koordinaten eines angegebenen Pixels im Videorahmen festgelegt. Sie können diese Nachricht explizit oder mithilfe des [**capsetscrollpos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) -Makros senden.


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*LPP*
</dt> <dd>

Adresse, die die gewünschte Scrollposition enthalten soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die Bild Lauf Position wirkt sich auf das Bild im Vorschau-und Überlagerungs Modus aus.

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

 

 





