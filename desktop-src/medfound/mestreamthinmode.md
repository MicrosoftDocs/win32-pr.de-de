---
description: Wird von einem Medienstream ausgelöst, wenn er den Stream startet oder beendet. Informationen zum Ausschmalen finden Sie unter Informationen zur Ratensteuerung.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: MEStreamThinMode-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13a9cc5b625a8b366bece1debc2017fce51e35d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479516"
---
# <a name="mestreamthinmode-event"></a>MEStreamThinMode-Ereignis

Wird von einem Medienstream ausgelöst, wenn er den Stream startet oder beendet. Informationen zur *Ausschmalung* finden Sie unter [Informationen zur Ratensteuerung.](about-rate-control.md)

Dieses Ereignis kann als Antwort auf die [**METHODE VONRATECONTROL::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) oder DIE [**METHODE DERQUALITYAdvise::SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) gesendet werden.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:




| VARTYPE | BESCHREIBUNG | 
|---------|-------------|
| VT_BOOL<br /> | Gibt an, ob die Ausschmalung gestartet oder beendet wurde.<br /><ul><li>VARIANT_TRUE: Die nach diesem Ereignis übermittelten Stichproben werden ausgesät.</li><li>VARIANT_FALSE: Stichproben, die nach diesem Ereignis übermittelt werden, werden nicht ausgesät.</li></ul><br /> | 




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

 

 




