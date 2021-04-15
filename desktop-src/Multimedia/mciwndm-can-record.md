---
title: MCIWNDM_CAN_RECORD Meldung (VFW. h)
description: Die mciwndm \_ kann die \_ Meldung aufzeichnen, ob ein MCI-Gerät eine Aufzeichnung unterstützt. Sie können diese Nachricht explizit oder mithilfe des mciwndcanrecord-Makros senden.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- MCIWNDM_CAN_RECORD-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acbc9efa3ca973c12112a599d1202ad936107a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478720"
---
# <a name="mciwndm_can_record-message"></a>Mciwndm \_ kann \_ Nachricht aufzeichnen

Die **mciwndm \_ kann \_** die Meldung aufzeichnen, ob ein MCI-Gerät eine Aufzeichnung unterstützt. Sie können diese Nachricht explizit oder mithilfe des [**mciwndcanrecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) -Makros senden.


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn das Gerät eine Aufzeichnung unterstützt oder andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndcanrecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





