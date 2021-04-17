---
title: MCIWNDM_GETSPEED Meldung (VFW. h)
description: Die mciwndm \_ getspeed-Meldung Ruft die Wiedergabegeschwindigkeit eines MCI-Geräts ab. Sie können diese Nachricht explizit oder mithilfe des mciwndgetspeed-Makros senden.
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- MCIWNDM_GETSPEED-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84a8ebb3e97d4543f68f3a237add8eed7706ae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478927"
---
# <a name="mciwndm_getspeed-message"></a>Mciwndm \_ getspeed-Meldung

Die **mciwndm \_ getspeed** -Meldung Ruft die Wiedergabegeschwindigkeit eines MCI-Geräts ab. Sie können diese Nachricht explizit oder mithilfe des [**mciwndgetspeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) -Makros senden.


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt die Wiedergabegeschwindigkeit zurück, wenn erfolgreich. Der Wert für die normale Geschwindigkeit ist 1000. Größere Werte weisen auf schnellere Geschwindigkeiten hin, kleinere Werte auf langsamere Geschwindigkeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetspeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 





