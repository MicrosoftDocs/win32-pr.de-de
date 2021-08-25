---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS -Struktur (Wmdrmsdk.h)
description: Die WMDRM ANALOG VIDEO RESTRICTIONS-Struktur enthält Informationen zu einer Einschränkung für die Wiedergabe \_ \_ von Inhalten als \_ analoges Video.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS struktur windows media format
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8221fe325983387107f4e0c03f5672a6762502d8865e1d5895a9e48e96b99d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928810"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a>WMDRM \_ ANALOG \_ VIDEO \_ RESTRICTIONS-Struktur

Die **WMDRM \_ ANALOG VIDEO \_ \_ RESTRICTIONS-Struktur** enthält Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**guidRestrictionID**
</dt> <dd>

Einschränkungsbezeichner.

</dd> <dt>

**dwRestrictionData**
</dt> <dd>

Einschränkungsdaten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird empfangen, wenn Sie [**IWMDRMLicense::GetAnalogVideoRestrictionLevels aufrufen.**](iwmdrmlicense-getanalogvideorestrictionlevels.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> <dt>

[**WMDRM \_ – \_ ANALOGE \_ VIDEOEINSCHRÄNKUNGEN \_ EX**](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





