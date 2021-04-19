---
title: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS Struktur (wmdrmsdk. h)
description: Die minimale DRM- \_ \_ Ausgabe \_ Schutz \_ Ebenen-Struktur enthält die minimalen Ausgabe Schutz Ebenen (opls) für die Wiedergabe verschiedener Inhaltstypen. Ein Gerät muss den minimalen OPL-Wert für einen Datentyp unterstützen, um diese Art von Daten vom Reader empfangen zu können.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: 060fdda4cd1c3cc665e396a72d46ac05e721abe4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353808"
---
# <a name="drm_minimum_output_protection_levels-structure"></a>DRM- \_ minimale \_ Ausgabe \_ Schutz Ebenen- \_ Struktur

Die **minimale DRM- \_ \_ Ausgabe \_ Schutz \_ Ebenen** -Struktur enthält die minimalen Ausgabe Schutz Ebenen (opls) für die Wiedergabe verschiedener Inhaltstypen. Ein Gerät muss den minimalen OPL-Wert für einen Datentyp unterstützen, um diese Art von Daten vom Reader empfangen zu können.

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

**wcompresseddigitalvideo**
</dt> <dd>

Mindestens erforderliche OPL für den Empfang komprimierter digitaler Videos.

</dd> <dt>

**wuncompresseddigitalvideo**
</dt> <dd>

Mindestens erforderliche OPL für den Empfang von unkomprimiertem digitalem Video.

</dd> <dt>

**wanalogvideo**
</dt> <dd>

Mindestens erforderliche OPL für den Empfang von analogen Videos.

</dd> <dt>

**wcompresseddigitalaudiodatei**
</dt> <dd>

Mindestens erforderliche OPL für den Empfang komprimierter digitaler Audiodaten.

</dd> <dt>

**wuncompresseddigitalaudiodatei**
</dt> <dd>

Mindestens erforderliche OPL zum Empfangen von unkomprimiertem digitaler Audiodaten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird als Mitglied der [**DRM-Wiedergabe- \_ \_ OPL**](drmdrm-play-opl.md) -Struktur verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





