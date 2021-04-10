---
title: MCIWNDM_SETSPEED Meldung (VFW. h)
description: Die mciwndm- \_ setSpeed-Nachricht legt die Wiedergabegeschwindigkeit eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mithilfe des mciwndsetspeed-Makros senden.
ms.assetid: 7658dd25-dc68-4bd1-b995-df06b509be16
keywords:
- MCIWNDM_SETSPEED-Nachricht (Multimedia)
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
ms.openlocfilehash: 282bb3a2e135b674605be55aaccaa455d30edbcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956773"
---
# <a name="mciwndm_setspeed-message"></a>Mciwndm- \_ setSpeed-Meldung

Die **mciwndm- \_ setSpeed** -Nachricht legt die Wiedergabegeschwindigkeit eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mithilfe des [**mciwndsetspeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) -Makros senden.


```C++
MCIWNDM_SETSPEED 
wParam = 0; 
lParam = (LPARAM) (UINT) iSpeed; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*
</dt> <dd>

Wiedergabegeschwindigkeit. Geben Sie 1000 für normale Geschwindigkeit, größere Werte für schnellere Geschwindigkeiten und kleinere Werte für langsamere Geschwindigkeiten an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndsetspeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
</dt> </dl>

 

 





