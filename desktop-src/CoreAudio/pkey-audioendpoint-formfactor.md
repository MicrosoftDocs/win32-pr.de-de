---
description: Die PKEY \_ AudioEndpoint \_ FormFactor-Eigenschaft gibt den Formfaktor des Audioendpunktgeräts an. Der Formfaktor gibt die physischen Attribute des Audioendpunktgeräts an, das der Benutzer bearbeitet.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76b53b91a03cda5e8484878f62c3c7a205e422f53ed647d29cca6435e0f14f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018338"
---
# <a name="pkey_audioendpoint_formfactor"></a>PKEY \_ AudioEndpoint \_ FormFactor

Die **PKEY \_ AudioEndpoint \_ FormFactor-Eigenschaft** gibt den Formfaktor des Audioendpunktgeräts an. Der Formfaktor gibt die physischen Attribute des Audioendpunktgeräts an, das der Benutzer bearbeitet.

Der **vt-Member** der **PROPVARIANT-Struktur** ist auf VT \_ UI4 festgelegt.

Der **uintVal-Member** der **PROPVARIANT-Struktur** enthält einen Enumerationswert, der in den Typ UINT typisiert wird. Sie wird auf einen der folgenden [**EndpointFormFactor-Enumerationswerte**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) festgelegt:

-   RemoteNetworkDevice
-   Speakers
-   LineLevel
-   Kopfhörer
-   Mikrofon
-   Headset
-   Mobilteil
-   UnknownDigitalPassthrough
-   Spdif
-   HDMI
-   UnknownFormFactor

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Audioendpunkteigenschaften**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




