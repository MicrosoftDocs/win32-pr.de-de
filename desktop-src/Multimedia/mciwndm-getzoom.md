---
title: MCIWNDM_GETZOOM Meldung (VFW. h)
description: Die mciwndm \_ getzoom-Nachricht Ruft den aktuellen Zoomwert ab, der von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mithilfe des mciwndgetzoom-Makros senden.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- MCIWNDM_GETZOOM-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb4ae1883787f1b86dcc17f2d4a3e0e0ee29ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476227"
---
# <a name="mciwndm_getzoom-message"></a>Mciwndm \_ getzoom-Meldung

Die **mciwndm \_ getzoom** -Nachricht Ruft den aktuellen Zoomwert ab, der von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**mciwndgetzoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) -Makros senden.


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt die neuesten Werte zurück, die mit [**mciwndm- \_ setzoom**](mciwndm-setzoom.md)verwendet werden.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert 100 gibt an, dass das Bild nicht verkleinert wird. Der Wert 200 gibt an, dass das Bild auf die doppelte Größe vergrößert wird. Der Wert 50 gibt an, dass das Bild auf die Hälfte seiner ursprünglichen Größe reduziert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetzoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[**mciwndm- \_ setzoom**](mciwndm-setzoom.md)
</dt> </dl>

 

 





