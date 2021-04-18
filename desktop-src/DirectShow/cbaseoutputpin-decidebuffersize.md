---
description: Die decidebuffersize-Methode legt die Puffer Anforderungen fest.
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: Cbaseoutputpin. decidebuffersize-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dcb3328b56a7e203575a3abbaab64cda6a9b87f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352094"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a>Cbaseoutputpin. decidebuffersize-Methode

Die- `DecideBufferSize` Methode legt die Puffer Anforderungen fest.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*palloc* 
</dt> <dd>

Ein Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners.

</dd> <dt>

*ppropinputrequest* 
</dt> <dd>

Ein Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die Puffer Anforderungen der Eingabe-PIN enthält. Wenn die Eingabe-PIN keine Anforderungen hat, sollte der Aufrufer die Elemente dieser Struktur vor dem Aufrufen der-Methode 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Überschreiben Sie diese Methode in der abgeleiteten Klasse. Aufrufen der [**imemzuzucator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) -Methode, um die Puffer Anforderungen anzugeben. In der Regel berücksichtigt die abgeleitete Klasse die Puffer Anforderungen der Eingabe-PIN, Sie ist jedoch nicht erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




