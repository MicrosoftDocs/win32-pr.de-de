---
title: MCIWNDM_CAN_CONFIG Meldung (VFW. h)
description: Die Meldung mciwndm \_ CAN \_ config bestimmt, ob ein MCI-Gerät ein Konfigurations Dialogfeld anzeigen kann. Sie können diese Nachricht explizit oder mithilfe des mciwndcanconfig-Makros senden.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- MCIWNDM_CAN_CONFIG-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816a8c1dfaec6fc7d7854f8873ce05e74e4de6bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479137"
---
# <a name="mciwndm_can_config-message"></a>Mciwndm \_ kann \_ Nachricht konfigurieren

Die Meldung **mciwndm \_ CAN \_ config** bestimmt, ob ein MCI-Gerät ein Konfigurations Dialogfeld anzeigen kann. Sie können diese Nachricht explizit oder mithilfe des [**mciwndcanconfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) -Makros senden.


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn das Gerät eine Konfiguration unterstützt, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndcanconfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





