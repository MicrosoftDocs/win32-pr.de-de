---
title: MCIWNDM_GETACTIVETIMER Meldung (VFW. h)
description: Die mciwndm \_ getactivetimer-Nachricht Ruft den Aktualisierungs Zeitraum ab, der verwendet wird, wenn das mciwnd-Fenster das aktive Fenster ist. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndgetactivetimer senden.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- MCIWNDM_GETACTIVETIMER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106532"
---
# <a name="mciwndm_getactivetimer-message"></a>Mciwndm \_ getactivetimer-Nachricht

Die **mciwndm \_ getactivetimer** -Nachricht Ruft den Aktualisierungs Zeitraum ab, der verwendet wird, wenn das mciwnd-Fenster das aktive Fenster ist. Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) senden.


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt den Update Zeitraum in Millisekunden zurück. Der Standardwert ist 500 Millisekunden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





