---
description: Die InitializeOutputSample-Methode ruft ein neues Ausgabebeispiel ab und initialisiert es.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: CTransformFilter.InitializeOutputSample-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 083867f2ef6b2e40462112036dbbb000c25bc3ad2bb443f011235e36bf245ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953619"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a>CTransformFilter.InitializeOutputSample-Methode

Die `InitializeOutputSample` -Methode ruft ein neues Ausgabebeispiel ab und initialisiert es.

## <a name="syntax"></a>Syntax


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Eingabebeispiels.

</dd> <dt>

*ppOutSample* 
</dt> <dd>

Empfängt einen Zeiger auf die **IMediaSample-Schnittstelle** des Ausgabebeispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Methode wird von der [**CTransformFilter::Receive-Methode aufgerufen,**](ctransformfilter-receive.md) um das Ausgabebeispiel vorzubereiten. Im Allgemeinen müssen Sie diese Methode nicht in der abgeleiteten Klasse aufrufen, es sei denn, Sie überschreiben die **Receive-Methode.**

Diese Methode ruft ein neues Beispiel aus der Zuweisung des Ausgabepins ab. Anschließend werden die Beispieleigenschaften aus dem Eingabebeispiel in das Ausgabebeispiel kopiert. Die Beispieleigenschaften werden in der [**AM \_ SAMPLE2 \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




