---
title: MCIWNDM_GETALIAS Meldung (Vfw.h)
description: Die MCIWNDM \_ GETALIAS-Nachricht ruft den Alias ab, der zum Öffnen eines MCI-Geräts oder einer MCI-Datei mit der mciSendString-Funktion verwendet wird. Sie können diese Nachricht explizit oder mithilfe des MCIWndGetAlias-Makros senden.
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- MCIWNDM_GETALIAS nachricht Windows Multimedia
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
ms.openlocfilehash: 857ea90205b5204cd7c4af19f27a420684e59543717b2689f178d97cd5a600de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137751"
---
# <a name="mciwndm_getalias-message"></a>MCIWNDM \_ GETALIAS-Nachricht

Die **MCIWNDM \_ GETALIAS-Nachricht** ruft den Alias ab, der zum Öffnen eines MCI-Geräts oder einer MCI-Datei mit der [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetAlias-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) senden.


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
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mciSendString**](/previous-versions//dd757161(v=vs.85))
</dt> <dt>

[**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

