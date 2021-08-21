---
title: MCIWNDM_GETREPEAT (Vfw.h)
description: Die MCIWNDM \_ GETREPEAT-Nachricht bestimmt, ob die fortlaufende Wiedergabe aktiviert wurde. Sie können diese Nachricht explizit oder mithilfe des Makros MCIWndGetRepeat senden.
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- MCIWNDM_GETREPEAT-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5045f56f2d189884e6d2dee978ec8800fa9c24c3ff01fc3fe93680b4ae7f53af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374197"
---
# <a name="mciwndm_getrepeat-message"></a>MCIWNDM \_ GETREPEAT-Nachricht

Die **MCIWNDM \_ GETREPEAT-Nachricht** bestimmt, ob die fortlaufende Wiedergabe aktiviert wurde. Sie können diese Nachricht explizit oder mithilfe des [**Makros MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) senden.


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die fortlaufende Wiedergabe aktiviert ist, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





