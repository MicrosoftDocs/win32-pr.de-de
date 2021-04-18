---
description: Die decidebuffersize-Methode legt die Puffer Anforderungen fest.
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Ctransformoutputpin. decidebuffersize-Methode (Transfrm. h)
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
ms.openlocfilehash: dc17314887094b7f62a43f38dd406d0ac9039de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372181"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a>Ctransformoutputpin. decidebuffersize-Methode

Die- `DecideBufferSize` Methode legt die Puffer Anforderungen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*palloc* 
</dt> <dd>

Ein Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners.

</dd> <dt>

*ppropinputrequest* 
</dt> <dd>

Zeiger eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die Puffer Anforderungen der Eingabe-PIN enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbaseoutputpin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) -Methode. Sie ruft die rein virtuelle [**ctransformfilter::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) -Methode des Filters auf, die von der abgeleiteten Klasse des Filters implementiert werden muss.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




