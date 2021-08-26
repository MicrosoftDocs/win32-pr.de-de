---
description: Die Copy-Methode kopiert ein Medienbeispiel.
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: CTransInPlaceFilter.Copy-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10a7a2927789ffe49d37912862580222f0ed06d9648b6312cbb044e357d6e61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053520"
---
# <a name="ctransinplacefiltercopy-method"></a>CTransInPlaceFilter.Copy-Methode

Die `Copy` -Methode kopiert ein Medienbeispiel.

## <a name="syntax"></a>Syntax


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSource* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die **IMediaSample-Schnittstelle** für das neue Beispiel zurück.

## <a name="remarks"></a>Hinweise

Diese Methode ruft einen leeren Puffer aus der Downstreamzuweisung ab. Er kopiert alle Beispieleigenschaften aus *pSource* zusammen mit den tatsächlichen Daten im Beispiel in das neue Beispiel. Wenn der Filter zwei Zuweisungen verwendet, ruft er diese Methode auf, um Daten pufferübergreifend zu kopieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




