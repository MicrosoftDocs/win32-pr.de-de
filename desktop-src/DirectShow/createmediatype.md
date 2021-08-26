---
description: Die CreateMediaType-Funktion ordnet eine neue AM \_ MEDIA \_ TYPE-Struktur zu, einschließlich des Formatblocks.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: CreateMediaType-Funktion (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0384b0a72e10b84cd94581816c0441de6a19fa5148a97fa9e55d72bdd63d678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871410"
---
# <a name="createmediatype-function"></a>CreateMediaType-Funktion

Die **CreateMediaType-Funktion** ordnet eine neue [**AM MEDIA \_ \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) zu, einschließlich des Formatblocks.

## <a name="syntax"></a>Syntax


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrc* 
</dt> <dd>

Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Die -Methode kopiert diese Struktur in die neue -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine neue [**AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) oder **NULL** zurück, wenn ein Fehler vorliegt.

## <a name="remarks"></a>Hinweise

Um den von dieser Funktion belegten Arbeitsspeicher freizugeben, rufen [**Sie DeleteMediaType auf.**](deletemediatype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Medientypfunktionen**](media-type-functions.md)
</dt> </dl>

 

 




