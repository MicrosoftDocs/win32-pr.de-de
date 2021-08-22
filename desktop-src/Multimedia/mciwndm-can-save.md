---
title: MCIWNDM_CAN_SAVE-Nachricht (Vfw.h)
description: Die MCIWNDM \_ CAN \_ SAVE-Nachricht bestimmt, ob ein MCI-Gerät Daten speichern kann. Sie können diese Nachricht explizit oder mithilfe des MCIWndCanSave-Makros senden.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- MCIWNDM_CAN_SAVE Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccab622381208b8213414ed8b156a84e431afffc55acdf2323b0c0a2d31014f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429630"
---
# <a name="mciwndm_can_save-message"></a>MCIWNDM \_ KANN \_ Nachricht speichern

Die **MCIWNDM \_ CAN \_ SAVE-Nachricht** bestimmt, ob ein MCI-Gerät Daten speichern kann. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndCanSave-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) senden.


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn das Gerät das Speichern unterstützt, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





