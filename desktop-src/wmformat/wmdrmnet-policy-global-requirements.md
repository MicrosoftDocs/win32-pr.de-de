---
title: WMDRMNET_POLICY_GLOBAL_REQUIREMENTS Struktur (wmdrmsdk. h)
description: Die Struktur der globalen Anforderungen der wmdrmnet- \_ Richtlinie \_ \_ enthält globale Anforderungen für Windows Media DRM für Netzwerkgeräte.
ms.assetid: 140b3a6f-ccba-4735-b48a-2e990f5ec570
keywords:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ccf13c881c9696d970a00ac902f3f8d08f13c58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369582"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>\_ \_ Struktur der globalen \_ Anforderungen der wmdrmnet-Richtlinie

Die Struktur der **\_ \_ globalen \_ Anforderungen der wmdrmnet-Richtlinie** enthält globale Anforderungen für Windows Media DRM für Netzwerkgeräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRMNET_POLICY_GLOBAL_REQUIREMENTS {
  WMDRMNET_POLICY_MINIMUM_ENVIRONMENT MinimumEnvironment;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**Minimumenvironment**
</dt> <dd>

[**Wmdrmnet \_ \_Minimale \_ Umgebungs Struktur der Richtlinie**](wmdrmnet-policy-minimum-environment.md) , die die minimalen Sicherheitsanforderungen für Windows Media DRM für Netzwerkgeräte enthält.

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

 

 





