---
title: MCIWNDM_GETSPEED-Nachricht (Vfw.h)
description: Die MCIWNDM \_ GETSPEED-Nachricht ruft die Wiedergabegeschwindigkeit eines MCI-Geräts ab. Sie können diese Nachricht explizit oder mithilfe des MCIWndGetSpeed-Makros senden.
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- MCIWNDM_GETSPEED nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42749fb2f99c446dbd45bc6e2497287ab3b0ce987c9343ed4580735c760cc892
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429250"
---
# <a name="mciwndm_getspeed-message"></a>MCIWNDM \_ GETSPEED-Nachricht

Die **MCIWNDM \_ GETSPEED-Nachricht** ruft die Wiedergabegeschwindigkeit eines MCI-Geräts ab. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetSpeed-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) senden.


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg die Wiedergabegeschwindigkeit zurück. Der Wert für die Normalgeschwindigkeit ist 1000. Größere Werte weisen auf höhere Geschwindigkeiten hin, kleinere Werte auf langsamere Geschwindigkeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 





