---
description: Wird von einer Medienquelle ausgelöst, um eine neue Wiedergaberate an fordern. Die Anwendung sollte MIT DER ANGEFORDERTEN Rate DIERATEControl::SetRate aufrufen. Eine Medienquelle kann dieses Ereignis möglicherweise aus, wenn sie die Wiedergabe nicht mit der aktuellen Rate fortsetzen kann.
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

Wird von einer Medienquelle ausgelöst, um eine neue Wiedergaberate an fordern. Die Anwendung sollte [**MIT DER ANGEFORDERTEN Rate DIERATEControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) aufrufen. Eine Medienquelle kann dieses Ereignis möglicherweise aus, wenn sie die Wiedergabe nicht mit der aktuellen Rate fortsetzen kann.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE           | BESCHREIBUNG                                             |
|-------------------|---------------------------------------------------------|
| VT \_ R4<br/> | Die angeforderte neue Wiedergaberate.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                                                    | BESCHREIBUNG                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**\_MF-EREIGNIS \_ \_ VERANKERN**](mf-event-do-thinning-attribute.md)<br/> | Gibt an, ob die Medienquelle auch eine Schlankerung angibt.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




