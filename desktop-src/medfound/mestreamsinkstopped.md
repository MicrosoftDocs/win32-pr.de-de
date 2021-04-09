---
description: Wird durch eine streamsenke ausgelöst, wenn der Übergang zum beendeten Zustand abgeschlossen wird. Der Übergang zu "beendet" tritt auf, wenn die imfpresentationclock-Stopp Methode auf der senkenpräsentationmuhr aufgerufen wird.
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: Mestreamsinkbeendete-Ereignis (mfobjects. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35313ab3d43c950184a82e403fa6ad0eb5b4ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042580"
---
# <a name="mestreamsinkstopped-event"></a>Mestreamsinkbeendete-Ereignis

Wird durch eine streamsenke ausgelöst, wenn der Übergang zum beendeten Zustand abgeschlossen wird. Der Übergang zu "beendet" tritt auf, wenn die [**imfpresentationclock:: Stopp**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) -Methode auf der Präsentations Uhr der Senke aufgerufen wird.

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

 

 




