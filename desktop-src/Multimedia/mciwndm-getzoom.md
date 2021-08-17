---
title: MCIWNDM_GETZOOM Meldung (Vfw.h)
description: Die MCIWNDM \_ GETZOOM-Nachricht ruft den aktuellen Zoomwert ab, der von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mithilfe des MCIWndGetZoom-Makros senden.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- MCIWNDM_GETZOOM nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c247230ffe6269f77b906d874a4cf82a21ed8d3388ffa18193417603e45fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374141"
---
# <a name="mciwndm_getzoom-message"></a>MCIWNDM \_ GETZOOM-Nachricht

Die **MCIWNDM \_ GETZOOM-Nachricht** ruft den aktuellen Zoomwert ab, der von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetZoom-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) senden.


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt die neuesten Werte zurück, die mit [**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md)verwendet werden.

## <a name="remarks"></a>Hinweise

Der Rückgabewert 100 gibt an, dass das Bild nicht vergrößert wird. Der Wert 200 gibt an, dass das Bild auf das Doppelte seiner ursprünglichen Größe vergrößert wird. Der Wert 50 gibt an, dass das Bild auf die Hälfte seiner ursprünglichen Größe reduziert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md)
</dt> </dl>

 

 





