---
description: Wenn eine Medienquelle eine neue Wiedergaberate angibt, gibt dieses Attribut an, ob die Quelle auch eine Schlankerung angibt. Eine Definition der Verankerung finden Sie unter Informationen zur Rate Control.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: MF_EVENT_DO_THINNING -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9305df2b17e00b03bd9788ecd8caf26db82b8e331d1c72626374b63e7dcaf15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104936"
---
# <a name="mf_event_do_thinning-attribute"></a>MF \_ EVENT \_ DO \_ THINNING-Attribut

Wenn eine Medienquelle eine neue Wiedergaberate angibt, gibt dieses Attribut an, ob die Quelle auch eine Schlankerung angibt. Eine Definition der Verankerung finden Sie unter [Informationen zur Rate Control.](about-rate-control.md)

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut wird mit dem [MESourceRateChangeRequested-Ereignis](mesourceratechangerequested.md) verwendet. Wenn der Wert **TRUE ist,** fordert die Medienquelle einen Wechsel zur schlanken Wiedergabe an.

Der Standardwert ist **FALSE**.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




