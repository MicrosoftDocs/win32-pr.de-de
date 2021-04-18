---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS Struktur (wmdrmsdk. h)
description: Die Struktur der DRM- \_ Video- \_ Ausgabe \_ Schutz- \_ IDs enthält ein Array von DRM- \_ Video- \_ Ausgabe \_ Schutzstrukturen.
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: 51af3ccebec52ab6f6863aeb376ed27f8c8e2467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364423"
---
# <a name="drm_video_output_protection_ids-structure"></a>Struktur der DRM- \_ Video- \_ Ausgabe \_ Schutz- \_ IDs

Die Struktur der **DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs** enthält ein Array von **DRM-Video- \_ \_ Ausgabe \_ Schutz** Strukturen.

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**centries**
</dt> <dd>

Anzahl der Elemente in dem Array, auf das von **rgvop** verwiesen wird.

</dd> <dt>

**rgvop**
</dt> <dd>

Die Adresse eines Arrays von **DRM- \_ Video- \_ ausgabeschutzstrukturen \_** . **DRM \_ Der Video \_ Ausgabe \_ Schutz** ist ein Typ, der als [**DRM- \_ Ausgabe \_ Schutz**](drm-output-protection.md)definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird als Mitglied der [**DRM-Wiedergabe- \_ \_ OPL**](drmdrm-play-opl.md) -Struktur verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM \_ - \_ Audioausgabe- \_ Schutz- \_ IDs**](drm-audio-output-protection-ids.md)
</dt> <dt>

[**DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs \_ Ex**](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





