---
description: Wird von einer Ausgabevertrauensstellungsstelle (Output Trust Authority, OTA) ausgelöst, wenn die METHODE DURCHDRoutputTrustAuthority::SetPolicy asynchron abgeschlossen wird.
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: MEPolicySet-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064cbb92e85e300aa2c2b7db28d08b01296834413ed92e36eb5b7ce88e5486c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877557"
---
# <a name="mepolicyset-event"></a>MEPolicySet-Ereignis

Wird von einer Ausgabevertrauensstellungsstelle (Output Trust Authority, OTA) ausgelöst, wenn die [**METHODE DURCHDRoutputTrustAuthority::SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) asynchron abgeschlossen wird.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |
| VT \_ UI4<br/> | Ein Bezeichner, der über das attribut "MF_POLICY_ID" für EINE [Kennungs-MF_POLICY_ID](mf-policy-id.md) werden kann. [](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)<br/> <br/> |



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

 

 




