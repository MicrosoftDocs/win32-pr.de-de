---
title: MCIWNDM_CAN_EJECT-Nachricht (Vfw.h)
description: Die MCIWNDM \_ CAN \_ EJECT-Nachricht bestimmt, ob ein MCI-Gerät seine Medien auswerfen kann. Sie können diese Nachricht explizit oder mithilfe des MCIWndCanEject-Makros senden.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- MCIWNDM_CAN_EJECT nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fde4c9fec3972fe0e22b0a562454e1ef680e9ccae3851c272d28468fc2c91f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429670"
---
# <a name="mciwndm_can_eject-message"></a>MCIWNDM \_ CAN \_ EJECT message

Die **MCIWNDM \_ CAN \_ EJECT-Nachricht** bestimmt, ob ein MCI-Gerät seine Medien auswerfen kann. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndCanEject-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) senden.


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn das Gerät sein Medium auswerfen kann, oder **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





