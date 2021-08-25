---
description: Die Eigenschaft PKEY AudioEndpoint ControlPanelPageProvider gibt die CLSID des registrierten Anbieters der Erweiterung device-properties für das \_ \_ Audioendpunktgerät an.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc39f471649487dcdbfc2fa94371466eabd9ec59a8f9de19bdeafcec9d4283b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695350"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a>PKEY \_ AudioEndpoint \_ ControlPanelPageProvider

Die **Eigenschaft PKEY \_ AudioEndpoint \_ ControlPanelPageProvider** gibt die CLSID des registrierten Anbieters der Erweiterung device-properties für das Audioendpunktgerät an. Die Erweiterung stellt die Eigenschaften des Audioendpunkts, die auf der Geräteeigenschaftenseite des Multimedia-Windows angezeigt werden, Mmsys.cpl. Weitere Informationen zu Mmsys.cpl finden Sie in der Windows DDK-Dokumentation.

Der **vt-Member** der **PROPVARIANT-Struktur** ist auf VT \_ LPWSTR festgelegt.

Der **pwszVal-Member** der **PROPVARIANT-Struktur** zeigt auf eine null terminierte Breitzeichenfolge, die eine GUID enthält, die den Anbieter der Systemsteuerungserweiterung identifiziert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Audioendpunkteigenschaften**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




