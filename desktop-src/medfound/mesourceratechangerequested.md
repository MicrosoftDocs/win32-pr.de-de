---
description: Wird von einer Medienquelle ausgelöst, um eine neue Wiedergaberate anzufordern. Die Anwendung sollte ÜBERRATEControl::SetRate mit der angeforderten Rate aufrufen. Eine Medienquelle kann dieses Ereignis auslösen, wenn die Wiedergabe mit der aktuellen Rate nicht fortgesetzt werden kann.
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: MESourceRateChangeRequested-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d8a88225fd3a0a95c56d549a712b295ba562cc684c08fe4b762c0169e3637c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974129"
---
# <a name="mesourceratechangerequested-event"></a>MESourceRateChangeRequested-Ereignis

Wird von einer Medienquelle ausgelöst, um eine neue Wiedergaberate anzufordern. Die Anwendung sollte [**ÜBERRATEControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) mit der angeforderten Rate aufrufen. Eine Medienquelle kann dieses Ereignis auslösen, wenn die Wiedergabe mit der aktuellen Rate nicht fortgesetzt werden kann.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE           | BESCHREIBUNG                                             |
|-------------------|---------------------------------------------------------|
| VT \_ R4<br/> | Die angeforderte neue Wiedergaberate.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                                                    | BESCHREIBUNG                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**MF \_ EVENT \_ DO \_ THINNING**](mf-event-do-thinning-attribute.md)<br/> | Gibt an, ob die Medienquelle ebenfalls eine Ausschmalung anfordert.<br/> <br/> |



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

 

 




