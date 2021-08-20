---
description: Die PKEY \_ AudioEndpoint \_ FullRangeSpeakers-Eigenschaft gibt die Kanalkonfigurationsmaske für die Vollbereichslautierer an, die mit dem Audioendpunktgerät verbunden sind.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad27e5623189ce3ba78707377837493c1ea8dccb248d02ddd3d8e2c64570bed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406446"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a>PKEY \_ AudioEndpoint \_ FullRangeSpeakers

Die **PKEY \_ AudioEndpoint \_ FullRangeSpeakers-Eigenschaft** gibt die Kanalkonfigurationsmaske für die Vollbereichslautierer an, die mit dem Audioendpunktgerät verbunden sind. Die Maske gibt die physische Konfiguration der Vollbereichslautler an und gibt die Zuweisung von Kanälen zu diesen Sprechern an.

Der **vt-Member** der **PROPVARIANT-Struktur** ist auf VT \_ UI4 festgelegt.

Der **uintVal-Member** der **PROPVARIANT-Struktur** enthält eine Kanalkonfigurationsmaske, die in den Typ **UINT** umgeformt wird.

Ein Full-Range-Lautsprecher ist in der Lage, Sounds über den gesamten Bereich von Dern bis treble abzuspielen. In der Regel sind größere Lautsprecher im vollen Bereich, aber kleinere Lautsprecher sind deutlich weniger in der Lage, Sound zu spielen. In Windows Vista verwendet die Audio-Engine diese Eigenschaft, um die Ebenen des Audioausgabestreams zu verwalten, der vom Audioendpunktgerät wiedergegeben wird.

Die Kanalkonfigurationsmaske für diese Eigenschaft hat das gleiche Format wie die Kanalkonfigurationsmaske für die [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers-Eigenschaft.**](pkey-audioendpoint-physicalspeakers.md) Weitere Informationen zu Kanalkonfigurationsmasken finden Sie in den folgenden Themen:

-   Die Beschreibung der KSPROPERTY \_ AUDIO \_ CHANNEL \_ CONFIG-Eigenschaft in der Windows DDK-Dokumentation.
-   Das Whitepaper "Audio Driver Support for Home Speaker Configurations" (Audiotreiberunterstützung für Home-Lautsprecherkonfigurationen) auf der Website [audio device technologies for Windows (Audiogerätetechnologien für Windows).](https://www.microsoft.com/whdc/device/audio/default.mspx)

Das System ruft die Kanalkonfigurationsmaske für die Eigenschaft PKEY \_ AudioEndpoint \_ FullRangeSpeakers vom Benutzer ab. Der Benutzer gibt diese Informationen über die Windows Multimedia-Systemsteuerung Mmsys.cpl ein. Weitere Informationen zu Mmsys.cpl finden Sie in der Windows DDK-Dokumentation.

Die Kanalkonfigurationsmaske für die PKEY \_ AudioEndpoint \_ FullRangeSpeakers-Eigenschaft eines Audioendpunktgeräts ist eine Teilmenge der Kanalkonfigurationsmaske für die PKEY \_ AudioEndpoint \_ PhysicalSpeakers-Eigenschaft desselben Geräts.

Wenn beispielsweise ein Audioendpunktgerät einen Satz von 5.1 Surround-Sound-Lautsprechern steuert, ist die Kanalkonfigurationsmaske für die PKEY \_ AudioEndpoint \_ PhysicalSpeakers-Eigenschaft KSAUDIO \_ SPEAKER \_ 5POINT1. Diese Maske gibt das Vorhandensein von Front-Left-, Front-Right-, Front-Center-, Side-Left- und Side-Right-Lautsprechern sowie einem Subwoofer an. Wenn der vordere linke und der vordere rechte Lautsprecher groß genug sind, um Laute zu erzeugen, aber die kleinere Front-Center- und Seitenlautsprechfunktion nicht, dann ist die Kanalkonfigurationsmaske für die PKEY \_ AudioEndpoint \_ FullRangeSpeakers-Eigenschaft KSAUDIO \_ SPEAKER \_ STEREO, die nur die Front-Left- und Front-Right-Lautsprecher angibt. Die Kanalkonfigurationsmasken KSAUDIO \_ SPEAKER \_ 5POINT1 und KSAUDIO \_ SPEAKER STEREO werden in der \_ Headerdatei Ksmedia.h definiert.

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
</dt> <dt>

[**PKEY \_ AudioEndpoint \_ PhysicalSpeakers-Eigenschaft**](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




