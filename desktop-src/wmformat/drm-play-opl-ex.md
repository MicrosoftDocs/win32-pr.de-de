---
title: DRM_PLAY_OPL_EX Struktur (wmdrmsdk. h)
description: Die DRM \_ Play \_ OPL \_ Ex-Struktur enthält Informationen zu den in einer Lizenz für Wiedergabe Aktionen angegebenen Ausgabe Schutz Ebenen (opls).
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- DRM_PLAY_OPL_EX Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: edf85ee664b33df9c63c390a870401b100327f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368469"
---
# <a name="drm_play_opl_ex-structure"></a>DRM \_ Play \_ OPL \_ Ex-Struktur

Die **DRM \_ Play \_ OPL \_ Ex** -Struktur enthält Informationen zu den in einer Lizenz für Wiedergabe Aktionen angegebenen Ausgabe Schutz Ebenen (opls).

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

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist mit der **DRM- \_ Wiedergabe- \_ OPL** -Struktur identisch, mit der Ausnahme, dass Sie eine Versionsnummer enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM- \_ Wiedergabe- \_ OPL**](drmdrm-play-opl.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





