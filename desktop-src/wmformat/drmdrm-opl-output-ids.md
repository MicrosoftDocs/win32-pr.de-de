---
title: DRM_OPL_OUTPUT_IDS -Struktur (Wmdrmsdk.h)
description: Die DRM OPL OUTPUT IDS-Struktur enthält eine Reihe von Ausgabebezeichnern für die \_ \_ \_ Ausgabeschutzebene (Output Protection Level, OPL).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- DRM_OPL_OUTPUT_IDS struktur windows media format
- Strukturfenster Medienformat
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
ms.openlocfilehash: 265e1015dd31281043d388debc802b390e7dd2d534f426ecbe24402efffd13df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658860"
---
# <a name="drm_opl_output_ids-structure"></a>DRM \_ \_ \_ OPL-Ausgabe-IDS-Struktur

Die **DRM \_ OPL \_ OUTPUT \_ IDS-Struktur** enthält eine Reihe von Ausgabebezeichnern für die Ausgabeschutzebene (Output Protection Level, OPL).

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**Cids**
</dt> <dd>

Anzahl der Bezeichner im Array, auf die von **rgIds verwiesen wird.**

</dd> <dt>

**rgIds**
</dt> <dd>

Adresse eines Arrays von GUIDs. Jedes Member des Arrays enthält einen OPL-Ausgabebezeichner.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird als Member der [**DRM \_ COPY \_ OPL-**](drmdrm-copy-opl.md) und [**DRM \_ PLAY \_ OPL-Strukturen**](drmdrm-play-opl.md) verwendet, um Gruppen von Ausgabebezeichnern zu identifizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





