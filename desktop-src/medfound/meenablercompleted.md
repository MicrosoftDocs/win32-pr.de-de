---
description: Wird von einem Content Enabler-Objekt ausgelöst, wenn die Objekte, die die Aktion aktivieren, abgeschlossen sind.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: MEEnablerCompleted-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2983cbcf3927626da88432c0cc04f28e2fc5d3e866d161b514dcbe5108bcf92a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013800"
---
# <a name="meenablercompleted-event"></a>MEEnablerCompleted-Ereignis

Wird von einem Content Enabler-Objekt ausgelöst, wenn die Aktivierungsaktion des Objekts abgeschlossen ist. Objekte, die die [**SCHNITTSTELLE "CONTENTContentEnabler"**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) verfügbar machen, können dieses Ereignis auslösen. Das -Ereignis wird ausgelöst, wenn einer der folgenden Ereignisse auftritt:

-   Die [**ASYNCHRONOUSContentEnabler::AutomaticEnable-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) wird asynchron abgeschlossen.
-   Die Anwendung ruft [**DIECONTENTContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)auf, und dann schließt die Anwendung die HTTP POST-Anforderung ab, wie in der **MonitorEnable-Methode** beschrieben.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Der Statuscode des Ereignisses kann einen der folgenden Werte enthalten.



| Wert                                     | Beschreibung                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **S \_ OK**                            | Der Vorgang wurde erfolgreich ausgeführt.                                                                                                                                                        |
| **NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED** | Die DRM-Lizenz wurde nicht erworben. Wenn beim vorherigen Versuch [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable)verwendet wurde, sollte die Anwendung versuchen, nicht automatisch zu erwerben. |
| **NS \_ S \_ DRM \_ MONITOR \_ CANCELLED**   | Der [**MonitorEnable-Vorgang**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) wurde abgebrochen.                                                                                            |



 

Um dieses Ereignis zu empfangen, fragen Sie die [**SCHNITTSTELLE "CONTENTContentEnabler"**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) nach der [**SCHNITTSTELLE "ARRANGEMediaEventGenerator"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) ab. Rufen Sie dann [**DENMEDIAEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)auf, wie im Thema [Medienereignisgeneratoren](media-event-generators.md)beschrieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CONTENTContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Medienereignisgeneratoren](media-event-generators.md)
</dt> <dt>

[Media Foundation-Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




