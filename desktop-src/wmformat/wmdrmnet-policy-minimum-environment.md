---
title: WMDRMNET_POLICY_MINIMUM_ENVIRONMENT Struktur (wmdrmsdk. h)
description: Die minimale Umgebungs Struktur der wmdrmnet- \_ Richtlinie \_ \_ enthält die minimalen Sicherheitsanforderungen für Windows Media DRM für Netzwerkgeräte.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: 4bf53fdec186a44eff375dd2e9cf9badfe0ba715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368663"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a>\_ \_ Minimale \_ Umgebungs Struktur der wmdrmnet-Richtlinie

Die **\_ \_ minimale \_ Umgebungs Struktur der wmdrmnet-Richtlinie** enthält die minimalen Sicherheitsanforderungen für Windows Media DRM für Netzwerkgeräte.

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

**wminimumsecuritylevel**
</dt> <dd>

Mindestens erforderliche Anwendungs Sicherheitsstufe.

</dd> <dt>

**dwminimumapprevocationlistversion**
</dt> <dd>

Mindestens erforderliche Version für die Sperr Liste für das Anwendungs Zertifikat.

</dd> <dt>

**dwminimumdevicerevocationlistversion**
</dt> <dd>

Mindestens erforderliche Sperr Liste für das Gerätezertifikat.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> <dt>

[**wmdrmnet- \_ Richtlinie**](wmdrmnet-policy.md)
</dt> </dl>

 

 





