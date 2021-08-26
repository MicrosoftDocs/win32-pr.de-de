---
description: Die DecideAllocator-Methode handelt eine Zuweisung mit dem Ausgabepin aus.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: CPullPin.DecideAllocator-Methode (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e02fe78631c6ddee01b7acc96d761f71b80e8d3e1738d2ed6f6ae40d70b0c5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055060"
---
# <a name="cpullpindecideallocator-method"></a>CPullPin.DecideAllocator-Methode

Die `DecideAllocator` -Methode handelt eine Zuweisung mit dem Ausgabepin aus.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAlloc* 
</dt> <dd>

Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der bevorzugten Zuweisung des Eingabepins oder **NULL.**

</dd> <dt>

*pProps* 
</dt> <dd>

Zeiger auf eine optionale [**ALLOCATOR \_ PROPERTIES-Struktur,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) die die Pufferanforderungen des Eingabepins enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder andernfalls einen Fehlercode.

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**IAsyncReader::RequestAllocator-Methode**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) auf, um eine Zuweisung auszuhandeln. Der *pAlloc-Parameter* wird direkt an die **RequestAllocator-Methode** übergeben. Der *pProps-Parameter* wird an **RequestAllocator** übergeben, wenn *pProps* ungleich **NULL** ist. Andernfalls wird eine **ALLOCATOR \_ PROPERTIES-Struktur** mit einer Standardanforderung von drei 64.000 Puffern erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> <dt>

[**CPullPin::Verbinden**](cpullpin-connect.md)
</dt> </dl>

 

 




