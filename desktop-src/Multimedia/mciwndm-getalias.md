---
title: MCIWNDM_GETALIAS Meldung (VFW. h)
description: Die mciwndm \_ getalias-Nachricht Ruft den Alias ab, mit dem ein MCI-Gerät oder eine MCI-Datei mit der mciSendString-Funktion geöffnet wird. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndgetalias senden.
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- MCIWNDM_GETALIAS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETALIAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e971c50b9abc450387ac29f9a7331bfdca5c38c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342182"
---
# <a name="mciwndm_getalias-message"></a>Mciwndm \_ getalias-Nachricht

Die **mciwndm \_ getalias** -Nachricht Ruft den Alias ab, mit dem ein MCI-Gerät oder eine MCI-Datei mit der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion geöffnet wird. Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetalias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) senden.


```C++
MCIWNDM_GETALIAS 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt den Gerätealias zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mciSendString**](/previous-versions//dd757161(v=vs.85))
</dt> <dt>

[**Mciwndgetalias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

