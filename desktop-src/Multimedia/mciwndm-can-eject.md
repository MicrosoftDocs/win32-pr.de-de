---
title: MCIWNDM_CAN_EJECT Meldung (VFW. h)
description: Die mciwndm \_ - \_ Nachricht kann ermitteln, ob ein MCI-Gerät seine Medien auswerfen kann. Sie können diese Nachricht explizit oder mithilfe des mciwndcaneject-Makros senden.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- MCIWNDM_CAN_EJECT-Nachricht (Multimedia)
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
ms.openlocfilehash: 00ba54c9263e23fdd9830be892e4559ae3755c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743688"
---
# <a name="mciwndm_can_eject-message"></a>Mciwndm \_ kann \_ Nachricht Auswerfen

Die **mciwndm-Nachricht \_ kann \_** ermitteln, ob ein MCI-Gerät seine Medien auswerfen kann. Sie können diese Nachricht explizit oder mithilfe des [**mciwndcaneject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) -Makros senden.


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn das Gerät seine Medien auswerfen kann, andernfalls " **false** ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndcaneject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





