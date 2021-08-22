---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX-Struktur (Wmdrmsdk.h)
description: Die DRM \_ VIDEO \_ OUTPUT PROTECTION \_ \_ IDS \_ EX-Struktur enthält ein Array von DRM \_ VIDEO OUTPUT \_ \_ PROTECTION-Strukturen.
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX Strukturfenster Medienformat
- Strukturfenster Medienformat
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
ms.openlocfilehash: f5482734c2ded470b4e3dc885e32505c556b3106a12518969622f8007cf6e4f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704087"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a>DRM \_ VIDEO OUTPUT PROTECTION \_ \_ \_ IDS \_ EX-Struktur

Die **DRM \_ VIDEO OUTPUT PROTECTION \_ \_ \_ IDS \_ EX-Struktur** enthält ein Array von **DRM VIDEO OUTPUT \_ \_ \_ PROTECTION-Strukturen.**

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

**c-Einträge**
</dt> <dd>

Anzahl der Elemente im Array, auf das **von rgVop** verwiesen wird.

</dd> <dt>

**rgVop**
</dt> <dd>

Adresse eines Arrays von **DRM \_ VIDEO OUTPUT \_ PROTECTION \_ \_ EX-Strukturen.** **DRM \_ VIDEO \_ OUTPUT \_ PROTECTION \_ EX** ist ein Typ, der als [**DRM OUTPUT PROTECTION \_ \_ \_ EX**](drm-output-protection-ex.md)definiert ist.

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

[**\_ \_ \_ SCHUTZ-IDS FÜR DRM-VIDEOAUSGABE \_**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





