---
title: WM_CAP_SET_PREVIEWRATE Meldung (Vfw.h)
description: Die MELDUNG WM \_ CAP \_ SET \_ PREVIEWRATE legt die Bildanzeigerate im Vorschaumodus fest. Sie können diese Nachricht explizit oder mithilfe des CapPreviewRate-Makros senden.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- WM_CAP_SET_PREVIEWRATE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9b9a24614a40c5efb545b91a80069bf915c77c4b7d8fb289ed581f750ac0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135082"
---
# <a name="wm_cap_set_previewrate-message"></a>WM \_ CAP \_ SET \_ PREVIEWRATE-Meldung

Die **MELDUNG WM CAP SET \_ \_ \_ PREVIEWRATE** legt die Bildanzeigerate im Vorschaumodus fest. Sie können diese Nachricht explizit oder mithilfe des [**CapPreviewRate-Makros**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) senden.


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*Wms*
</dt> <dd>

Rate in Millisekunden, mit der neue Frames erfasst und angezeigt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, oder **FALSE,** wenn das Erfassungsfenster nicht mit einem Erfassungstreiber verbunden ist.

## <a name="remarks"></a>Hinweise

Im Vorschaumodus werden erhebliche CPU-Ressourcen verwendet. Anwendungen können die Vorschau deaktivieren oder die Vorschaurate verringern, wenn eine andere Anwendung den Fokus hat. Während der Videoaufzeichnung im Streaming hat die Vorschauaufgabe eine niedrigere Priorität als das Schreiben von Frames auf den Datenträger, und Vorschauframes werden nur angezeigt, wenn keine anderen Puffer zum Schreiben verfügbar sind.

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

 

 





