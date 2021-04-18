---
title: MCIWNDM_GETINACTIVETIMER Meldung (VFW. h)
description: Die mciwndm \_ getinactivetimer-Nachricht Ruft den Aktualisierungs Zeitraum ab, der verwendet wird, wenn das mciwnd-Fenster das inaktive Fenster ist. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndgetinactivetimer senden.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- MCIWNDM_GETINACTIVETIMER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339123"
---
# <a name="mciwndm_getinactivetimer-message"></a>Mciwndm \_ getinactivetimer-Nachricht

Die **mciwndm \_ getinactivetimer** -Nachricht Ruft den Aktualisierungs Zeitraum ab, der verwendet wird, wenn das mciwnd-Fenster das inaktive Fenster ist. Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetinactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) senden.


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt den Aktualisierungs Zeitraum in Millisekunden zurück. Der Standardwert beträgt 2.000 Millisekunden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetinactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





