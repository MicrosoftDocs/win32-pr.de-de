---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX -Struktur (Wmdrmsdk.h)
description: Die WMDRM ANALOG VIDEO RESTRICTIONS EX-Struktur enthält erweiterte Informationen zu einer Einschränkung für die Wiedergabe von \_ \_ Inhalten als \_ \_ analoges Video.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX struktur windows media format
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9cbacff2d330c869c35eb7a3d1ca46ae6c80a030495ffec42eabc3726436c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006540"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a>WMDRM \_ ANALOG VIDEO RESTRICTIONS EX \_ \_ \_ structure

Die **WMDRM \_ ANALOG VIDEO RESTRICTIONS \_ \_ \_ EX-Struktur** enthält erweiterte Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**dwVersion**
</dt> <dd>

Versionsnummer:

</dd> <dt>

**guidRestrictionID**
</dt> <dd>

Einschränkungs-ID.

</dd> <dt>

**cbRestrictionData**
</dt> <dd>

Größe der Einschränkungsdaten in Bytes.

</dd> <dt>

**pbRestrictionData**
</dt> <dd>

Einschränkungsdaten.

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

[**WMDRM – \_ EINSCHRÄNKUNGEN FÜR \_ ANALOGE \_ VIDEOS**](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





