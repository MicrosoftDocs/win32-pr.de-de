---
title: WIM_CLOSE Meldung (MMSYSTEM. h)
description: Die WIM \_ -Schließen-Nachricht wird an die angegebene Waveform-audioeingaberückruf-Funktion gesendet, wenn ein Waveform-Audioeingabegerät geschlossen wird. Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.
ms.assetid: 3774b8b4-b03b-49e7-b9cd-cf3f194df847
keywords:
- WIM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6028ac6c45aa013138aab227e79d8d210ad70bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478717"
---
# <a name="wim_close-message"></a>Wim- \_ Schließen-Nachricht

Die **WIM- \_ Schließen** -Nachricht wird an die angegebene Waveform-audioeingaberückruf-Funktion gesendet, wenn ein Waveform-Audioeingabegerät geschlossen wird. Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.


```C++
WIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Bleiben muss 0 (null) sein.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
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

 

 





