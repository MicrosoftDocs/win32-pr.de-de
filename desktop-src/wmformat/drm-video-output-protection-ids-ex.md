---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX Struktur (wmdrmsdk. h)
description: Die DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs in der Struktur enthalten \_ ein Array von DRM- \_ Video- \_ Ausgabe \_ Schutzstrukturen.
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350751"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a>DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs Ex- \_ Struktur

Die **DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs \_** in der Struktur enthalten ein Array von **DRM-Video- \_ \_ Ausgabe \_ Schutz** Strukturen.

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**dwVersion**
</dt> <dd>

Versionsnummer:

</dd> <dt>

**centries**
</dt> <dd>

Anzahl der Elemente in dem Array, auf das von **rgvop** verwiesen wird.

</dd> <dt>

**rgvop**
</dt> <dd>

Adresse eines Arrays von **DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ Ex** -Strukturen. **DRM \_ Der Video- \_ Ausgabe \_ Schutz \_ Ex** ist ein Typ, der als [**DRM- \_ Ausgabe \_ Schutz \_ Ex**](drm-output-protection-ex.md)definiert ist.

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

 

 





