---
description: Die Struktur der TAPI \_ -Stream-Konfigurations Ober \_ \_ Grenzen enthält entweder Video-oder audiodatenstream-Konfigurationsinformationen.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: TAPI_STREAM_CONFIG_CAPS Struktur (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379ca481d3bebaf8ceb11bfc2dbdab6642ca20b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357709"
---
# <a name="tapi_stream_config_caps-structure"></a>Struktur der TAPI- \_ \_ streamkonfigurationscaps \_

\[ Diese Struktur ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die Struktur der TAPI-Stream-Konfigurations Ober **\_ \_ \_ Grenzen** enthält entweder Video-oder audiodatenstream-Konfigurationsinformationen.

## <a name="syntax"></a>Syntax


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Member

<dl> <dt>

**Capstype**
</dt> <dd>

Definiert, ob das Unionmember Video-oder Audioinformationen enthält.

</dd> <dt>

**VideoCap**
</dt> <dd>

Eine [**TAPI \_ - \_ Dateistream- \_ config \_**](tapi-video-stream-config-caps.md) -Struktur, die die videostreamfunktionen enthält.

</dd> <dt>

**Audiocap**
</dt> <dd>

Eine [**TAPI \_ -Daten \_ Strom- \_ config \_ -**](tapi-audio-stream-config-caps.md) Struktur, die die audiostreamfunktionen enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itformatcontrol:: getstreamcaps**](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[**Streamconfigcapstype**](streamconfigcapstype.md)
</dt> <dt>

[**TAPI- \_ Video Daten \_ Strom- \_ Konfigurations \_ Caps**](tapi-video-stream-config-caps.md)
</dt> <dt>

[**TAPI \_ - \_ Audiodatenstrom- \_ Konfigurations \_ Caps**](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




