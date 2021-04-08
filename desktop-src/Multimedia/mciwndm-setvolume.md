---
title: MCIWNDM_SETVOLUME Meldung (VFW. h)
description: Die mciwndm- \_ Nachricht SetVolume legt die Volumeebene eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndsetvolume senden.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- MCIWNDM_SETVOLUME-Nachricht (Multimedia)
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
ms.openlocfilehash: 2215f8df3ea6f7b36b224318ebac68175ff9c265
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740232"
---
# <a name="mciwndm_setvolume-message"></a>Mciwndm- \_ SetVolume-Meldung

Die **mciwndm-Nachricht \_ SetVolume** legt die Volumeebene eines MCI-Geräts fest. Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndsetvolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) senden.


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*ivol*
</dt> <dd>

Neue Volumeebene. Geben Sie 1000 für die normale Volumeebene an. Geben Sie einen höheren Wert für ein höheres Volume oder einen niedrigeren Wert für ein ruhigeres Volume an.

</dd> </dl>

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

[**Mciwndsetvolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





