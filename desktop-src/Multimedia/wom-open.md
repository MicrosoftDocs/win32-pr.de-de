---
title: WOM_OPEN Meldung (Mmsystem.h)
description: Die WOM \_ OPEN-Nachricht wird an eine Waveform-Audio-Ausgaberückruffunktion gesendet, wenn ein Waveform-Audio-Ausgabegerät geöffnet wird.
ms.assetid: 7fa175d3-7c07-4ca0-a0bd-4526fbc24f8d
keywords:
- WOM_OPEN nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d0e145bf533bf9b48b88a87d449679e7728b679e72ed70a787168b5936f5aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940657"
---
# <a name="wom_open-message"></a>WOM \_ OPEN-Nachricht

Die **WOM \_ OPEN-Nachricht** wird an eine Waveform-Audio-Ausgaberückruffunktion gesendet, wenn ein Waveform-Audio-Ausgabegerät geöffnet wird.


```C++
WOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Reserviert; muss 0 (null) sein.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Reserviert; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Waveform-Audio](waveform-audio.md)
</dt> <dt>

[Wellenformnachrichten](waveform-messages.md)
</dt> </dl>

 

 





