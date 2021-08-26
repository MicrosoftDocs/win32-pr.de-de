---
description: Die DeleteMediaType-Funktion löscht eine zugeordnete AM \_ MEDIA \_ TYPE-Struktur, einschließlich des Formatblocks.
ms.assetid: 970f6b2b-2bf5-418d-b4ae-637561cd6765
title: DeleteMediaType-Funktion (Mtype.h)
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
ms.openlocfilehash: 6035b65d6bf292f6ca35c4323ac5ad90c747b0cfd4bfa756b1f054d7b693d998
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998390"
---
# <a name="deletemediatype-function"></a>DeleteMediaType-Funktion

Die **DeleteMediaType-Funktion** löscht eine zugeordnete [**AM MEDIA \_ \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) einschließlich des Formatblocks.

## <a name="syntax"></a>Syntax


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pmt* 
</dt> <dd>

Ein Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Funktion, um jede Medientypstruktur freizugeben, die entweder mit [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) oder [**CreateMediaType**](createmediatype.md)zugeordnet wurde.

Diese Funktion ist in der [DirectShow-Basisklassenbibliothek](directshow-base-classes.md) definiert. Wenn Sie keine Verknüpfung mit der Basisklassenbibliothek verwenden möchten, können Sie den folgenden Code verwenden:


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
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FreeMediaType**](freemediatype.md)
</dt> <dt>

[**Medientypfunktionen**](media-type-functions.md)
</dt> </dl>

 

