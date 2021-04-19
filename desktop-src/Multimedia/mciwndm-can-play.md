---
title: MCIWNDM_CAN_PLAY Meldung (VFW. h)
description: Die mciwndm \_ kann \_ Nachricht wiedergeben bestimmt, ob ein MCI-Gerät eine Datendatei oder einen Inhalt einer anderen Art wiedergeben kann. Sie können diese Nachricht explizit oder mithilfe des mciwndcanplay-Makros senden.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- MCIWNDM_CAN_PLAY-Nachricht (Multimedia)
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
ms.openlocfilehash: 043a0fc15260f7448df8d009a6b468616244269d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346763"
---
# <a name="mciwndm_can_play-message"></a>Mciwndm \_ kann \_ Nachricht wiedergeben

Die **mciwndm \_ kann \_** Nachricht wiedergeben bestimmt, ob ein MCI-Gerät eine Datendatei oder einen Inhalt einer anderen Art wiedergeben kann. Sie können diese Nachricht explizit oder mithilfe des [**mciwndcanplay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) -Makros senden.


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn das Gerät die Wiedergabe der Daten unterstützt, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndcanplay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





