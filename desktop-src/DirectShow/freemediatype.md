---
description: Die Funktion "fremediatype" löscht den Format Block in \_ einer \_ Medientyp-Struktur.
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Fremediatype-Funktion (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f332ccc9a60473a9d814481b759221dc6468d5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365586"
---
# <a name="freemediatype-function"></a>Fremediatype-Funktion

Die Funktion " **fremediatype** " löscht den Format Block in einer [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.

## <a name="syntax"></a>Syntax


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MT* \[ atur\]
</dt> <dd>

Ein Verweis auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Format Block wird dem Heap zugeordnet. Der **pbformat** -Member des [**am- \_ Medien \_ Typs**](/windows/win32/api/strmif/ns-strmif-am_media_type) verweist auf den Format Block. Verwenden Sie diese Funktion, um nur den Format Block freizugeben. Um eine zugeordnete **\_ \_ Medientyp** Struktur zu löschen, nennen Sie [**deletemediatype**](deletemediatype.md).

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
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Deletemediatype**](deletemediatype.md)
</dt> <dt>

[**Medientyp Funktionen**](media-type-functions.md)
</dt> </dl>

 

 




