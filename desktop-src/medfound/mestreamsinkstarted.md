---
description: Wird durch eine streamsenke ausgelöst, wenn der Übergang in den Status "wird ausgeführt" versetzt wird.
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: Mestreamsink Started-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407ab885da04746034b7126a8d9bb9389d2928f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348516"
---
# <a name="mestreamsinkstarted-event"></a>Mestreamsink Started-Ereignis

Wird durch eine streamsenke ausgelöst, wenn der Übergang in den Status "wird ausgeführt" versetzt wird. Der Übergang zu "wird ausgeführt" erfolgt, wenn die [**imfpresentationclock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) -Methode auf der Präsentations Uhr der Senke aufgerufen wird. Die Medien Senke empfängt die Benachrichtigung über die [**imfclockstaatink:: onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) -Methode oder die [**imfclockstaatink:: onclockrestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) -Methode.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> <dt>

[Medien senken](media-sinks.md)
</dt> </dl>

 

 




