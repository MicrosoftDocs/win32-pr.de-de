---
description: Die TAPI AUDIO STREAM CONFIG CAPS-Struktur ist in der TAPI STREAM CONFIG CAPS-Struktur enthalten, wenn das CapsType-Member auf das AudioCap-Member der \_ \_ \_ \_ \_ \_ \_ StreamConfigCapsType-Union festgelegt ist.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: TAPI_AUDIO_STREAM_CONFIG_CAPS -Struktur (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51fc4777e6d174f7d4aaeac9bbd3f6d467123275b4030c9fa21363223584e8b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861219"
---
# <a name="tapi_audio_stream_config_caps-structure"></a>TAPI \_ AUDIO \_ STREAM \_ CONFIG \_ CAPS structure

\[Diese Struktur ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **TAPI \_ AUDIO STREAM \_ \_ CONFIG \_ CAPS-Struktur** ist in der [**TAPI STREAM \_ \_ CONFIG \_ CAPS-Struktur**](tapi-stream-config-caps.md) enthalten, wenn das **CapsType-Member** auf das **AudioCap-Member** der [**StreamConfigCapsType-Union**](streamconfigcapstype.md) festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Member

<dl> <dt>

**Beschreibung**
</dt> <dd>

Eine benutzerfreundliche Beschreibung des Audiostream-Konfigurationstyps für die Anzeige für Anwendungsbenutzer.

</dd> <dt>

**MinimumChannels**
</dt> <dd>

Die Mindestanzahl von Kanälen, die dem Stream zugeordnet sind.

</dd> <dt>

**MaximumChannels**
</dt> <dd>

Die maximale Anzahl von Kanälen, die dem Stream zugeordnet sind.

</dd> <dt>

**ChannelsGranularity**
</dt> <dd>

Die Granularität der Kanalanzahl.

</dd> <dt>

**MinimumBitsPerSample**
</dt> <dd>

Die Mindestanzahl von Bits pro Stichprobe.

</dd> <dt>

**MaximumBitsPerSample**
</dt> <dd>

Die maximale Anzahl von Bits pro Stichprobe.

</dd> <dt>

**BitsPerSampleGranularity**
</dt> <dd>

Die Granularität der Bits pro Beispielwerten.

</dd> <dt>

**MinimumSampleFrequency**
</dt> <dd>

Die minimale Samplinghäufigkeit.

</dd> <dt>

**MaximumSampleFrequency**
</dt> <dd>

Die maximale Samplinghäufigkeit.

</dd> <dt>

**SampleFrequencyGranularity**
</dt> <dd>

Die Granularität der Samplinghäufigkeitswerte.

</dd> <dt>

**MinimumAvgBytesPerSec**
</dt> <dd>

Die durchschnittlichen Mindestbytes pro Sekunde.

</dd> <dt>

**MaximumAvgBytesPerSec**
</dt> <dd>

Die maximale durchschnittliche Anzahl von Bytes pro Sekunde.

</dd> <dt>

**AvgBytesPerSecGranularity**
</dt> <dd>

Die Granularität der Bytes pro Sekunde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TAPI \_ STREAM \_ CONFIG \_ CAPS**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




