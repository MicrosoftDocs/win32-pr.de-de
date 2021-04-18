---
title: DRM_COPY_OPL Struktur (wmdrmsdk. h)
description: Die DRM- \_ Kopier- \_ OPL-Struktur enthält Informationen zu den in einer Lizenz für Kopieraktionen angegebenen Ausgabe Schutz Ebenen (opls).
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- DRM_COPY_OPL Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: d28655e220588bb704567de033e1117dd569d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372182"
---
# <a name="drm_copy_opl-structure"></a>DRM- \_ Kopier- \_ OPL-Struktur

Die **DRM- \_ Kopier- \_ OPL** -Struktur enthält Informationen zu den in einer Lizenz für Kopieraktionen angegebenen Ausgabe Schutz Ebenen (opls).

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

**wminimumcopylevel**
</dt> <dd>

Minimale OPL für Kopieraktionen.

</dd> <dt>

**oplidincludes**
</dt> <dd>

[**DRM \_ Struktur der OPL- \_ Ausgabe- \_ IDs**](drmdrm-opl-output-ids.md) , die die Bezeichner der zu Zulassungs enden Technologien enthält. Dieser Member wird für Ausgabe Technologien verwendet, denen opls zugewiesen sind, die niedriger als die mindestkopieebene sind, aber auf die der Inhalt kopiert werden kann.

</dd> <dt>

**oplidexcludes**
</dt> <dd>

[**DRM \_ Struktur der OPL- \_ Ausgabe- \_ IDs**](drmdrm-opl-output-ids.md) , die die Ausgabe Bezeichner der zu Beschränkungs enden Technologien enthält. Dieser Member wird für Ausgabe Technologien verwendet, denen opls zugewiesen sind, die die mindestkopieebene überschreiten, aber dass der Lizenz Aussteller keine Rechte zum Kopieren in erteilt.

</dd> </dl>

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

 

 





