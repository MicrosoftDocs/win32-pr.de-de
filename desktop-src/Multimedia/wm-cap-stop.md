---
title: WM_CAP_STOP Meldung (VFW. h)
description: Die WM- \_ Obergrenze für das \_ Beenden hält den Aufzeichnungs Vorgang an. Sie können diese Nachricht explizit oder mithilfe des capcapturestoppt-Makros senden.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- WM_CAP_STOP-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ded89ea8999fa2b29f576a6d047f5147d492bc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743537"
---
# <a name="wm_cap_stop-message"></a>Meldung zum Abbrechen der WM- \_ Begrenzung \_

Die **WM- \_ Obergrenze \_** für das Beenden hält den Aufzeichnungs Vorgang an. Sie können diese Nachricht explizit oder mithilfe des [**capcapturestoppt**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) -Makros senden.

In Schritt Frame Erfassung werden die Bilddaten, die vor dem Senden dieser Nachricht erfasst wurden, in der Erfassungs Datei aufbewahrt. Eine entsprechende Dauer von Audiodaten wird auch in der Erfassungs Datei aufbewahrt, wenn die Audioerfassung aktiviert war.


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Der Aufzeichnungs Vorgang muss durchführen, um diese Meldung zu verwenden. Verwenden Sie die Abbruch Meldung "WM Cap", um den aktuellen Aufzeichnungs Vorgang [**\_ \_ abzubrechen**](wm-cap-abort.md) .

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

 

 





