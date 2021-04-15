---
title: MCIWNDM_CAN_SAVE Meldung (VFW. h)
description: Die mciwndm \_ kann die \_ Nachricht speichern, um zu ermitteln, ob ein MCI-Gerät Daten speichern kann. Sie können diese Nachricht explizit oder mithilfe des mciwndcansave-Makros senden.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- MCIWNDM_CAN_SAVE-Nachricht (Multimedia)
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
ms.openlocfilehash: 11b60b8a5d93ac80befc8beeb6665399efe44f1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475681"
---
# <a name="mciwndm_can_save-message"></a>Mciwndm \_ kann \_ Nachricht speichern.

Die **mciwndm \_ kann \_** die Nachricht speichern, um zu ermitteln, ob ein MCI-Gerät Daten speichern kann. Sie können diese Nachricht explizit oder mithilfe des [**mciwndcansave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) -Makros senden.


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn das Gerät das Speichern oder **false** unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndcansave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





