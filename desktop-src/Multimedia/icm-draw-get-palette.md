---
title: ICM_DRAW_GET_PALETTE Meldung (VFW. h)
description: Die ICM \_ Draw \_ get- \_ palettennachricht fordert einen renderingtreiber an, eine Palette zurückzugeben.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- ICM_DRAW_GET_PALETTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040223"
---
# <a name="icm_draw_get_palette-message"></a>ICM- \_ Zeichnen- \_ \_ palettennachricht

Die **ICM \_ Draw \_ get- \_ palettennachricht** fordert einen renderingtreiber an, eine Palette zurückzugeben.


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Der Treiber sollte eines der folgenden Werte zurückgeben: ein Handle der verwendeten Palette, **null** , wenn kein Handle vorhanden ist, oder ICERR wird \_ nicht unterstützt, wenn keine Paletten unterstützt werden.

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

 

 





