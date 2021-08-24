---
title: MCIWNDM_GETSTART (Vfw.h)
description: Die MCIWNDM GETSTART-Nachricht ruft den Speicherort des Anfangs des Inhalts eines MCI-Geräts oder einer \_ MCI-Datei ab. Sie können diese Nachricht explizit oder mithilfe des MCIWndGetStart-Makros senden.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- MCIWNDM_GETSTART von Windows Multimedia
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
ms.openlocfilehash: e0efb5689009fdd6928afd1d2f232bcb1bbeb2160aecf3d79ddb263ed6f315de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429230"
---
# <a name="mciwndm_getstart-message"></a>MCIWNDM \_ GETSTART-Nachricht

Die **MCIWNDM \_ GETSTART-Nachricht** ruft den Speicherort des Anfangs des Inhalts eines MCI-Geräts oder einer MCI-Datei ab. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetStart-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) senden.


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt die Position im aktuellen Zeitformat zurück.

## <a name="remarks"></a>Hinweise

In der Regel ist der Rückgabewert 0 (null). einige Geräte verwenden jedoch einen Startort ungleich 0 (null). Bei der Suche nach diesem Speicherort wird das Gerät auf den Start des Mediums fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





