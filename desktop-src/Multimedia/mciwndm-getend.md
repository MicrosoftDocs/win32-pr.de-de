---
title: MCIWNDM_GETEND Meldung (VFW. h)
description: Die mciwndm \_ GetEnd-Nachricht Ruft den Speicherort ab, an dem das Ende des Inhalts eines MCI-Geräts oder einer MCI-Datei gespeichert ist. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndgetend senden.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- MCIWNDM_GETEND-Nachricht (Multimedia)
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
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859220"
---
# <a name="mciwndm_getend-message"></a>Mciwndm \_ GetEnd-Nachricht

Die **mciwndm \_ GetEnd** -Nachricht Ruft den Speicherort ab, an dem das Ende des Inhalts eines MCI-Geräts oder einer MCI-Datei gespeichert ist. Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetend**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) senden.


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt den Speicherort im aktuellen Zeitformat zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetend**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





