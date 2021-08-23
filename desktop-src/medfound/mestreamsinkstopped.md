---
description: Wird von einer Streamsenke ausgelöst, wenn der Übergang in den beendeten Zustand abgeschlossen ist. Der Übergang zu "Beendet" tritt auf, wenn die STOPPresentationClock-Methode für die Präsentationsuhr der Senken aufgerufen wird.
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: MEStreamSinkStopped-Ereignis (Mfobjects.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7bf6a39dca8f50fed8fdd1d0137405225624999fab42771e485174ba4f0afa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715100"
---
# <a name="mestreamsinkstopped-event"></a>MEStreamSinkStopped-Ereignis

Wird von einer Streamsenke ausgelöst, wenn der Übergang in den beendeten Zustand abgeschlossen ist. Der Übergang zu "Beendet" tritt auf, wenn die [**METHODE VORREDPresentationClock::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) für die Präsentationsuhr der Senke aufgerufen wird.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | Beschreibung                           |
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

 

 




