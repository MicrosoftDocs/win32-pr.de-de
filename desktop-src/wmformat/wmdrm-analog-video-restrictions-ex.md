---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX Struktur (wmdrmsdk. h)
description: Die WMDRM-unterschiedlichen \_ analogen \_ Video \_ Einschränkungen \_ in der Struktur enthalten erweiterte Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: 59c9ca5f58cf2adadeb5a6a0618457472cde976c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364650"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a>WMDRM \_ - \_ Einschränkungen für analoge Videos Ex- \_ \_ Struktur

Die **WMDRM-unterschiedlichen \_ analogen \_ Video \_ Einschränkungen \_** in der Struktur enthalten erweiterte Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.

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

**guidrestrictionid**
</dt> <dd>

Einschränkungs-ID.

</dd> <dt>

**cbrestrictiondata**
</dt> <dd>

Größe der Einschränkungs Daten in Bytes.

</dd> <dt>

**pbrestrictiondata**
</dt> <dd>

Einschränkungs Daten.

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

[**\_Einschränkungen für analoge \_ Videos \_ in WMDRM**](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





