---
title: DRM_OUTPUT_PROTECTION_EX Struktur (wmdrmsdk. h)
description: Die DRM- \_ Ausgabe \_ Schutz-Ex- \_ Struktur enthält Informationen zu einer Ausgabe Schutz Technologie. Diese Struktur erweitert den DRM- \_ Ausgabe \_ Schutz durch Hinzufügen einer Versionsnummer.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- DRM_OUTPUT_PROTECTION_EX Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371758"
---
# <a name="drm_output_protection_ex-structure"></a>DRM- \_ Ausgabe \_ Schutz-Ex- \_ Struktur

Die **DRM- \_ Ausgabe \_ Schutz- \_ Ex** -Struktur enthält Informationen zu einer Ausgabe Schutz Technologie. Diese Struktur erweitert den **DRM- \_ Ausgabe \_ Schutz** durch Hinzufügen einer Versionsnummer.

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

**guidid darf**
</dt> <dd>

GUID, die die Ausgabe Schutz Technologie identifiziert.

</dd> <dt>

**dwconfigdata**
</dt> <dd>

Konfigurationsdaten für die Technologie.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**DRM \_ Der \_ audioausgabeschutz \_ \_ Ex** und der **DRM-Video-Ausgabe Schutz \_ \_ \_ \_ Ex** sind beide als **DRM- \_ Ausgabe \_ Schutz** in **typedef** -Anweisungen definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM- \_ Ausgabe \_ Schutz**](drm-output-protection.md)
</dt> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





