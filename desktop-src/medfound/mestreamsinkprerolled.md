---
description: Wird von einer Streamsenke ausgelöst, wenn der Stream genügend Vorabrolldaten empfangen hat, um mit dem Rendern zu beginnen. Dieses Ereignis wird von Mediensenken ausgelöst, die die INTERFACESMediaSinkPreroll-Schnittstelle unterstützen.
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: MEStreamSinkPrerolled-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d46c4c4e076651cb38318bb908df280c503c0880a256087f4192433ecdb5406a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464800"
---
# <a name="mestreamsinkprerolled-event"></a>MEStreamSinkPrerolled-Ereignis

Wird von einer Streamsenke ausgelöst, wenn der Stream genügend Vorabrolldaten empfangen hat, um mit dem Rendern zu beginnen. Dieses Ereignis wird von Mediensenken ausgelöst, die die [**INTERFACESMediaSinkPreroll-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) unterstützen.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> <dt>

[Mediensenken](media-sinks.md)
</dt> </dl>

 

 




