---
title: DRM_PLAY_OPL Struktur (wmdrmsdk. h)
description: Die DRM- \_ Wiedergabe- \_ OPL-Struktur enthält Informationen zu den in einer Lizenz für Wiedergabe Aktionen angegebenen Ausgabe Schutz Ebenen (opls).
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- DRM_PLAY_OPL Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365424"
---
# <a name="drm_play_opl-structure"></a>DRM- \_ Wiedergabe- \_ OPL-Struktur

Die **DRM- \_ Wiedergabe- \_ OPL** -Struktur enthält Informationen zu den in einer Lizenz für Wiedergabe Aktionen angegebenen Ausgabe Schutz Ebenen (opls).

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**minopl**
</dt> <dd>

[**DRM \_ Minimale \_ Ausgabe \_ Schutz \_ Ebenen**](drmdrm-minimum-output-protection-levels.md) -Struktur, die die minimale OPL enthält, die für die Wiedergabe von Inhalten in verschiedenen Formaten erforderlich

</dd> <dt>

**oplidreserved**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**vopi**
</dt> <dd>

[**DRM \_ Die Video- \_ Ausgabe \_ Schutz- \_ IDs**](drmdrm-video-output-protection-ids.md) -Struktur, die die für die Wiedergabe des Inhalts geltenden Video-Ausgabe Schutz Bezeichner enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM- \_ Kopier- \_ OPL**](drmdrm-copy-opl.md)
</dt> <dt>

[**DRM \_ Play \_ OPL \_ Ex**](drm-play-opl-ex.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





