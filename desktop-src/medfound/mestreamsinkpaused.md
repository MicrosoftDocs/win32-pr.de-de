---
description: Wird von einer Streamsenke ausgelöst, wenn der Übergang in den angehaltenen Zustand abgeschlossen ist.
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: MEStreamSinkPaused-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bd3e278c4aeb72300af5ef3821a465ac493efa554ed86d798716ff6dffbf1ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228600"
---
# <a name="mestreamsinkpaused-event"></a>MEStreamSinkPaused-Ereignis

Wird von einer Streamsenke ausgelöst, wenn der Übergang in den angehaltenen Zustand abgeschlossen ist. Der Übergang zu "angehalten" tritt auf, wenn die [**METHODEPRESENTPresentationClock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) für die Präsentationsuhr der Senke aufgerufen wird.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> <dt>

[Mediensenken](media-sinks.md)
</dt> </dl>

 

 




