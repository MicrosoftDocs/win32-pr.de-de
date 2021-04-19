---
title: WMDRM_OUTPUT_PROTECTION_LEVELS Struktur (wmdrmsdk. h)
description: Die Struktur der WMDRM- \_ Ausgabe \_ Schutz \_ Ebenen enthält die von einer Lizenz für die Durchführung verschiedener Aktionen benötigten Ausgabe Schutz Ebenen (Output Protection Levels, opls).
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- WMDRM_OUTPUT_PROTECTION_LEVELS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d720a8aef42178da188b71a1635d97031b138397
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358332"
---
# <a name="wmdrm_output_protection_levels-structure"></a>WMDRM- \_ Ausgabe \_ Schutz Ebenen- \_ Struktur

Die Struktur der **WMDRM- \_ Ausgabe \_ Schutz \_ Ebenen** enthält die von einer Lizenz für die Durchführung verschiedener Aktionen benötigten Ausgabe Schutz Ebenen (Output Protection Levels, opls).

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
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

</dd> <dt>

**wminimumcopyschutzlevel**
</dt> <dd>

Mindestens erforderliche OPL zum Kopieren des Inhalts.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird von der [**iwmdrmlicense:: getoutputschutzlevels**](iwmdrmlicense-getoutputprotectionlevels.md) -Methode verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





