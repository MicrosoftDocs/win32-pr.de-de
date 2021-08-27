---
description: Wird von einem Medienstream ausgelöst, wenn die METHODE "Source::P ause" asynchron abgeschlossen wird.
ms.assetid: 8fafb9a1-95a4-44b6-acd6-fb007d515915
title: MEStreamPaused-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c71415ba147767f771c06cd1cbc8370fd1c3276d6932f791f32fe2212f843694
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113960"
---
# <a name="mestreampaused-event"></a>MEStreamPaused-Ereignis

Wird von einem Medienstream ausgelöst, wenn die [**160-:P ause-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) asynchron abgeschlossen wird.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




