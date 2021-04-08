---
description: Wird durch eine streamsenke ausgelöst, wenn der Stream genug vorab Rollendaten empfangen hat, um das Rendering zu beginnen. Dieses Ereignis wird von Medien senken ausgelöst, die die imfmediasinkpreroll-Schnittstelle unterstützen.
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: Mestreamsinkprerolled-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312daa90c995ccbbe8667cfa5acdf47975248474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754289"
---
# <a name="mestreamsinkprerolled-event"></a>Mestreamsinkprerolled-Ereignis

Wird durch eine streamsenke ausgelöst, wenn der Stream genug vorab Rollendaten empfangen hat, um das Rendering zu beginnen. Dieses Ereignis wird von Medien senken ausgelöst, die die [**imfmediasinkpreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) -Schnittstelle unterstützen.

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

 

 




