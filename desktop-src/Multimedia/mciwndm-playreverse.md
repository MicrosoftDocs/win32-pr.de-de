---
title: MCIWNDM_PLAYREVERSE Meldung (VFW. h)
description: Die mciwndm \_ -playreverse-Nachricht gibt den aktuellen Inhalt in umgekehrter Richtung an, beginnend an der aktuellen Position und endet am Anfang des Inhalts, oder bis ein anderer Befehl die Wiedergabe beendet.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- MCIWNDM_PLAYREVERSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102839"
---
# <a name="mciwndm_playreverse-message"></a>Mciwndm- \_ playreverse-Nachricht

Die **mciwndm- \_ playreverse** -Nachricht gibt den aktuellen Inhalt in umgekehrter Richtung an, beginnend an der aktuellen Position und endet am Anfang des Inhalts, oder bis ein anderer Befehl die Wiedergabe beendet. Sie können diese Nachricht explizit oder mithilfe des [**mciwndplayreverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) -Makros senden.


```C++
MCIWNDM_PLAYREVERSE 
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

[**Mciwndplayreverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





