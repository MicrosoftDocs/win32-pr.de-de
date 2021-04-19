---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS Struktur (wmdrmsdk. h)
description: Die Struktur der DRM \_ -audioausgabeschutz- \_ \_ \_ IDs enthält eine Liste der audioausgabeschutzbezeichner.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366876"
---
# <a name="drm_audio_output_protection_ids-structure"></a>Struktur der DRM \_ -audioausgabeschutzids \_ \_ \_

Die Struktur der **DRM \_ -audioausgabeschutz- \_ \_ \_ IDs** enthält eine Liste der audioausgabeschutzbezeichner.

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**centries**
</dt> <dd>

Anzahl der Einträge im **rgaop** -Array.

</dd> <dt>

**rgaop**
</dt> <dd>

Array von **DRM \_ - \_ audioausgabeschutzstrukturen \_** . **DRM \_ Der \_ audioausgabeschutz \_** ist ein Typ, der als [**DRM- \_ Ausgabe \_ Schutz**](drm-output-protection.md)definiert ist

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM \_ - \_ audioausgabeschutz- \_ \_ IDs \_ Ex**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





