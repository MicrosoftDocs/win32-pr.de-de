---
title: MCIWNDM_GETPALETTE Meldung (VFW. h)
description: Die mciwndm \_ getpalette-Nachricht Ruft ein Handle der Palette ab, die von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mithilfe des mciwndgetpalette-Makros senden.
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- MCIWNDM_GETPALETTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faec3dd5d9c401d943fbc55ca58e452d3fb25497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040216"
---
# <a name="mciwndm_getpalette-message"></a>Mciwndm \_ getpalette-Nachricht

Die **mciwndm \_ getpalette** -Nachricht Ruft ein Handle der Palette ab, die von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**mciwndgetpalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) -Makros senden.


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt das Handle der Palette zurück, wenn erfolgreich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetpalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 





