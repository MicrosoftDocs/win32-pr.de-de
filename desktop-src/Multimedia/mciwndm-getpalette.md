---
title: MCIWNDM_GETPALETTE Nachricht (Vfw.h)
description: Die MCIWNDM \_ GETPALETTE-Nachricht ruft ein Handle der Palette ab, die von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mithilfe des MCIWndGetPalette-Makros senden.
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- MCIWNDM_GETPALETTE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319fe1fedc21c064896c3316d0a45132c034b73c25bf107ee667269a13ed678b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137701"
---
# <a name="mciwndm_getpalette-message"></a>MCIWNDM \_ GETPALETTE-Nachricht

Die **MCIWNDM \_ GETPALETTE-Nachricht** ruft ein Handle der Palette ab, die von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetPalette-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) senden.


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg das Handle der Palette zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 





