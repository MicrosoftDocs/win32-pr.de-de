---
title: WMDRMNET_POLICY_GLOBAL_REQUIREMENTS -Struktur (Wmdrmsdk.h)
description: Die WMDRMNET POLICY GLOBAL REQUIREMENTS-Struktur enthält globale Anforderungen für Windows \_ \_ \_ Medien-DRM für Netzwerkgeräte.
ms.assetid: 140b3a6f-ccba-4735-b48a-2e990f5ec570
keywords:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS struktur windows media format
- Strukturfenster Medienformat
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
ms.openlocfilehash: 4e2a8dc7be95638e171126eb4a55c50744ee3e5126d3e0b49eb8f229ec0257e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843971"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>WMDRMNET \_ POLICY \_ GLOBAL \_ REQUIREMENTS-Struktur

Die **WMDRMNET \_ POLICY GLOBAL \_ \_ REQUIREMENTS-Struktur** enthält globale Anforderungen für Windows Medien-DRM für Netzwerkgeräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRMNET_POLICY_GLOBAL_REQUIREMENTS {
  WMDRMNET_POLICY_MINIMUM_ENVIRONMENT MinimumEnvironment;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**MinimumEnvironment**
</dt> <dd>

[**WMDRMNET \_ POLICY \_ MINIMUM \_ ENVIRONMENT structure**](wmdrmnet-policy-minimum-environment.md) containing the minimum security requirements for Windows Media DRM for Network Devices.

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

[**WMDRMNET-RICHTLINIE \_**](wmdrmnet-policy.md)
</dt> </dl>

 

 





