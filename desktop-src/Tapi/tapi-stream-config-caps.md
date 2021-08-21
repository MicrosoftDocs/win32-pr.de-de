---
description: Die TAPI \_ STREAM \_ CONFIG \_ CAPS-Struktur enthält Konfigurationsinformationen zum Video- oder Audiostream.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: TAPI_STREAM_CONFIG_CAPS-Struktur (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbbb3b3ec72cc99810311cc510e36c2adc8242e2b3d98b321fd8bc8c6a9ab4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002648"
---
# <a name="tapi_stream_config_caps-structure"></a>TAPI \_ STREAM \_ CONFIG \_ CAPS-Struktur

\[Diese Struktur ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **TAPI \_ STREAM \_ CONFIG \_ CAPS-Struktur** enthält Konfigurationsinformationen zum Video- oder Audiostream.

## <a name="syntax"></a>Syntax


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Member

<dl> <dt>

**CapsType**
</dt> <dd>

Definiert, ob das Union-Element Video- oder Audioinformationen enthält.

</dd> <dt>

**VideoCap**
</dt> <dd>

Eine [**TAPI \_ VIDEO \_ \_ \_ STREAM-KONFIGURATIONS-CAPS-Struktur,**](tapi-video-stream-config-caps.md) die die Videostreamfunktionen enthält.

</dd> <dt>

**AudioCap**
</dt> <dd>

Eine [**\_ TAPI-AUDIOSTREAM-KONFIGURATIONS-CAPS-Struktur, \_ \_ \_**](tapi-audio-stream-config-caps.md) die die Audiostreamfunktionen enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITFormatControl::GetStreamCaps**](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[**StreamConfigCapsType**](streamconfigcapstype.md)
</dt> <dt>

[**TAPI \_ VIDEO \_ STREAM \_ CONFIG \_ CAPS**](tapi-video-stream-config-caps.md)
</dt> <dt>

[**TAPI \_ AUDIO \_ STREAM \_ CONFIG \_ CAPS**](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




