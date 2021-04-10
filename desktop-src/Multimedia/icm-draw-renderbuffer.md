---
title: ICM_DRAW_RENDERBUFFER Meldung (VFW. h)
description: Mit der ICM \_ Draw- \_ renderbuffer-Meldung wird ein renderingertreiber benachrichtigt, um die Frames zu zeichnen, die an ihn übermittelt wurden. Sie können diese Nachricht explizit oder mithilfe des icdrawrenderbuffer-Makros senden.
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- ICM_DRAW_RENDERBUFFER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956935"
---
# <a name="icm_draw_renderbuffer-message"></a>ICM \_ Draw- \_ renderbuffer-Meldung

Mit der **ICM Draw-renderbuffer-Meldung wird ein \_ \_ renderingertreiber** benachrichtigt, um die Frames zu zeichnen, die an ihn übermittelt wurden. Sie können diese Nachricht explizit oder mithilfe des [**icdrawrenderbuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) -Makros senden.


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Meldung mit Hardware, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.

Diese Meldung wird in der Regel verwendet, um einen Suchvorgang auszuführen, wenn der Treiber speziell angewiesen werden muss, jeden Video Frame, der an ihn übergeben wird, anzuzeigen, anstatt eine Sequenz von Video Frames zu spielen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Video Komprimierungs Meldungen](video-compression-messages.md)
</dt> </dl>

 

 





