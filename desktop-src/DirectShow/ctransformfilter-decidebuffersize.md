---
description: 'CTransformFilter.DecideBufferSize-Methode: Die DecideBufferSize-Methode legt die Pufferanforderungen des Ausgabepins fest.'
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: CTransformFilter.DecideBufferSize-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1aba3ec43318079a73f0c94c8446b637ece29a5b61752462eeb8fc5898f5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907700"
---
# <a name="ctransformfilterdecidebuffersize-method"></a>CTransformFilter.DecideBufferSize-Methode

Die `DecideBufferSize` -Methode legt die Pufferanforderungen des Ausgabepins fest.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAlloc* 
</dt> <dd>

Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) auf der Zuweisung des Ausgabepins.

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Zeiger auf eine [**ALLOCATOR \_ PROPERTIES-Struktur,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) die Pufferanforderungen des downstream-Eingabepins enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Die [**CTransformOutputPin::D ecideBufferSize-Methode**](ctransformoutputpin-decidebuffersize.md) des Ausgabepins ruft diese Methode auf. Die abgeleitete Klasse muss diese Methode implementieren. Weitere Informationen finden Sie unter [**CBaseOutputPin::D ecideBufferSize.**](cbaseoutputpin-decidebuffersize.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




