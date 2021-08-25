---
title: DRM_OUTPUT_PROTECTION-Struktur (Wmdrmsdk.h)
description: Die DRM \_ OUTPUT \_ PROTECTION-Struktur enthält Informationen zu einer Ausgabeschutztechnologie.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- DRM_OUTPUT_PROTECTION Strukturfenster Medienformat
- Strukturfenster Medienformat
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
ms.openlocfilehash: 82454d8b4982e6546b003ae3977c7a98869d46ba393ea49f0b97773f95572777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881130"
---
# <a name="drm_output_protection-structure"></a>DRM \_ OUTPUT \_ PROTECTION-Struktur

Die **DRM \_ OUTPUT \_ PROTECTION-Struktur** enthält Informationen zu einer Ausgabeschutztechnologie.

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**guidId**
</dt> <dd>

GUID, die die Ausgabeschutztechnologie identifiziert.

</dd> <dt>

**bConfigData**
</dt> <dd>

Konfigurationsdaten für die Technologie.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**DRM \_ AUDIO \_ OUTPUT \_ PROTECTION** und **DRM VIDEO OUTPUT \_ \_ \_ PROTECTION** werden in **typedef-Anweisungen** als **DRM OUTPUT \_ \_ PROTECTION** definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM \_ OUTPUT \_ PROTECTION \_ EX**](drm-output-protection-ex.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





