---
title: DRM_COPY_OPL-Struktur (Wmdrmsdk.h)
description: Die DRM \_ COPY \_ OPL-Struktur enthält Informationen zu den Ausgabeschutzebenen (Output Protection Levels, OPLs), die in einer Lizenz für Kopieraktionen angegeben sind.
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- DRM_COPY_OPL Strukturfenster Medienformat
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ec6e376b2df4cd3e5462766d6fd992ed7d2356a1bc81d0ff74c662a99697af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708980"
---
# <a name="drm_copy_opl-structure"></a>DRM \_ COPY \_ OPL-Struktur

Die **DRM \_ COPY \_ OPL-Struktur** enthält Informationen zu den Ausgabeschutzebenen (Output Protection Levels, OPLs), die in einer Lizenz für Kopieraktionen angegeben sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**wMinimumCopyLevel**
</dt> <dd>

Minimale OPL für Kopieraktionen.

</dd> <dt>

**oplIdIncludes**
</dt> <dd>

[**DRM \_ OPL \_ OUTPUT \_ IDS-Struktur,**](drmdrm-opl-output-ids.md) die die Bezeichner der zuzulassenden Technologien enthält. Dieser Member wird für Ausgabetechnologien verwendet, denen OPLs zugewiesen werden, die niedriger als die minimale Kopierebene sind, aber in die der Inhalt kopiert werden kann.

</dd> <dt>

**oplIdExcludes**
</dt> <dd>

[**DRM \_ OPL \_ OUTPUT \_ IDS-Struktur,**](drmdrm-opl-output-ids.md) die die Ausgabebezeichner der einzuschränkenden Technologien enthält. Dieses Element wird für Ausgabetechnologien verwendet, denen OPLs zugewiesen sind, die den Mindestkopiergrad überschreiten, der Lizenzaussteller jedoch keine Rechte zum Kopieren in gewährt.

</dd> </dl>

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

 

 





