---
title: WMDRMNET_POLICY_TRANSCRYPTPLAY -Struktur (Wmdrmsdk.h)
description: Die WMDRMNET POLICY TRANSCRYPTPLAY-Struktur enthält die Richtlinieninformationen für die Wiedergabe von Inhalten mithilfe Windows \_ \_ Media DRM für Netzwerkgeräte.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- WMDRMNET_POLICY_TRANSCRYPTPLAY struktur windows media format
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fe64c796a1f2f15e4733e7dd3d82e918306fb95d78c61fb85ad2d813d946d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195505"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY-Struktur

Die **WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY-Struktur** enthält die Richtlinieninformationen für die Wiedergabe von Inhalten mithilfe Windows Media DRM für Netzwerkgeräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**Globals**
</dt> <dd>

Globale Richtlinienstruktur.

</dd> <dt>

**playOPLs**
</dt> <dd>

Ausgabeschutzebenen für die Wiedergabe. **WMDRMNET \_ POLICY \_ PLAY \_ OPL ist** ein Typ, der als [**DRM PLAY \_ \_ OPL EX definiert \_ ist.**](drm-play-opl-ex.md)

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

 

 





