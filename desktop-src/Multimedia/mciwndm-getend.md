---
title: MCIWNDM_GETEND (Vfw.h)
description: Die MCIWNDM GETEND-Nachricht ruft den Speicherort des Endes des Inhalts eines MCI-Geräts oder einer \_ MCI-Datei ab. Sie können diese Nachricht explizit oder mithilfe des MCIWndGetEnd-Makros senden.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- MCIWNDM_GETEND-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880b1a464d671ca57e1955d4131776a999d1fb6bd8f17ad5d08139abc64a757b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137731"
---
# <a name="mciwndm_getend-message"></a>MCIWNDM \_ GETEND-Nachricht

Die **MCIWNDM \_ GETEND-Nachricht** ruft den Speicherort des Endes des Inhalts eines MCI-Geräts oder einer MCI-Datei ab. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetEnd-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) senden.


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt die Position im aktuellen Zeitformat zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





