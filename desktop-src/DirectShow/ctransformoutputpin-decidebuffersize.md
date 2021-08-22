---
description: 'CTransformOutputPin.DecideBufferSize-Methode: Die DecideBufferSize-Methode legt die Pufferanforderungen fest.'
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: CTransformOutputPin.DecideBufferSize-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c6ea09c348fa465e1bffac2bdf426b635ed4cb4b76013a053ab775e78199612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538220"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a>CTransformOutputPin.DecideBufferSize-Methode

Die `DecideBufferSize` -Methode legt die Pufferanforderungen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAlloc* 
</dt> <dd>

Zeiger auf die [**IMemAllocator-Schnittstelle der Zuweisung.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Zeiger auf eine [**ALLOCATOR \_ PROPERTIES-Struktur,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) die die Pufferanforderungen des Eingabepins enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseOutputPin::D ecideBufferSize-Methode.**](cbaseoutputpin-decidebuffersize.md) Sie ruft die rein virtuelle [**CTransformFilter::D ecideBufferSize-Methode**](ctransformfilter-decidebuffersize.md) des Filters auf, die die abgeleitete Klasse des Filters implementieren muss.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




