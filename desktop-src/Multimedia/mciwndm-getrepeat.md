---
title: MCIWNDM_GETREPEAT Meldung (VFW. h)
description: Die mciwndm \_ getretorf-Nachricht bestimmt, ob die fortlaufende Wiedergabe aktiviert wurde. Sie können diese Nachricht explizit oder mithilfe des mciwndgetrepeat-Makros senden.
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- MCIWNDM_GETREPEAT-Nachricht (Multimedia)
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
ms.openlocfilehash: ef47dc4f639c7aa34f7a00341e6ad2e19be909d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103050"
---
# <a name="mciwndm_getrepeat-message"></a>Mciwndm \_ getretorf-Nachricht

Die **mciwndm \_ getretorf** -Nachricht bestimmt, ob die fortlaufende Wiedergabe aktiviert wurde. Sie können diese Nachricht explizit oder mithilfe des [**mciwndgetrepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) -Makros senden.


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die fortlaufende Wiedergabe aktiviert ist, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetrepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





