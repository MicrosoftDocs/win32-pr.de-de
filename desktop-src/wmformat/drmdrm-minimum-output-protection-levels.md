---
title: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS -Struktur (Wmdrmsdk.h)
description: Die DRM MINIMUM OUTPUT PROTECTION LEVELS-Struktur enthält \_ \_ die \_ \_ mindesten Ausgabeschutzebenen (OUTPUT Protection Levels, OPLs) für die Wiedergabe verschiedener Inhaltstypen. Ein Gerät muss die Mindestanzahl von OPL unterstützen, damit ein Datentyp diese Art von Daten vom Reader empfangen kann.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS struktur windows media format
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5559527507f0399a09661dfe380f51d11e10750eddf7d996b38d110e4f38e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708920"
---
# <a name="drm_minimum_output_protection_levels-structure"></a>STRUKTUR DER \_ MINIMALEN \_ \_ DRM-AUSGABESCHUTZEBENEN \_

Die **DRM \_ MINIMUM OUTPUT \_ PROTECTION \_ \_ LEVELS-Struktur** enthält die mindesten Ausgabeschutzebenen (OUTPUT Protection Levels, OPLs) für die Wiedergabe verschiedener Inhaltstypen. Ein Gerät muss die Mindestanzahl von OPL unterstützen, damit ein Datentyp diese Art von Daten vom Reader empfangen kann.

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**wCompressedDigitalVideo**
</dt> <dd>

Mindestens erforderliche OPL zum Empfangen komprimierter digitaler Videos.

</dd> <dt>

**wUncompressedDigitalVideo**
</dt> <dd>

Mindestens erforderliche OPL für den Empfang nicht komprimierter digitaler Videos.

</dd> <dt>

**wAnalogVideo**
</dt> <dd>

Mindestens erforderliche OPL für den Empfang analoger Videos.

</dd> <dt>

**wCompressedDigitalAudio**
</dt> <dd>

Mindestens erforderliche OPL zum Empfangen komprimierter digitaler Audiodaten.

</dd> <dt>

**wUncompressedDigitalAudio**
</dt> <dd>

Mindestens erforderliche OPL für den Empfang unkomprimierten digitalen Audios.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird als Member der [**DRM \_ PLAY \_ OPL-Struktur**](drmdrm-play-opl.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





