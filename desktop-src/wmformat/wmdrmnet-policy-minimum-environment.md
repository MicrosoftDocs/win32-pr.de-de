---
title: WMDRMNET_POLICY_MINIMUM_ENVIRONMENT-Struktur (Wmdrmsdk.h)
description: Die WMDRMNET \_ POLICY \_ MINIMUM \_ ENVIRONMENT-Struktur enthält die Mindestsicherheitsanforderungen für Windows Medien-DRM für Netzwerkgeräte.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT Strukturfenster Medienformat
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c11cf02d7cfcd2e3ab62c4e6b110e2c20b77cf6f79251a23f642b38d4df553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027461"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a>WMDRMNET POLICY MINIMUM ENVIRONMENT structure (WMDRMNET \_ POLICY \_ MINIMUM \_ ENVIRONMENT-Struktur)

Die **WMDRMNET \_ POLICY MINIMUM \_ \_ ENVIRONMENT-Struktur** enthält die Mindestsicherheitsanforderungen für Windows Medien-DRM für Netzwerkgeräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**wMinimumSecurityLevel**
</dt> <dd>

Mindestens erforderliche Anwendungssicherheitsstufe.

</dd> <dt>

**dwMinimumAppRevocationListVersion**
</dt> <dd>

Mindestens erforderliche Version der Anwendungszertifikatsperrliste.

</dd> <dt>

**dwMinimumDeviceRevocationListVersion**
</dt> <dd>

Mindestens erforderliche Sperrliste für Gerätezertifikate.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> <dt>

[**\_WMDRMNET-RICHTLINIE**](wmdrmnet-policy.md)
</dt> </dl>

 

 





