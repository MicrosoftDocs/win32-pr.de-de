---
title: MCIWNDM_EJECT (Vfw.h)
description: Die MCIWNDM-EJECT-Nachricht sendet einen Befehl an ein \_ MCI-Gerät, um seine Medien auswerfen zu können. Sie können diese Nachricht explizit oder mithilfe des Makros MCIWndEject senden.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- MCIWNDM_EJECT von Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c752f192e8f74f2c6e861e581fd22a561bafd9ff6c0f369ba669bc4bf87fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429430"
---
# <a name="mciwndm_eject-message"></a>\_MCIWNDM-EJECT-Nachricht

Die **\_ MCIWNDM-EJECT-Nachricht** sendet einen Befehl an ein MCI-Gerät, um seine Medien auswerfen zu können. Sie können diese Nachricht explizit oder mithilfe des [**Makros MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) senden.


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





