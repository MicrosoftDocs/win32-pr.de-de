---
description: Die deletemediatype-Funktion löscht eine zugeordnete am- \_ \_ Medientyp Struktur, einschließlich des Format Blocks.
ms.assetid: 970f6b2b-2bf5-418d-b4ae-637561cd6765
title: Deletemediatype-Funktion (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db0de399ab1be7808370a6d0da57c4c3ca7b8de1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369467"
---
# <a name="deletemediatype-function"></a>Deletemediatype-Funktion

Die **deletemediatype** -Funktion löscht eine zugeordnete [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, einschließlich des Format Blocks.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* 
</dt> <dd>

Ein Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Funktion, um eine beliebige Medientyp Struktur freizugeben, die entweder mithilfe von [**cotaskmemzugc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) oder mit dem Wert von " [**kreatemediatype**](createmediatype.md)

Diese Funktion ist in der [DirectShow-Basisklassen](directshow-base-classes.md) Bibliothek definiert. Wenn Sie keine Verknüpfung mit der Basisklassen Bibliothek herstellen möchten, können Sie den folgenden Code verwenden:


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}


// Delete a media type structure that was allocated on the heap.
void _DeleteMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt != NULL)
    {
        _FreeMediaType(*pmt); 
        CoTaskMemFree(pmt);
    }
}
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Freimediatype**](freemediatype.md)
</dt> <dt>

[**Medientyp Funktionen**](media-type-functions.md)
</dt> </dl>

 

