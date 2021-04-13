---
title: MCIWNDM_GETSTART Meldung (VFW. h)
description: Die mciwndm \_ GETSTART-Meldung Ruft den Speicherort ab, an dem der Inhalt eines MCI-Geräts oder einer MCI-Datei beginnt. Sie können diese Nachricht explizit oder mithilfe des mciwndgetstart-Makros senden.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- MCIWNDM_GETSTART-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbe88df006f1f98854e42259074d82bbd87dc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475525"
---
# <a name="mciwndm_getstart-message"></a>Mciwndm \_ GETSTART-Meldung

Die **mciwndm \_ GETSTART** -Meldung Ruft den Speicherort ab, an dem der Inhalt eines MCI-Geräts oder einer MCI-Datei beginnt. Sie können diese Nachricht explizit oder mithilfe des [**mciwndgetstart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) -Makros senden.


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt den Speicherort im aktuellen Zeitformat zurück.

## <a name="remarks"></a>Bemerkungen

In der Regel ist der Rückgabewert 0 (null). Einige Geräte verwenden jedoch einen Start Speicherort, der nicht NULL ist. Durch die Suche nach diesem Speicherort wird das Gerät auf den Anfang des Mediums festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetstart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





