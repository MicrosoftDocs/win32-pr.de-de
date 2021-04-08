---
title: WOM_OPEN Meldung (MMSYSTEM. h)
description: Die WOM- \_ Meldung wird geöffnet, wenn ein Waveform-Audioausgabegerät geöffnet wird.
ms.assetid: 7fa175d3-7c07-4ca0-a0bd-4526fbc24f8d
keywords:
- WOM_OPEN-Nachricht (Multimedia)
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
ms.openlocfilehash: 3cfca721019b28a5bf039e8c56c75892d85bd5e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102835"
---
# <a name="wom_open-message"></a>WOM \_ geöffnete Nachricht

Die **WOM \_** -Meldung wird geöffnet, wenn ein Waveform-Audioausgabegerät geöffnet wird.


```C++
WOM_OPEN 
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

 

 





