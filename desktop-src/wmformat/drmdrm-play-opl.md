---
title: DRM_PLAY_OPL -Struktur (Wmdrmsdk.h)
description: Die DRM PLAY OPL-Struktur enthält Informationen zu den Ausgabeschutzebenen \_ \_ (OUTPUT Protection Levels, OPLs), die in einer Lizenz für Wiedergabeaktionen angegeben sind.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- DRM_PLAY_OPL struktur windows media format
- Strukturfenster Medienformat
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
ms.openlocfilehash: 3f649263db5435310d076386c49b2e77960552646e7ea2325190c3f0b94f27bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708310"
---
# <a name="drm_play_opl-structure"></a>DRM \_ PLAY \_ OPL-Struktur

Die **DRM \_ PLAY \_ OPL-Struktur** enthält Informationen zu den Ausgabeschutzebenen (OUTPUT Protection Levels, OPLs), die in einer Lizenz für Wiedergabeaktionen angegeben sind.

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

**minOPL**
</dt> <dd>

[**DRM \_ MINIMUM \_ OUTPUT \_ PROTECTION \_ LEVELS-Struktur,**](drmdrm-minimum-output-protection-levels.md) die die mindest erforderliche OPL enthält, um Inhalte in verschiedenen Formaten wieder zu spielen.

</dd> <dt>

**oplIdReserved**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**vopi**
</dt> <dd>

[**DRM \_ VIDEO \_ OUTPUT \_ PROTECTION \_ IDS-Struktur,**](drmdrm-video-output-protection-ids.md) die die Bezeichner für den Videoausgabeschutz enthält, die für die Wiedergabe des Inhalts gelten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM \_ COPY \_ OPL**](drmdrm-copy-opl.md)
</dt> <dt>

[**DRM \_ PLAY \_ OPL \_ EX**](drm-play-opl-ex.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





