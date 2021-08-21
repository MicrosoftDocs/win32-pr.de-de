---
title: MCIWNDM_CAN_PLAY (Vfw.h)
description: Die MCIWNDM CAN PLAY-Nachricht bestimmt, ob ein MCI-Gerät eine Datendatei oder einen anderen Inhalt \_ \_ wieder geben kann. Sie können diese Nachricht explizit oder mithilfe des MCIWndCanPlay-Makros senden.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- MCIWNDM_CAN_PLAY von Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84d067b01dbce8aaab7c78ab24c3d11fc5d4a3a19b9bfdb663eb653ebc0c553c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374242"
---
# <a name="mciwndm_can_play-message"></a>MCIWNDM \_ CAN \_ PLAY-Nachricht

Die **MCIWNDM \_ CAN \_ PLAY-Nachricht** bestimmt, ob ein MCI-Gerät eine Datendatei oder einen anderen Inhalt wieder geben kann. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndCanPlay-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) senden.


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn das Gerät die Wiedergabe der Daten unterstützt, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





