---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS Struktur (wmdrmsdk. h)
description: Die Struktur der analogen WMDRM- \_ \_ Video \_ Einschränkungen enthält Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: e3d6b8fe957468baebb6da06f45ba7b37756413c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358334"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a>WMDRM \_ - \_ Struktur für analoge Video \_ Einschränkungen

Die Struktur der **analogen WMDRM- \_ \_ Video \_ Einschränkungen** enthält Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**guidrestrictionid**
</dt> <dd>

Einschränkungs Bezeichner.

</dd> <dt>

**dwrestrictiondata**
</dt> <dd>

Einschränkungs Daten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird empfangen, wenn Sie [**iwmdrmlicense:: getanalogvideorestrictionlevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md)aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> <dt>

[**Einschränkungen für Analog zum WMDRM- \_ \_ Video \_ \_**](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





