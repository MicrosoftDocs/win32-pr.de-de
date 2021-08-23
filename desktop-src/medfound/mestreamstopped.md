---
description: Wird von einem Mediendatenstrom ausgelöst, wenn die METHODE VONMEDIASOURCE::Stop asynchron abgeschlossen wird.
ms.assetid: 80280820-b618-43d9-881e-6119dfa36e22
title: MEStreamStopped-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35fc2dc010b75b0707d17d327f9ed7c7f5d4821ccffe3c0f1a2e9ec567e6602d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464620"
---
# <a name="mestreamstopped-event"></a>MEStreamStopped-Ereignis

Wird von einem Mediendatenstrom ausgelöst, wenn die [**METHODE VONMEDIASOURCE::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) asynchron abgeschlossen wird.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Jeder aktive Stream in der Präsentation sendet dieses Ereignis.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




