---
description: Die Struktur der TAPI-Video Datenstrom-Konfigurations Obergrenze \_ \_ \_ \_ ist in der Struktur der TAPI- \_ Stream-Konfigurations Obergrenze enthalten \_ \_ , wenn der capstype-Member auf den VideoCap-Member der streamconfigcapstype-Union festgelegt ist
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: TAPI_VIDEO_STREAM_CONFIG_CAPS Struktur (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365607"
---
# <a name="tapi_video_stream_config_caps-structure"></a>Struktur des TAPI- \_ Video Daten \_ Strom- \_ Konfigurations \_ Caps

\[ Diese Struktur ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die Struktur der **TAPI- \_ Video Datenstrom- \_ \_ Konfigurations \_** Obergrenze ist in der Struktur der [**TAPI-Stream- \_ \_ Konfigurations \_**](tapi-stream-config-caps.md) Obergrenze enthalten, wenn der **capstype** -Member auf den **VideoCap** -Member der [**streamconfigcapstype**](streamconfigcapstype.md) -Union festgelegt ist

## <a name="syntax"></a>Syntax


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Member

<dl> <dt>

**Beschreibung**
</dt> <dd>

Eine benutzerfreundliche Beschreibung des audiostreamkonfigurationstyp für die Anzeige für Anwendungs Benutzer.

</dd> <dt>

**Videostandard**
</dt> <dd>

Der verwendete Video Standard.

</dd> <dt>

**Input size**
</dt> <dd>

Eingabe Größe von Frame.

</dd> <dt>

**Mincroppingsize**
</dt> <dd>

Mindestgröße für das Zuschneiden.

</dd> <dt>

**Maxcroppingsize**
</dt> <dd>

Maximale zuschneidungs Größe.

</dd> <dt>

**Cropgranularityx**
</dt> <dd>

Die Granularität für das Zuschneiden auf der x-Achse.

</dd> <dt>

**Cropgranularityy**
</dt> <dd>

Die Granularität für das Zuschneiden auf der y-Achse.

</dd> <dt>

**Cropalignx**
</dt> <dd>

Ausrichtung von Zuschneiden der x-Achse.

</dd> <dt>

**Cropaligny**
</dt> <dd>

Ausrichtung von y-Achsen zuschneiden.

</dd> <dt>

**Minoutputsize**
</dt> <dd>

Mindestens resultierende Größe des Videofensters.

</dd> <dt>

**Maxoutputsize**
</dt> <dd>

Maximale resultierende Größe des Videofensters.

</dd> <dt>

**Outputgranularityx**
</dt> <dd>

Die Granularität der Ausgabegröße entlang der x-Achse.

</dd> <dt>

**Outputgranularityy**
</dt> <dd>

Die Granularität der Ausgabegröße entlang der y-Achse.

</dd> <dt>

**Stretchtapsx**
</dt> <dd>

Streckung entlang der x-Achse.

</dd> <dt>

**Stretchtapsy**
</dt> <dd>

Streckung entlang der y-Achse.

</dd> <dt>

**Shrinktapsx**
</dt> <dd>

Verkleinern entlang der x-Achse.

</dd> <dt>

**Shrinktapsy**
</dt> <dd>

Verkleinern entlang der y-Achse.

</dd> <dt>

**Minframeinterval**
</dt> <dd>

Minimaler Video Frame Intervall.

</dd> <dt>

**Maxframeinterval**
</dt> <dd>

Maximales Video Frame Intervall.

</dd> <dt>

**Minbitspersecond**
</dt> <dd>

Minimale Bits pro Sekunde.

</dd> <dt>

**Maxbitspersecond**
</dt> <dd>

Maximale Anzahl von Bits pro Sekunde.

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

 

 




