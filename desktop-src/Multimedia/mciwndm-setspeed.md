---
title: MCIWNDM_SETSPEED (Vfw.h)
description: Die MCIWNDM-Nachricht \_ SETSPEED legt die Wiedergabegeschwindigkeit eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mithilfe des MCIWndSetSpeed-Makros senden.
ms.assetid: 7658dd25-dc68-4bd1-b995-df06b509be16
keywords:
- MCIWNDM_SETSPEED-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6de0d78fef7723dab0ae2e2d3923f73f872e38dfd9c3e0f42443f7141f020336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782990"
---
# <a name="mciwndm_setspeed-message"></a>MCIWNDM \_ SETSPEED-Meldung

Die **MCIWNDM-Nachricht \_ SETSPEED legt** die Wiedergabegeschwindigkeit eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndSetSpeed-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) senden.


```C++
MCIWNDM_SETSPEED 
wParam = 0; 
lParam = (LPARAM) (UINT) iSpeed; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*
</dt> <dd>

Wiedergabegeschwindigkeit. Geben Sie 1000 für normale Geschwindigkeit, größere Werte für höhere Geschwindigkeiten und kleinere Werte für langsamere Geschwindigkeiten an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
</dt> </dl>

 

 





