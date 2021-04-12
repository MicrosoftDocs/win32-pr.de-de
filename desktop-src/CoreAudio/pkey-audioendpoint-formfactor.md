---
description: Die pkey \_ audioendpoint \_ FormFactor-Eigenschaft gibt den Formfaktor des audioendpunktgeräts an. Der Formular Faktor gibt die physischen Attribute des audioendpunktgeräts an, das der Benutzer bearbeitet.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483683"
---
# <a name="pkey_audioendpoint_formfactor"></a>Pkey- \_ audioendpoint- \_ FormFactor

Die **pkey \_ audioendpoint \_ FormFactor** -Eigenschaft gibt den Formfaktor des audioendpunktgeräts an. Der Formular Faktor gibt die physischen Attribute des audioendpunktgeräts an, das der Benutzer bearbeitet.

Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ UI4 festgelegt.

Der **uintval** -Member der **PROPVARIANT** -Struktur enthält einen Enumerationswert, der in den uint-Typ umgewandelt wird. Sie wird auf einen der folgenden [**endpointformfactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) -Enumerationswerte festgelegt:

-   Remotenetworkdevice
-   Speakers
-   Linelevel
-   Aufgesetzt
-   Mikrofon
-   Headset
-   Ge
-   Unknowndigitalpassthrough
-   SPDIF
-   HDMI
-   Unknownformfactor

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften des audioendpunkts**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




