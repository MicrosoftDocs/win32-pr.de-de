---
title: MM_WOM_CLOSE Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm WOM \_ Close wird an ein Fenster gesendet, wenn ein Waveform-Audioausgabegerät geschlossen wird. Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- MM_WOM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dccdae49efc107a513e047282922f3a6de73e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343070"
---
# <a name="mm_wom_close-message"></a>Meldung zum Schließen von mm \_ WOM \_

Die Meldung **mm \_ WOM \_ Close** wird an ein Fenster gesendet, wenn ein Waveform-Audioausgabegerät geschlossen wird. Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*houtputdev*
</dt> <dd>

Handle für das Gerät, das geschlossen wurde.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Bleiben muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Waveform-Audiodatei](waveform-audio.md)
</dt> <dt>

[Wellenform Meldungen](waveform-messages.md)
</dt> </dl>

 

 





