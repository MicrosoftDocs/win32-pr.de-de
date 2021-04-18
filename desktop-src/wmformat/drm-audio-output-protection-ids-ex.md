---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX Struktur (wmdrmsdk. h)
description: Die- \_ IDs der DRM- \_ audioausgabeschutz- \_ \_ IDs \_ in der Struktur enthalten eine Liste von Schutz Bezeichnungen für den Diese Struktur erweitert DRM \_ - \_ audioausgabeschutz- \_ \_ IDs durch Hinzufügen einer Versionsnummer.
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354764"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a>DRM \_ - \_ audioausgabeschutz- \_ \_ IDs \_ Ex-Struktur

Die **- \_ IDs der DRM-audioausgabeschutz- \_ \_ \_ IDs \_** in der Struktur enthalten eine Liste von Schutz Bezeichnungen für den Diese Struktur erweitert **DRM \_ - \_ audioausgabeschutz- \_ \_ IDs** durch Hinzufügen einer Versionsnummer.

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
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

Anzahl der Einträge im **rgaop** -Array.

</dd> <dt>

**rgaop**
</dt> <dd>

Array von **DRM \_ - \_ audioausgabeschutz \_ \_ -und-** Strukturen. **DRM \_ Der \_ \_ \_ audioausgabeschutz** ist ein Typ, der als [**DRM- \_ Ausgabe \_ Schutz \_ Ex**](drm-output-protection-ex.md)definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

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

 

 





