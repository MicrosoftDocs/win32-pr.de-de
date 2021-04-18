---
title: MCIWNDM_GETVOLUME Meldung (VFW. h)
description: Die mciwndm \_ getvolume-Nachricht Ruft die aktuelle volumeeinstellung eines MCI-Geräts ab. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndgetvolume senden.
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- MCIWNDM_GETVOLUME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa11fb13a56dda7cb83e3d6c98b4b66083e91b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392180"
---
# <a name="mciwndm_getvolume-message"></a>Mciwndm \_ getvolume-Meldung

Die **mciwndm \_ getvolume** -Nachricht Ruft die aktuelle volumeeinstellung eines MCI-Geräts ab. Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetvolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) senden.


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt die aktuelle volumeeinstellung zurück. Der Standardwert lautet „1000“. Höhere Werte geben höhere Volumes an, niedrigere Werte weisen auf ruhigere Volumes hin.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetvolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 





