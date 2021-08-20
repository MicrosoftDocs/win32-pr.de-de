---
title: DRM_OUTPUT_PROTECTION_EX-Struktur (Wmdrmsdk.h)
description: Die DRM \_ OUTPUT \_ PROTECTION \_ EX-Struktur enthält Informationen zu einer Ausgabeschutztechnologie. Diese Struktur erweitert DRM \_ OUTPUT PROTECTION durch Hinzufügen einer \_ Versionsnummer.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- DRM_OUTPUT_PROTECTION_EX Strukturfenster Medienformat
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac3033482dc84ad8a25e2e18c359cd621228fef37cc97673f9a5eeae9a57b1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029584"
---
# <a name="drm_output_protection_ex-structure"></a>DRM \_ OUTPUT \_ PROTECTION \_ EX-Struktur

Die **DRM \_ OUTPUT PROTECTION \_ \_ EX-Struktur** enthält Informationen zu einer Ausgabeschutztechnologie. Diese Struktur erweitert **DRM \_ OUTPUT \_ PROTECTION** durch Hinzufügen einer Versionsnummer.

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**dwVersion**
</dt> <dd>

Versionsnummer:

</dd> <dt>

**guidId**
</dt> <dd>

GUID, die die Ausgabeschutztechnologie identifiziert.

</dd> <dt>

**dwConfigData**
</dt> <dd>

Konfigurationsdaten für die Technologie.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**DRM \_ AUDIO \_ OUTPUT \_ PROTECTION \_ EX** und **DRM VIDEO OUTPUT PROTECTION \_ \_ \_ \_ EX** sind beide in **typedef-Anweisungen** als **DRM OUTPUT \_ \_ PROTECTION** definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_DRM-AUSGABESCHUTZ \_**](drm-output-protection.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





