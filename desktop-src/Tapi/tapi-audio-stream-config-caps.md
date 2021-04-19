---
description: Die Struktur der TAPI \_ - \_ \_ audiostreamkonfigurationscaps \_ ist in der TAPI-Struktur der Daten \_ Strom \_ Konfiguration enthalten \_ , wenn das capstype-Element auf den audiocap-Member der streamconfigcapstype-Union festgelegt ist.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: TAPI_AUDIO_STREAM_CONFIG_CAPS Struktur (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354146"
---
# <a name="tapi_audio_stream_config_caps-structure"></a>Struktur der TAPI \_ - \_ Audiostream- \_ Konfigurations Ober \_ Grenzen

\[ Diese Struktur ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die Struktur der **TAPI \_ - \_ \_ audiostreamkonfigurationscaps \_** ist in der TAPI-Struktur der Daten [**\_ Strom \_ Konfiguration \_**](tapi-stream-config-caps.md) enthalten, wenn das **capstype** -Element auf den **audiocap** -Member der [**streamconfigcapstype**](streamconfigcapstype.md) -Union festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Member

<dl> <dt>

**Beschreibung**
</dt> <dd>

Eine benutzerfreundliche Beschreibung des audiostreamkonfigurationstyp für die Anzeige für Anwendungs Benutzer.

</dd> <dt>

**Minimumchannels**
</dt> <dd>

Die Mindestanzahl von Kanälen, die dem Stream zugeordnet sind.

</dd> <dt>

**Maximumchannels**
</dt> <dd>

Die maximale Anzahl von Kanälen, die dem Stream zugeordnet sind.

</dd> <dt>

**Channelsgranularität**
</dt> <dd>

Die Granularität der Kanalanzahl.

</dd> <dt>

**Minimumbitspersample**
</dt> <dd>

Die minimale Anzahl von Bits pro Stichprobe.

</dd> <dt>

**Maximumbitspersample**
</dt> <dd>

Die maximale Anzahl von Bits pro Stichprobe.

</dd> <dt>

**Bitspersamplegranularität**
</dt> <dd>

Die Granularität der Bits pro Stichproben Werten.

</dd> <dt>

**Minimumsamplefrequency**
</dt> <dd>

Die minimale Stichproben Häufigkeit.

</dd> <dt>

**Maximumsamplefrequency**
</dt> <dd>

Die maximale Stichproben Häufigkeit.

</dd> <dt>

**Samplefrequkocygranularität**
</dt> <dd>

Die Granularität der Werte für die Stichproben Häufigkeit.

</dd> <dt>

**Minimumavgbytespersec**
</dt> <dd>

Die minimalen durchschnittlichen Bytes pro Sekunde.

</dd> <dt>

**Maximumavgbytespersec**
</dt> <dd>

Die maximale durchschnittliche Anzahl von Bytes pro Sekunde.

</dd> <dt>

**Avgbytespersecgranularität**
</dt> <dd>

Die Granularität der Bytes pro Sekunde-Werte.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TAPI \_ - \_ streamkonfigurationscaps \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




