---
title: DRM_OUTPUT_PROTECTION Struktur (wmdrmsdk. h)
description: Die DRM- \_ Ausgabe \_ Schutz Struktur enthält Informationen zu einer Ausgabe Schutz Technologie.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- DRM_OUTPUT_PROTECTION Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371155"
---
# <a name="drm_output_protection-structure"></a>DRM- \_ Ausgabe \_ Schutz Struktur

Die **DRM- \_ Ausgabe \_ Schutz** Struktur enthält Informationen zu einer Ausgabe Schutz Technologie.

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**guidid darf**
</dt> <dd>

GUID, die die Ausgabe Schutz Technologie identifiziert.

</dd> <dt>

**bconfigdata**
</dt> <dd>

Konfigurationsdaten für die Technologie.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**DRM \_ Der \_ \_ audioausgabeschutz** und der **DRM- \_ Video \_ Ausgabe \_ Schutz** werden in **typedef** -Anweisungen als **DRM- \_ Ausgabe \_ Schutz** definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM- \_ Ausgabe \_ Schutz ( \_ Ex)**](drm-output-protection-ex.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





