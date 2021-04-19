---
title: WMDRMNET_POLICY_TRANSCRYPTPLAY Struktur (wmdrmsdk. h)
description: Die transryptplay-Struktur der wmdrmnet- \_ Richtlinie \_ enthält die Richtlinien Informationen für die Wiedergabe von Inhalten mithilfe von Windows Media DRM für Netzwerkgeräte.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- WMDRMNET_POLICY_TRANSCRYPTPLAY Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357937"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>\_Transryptplay-Struktur der wmdrmnet-Richtlinie \_

Die **\_ \_ transryptplay-Struktur der wmdrmnet-Richtlinie** enthält die Richtlinien Informationen für die Wiedergabe von Inhalten mithilfe von Windows Media DRM für Netzwerkgeräte.

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

Globale Richtlinien Struktur.

</dd> <dt>

**playopls**
</dt> <dd>

Ausgabe Schutz Ebenen für die Wiedergabe. **Wmdrmnet \_ Die Richtlinien \_ Wiedergabe- \_ OPL** ist ein Typ, der als [**DRM \_ Play \_ OPL \_ Ex**](drm-play-opl-ex.md)definiert ist.

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

 

 





