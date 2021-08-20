---
title: ICM_DRAW_GET_PALETTE-Nachricht (Vfw.h)
description: Die ICM \_ DRAW \_ GET \_ PALETTE-Nachricht fordert einen Renderingtreiber an, eine Palette zurückzugeben.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- ICM_DRAW_GET_PALETTE nachricht Windows Multimedia
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
ms.openlocfilehash: 6ef07085bef92d6191cea69429a5b544d5d2f706e1771baa404741aa98a5812b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987390"
---
# <a name="icm_draw_get_palette-message"></a>\_ICM DRAW \_ GET \_ PALETTE-Nachricht

Die **ICM DRAW GET \_ \_ \_ PALETTE-Nachricht** fordert einen Renderingtreiber an, eine Palette zurückzugeben.


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Der Treiber sollte einen der folgenden Werte zurückgeben: ein Handle der verwendeten Palette, **NULL,** wenn kein Handle zurückgegeben werden muss, oder ICERR \_ UNSUPPORTED, wenn er paletten nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

 





