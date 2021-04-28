---
description: 'CBaseOutputPin.DecideBufferSize-Methode: Die DecideBufferSize-Methode legt die Pufferanforderungen fest.'
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: CBaseOutputPin.DecideBufferSize-Methode (Amfilter.h)
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
ms.openlocfilehash: 7a76f058e2f9c07a344453db87046704e26280a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099528"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a>CBaseOutputPin.DecideBufferSize-Methode

Die `DecideBufferSize` -Methode legt die Pufferanforderungen fest.

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

Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der Zuweisung.

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Zeiger auf eine [**ALLOCATOR \_ PROPERTIES-Struktur,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) die die Pufferanforderungen des Eingabepins enthält. Wenn der Eingabepin keine Anforderungen hat, sollte der Aufrufer die Member dieser Struktur vor dem Aufrufen der -Methode auf null setzen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Überschreiben Sie diese Methode in der abgeleiteten Klasse. Rufen Sie die [**IMemAllocator::SetProperties-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) auf, um Ihre Pufferanforderungen anzugeben. In der Regel berücksichtigt die abgeleitete Klasse die Pufferanforderungen des Eingabepins, dies ist jedoch nicht erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




