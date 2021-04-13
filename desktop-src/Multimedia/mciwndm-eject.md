---
title: MCIWNDM_EJECT Meldung (VFW. h)
description: Die mciwndm- \_ Ausgabenachricht sendet einen Befehl an ein MCI-Gerät, um Ihre Medien auszuewerfen. Sie können diese Nachricht explizit oder mithilfe des mciwndeject-Makros senden.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- MCIWNDM_EJECT-Nachricht (Multimedia)
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
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391644"
---
# <a name="mciwndm_eject-message"></a>Mciwndm- \_ Ausgabenachricht

Die **mciwndm \_ -Ausgabenachricht** sendet einen Befehl an ein MCI-Gerät, um Ihre Medien auszuewerfen. Sie können diese Nachricht explizit oder mithilfe des [**mciwndeject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) -Makros senden.


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



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

[**Mciwndebug**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





