---
description: Die Funktion "anatemediatype" weist eine neue am- \_ \_ Medientyp Struktur, einschließlich des Format Blocks, zu.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Funktion "deatemediatype" (mtype. h)
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
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369195"
---
# <a name="createmediatype-function"></a>Funktion "kreatemediatype"

Die Funktion " **anatemediatype** " weist eine neue [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, einschließlich des Format Blocks, zu.

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

Zeiger auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur. Die-Methode kopiert diese-Struktur in die neue-Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine neue [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur zurück, oder **null** , wenn ein Fehler vorliegt.

## <a name="remarks"></a>Bemerkungen

Um den von dieser Funktion belegten Arbeitsspeicher freizugeben, nennen Sie [**deletemediatype**](deletemediatype.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medientyp Funktionen**](media-type-functions.md)
</dt> </dl>

 

 




