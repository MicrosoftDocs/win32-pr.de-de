---
title: MCIWNDM_GETDEVICEID Meldung (VFW. h)
description: Die mciwndm \_ getdeviceid-Meldung Ruft den Bezeichner des derzeit geöffneten MCI-Geräts ab, das mit der mciSendCommand-Funktion verwendet werden soll. Sie können diese Nachricht explizit oder mit dem mciwndgetdeviceid-Makro senden.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- MCIWNDM_GETDEVICEID-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040217"
---
# <a name="mciwndm_getdeviceid-message"></a>Mciwndm \_ getdeviceid-Meldung

Die **mciwndm \_ getdeviceid** -Meldung Ruft den Bezeichner des derzeit geöffneten MCI-Geräts ab, das mit der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion verwendet werden soll. Sie können diese Nachricht explizit oder mit dem [**mciwndgetdeviceid**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) -Makro senden.


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt den Geräte Bezeichner zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**Mciwndgetde viceid**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 

