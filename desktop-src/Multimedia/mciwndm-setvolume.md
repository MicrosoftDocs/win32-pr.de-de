---
title: MCIWNDM_SETVOLUME (Vfw.h)
description: Die MCIWNDM \_ SETVOLUME-Nachricht legt die Volumeebene eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mithilfe des MCIWndSetVolume-Makros senden.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- MCIWNDM_SETVOLUME-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8c40d2c8b2c7c4cb309b5c6e5b21dcd29e6c8ee27b9ca8c97556cb14927a121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428540"
---
# <a name="mciwndm_setvolume-message"></a>MCIWNDM \_ SETVOLUME-Nachricht

Die **MCIWNDM \_ SETVOLUME-Nachricht legt** die Volumeebene eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndSetVolume-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) senden.


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*
</dt> <dd>

Neue Volumeebene. Geben Sie 1000 für die normale Volumeebene an. Geben Sie einen höheren Wert für ein lauteres Volume oder einen niedrigeren Wert für ein stilleres Volume an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





