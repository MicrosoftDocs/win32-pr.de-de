---
title: WMDRM_OUTPUT_PROTECTION_LEVELS -Struktur (Wmdrmsdk.h)
description: Die WMDRM OUTPUT PROTECTION LEVELS-Struktur enthält die Ausgabeschutzebenen \_ \_ (OUTPUT Protection Levels, OPLs), die für eine Lizenz zum Ausführen \_ verschiedener Aktionen erforderlich sind.
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- WMDRM_OUTPUT_PROTECTION_LEVELS struktur windows media format
- Strukturfenster Medienformat
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
ms.openlocfilehash: 4a19d7098266857f8a17e395ad749b216e45ce101278812f67c032943933955a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843961"
---
# <a name="wmdrm_output_protection_levels-structure"></a>WMDRM \_ OUTPUT \_ PROTECTION \_ LEVELS-Struktur

Die **WMDRM \_ OUTPUT PROTECTION \_ \_ LEVELS-Struktur** enthält die Ausgabeschutzebenen (OUTPUT Protection Levels, OPLs), die für eine Lizenz zum Ausführen verschiedener Aktionen erforderlich sind.

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

</dd> <dt>

**wMinimumCopyProtectionLevel**
</dt> <dd>

Mindestens erforderliche OPL zum Kopieren des Inhalts.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird von der [**IWMDRMLicense::GetOutputProtectionLevels-Methode**](iwmdrmlicense-getoutputprotectionlevels.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





