---
title: DRM_PLAY_OPL_EX-Struktur (Wmdrmsdk.h)
description: Die DRM \_ PLAY \_ OPL \_ EX-Struktur enthält Informationen zu den Ausgabeschutzebenen (Output Protection Levels, OPLs), die in einer Lizenz für Wiedergabeaktionen angegeben sind.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- DRM_PLAY_OPL_EX Strukturfenster Medienformat
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89ca0c6b1cf33a422265fb177e1b1432a52fbd12b3f9fda658125682f3888ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848439"
---
# <a name="drm_play_opl_ex-structure"></a>DRM \_ PLAY \_ OPL \_ EX-Struktur

Die **DRM \_ PLAY \_ OPL \_ EX-Struktur** enthält Informationen zu den Ausgabeschutzebenen (Output Protection Levels, OPLs), die in einer Lizenz für Wiedergabeaktionen angegeben sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**dwVersion**
</dt> <dd>

Versionsnummer:

</dd> <dt>

**minOPL**
</dt> <dd>

[**DRM \_ MINIMUM \_ OUTPUT \_ PROTECTION \_ LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.

</dd> <dt>

**oplIdReserved**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**vopi**
</dt> <dd>

[**DRM \_ VIDEO \_ OUTPUT \_ PROTECTION \_ IDS-Struktur,**](drmdrm-video-output-protection-ids.md) die die Videoausgabeschutz-IDs enthält, die für die Wiedergabe des Inhalts gelten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur ist mit der **DRM \_ PLAY \_ OPL-Struktur** identisch, mit der Ausnahme, dass sie eine Versionsnummer enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





