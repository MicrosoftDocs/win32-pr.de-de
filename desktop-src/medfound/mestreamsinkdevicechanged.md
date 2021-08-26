---
description: Wird von den Streamsenken des erweiterten Videorenderers (Enhanced Video Renderer, EVR) ausgelöst, wenn sich das Videogerät ändert.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: MEStreamSinkDeviceChanged-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb760a45125ae7434ff2a58d43f087d2ec3c030cb29351ea4d2113ca8fe10c0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061010"
---
# <a name="mestreamsinkdevicechanged-event"></a>MEStreamSinkDeviceChanged-Ereignis

Wird von den Streamsenken des erweiterten Videorenderers (Enhanced Video Renderer, EVR) ausgelöst, wenn sich das Videogerät ändert. Beispielsweise löst die EVR dieses Ereignis aus, wenn sie ein [**EC \_ DISPLAY \_ CHANGED-Ereignis**](../directshow/ec-display-changed.md) empfängt.

Die Media Foundation Pipeline reagiert auf dieses Ereignis, indem alle Beispielanforderungen erneut übermittelt werden, die beim Ändern des Geräts fehlgeschlagen sind.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> <dt>

[Mediensenken](media-sinks.md)
</dt> </dl>

 

 
