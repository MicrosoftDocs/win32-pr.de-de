---
title: MCIWNDM_GETDEVICEID (Vfw.h)
description: Die MCIWNDM GETDEVICEID-Nachricht ruft den Bezeichner des derzeit geöffneten MCI-Geräts ab, das mit der \_ mciSendCommand-Funktion verwendet werden soll. Sie können diese Nachricht explizit oder mithilfe des Makros MCIWndGetDeviceID senden.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- MCIWNDM_GETDEVICEID von Windows Multimedia
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
ms.openlocfilehash: c465ae0a213559c931d8d2e7d6f03da874b9c6c5e7a2ab317e3487d33800656b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986050"
---
# <a name="mciwndm_getdeviceid-message"></a>MCIWNDM \_ GETDEVICEID-Nachricht

Die **MCIWNDM \_ GETDEVICEID-Nachricht** ruft den Bezeichner des derzeit geöffneten MCI-Geräts ab, das mit der [**mciSendCommand-Funktion verwendet werden**](/previous-versions//dd757160(v=vs.85)) soll. Sie können diese Nachricht explizit oder mithilfe des [**Makros MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) senden.


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt den Gerätebezeichner zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 

