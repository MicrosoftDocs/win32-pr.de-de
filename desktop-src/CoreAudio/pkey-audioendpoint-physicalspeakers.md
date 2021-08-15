---
description: 'Weitere Informationen finden Sie unter: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358623626274a0ab3a0898e9e912e4f5f990c14d00dd6f6ef57bb4050297403f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406416"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a>PKEY \_ AudioEndpoint \_ PhysicalSpeakers

Die **PKEY \_ AudioEndpoint \_ PhysicalSpeakers-Eigenschaft** gibt die Kanalkonfigurationsmaske für das Audioendpunktgerät an. Die Maske gibt die physische Konfiguration einer Gruppe von Sprechern an und gibt die Zuweisung von Kanälen zu Sprechern an. Weitere Informationen zu Kanalkonfigurationsmasken finden Sie in den folgenden Themen:

1.  Die Beschreibung der KSPROPERTY \_ AUDIO \_ CHANNEL \_ CONFIG-Eigenschaft in der Windows DDK-Dokumentation.
2.  Das Whitepaper "Audio Driver Support for Home Home Speaker Speaker Configurations" (Audiotreiberunterstützung für Home-Lautsprecher-Sprecherkonfigurationen) auf der Website [audio device technologies for Windows (Audiogerätetechnologien für](https://www.microsoft.com/whdc/device/audio/default.mspx) Windows Website).

Der **vt-Member** der **PROPVARIANT-Struktur** ist auf VT \_ UI4 festgelegt.

Der **uintVal-Member** der **PROPVARIANT-Struktur** enthält eine Kanalkonfigurationsmaske, die in den Typ **UINT umgeformt wird.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Audioendpunkteigenschaften**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




