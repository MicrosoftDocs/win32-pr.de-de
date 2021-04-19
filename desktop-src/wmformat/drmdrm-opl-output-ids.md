---
title: DRM_OPL_OUTPUT_IDS Struktur (wmdrmsdk. h)
description: Die Struktur der DRM- \_ OPL- \_ Ausgabe- \_ IDs enthält eine Reihe von OPL-Ausgabe bezeichlern (Output Protection Level).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- DRM_OPL_OUTPUT_IDS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365532"
---
# <a name="drm_opl_output_ids-structure"></a>Struktur der DRM- \_ OPL- \_ Ausgabe- \_ IDs

Die Struktur der **DRM- \_ OPL- \_ Ausgabe- \_ IDs** enthält eine Reihe von OPL-Ausgabe bezeichlern (Output Protection Level).

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**cIds**
</dt> <dd>

Anzahl der Bezeichner in dem Array, auf das von **rgids** verwiesen wird.

</dd> <dt>

**rgids**
</dt> <dd>

Adresse eines Arrays von GUIDs. Jeder Member des Arrays enthält einen OPL-Ausgabe Bezeichner.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird als Mitglied der [**DRM-Kopier- \_ \_ OPL**](drmdrm-copy-opl.md) -und [**DRM \_ Play \_ OPL**](drmdrm-play-opl.md) -Strukturen verwendet, um Gruppen von Ausgabe bezeichatoren zu identifizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





