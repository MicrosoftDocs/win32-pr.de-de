---
description: Wird von einem inhaltsenabler-Objekt ausgelöst, wenn die Aktion zum Aktivieren von Objekten abgeschlossen ist.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Meenablerabgeschlossene-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a74f7379ccc2983abd2327e1250bcf1ca14e688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130745"
---
# <a name="meenablercompleted-event"></a>Meenablerabgeschlossene-Ereignis

Wird von einem inhaltsenabler-Objekt ausgelöst, wenn die Aktivierungs Aktion des Objekts abgeschlossen ist. Objekte, die die [**imbcontentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle verfügbar machen, können dieses Ereignis erhöhen. Das-Ereignis wird ausgelöst, wenn eines der folgenden Ereignisse eintritt:

-   Die [**imfcontentenabler:: automaticenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) -Methode wird asynchron abgeschlossen.
-   Die Anwendung ruft [**IMF contentenabler:: monitorenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)auf, und die Anwendung schließt dann die HTTP POST-Anforderung ab, wie in der **monitorenable** -Methode beschrieben.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Der Statuscode aus dem Ereignis kann einen der folgenden Werte enthalten.



|                                      |                                                                                                                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **S \_ OK**                            | Der Vorgang wurde erfolgreich ausgeführt.                                                                                                                                                        |
| **NS \_ E \_ DRM- \_ Lizenz \_ notbezogen** | Die DRM-Lizenz wurde nicht erworben. Wenn beim vorherigen Versuch [**automaticenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable)verwendet wurde, sollte die Anwendung den nicht automatischen Erwerb testen. |
| **NS \_ S- \_ DRM- \_ Monitor \_ abgebrochen**   | Der [**monitorenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) -Vorgang wurde abgebrochen.                                                                                            |



 

Um dieses Ereignis zu erhalten, Fragen Sie die [**imfcontentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle für die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle ab. Aufrufen Sie dann [**imfmediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), wie im Thema [Medienereignis-Generatoren](media-event-generators.md)beschrieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF contentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Medienereignis Generatoren](media-event-generators.md)
</dt> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




