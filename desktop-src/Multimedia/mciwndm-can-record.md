---
title: MCIWNDM_CAN_RECORD-Nachricht (Vfw.h)
description: Die MCIWNDM \_ CAN \_ RECORD-Nachricht bestimmt, ob ein MCI-Gerät die Aufzeichnung unterstützt. Sie können diese Nachricht explizit oder mithilfe des MCIWndCanRecord-Makros senden.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- MCIWNDM_CAN_RECORD Windows Multimedia
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
ms.openlocfilehash: 5df46ce0cbffe17f890e50159a13a93192e67f60e323d6ba711bee6af7ac3f79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429650"
---
# <a name="mciwndm_can_record-message"></a>MCIWNDM \_ CAN \_ RECORD message

Die **MCIWNDM \_ CAN \_ RECORD-Nachricht** bestimmt, ob ein MCI-Gerät die Aufzeichnung unterstützt. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndCanRecord-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) senden.


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn das Gerät die Aufzeichnung unterstützt, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





