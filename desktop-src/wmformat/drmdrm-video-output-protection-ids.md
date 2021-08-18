---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS -Struktur (Wmdrmsdk.h)
description: Die DRM \_ VIDEO \_ OUTPUT PROTECTION \_ \_ IDS-Struktur enthält ein Array von DRM \_ VIDEO OUTPUT \_ \_ PROTECTION-Strukturen.
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS struktur windows media format
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9439328ed817da40630c3a600cf7e6db553738a12799babbe9e71c48f28923b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119085872"
---
# <a name="drm_video_output_protection_ids-structure"></a>\_IDS-Struktur des DRM-VIDEOAUSGABESCHUTZES \_ \_ \_

Die **DRM \_ VIDEO OUTPUT PROTECTION \_ \_ \_ IDS-Struktur** enthält ein Array von **DRM VIDEO OUTPUT \_ \_ \_ PROTECTION-Strukturen.**

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**cEntries**
</dt> <dd>

Anzahl der Elemente im Array, auf die von **rgVop verwiesen wird.**

</dd> <dt>

**rgVop**
</dt> <dd>

Adresse eines Arrays von **DRM \_ VIDEO OUTPUT \_ \_ PROTECTION-Strukturen.** **DRM \_ VIDEO \_ OUTPUT \_ PROTECTION ist** ein Typ, der als [**DRM OUTPUT PROTECTION definiert \_ \_ ist.**](drm-output-protection.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird als Member der [**DRM \_ PLAY \_ OPL-Struktur**](drmdrm-play-opl.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_ \_ \_ DRM-AUDIOAUSGABESCHUTZ-IDS \_**](drm-audio-output-protection-ids.md)
</dt> <dt>

[**DRM \_ VIDEO \_ OUTPUT \_ PROTECTION \_ IDS \_ EX**](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





