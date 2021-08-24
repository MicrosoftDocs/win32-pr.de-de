---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS -Struktur (Wmdrmsdk.h)
description: Die IDS-Struktur von DRM \_ AUDIO OUTPUT PROTECTION enthält eine Liste mit \_ \_ \_ Audioausgabeschutzbezeichnern.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS struktur windows media format
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e31589a229dcd5e32a0198cf7f3679846574bdb605e25a8df272b1793704b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659010"
---
# <a name="drm_audio_output_protection_ids-structure"></a>\_IDS-Struktur des DRM-AUDIOAUSGABESCHUTZES \_ \_ \_

Die **\_ \_ \_ \_ IDS-Struktur von DRM AUDIO OUTPUT PROTECTION** enthält eine Liste mit Audioausgabeschutzbezeichnern.

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**cEntries**
</dt> <dd>

Anzahl der Einträge im **rgAop-Array.**

</dd> <dt>

**rgAop**
</dt> <dd>

Array von **DRM \_ AUDIO OUTPUT \_ \_ PROTECTION-Strukturen.** **DRM \_ AUDIO \_ OUTPUT \_ PROTECTION ist** ein Typ, der als [**DRM OUTPUT PROTECTION definiert \_ \_ ist.**](drm-output-protection.md)

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM \_ AUDIO \_ OUTPUT \_ PROTECTION \_ IDS \_ EX**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**\_ \_ \_ DRM-VIDEOAUSGABESCHUTZ-IDS \_**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





